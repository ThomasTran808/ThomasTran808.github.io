---
layout: essay
type: essay
title: "The Tool I Actually Used"
date: 2026-05-11
published: true
labels:
  - Software Engineering
  - Artificial Intelligence
  - Reflection
  - ICS 314
---

<img class="img-fluid" src="../img/ai-reflection.png">

## The Tool I Actually Used

## I. Introduction

AI is a normal part of software engineering now, and ICS 314 treated it that way. We were expected to use it, think about how we used it, and be honest about what it did and did not actually help with. That framing made sense to me.

The tool I used was Claude (Anthropic, claude-sonnet-4). I did not use ChatGPT, Copilot, or Bard. My pattern was consistent all semester. I reached for it when I hit something I did not understand, or when a bug had me stuck long enough that I needed another angle. I was not using it to generate code and call it done. That distinction matters for everything I am about to say.

## II. Personal Experience with AI

**Experience WODs (e.g. E18)**

I did not use AI on the experience WODs as a first step. Those existed so I could actually learn the material before the timed version. If I got through one and still did not understand why something worked, I would ask Claude afterward to fill the gap. After one of the Underscore WODs I asked something like "explain how _.map actually differs from a regular for loop in terms of what it returns." That kind of question after the fact helped more than asking it during would have.

**In-class Practice WODs**

I did not use AI during practice WODs. The whole point is finding out what you actually know. Using Claude mid-problem would have told me nothing useful about where my gaps were.

**In-class WODs**

I did use Claude during in-class WODs when I was genuinely stuck. Not to write the solution, but to get unstuck fast enough to keep moving. If I could not remember the exact syntax for a Prisma query or a specific React hook, I would ask a quick targeted question and then implement it myself. The alternative was burning the whole time on one thing and not finishing.

**Essays**

I used Claude for grammar review on my essays, including this one. I did not use it to write or structure my arguments. The ideas come from my own experience. Claude just catches awkward sentences before I post.

**Final Project**

Bow-lletins is where I used Claude most, and in the most varied ways. When our Prisma schema was not behaving as expected with relational queries, I would paste the schema and the error and ask what was going wrong. When I needed to understand how NextAuth.js session data flows into a page component, I asked Claude to walk me through it before reading the docs. I always verified any code suggestions by running them myself. It was never about getting code to paste in. It was about understanding what I was building.

**Learning a Concept / Tutorial**

This is where Claude was most consistently useful. When I hit something unfamiliar like Prisma relations, Next.js App Router conventions, or TypeScript generics, I would ask Claude to explain it before touching the official docs. The back-and-forth worked better for me than documentation because I could follow up in real time. "Why does this break when I put it in a Server Component?" gets an answer in thirty seconds. Finding that answer in the Next.js docs takes longer and assumes you already know what to search for.

**Answering a Question in Class or in Discord**

I did not answer questions in Discord using AI. If I answered something there it was because I actually knew it.

**Asking or Answering a Smart-Question**

I did use Claude to help me formulate smart questions. Not to write them, but to figure out what I was actually asking. When I was confused about something and could not articulate the problem cleanly, I would talk it through with Claude first to get to the real question. That made whatever I eventually posted more specific and more useful to whoever answered it.

**Coding Example (e.g. "give an example of using Underscore .pluck")**

I did not use Claude for standalone coding examples. If I needed to see how something worked, I would look at the docs or trace through existing code in the project. That forced me to actually read and understand what was there rather than getting a clean snippet handed to me.

**Explaining Code**

I used this more than I expected. When I came back to something I had written a week before, or was reading a teammate's code, I would sometimes paste a block and ask Claude to walk through what it was doing. Faster than re-reading cold, and it usually surfaced the thing I was actually confused about.

**Writing Code**

I did not ask Claude to write features for me. I would write it, get it mostly working, and then debug with Claude's help when something was wrong. Writing it yourself first is what builds the mental model. Using Claude to generate code I could not explain would have worked for the grade and nothing else.

**Documenting Code**

I did not use Claude for this. Documentation is fast enough to write yourself, and it is also one of the ways you figure out whether you actually understand what the code does. If I cannot explain it in a comment, that is a sign I need to understand it better, not a reason to outsource the explanation.

**Quality Assurance**

This was a legitimate use case. When ESLint threw an error I could not parse, I would paste the error and the relevant code and ask what was wrong. Something like: "ESLint is throwing no-unused-vars on this line but I'm using the variable in the JSX below, why?" Claude usually caught it faster than I would have. I made sure I understood the fix before applying it.

**Other Uses**

Conceptual debugging came up a lot. Not code errors, but situations where my mental model was wrong and producing the wrong result. "Why would a useEffect run twice in development?" or "What is the actual difference between a Server Component and a Client Component?" Those questions filled gaps that were causing bugs I would not have traced to the right source otherwise.

## III. Impact on Learning and Understanding

Claude made me faster at picking up new concepts without replacing the actual learning, because I used it that way on purpose. The risk with AI in a course like this is that it creates the appearance of understanding. You get code that runs, you submit it, and three weeks later you cannot build on it.

The pattern I stuck to, use it to understand and not to produce, mostly avoided that. I noticed that tasks I had talked through with Claude beforehand ran closer to my time estimates. Tasks I went in cold on ran over. That gap was data. It told me my estimates assumed I already understood the tool, and when I did not, I needed to budget real learning time.

The one place it cost me something was debugging instincts. When Claude catches a bug faster than I would have, I miss the process of finding it. That process is where real debugging skill comes from. I started trying to sit with a bug longer before reaching for help. Did not always work, but I was at least aware of the tradeoff.

## IV. Practical Applications

Outside of ICS 314, I used Claude on a Python auction tracking tool I built to monitor Pokemon TCG card prices. No rubric, no spec, just build it and see if it works. Claude was useful the same way it was in class: explain this library, help me understand why this API is returning unexpected data, walk me through what this expression is actually doing.

That context made one thing clear. AI is only as useful as your ability to evaluate what it gives you. When I was working in Python I understood enough to catch when something was wrong. That judgment comes from knowing the domain. The tool does not replace that. It assumes it.

## V. Challenges and Opportunities

The main challenge is one most people recognize but few are honest about. It is easy to use AI in a way that feels productive but is not. Getting code that runs is not the same as understanding why it runs. A course's feedback loop of submit, get a grade, and move on does not always surface that gap until you have to build something from scratch.

The opportunity is real though. AI can meet you where you are and explain things in terms of your actual current knowledge. Documentation is often written for people who already know the concepts. Claude does not have that assumption, and that is genuinely useful.

## VI. Comparative Analysis

Traditional instruction gave me context AI cannot replace. Understanding why software engineering practices exist and what problems they solve comes from the framing a person puts around them. A lecture on functional programming is an argument for a way of thinking. AI demonstrates the syntax. It does not make the argument.

Where AI is better is availability. Office hours are scheduled. Documentation assumes a baseline. Claude is there when I am debugging at midnight and need to understand an error right now. The two complement each other. The course gave me framing and real stakes. AI filled gaps in real time.

## VII. Future Considerations

AI is not going away from software engineering, and the more useful question is what skills still matter when AI handles certain categories of work. My answer from this semester is judgment, debugging instincts, and the ability to evaluate output. These are exactly what atrophy when you use AI badly, and what improve when you use it well. A developer who cannot tell when AI-generated code is wrong is not made safer by using AI. They are made more dangerous.

For future courses, grading explanation more heavily would help. Not just "does the code work" but "explain what this does and why you did it this way." That is much harder to outsource than working code.

## VIII. Conclusion

I used AI a lot this semester and I think I used it in a way that mostly helped. The key was reaching for it to understand things rather than to produce things I did not understand. That is easy to say and genuinely hard to maintain when you are behind and Claude can make an error disappear in thirty seconds.

The advice I would give to future students is specific: sit with the problem first. Not because AI is bad, but because the struggle is where the learning happens. Use it to accelerate your understanding of why something works, not to skip to the part where it runs. That is the version of this tool that is worth using.

*I used Claude AI for grammar review of this essay.*
