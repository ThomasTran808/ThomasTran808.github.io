---
layout: essay
type: essay
title: "ESLint Errors Made Me a Better Programmer"
date: 2026-02-12
published: true
labels:
  - Coding Standards
  - ESLint
  - TypeScript
  - Software Engineering
---

<img class="img-fluid" src="../img/eslint-header.png">

## Fighting the Red Underlines

My first week using ESLint with VSCode felt like the tool was working against me. I'd write code that ran fine and produced the correct output but ESLint would light up my editor with red and yellow underlines everywhere. Missing return types on functions. Using `let` when the variable never gets reassigned. Inconsistent spacing around arrow functions. I was also dealing with GitHub issues at the same time trying to get my repository set up correctly and pushing code without breaking my project structure. Between ESLint complaints and GitHub merge conflicts I spent more time fixing environment problems than actually writing logic. It was frustrating because the code worked. Why did it matter if I used `let` instead of `const` or left out a type annotation?

## When the Rules Started Making Sense

After a few days of fixing ESLint errors repeatedly I started noticing patterns. The tool wasn't being difficult for no reason. It was teaching me TypeScript conventions that I hadn't internalized yet. For example when working on an exercise implementing five fundamental functions every CS major should know I kept writing things like this:

```typescript
let isUnique = (arr) => {
  let seen = [];
  for (let i = 0; i < arr.length; i++) {
    if (seen.indexOf(arr[i]) !== -1) {
      return false;
    }
    seen.push(arr[i]);
  }
  return true;
}
```

ESLint flagged almost every line. Use `const` instead of `let` for `isUnique` because the function reference never changes. Same for `seen` because even though I push to the array the reference itself doesn't change. Add type annotations for the parameter and return type. After fixing everything the code looked like this:

```typescript
const isUnique = (arr: number[]): boolean => {
  const seen: number[] = [];
  for (let i = 0; i < arr.length; i++) {
    if (seen.indexOf(arr[i]) !== -1) {
      return false;
    }
    seen.push(arr[i]);
  }
  return true;
};
```

The second version does the same thing but now anyone reading the function immediately knows it takes an array of numbers and returns a boolean. The `const` declarations tell you that `isUnique` won't get reassigned and `seen` always points to the same array. These aren't cosmetic changes. They communicate intent to whoever reads the code next including myself two weeks later when I've forgotten what I wrote.

## Coding Standards Are More Than Formatting

People treat coding standards like they're about tabs versus spaces or where to put curly braces. Those things matter for consistency but the real value goes deeper. When ESLint forces me to add type annotations it prevents bugs before they happen. If I accidentally pass a string into a function that expects a number the type system catches it at development time instead of letting it fail silently at runtime. When it tells me to use `const` instead of `let` it forces me to think about whether a variable actually needs to change. Most of the time it doesn't and making it `const` reduces the surface area for mistakes.

I think coding standards are one of the most effective ways to learn a programming language because they encode the patterns that experienced developers already follow. Instead of figuring out best practices through trial and error over months ESLint gives you that feedback immediately. Every error is a lesson about how TypeScript is meant to be written. I didn't fully understand the difference between `let` and `const` in practice until ESLint made me justify every variable declaration.

## The Practical Payoff

Now that I've spent more time with ESLint the red underlines don't bother me. I actually write cleaner code on the first pass because the standards are becoming habits. I catch myself choosing `const` by default and adding return types before ESLint has to remind me. The initial pain of fixing dozens of errors per file taught me patterns that now save time because I'm not debugging issues that proper typing would have prevented.

For anyone who thinks coding standards are just about making code look pretty I'd push back on that. They're about making code that communicates clearly and fails less. The formatting consistency is a bonus. The real value is that following strict standards forces you to understand the language at a deeper level than just getting your output to match the expected result. ESLint didn't just check my code. It taught me TypeScript.

*I used Claude AI for grammar corrections and formatting assistance.*
