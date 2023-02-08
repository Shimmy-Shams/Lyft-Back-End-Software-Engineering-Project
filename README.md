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
