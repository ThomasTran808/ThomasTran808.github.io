---
layout: essay
type: essay
title: "The Blueprint Already Exists"
date: 2026-04-30
published: true
labels:
  - Software Engineering
  - Design Patterns
  - Next.js
  - React
---

<img class="img-fluid" src="../img/design-patterns-header.png">

## Nobody Starts From Zero

My first instinct when I started writing code was to figure everything out from scratch. If I needed to manage state, I would think through how to manage state. If I needed to connect to a database, I would work out how to connect to a database. It felt like the right approach. You understand something better when you derive it yourself.

That instinct was not wrong, but it was incomplete. At some point I realized experienced developers were not starting from zero every time. They were reaching for solutions that already had names — solutions that showed up across codebases in different languages and different frameworks because the underlying problems were always the same. That is what design patterns are. Not code you copy, but documented approaches to problems that come up over and over. The Gang of Four formalized a lot of them in 1994, but developers had been using them long before anyone wrote them down. Patterns get named after the fact, once enough people have solved the same problem the same way.

The reason they matter is not academic. Recognizing a pattern means you know what problem you are dealing with and you know the shape of the solution before you start. It also gives you a shared vocabulary. Saying "that is observer" communicates a structural decision in two seconds. Saying "the component updates when the state changes" says the same thing slower, and only if the other person can already picture what you mean. The name carries the information.

## What Bow-lletins Actually Uses

My team's final project is Bow-lletins, a campus bulletin board app for UH Mānoa. The problem it solves is real. UH's existing bulletin board is cluttered and hard to use. Students miss events, study groups, job postings, and announcements because the information is scattered across places that are not built for them. Bow-lletins puts it in one place with a clean interface. We built it in Next.js with PostgreSQL, Prisma, React, and Bootstrap 5. Building it meant running into the same structural problems every multi-user web app runs into. We solved them with patterns whether we named them or not.

<img class="img-fluid" src="../img/bowlletins-mockup.png">

**Model-View-Controller** is the most visible one. Next.js pushes you toward this structure almost automatically. The Prisma schema defines the models — `User`, `Listing`, `Category`. The API routes under `/app/api/` handle controller logic: receive a request, query the database, return a response. The React components handle the view. The separation is not perfect in practice and some components do more than just render, but the architecture's gravity pulls toward MVC. That is why the codebase stays navigable as it grows.

**Observer** is everywhere in the React layer, even when it is invisible. Every time a component re-renders because its state changed, that is observer. The component subscribed to a piece of state. The state changed. The component updated. When a user posts a new listing and the feed shows it without a page reload, observer is what made that happen. We did not implement it ourselves. React's entire model is built on it. But recognizing it explains why the UI behaves the way it does, and it explains what breaks when you mismanage state.

**Singleton** shows up in the database connection setup. With Prisma in a Next.js development environment, hot reloading creates a new Prisma client instance on every file save unless you guard against it. The fix is the standard singleton pattern: check if an instance already exists, reuse it if it does, create one if it does not. Skipping this causes connection pool exhaustion in development and worse problems in production. The pattern name tells you exactly what the code is doing and why it has to be that way.

**Publish-Subscribe** connects user actions to state updates that span components with no direct relationship. When someone posts a listing, that event needs to update the feed, a notification badge, and a post count — components that do not share a parent-child hierarchy. Pub/sub decouples the event from whoever responds to it. The poster publishes. The subscribers update. The components do not need to know about each other.

## Why the Names Matter

There is a version of this essay where I just describe what the code does without naming the patterns, and it would be longer and less clear. Saying "components update when state changes" is true but vague. Saying "we use observer" is precise. It connects to documented knowledge that exists outside our codebase and tells another developer everything they need to know about that part of the system before they read a single line of code.

That is the real value. Design patterns are not trivia for interviews, though they help there too. They are the accumulated knowledge of what breaks in software and how to prevent it. Learning them now means not discovering those failure modes the hard way later when the system is bigger and the stakes are higher.

*I used Claude AI for grammar review and editing assistance.*
