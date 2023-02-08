# Lyft-Back-End-Software-Engineering-Project
Here are some key facts about this program:

- You are working as a Back-End Engineer at Lyft.
- As a Back-End Engineer you collaborate within a larger team made up of software engineering, product, data science, analytics and operations.
- Your team is responsible for Lyft Rentals. Lyft Rentals provides vehicles for riders who are looking to rent a vehicle for personal use such as a weekend vacation.

- Throughout the program your team will takeover an unfinished project to:

  1. Come up with a clean design for an existing, unfinished component
  2. Refactor a messy codebase
  3. Write unit tests for your newly refactored system
  4. Add new functionality to your system using Test-Driven Development

You’ll receive guidance and support at each step of the journey. That being said, to complete this program, it’s advised that you have a baseline understanding of Python.

---
---

# Key Roles and Responsibilities of a Back-End Engineer at Lyft

A back-end engineer is responsible for creating the skeleton to ensure a website performs correctly. The focus for a back-end engineer is on:

- Back-end logic
- Database management
- Application program interfaces (APIs)
- Architecture
- Servers

As a Back-End Engineer at Lyft in the Lyft Rentals team, you’ll get to work across a range of different problems to ensure that you deliver the world’s most delightful and easy to use car rental experience.

Now you know a bit more about the role, let’s get jump into the problem that you and the team have been assigned.

---
---

# The project at hand

Lyft is in the process of rolling out a new rental fleet in the hopes of encouraging more connected, sustainable cities across the US.

Your team has inherited an urgent project from a fellow colleague here at Lyft who had to make a pivot to a different project. The colleague was in the process of developing a component that is used by the rental fleet’s new logistics system. Unfortunately that component was only partially completed and your team’s responsibility is to now finalize that component and make it functional.

The component itself is responsible for determining whether cars in Lyft’s new rental fleet should be serviced when they are returned. The work you will do on this component will be carried through the each of the tasks within this program.

Before we begin, let’s understand the criteria that the component must consider.

---
---

# Criteria for car servicing
Whether or not a Lyft rental car should be serviced depends on two factors at the moment:

- The engine; and
- The battery.

Each of the three types of engines has its own criteria for determining when it should be serviced. The same applies to each type of battery.

The current service criteria are as follows:


|  | Service criteria |
| --------------- | ------------------------------------ |  
| Capulet Engine | Once every 30,000 miles | 
| Willoughby Engine	| Once every 60,000 miles | 
| Sternman Engine	| Only when the warning indicator is on | 
| Spindler Battery	| Once every 2 years | 
| Nubbin Battery	| Once every 4 years | 

There are five car models in Lyft’s fleet, each with a different engine-battery combination. These are outlined below:

| Car	| Engine	| Battery | 
| ---------- | ---------- | -----------------| 
| Calliope	| Capulet Engine	| Spindler Battery | 
| Glissade	| Willoughby Engine	| Spindler Battery | 
| Palindrome | Sternman Engine	| Spindler Battery | 
| Rorschach	| Willoughby Engine	| Nubbin Batte | 
| Thovex	| Capulet Engine	| Nubbin Battery | 

These service criteria will change somewhat frequently in the future, and new car models are bound to be added to the fleet. This is an important consideration throughout the program.

With this in mind, it’s very important that the component is extensible and easy to modify, so new service criteria can be added quickly and efficiently. Just today, you learned that the system must also take tires into account when determining if a car should be serviced in the future.

Tacking this functionality onto the current system would be difficult and messy - instead, you have been instructed to take the time to refactor the codebase prior to making the change. The first step of this process is to draft up a new (clean) system architecture that will allow for the seamless inclusion of the new functionality. Your task is to draft and submit a class diagram that maps out how the system will be reorganized.

Now we understand this background information, let’s get started with the task.

---
---

# Task 1 

To begin to take over the work on the unfinished component, we need to clone the starter repository to your machine.

In this step, you will need to clone the following repo to your machine: https://github.com/vagabond-systems/forage-lyft-starter-repo

The repo you just cloned contains the core functionality of the fleet service component referenced above. In order to come up with a better design, you must first fully comprehend the current state of the codebase. Spend some time reading through each file and figuring out how things are organized.

 ###  In this last step of the task, you will draft a UML class diagram that represents a new reorganized architecture.

Now that you have a good handle on the current system, think through the best way it could be reorganized. Your plan should allow easy extensibility going forward. It should be easy for future team members to add new service criteria and change which parts each car model includes (e.g. change the battery installed on the Thovex from a Nubbin to a Spindler).

Additionally, making a change to the service criteria for a given car part should only require making a change in one place. If you are having trouble coming up with a good design, take a look at the following resources:

- https://en.wikipedia.org/wiki/Composition_over_inheritance
- https://sourcemaking.com/design_patterns/behavioral_patterns
- https://www.visual-paradigm.com/guide/uml-unified-modeling-language/uml-class-diagram-tutorial/

Estimated time for task completion: 1 hour depending on your learning style.

---
---

# Task 2

Let’s bring some order to the messy code you’ve been given.

So, now that you’ve set out a new reorganized architecture, what’s next?

It’s time to roll up our sleeves and get to know the code that we’re working with. A good starting point for us is to refactor the existing code that we’ve inherited. Don’t worry if you haven’t done any code refactoring before, we’ll take you through each step and provide support along the way.

Let's go!

---

## What is code refactoring
So let’s start with understanding what code refactoring is:

- Refactoring is the art of reorganizing a codebase without modifying its behavior.
- Any code that exists longer than the duration of a school project is fluid - it is a living, changing thing. No codebase is open and shut, there are always bugs to thump and features to add.
- As a codebase grows older, it begins to accumulate code smells. New features are tacked on, dirty fixes are settled for, and technical debt is accrued. All of these things contribute to the overall messiness of the project.
- Did you say smells? Yes, code smells are indicators of problems that can be addressed during refactoring.
- While code smells do not hamper the correctness of a system, they do impair your ability to make changes, and tend to fill programmers with a sense of lingering dread. Eventually, the aroma becomes unbearable, and the decision is made to refactor. Refactoring is cleanliness, and cleanliness is what separates code that lasts from code that doesn’t.

The goal of this task is to rewrite the codebase to bring it in line with the new design. So with that in mind, spend some time understanding:

- How each class fits together
- What is the justification for each design decision
- How that new design might be reflected in the existing messy codebase

If any part of the diagram confuses you, read through the resources below:

- https://refactoring.guru/design-patterns/factory-method
- https://refactoring.guru/design-patterns/strategy

Pay special attention to the strategy and factory patterns.

Once you’ve deeply understood the new system architecture, get started.

---
---

# Task 3 

Now you have a good understanding of your newly designed component & you’ve refactored the code - it’s time to write some unit tests.

Firstly, let’s understand what unit tests are and why they an imperative part of any coding workflow.

- Put simply, a unit test is a software testing method whereby “units” — the individual components that make up software — are tested.
- Software Engineers write unit tests for their code in order to make sure the code works as expected. This helps to detect any errors and protect against bugs. 
- Unit tests are necessary for any production system, and directly correlate with the quality of sleep everyone on the engineering team experiences.

---
Unit tests serve many purposes, the most of which are outlined below:

- Unit tests most obviously provide a means of assessing the correctness of a system. They describe the expected behavior of a piece of code, and allow you to check that it works with the click of a button. It’s easy to miss something with static analysis alone - unit tests give you instantaneous, quantitative feedback regarding whether the system works as expected.

- Unit tests provide a sort of documentation for the code - describing expected inputs and outputs, as well as the correct way to use a component. By reading the unit tests for a codebase you are unfamiliar with, you can gain a clearer understanding of how each component should be used, and how they fit together.

- Unit tests allow you to easily check if a change to the system breaks something. Suppose you modify part A of the system, which is tightly coupled with part B - by running the unit tests for part B, you can instantly ensure that your change did not break that component (provided the tests are written well).

- Unit tests provide yet another way to assess the cleanliness of your codebase. If a piece of code is difficult to test, it is almost always a code smell. Clean code is easy to test; if you are struggling to write clean tests for a piece of code, chances are the code needs to be reorganized, not the tests.

- Unit tests assist in development using workflows like TDD (test-driven development). By writing unit tests as you code, you are granted all of the above metrics and indications immediately. They can then respond to them as they crop up. We’ll circle back to this point in the next task.

- Unit tests provide a sandbox for thoroughly considering every edge case. The art of writing a good test case is the art of coming up with clever ways to break your own code. By spending time considering all the ways your code could malfunction in a chaotic fashion and hardening your code against them, you will end up with a more robust codebase.

In this task, you will focus primarily on unit tests as a means of ensuring the correctness of a system.

Engineers at Lyft take an immense amount of pride in their work, so pushing an untested component to production would be unthinkable!

Your task is to write unit tests for each of the battery and engine classes in the codebase.

Some key points to consider when writing your unit tests are:

- In a real-world environment, you should always check that parameters are what you expect, especially in a loosely typed language like Python. Part of the point of unit testing is to ensure your system does not fail in the presence of edge cases, including ridiculous ones (users can’t be trusted with anything these days).

- That being said, this task is focused on unit testing as it applies to refactoring, so, for the sake of time, you may assume all inputs to the system are valid (i.e all parameters are the expected type and all values are within reasonable bounds).

---
## Instructions for adding unit tests
Using the same repo you’ve been working on over the course of this program, add unit tests to the codebase.

Here are some important considerations for you to add your unit tests:

- You’ll need to replace the old test suite in the tests folder with your own series of unit tests.
- The old test suite should be broken (since you replaced all the classes it tests in the last step), but it should still serve as a handy template to speed you on your way.
- Note that you need only test concrete implementations of the engine and battery classes for this task. You may ignore testing on everything else.
- If you run into problems with the code you wrote in the last task while drafting unit tests, fix it! The goal of testing in this instance is to refine the draft codebase you created in the last task into something that’s guaranteed to work.

Estimated time for task completion: 1 hour depending on your learning style.

---
---

# Task 4

Before we begin, let’s recap what we’ve worked on so far as a Lyft Back-End engineer:

- In task 1, you drafted a newly designed architecture for your component;
- In task 2, you refactored the messy codebase; and
- In task 3, you introduced unit tests for your newly refactored system.

In this final task, you’ll be asked to add some new functionality to the system. You will be using a test-driven development workflow - often abbreviated TDD - to make the changes.

TDD is a hybrid workflow that combines testing, coding and refactoring, where you constantly bounce back and forth between writing code and writing test cases for it. The workflow encourages good habits, helps you consider all possible edge cases, and leads to a robust, comprehensive test suite upon completion of the project.

---
### Is TDD the gold standard workflow for writing code?

The short-answer is no.

TDD is not the best or the only coding workflow - every programmer develops (through much time and experience) their own processes, which work for them.

Some software engineers swear by it, some can’t stand it; neither is made a better developer for their view of the paradigm.

Figuring out what works for you requires years of practice and refinement, so as you take your first steps out of the syntax nursery and into the mystical world of theory, it’s important to expose yourself to the various competing schools of thought built around writing clean code.

TDD is a classic approach, and even if you don’t strictly adhere to the admittedly rigid testing cadence in the workflow you develop, there are still valuable lessons to be garnered from the doctrine. The most important thing to remember is to eschew dogma in favor of what actually works for you, provided you take the time to fully comprehend and play with the workflows you have available.

---

## Ready to practice test-driven development?

Using the same codebase you’ve been working on throughout this program, your task is to add some new functionality.

Throughout this task, you should use a test-driven development workflow - write tests that check for the expected behavior, write code to satisfy those tests, rinse and repeat.

In adding new functionality, you will be making the following two changes:

- Upgrade Spindler batteries
  
  1. First, modify the Spindler battery so it requires service after three years instead of two.
  2. Notice how easy it is to make this change - you only need to touch one line of code instead of several, and the place where that line of code lives should be immediately obvious.
  3. Consider what steps would have been required to make this change to the original system architecture, and how much more difficult it would have been, especially if you were new to working on the codebase.

- Add tire servicing criteria
  1. There are two types of tires currently in use by the Lyft fleet - Carrigan tires and Octoprime tires.
  2. The new tire wear sensors produce an array of four numbers between 0 and 1 inclusive, representing how worn each of the tires are.
  3. This array will be passed to each function in the car factory class, to be used by your tire implementation.
  4. Carrigan tires should be serviced only when one or more of the values in the tire wear array is greater than or equal to 0.9.
  5. Octoprime tires should be serviced only when the sum of all values in the tire wear array is greater than or equal to 3.
  6. Think carefully about the cleanest way to implement the new tire service criteria, then modify the system to complete the change.

Estimated time for task completion: 1 hour depending on your learning style.

---
---
