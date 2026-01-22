---
layout: project
type: project
image: img/calorie-tracker-square.png
title: "Thomas Calorie Tracker"
date: 2025-01-21
published: true
labels:
  - JavaScript
  - HTML
  - CSS
  - Web Development
summary: "A web-based calorie tracking application that helps users monitor their daily food intake and stay within their calorie goals."
---

<img class="img-fluid" src="../img/calorie-tracker-header.png">

Thomas Calorie Tracker is a clean and intuitive web application I developed to help users track their daily calorie intake. The application features a modern, responsive design that works seamlessly across desktop and mobile devices.

## Key Features

The tracker provides real-time calculation of total calories consumed versus daily goals, with a visual progress bar that changes color when the goal is exceeded. Users can quickly add meals with their calorie counts, view a complete log of all entries with timestamps, and edit their daily calorie goal on the fly.

The application uses local storage to persist data throughout the day, automatically resetting at midnight while preserving the user's preferred calorie goal. This ensures users start fresh each day without losing their configuration.

## Technical Implementation

Built with vanilla JavaScript using object-oriented programming principles, the CalorieTracker class manages all application state and user interactions. The interface uses modern CSS with flexbox for responsive layouts and smooth transitions for an enhanced user experience.

I implemented event listeners for keyboard shortcuts (Enter key to add meals) and form validation to ensure data integrity. The local storage integration required careful handling of date comparisons to manage the daily reset functionality while maintaining user preferences.

## Learning Outcomes

This project helped me strengthen my understanding of DOM manipulation, event handling, and state management in JavaScript. I also gained experience with CSS styling techniques and creating responsive designs that work well on various screen sizes. The local storage implementation taught me about data persistence in web applications and the importance of handling edge cases like date transitions.

Source: <a href="https://github.com/ThomasTran808/calorie-tracker"><i class="large github icon"></i>ThomasTran808/calorie-tracker</a>
