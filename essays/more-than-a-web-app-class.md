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
  - Coding Standards
  - ICS 314
---

<img class="img-fluid" src="../img/se-reflection.png">

## More Than a Web App Class

## I. Introduction

By the end of ICS 314, you have written TypeScript, built UI components in React, deployed a full-stack Next.js app with a real database, and shipped a team project that actually works. It is easy to walk away thinking the class taught you a web stack. It did. But the more durable thing it taught was how to work on software at a level beyond just getting code to run. Two concepts from this class that I think matter far outside the context of web development are coding standards and Issue Driven Project Management.

## II. Coding Standards

A coding standard is a set of agreed-upon rules for how code should be written across a codebase. Not what the code does, but how it looks, how it is organized, and what patterns it follows. In ICS 314, that meant ESLint enforcing rules like no unused variables, consistent spacing, and specific TypeScript conventions. An ESLint error was not a warning you could ignore. It blocked you.

That felt annoying at first, especially when ESLint flagged something that still ran fine. But the point is not whether your code works in isolation. The point is whether another person can read it, maintain it, and build on it without constantly asking you what you meant. A codebase is a shared document. The standard is what keeps it readable as it grows and as different people touch different parts.

This applies to any software project, not just web apps. A Python data pipeline, a C embedded system, a shell scripting environment — all of them benefit from consistent style because all of them are eventually read by someone other than the original author. The specific rules change by language and team. The reason for having them does not.

What I took from ESLint specifically was learning to treat style errors as real errors. The instinct when something works is to ship it. But works on my machine in this moment is a low bar. Readable, consistent, and maintainable is a higher bar, and the discipline of hitting it on every file is something I will carry into any engineering environment.

## III. Issue Driven Project Management

Project management is the problem of getting people and work aligned toward a shared goal on a fixed timeline. In ICS 314, we used a specific approach called Issue Driven Project Management, which is built on top of Agile principles.

Agile is a broad philosophy that prioritizes short delivery cycles, continuous feedback, and flexibility over rigid long-term planning. The idea is that requirements change, and a process that treats the plan as fixed will produce something that no longer fits by the time it ships. Agile breaks work into shorter iterations and adjusts after each one.

Issue Driven Project Management takes that philosophy and makes it concrete. Every piece of work lives as a discrete issue in a tracker. Each issue is scoped to one person, has a clear definition of done, and moves through a board from backlog to in progress to done. Milestones group issues into time-boxed targets so the team can see what is due and when.

On Bow-lletins, this made a real difference. Early on we talked about the project in broad terms: someone would handle the profile page, someone would handle posting. As soon as we moved to actual issues, the work became trackable. "Implement bulletin card component" is a task. "Handle the front end" is not. When something was falling behind, we could see it on the board before the deadline instead of discovering it the night before the milestone was due.

The part worth emphasizing is that none of this is specific to web applications. A research lab building a data processing pipeline could run on the same board structure. A small team writing firmware for an embedded device could use the same milestone system. The tool might be GitHub Projects or Jira or a physical board. The underlying structure of small tasks with clear owners and regular check-ins transfers to any team doing any kind of complex work together.

## IV. Why the Distinction Matters

Both of these concepts are about discipline. Coding standards are the discipline of writing for someone else, not just for the compiler. Issue Driven Project Management is the discipline of making work visible and accountable instead of assuming everyone knows what is happening.

These are not web skills. They are engineering skills. The web stack is what ICS 314 used to teach them, and I am glad I learned Next.js and Prisma and React. But the things I expect to still be using in ten years regardless of what stack I am working in are the habits around how I write code and how I manage work with a team. That is what the class was actually about.

*I used Claude AI for grammar review of this essay.*