---
title: Requirements Capture
catalog: true
mathjax: true
abbrlink: '12806021'
tags: Requirements
date: 2020-10-28 19:10:23
---

The system should provide an assessment mechanism on how users interpret and interact with simulations by following their eye movements

**Requirement for the system as a whole**

- To build a tool a user can use to score the simulation
- Look at how user interpret and interact with simulations by following their eye movements
- Analyze the whole process

## Functional

| **Requirements for the system as a whole**                                                                              | **Importance**  |
| :---------------------------------------------------------------------------------------------------------------------- | :-------------- |
| Building a tool that users can use to score the simulation experience.                                                  | Important       |
| The system should enable inspecting how users interpret and interact with simulations by following their eye movements. | High Importance |
| The system should be able to quantitatively analyze the x and y value of each gazing point.                             | Important       |

1. Users should be able to log in to the system with a correct account.
2. Users should be able to register a new account with their names, passwords and e-mails.
3. Each username should be unique which is used to identify users.
4. The information of the current account shall be shown at the left corner of the page.
5. Users are able to log out by pressing the “Log out” button on the hamburger menu.
6. Users can check out the guidance and detailed information about this application by clicking “Guidance” and “About” buttons on the hamburger menu.
7. When the user press the “Start Now” button, the system shall turn to the simulation page.
8. There should be nine different simulations for users to choose from.
9. After one simulation is selected, a dialogue with a brief introduction of the simulation pop out.
10. Once a simulation starts, users cannot stop the simulation until it stops itself. But users can interact with it by clicking some buttons on the simulation.
11. When the simulation stops, users are able to score the simulation based on the content and design of it.
12. After one simulation is finished, users are able to watch other simulations by clicking on the ‘Simulation’ button on the top menu bar.
13. The algorithm devised by developers is able to score the simulation automatically and intelligently.
14. After ratifying the simulation, users are able to see the result on visualization page, and also the score marked by the algorithm.
15. Users can check out a heatmap of the distribution of gazing points on visualization page.
16. Users can check the records by clicking the “Records” button in the hamburger button.
17. Users are able to upload and download the records from the cloud end through the buttons on the top rightmost corner.
18. Users can only upload and download the records after logging into the system.

## Specification

- When the User press ‘Start’ button, the system will turn on camera and start to track user’s eyes
- When the simulation stops, the data will be shown to the customer, which shows the time and position the user is staring at
- The algorithm provided by the programmer will score the simulation automatically
- When a user presses ‘Next’, he will be asked to rate the simulation from 1 to 10

## Non-functional

1. The system should be developed using open source eye-tracking software in Python and Java.
2. The system should restrict the format of usernames, passwords and e-mails when users register.
3. The system should be able to detect human eyes within 2 seconds as soon as the simulation starts.
4. Each simulation should be played successfully for at most 60 seconds.
5. Each simulation should be scored by the algorithm of the program.
6. The system should be able to continue tracking human eyes during the whole simulation playing time.
7. The system should detect human eyes accurately with a tolerance of less than 20%.
8. Data acquired from the eye-tracking system should be compatible with the machine learning tool.
9. The cloud end should have at least 1G space to store the records.
10. Each record is able ti visualized on the visualization page.

## User stories

As a user Max, I want to rate the simulation related to Ningbo provided by the eye tracking system so that I can know how effective the eye tracking system is.

1. Max presses ‘Start’.
2. He watches the simulation on the screen using his eyes without any interruption, then he presses the stop button to exit the simulation
3. The score given by the algorithm is 90 out of 100.
4. The results show that Max looks at upper right corner for 30 times, looks at bottom for 5 times.
5. He rates the system 9 out of 10, because he thinks the simulation designed quite well.

## Activity Diagram

![](/archives/12806021/activity-diagram.png)

## Use Case Diagram

![](/archives/12806021/use-case-diagram.png)

## Sequence Diagram

![](/archives/12806021/sequence-diagram.jpg)

## Context Diagram

![](/archives/12806021/context-diagram.jpg)
