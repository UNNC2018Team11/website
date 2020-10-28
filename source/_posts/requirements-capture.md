---
title: Requirements Capture
catalog: true
mathjax: true
abbrlink: '12806021'
tags: Requirements
date: 2020-10-28 19:10:23
---

The system should provide an assessment mechanism on how users interpret and interact with simulations by following their eye movements

## Functional

- Users should be able to log in through username and password if they have an account
- Users should be able to register if they don’t have an account, they will be instructed to set their username, password, and confirm the password
- Users should be allowed to reset their password and security question (security question must be answered)
- Users should be provided with a way to find back their password in case they forget it (use email address to verify)
- When the User press ‘**Start Simulation**’ button, the system will then allow user to select simulation level. The information for current account will be shown at the right corner of the page
- Users should be provided with a certain amount of topics to choose from. Further, under that topic, they should be provided with several simulations to watch [ There are currently **six** different levels to be chosen from, they are ‘**Ningbo**’, ‘**Comic**’, ‘**Animals**’, ‘**Traffic**’, ‘**Building**’ and ‘**Sports**’ ]
- User can stop the simulation any time they want by clicking the button under the simulation
- When the simulation stops, the data will be shown to the customer, which shows the time the user looks at different part in the simulation
- The user can try the simulation again if he presses ‘**Try Again**’
- The algorithm provided by the programmer will score the simulation automatically
- When a user presses ‘Next’, he will be asked to rate the simulation from 1 to 10
- User can check their record by clicking ‘My account’ – ‘My record’

## Non-functional

| Aspect         | Description                                                  |
| -------------- | ------------------------------------------------------------ |
| Performance    | The system should be user-friendly and highly efficient when users are watching the simulation, with the eye tracker correctly working behind |
| Implementation | The system should be developed using open source eye tracking software in Python & java (for the main logic and interface of the system) |
| Usability      | Data acquired from experiments should be usable on machine learning analysis and the system should work correctly for different users and simulations. |
| Security       | The privacy of users must not be exposed to irrelevant people. |

TBC...

## User stories

As a user Max, I want to rate the simulation related to Ningbo provided by the eye tracking system so that I can know how effective the eye tracking system is.

- Max already has an account, so he enters his username (Max), and his password (123456) into the input box.
- He then presses ‘Log in’. 
- He then presses ‘Start Simulation!’.
- He chooses ‘Ningbo’.
- After that, he presses ‘Airport’ to start the eye tracking task.
- He watches the simulation on the screen using his eyes without any interruption, then he presses the stop button to exit the simulation
- The score given by the algorithm is 90 out of 100.
- The results show that Max looks at upper right corner for 30 times, looks at bottom for 5 times.
- He decides to quit the system, so he presses ‘Next’
- He rates the system 9 out of 10, because he thinks the simulation designed quite well.

## Use Case Diagram

![](/archives/12806021/use-case-diagram.jpg)

## Sequence Diagram

![](/archives/12806021/sequence-diagram.jpg)

## Context Diagram

![](/archives/12806021/context-diagram.jpg)