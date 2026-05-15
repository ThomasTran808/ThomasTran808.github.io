---
layout: essay
type: essay
title: "More Than a Web App Class"
date: 2026-05-14
published: true
labels:
  - Software Engineering
  - Reflection
  - Agile Project Management
  - Design Patterns
  - ICS 314
---

<img class="img-fluid" src="../img/se-reflection.png">

## More Than a Web App Class

## I. Introduction

By the end of ICS 314, you have built a full-stack web application with a real team, hit real deadlines, and shipped something that works. It is easy to walk away thinking the class was about Next.js, React, and Prisma. Those were the tools. The actual subject was software engineering, and the distinction matters. The concepts we worked with  how you manage a project, how you structure code so it does not fall apart, how you make decisions as a team  apply to any software context, not just web apps. I want to focus on two of them: Agile Project Management and Design Patterns.

## II. Agile Project Management

Project management is the problem of coordinating people and work toward a shared goal. It sounds simple until you have five people, conflicting schedules, unclear requirements, and a deadline that does not move. There are a lot of ways to approach that problem and they are not all equivalent.

Agile Project Management is a family of approaches that share a core idea: break the work into short cycles, ship something at the end of each one, and adjust based on what you learned. The alternative is planning everything upfront, executing the full plan, and delivering at the end. That works when requirements are fixed and well understood. In software, they rarely are.

The specific flavor we used in ICS 314 is called Issue Driven Project Management. The idea is that all work lives as discrete issues in a tracker, in our case GitHub Projects. Each issue describes a specific, scoped task. You assign it to one person, put it on a board, and move it from backlog to in progress to done. Milestones group related issues into time-boxed delivery targets. When a milestone is up, you look at what got done, what did not, and what needs to shift going into the next one.

On Bow-lletins, this actually changed how the team worked. Instead of someone saying "I'll handle the front end," we broke front end into specific issues: implement the bulletin card component, set up the filter by category, wire the create form to the API. Those tasks could be picked up by anyone and tracked independently. When something slipped, we could see it early instead of finding out at the end of the milestone that a whole feature was missing.

None of this is web specific. Issue Driven Project Management would work for a firmware team, a data pipeline project, or a research group writing a codebase for simulation. The core structure of small tasks, clear ownership, and regular delivery is general. The tool might change. The practice is the same. I could see using this on any group project involving software, regardless of what that software does.

## III. Design Patterns

A design pattern is a named solution to a recurring problem in software structure. The key word is recurring. If a problem shows up once in one codebase, you solve it however makes sense. If the same structural problem shows up in codebases across different domains, languages, and teams, it is worth naming the solution so people can communicate about it and reach for it without reinventing it every time.

The patterns I worked with most in ICS 314 were not always labeled as such in the moment, but they were there. The one that came up constantly on the final project was the Observer pattern, specifically how React's component model handles state. When state changes, everything that depends on it re-renders. The component does not call its children and tell them to update. The children are subscribed to the state and they respond when it changes. That is the Observer pattern: a subject, a set of observers, and a mechanism for notification.

Another pattern that shaped how we structured the project was the Model View Controller split. The Prisma schema defined the data model. The Next.js server components and API routes handled the logic. The React components handled what the user sees. Keeping those concerns separated made it easier to change one without breaking the others. When we needed to add a field to the database, we changed the schema and the API. The front end component just had to display whatever it received. That separation is not Next.js specific. It shows up in desktop applications, mobile apps, and game engines. The language and the tools change. The pattern persists.

Understanding these as patterns rather than just "how React works" is the useful thing. When I encounter a new system in a different context, I can ask what pattern it is using. That question gives me a starting point instead of approaching it cold. Patterns are a shared vocabulary for structure. The web application was just the context where I learned to see them.

## IV. Why This Matters

These concepts are not specific to web development. They are tools for thinking about software: how to manage it, how to structure it, how to build it with other people. The web stack was the environment where I worked with them, but they transfer.

That transfer is actually the thing worth being deliberate about. It is possible to finish a course like ICS 314 and walk away thinking you learned how to build web apps. You did. But the more durable thing is the mental models underneath — what makes a project manageable, what makes code adaptable. Those apply anywhere you are building software with other people, and that is almost everywhere you will end up.

*I used Claude AI for grammar review of this essay.*