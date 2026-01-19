# Content
- Watch lessons 2.1 through 2.2 (1)
- Watch lessons 3.1 through 3.2 (1.5)

# Assignments
- Complete Homework 1 (4)
- Begin work on Homework 2 (1.5)

# Readings

Lesson 2.1 (Introduction to Principles)
- Norman, D. A. (1986). Cognitive engineering Links to an external site.. In D. A. Norman & S. W. Draper (Eds.) User-Centered System Design: New Perspectives on Human-Computer Interaction. (pp. 32-61). Hillsdale, NJ: Lawrence Erlbaum Associates.

Lesson 2.2 (Feedback Cycles)
- Norman, D. (2013). Chapter 2: The Psychology of Everyday Actions. In The Design of Everyday Things: Revised and Expanded Edition. (pp. 37-73). Arizona: Basic Books.

Lesson 3.2 (Ethics and Human Research)
- Hallinan, B., Brubaker, J. R., & Fiesler, C. (2020). Unexpected expectations: Public reaction to the Facebook emotional contagion study. New Media & Society, 22(6), 1076-1094.

# Miscellany
- Work on additional participation credit opportunities (2)

# 2.1: Introduction to Principles

## Introduction to Principles
- Focus on task in HCI, not on tools and interfaces on their own
- Talk about role of interface  and how it mediates user and task
- Different view on roles on the system
- UX at multiple levels

## Interfaces: Between Users and Tasks
- Our focus should be user and task, not interface
- To design good interface, need to find user's goal and what they want to achieve
- In thermostat example, by focussing ont he task instead of just the interface, we can come up with more revolutionary design like Nest, instead of the traditioanal thermostat

## Tips: identifying the task
- Video of someone paying by swiping her credit card. What is the task? Swiping is too narrow so answer is paying for groceries
- 5 quick tips
  - Watch real users
  - Talk to them - what their goals and motives
  - Start small - individual interactions
  - Abstract up - working from smaller obs, try to understand task they're trying to complete
  - You are not your user - leave behind previous experience, biases

    
## Usefulness and Usability
- Useful: interface allows the user to achieve their goal, but it is the lowest bar, 
- Usability: most important, how easy it is to use the interface to achieve their goal, Google Maps to replace paper map

## Views of the User: Processor
- Need to understand the role human has in the system
- Processor, predictor, participant
- Interface must fit within human limits
- Evaluated by: quantitative experiments, take numeric measurements of how fast they can complete a task and etc

## Views of the User: Predictor
- Care deeply about knowledge, experience and thought process
- Want them to be able to get input and give output
- Interface must fit with knowledge
- Evaluated by qualitative studies: ex situ studies, cognitive walk thru to understand how user thinks about the system
- We still focus on one user, and one task, but we might wanna see it more broadly. Hence participant view

## Views of the User: Participant
- Not just interested in their head, but around them. like what kind of people they interacting with
- What's competing for their attention, their cognitive load
- Interface must: fit with the context: actually interact with the system where they are need
- Evaluated by: in situ studies (within the authentic context), context that are relevant

## Views of the User and Psychological Schools of Thoughts
- Processor - behaviorism: aim to provide systematic way of investigating behavior in human and animals
- Little Robert experiment
- Attempts to understand behavior, just by observing the behavior
- Our design process focus on testing observable behaviors


- Predictor - cognitivism: concern with what's going on inside the mind
- Memory creativy and etc
- Care about what the user is thinking
- Predictive model of the user, what the user is predicting
- We ask question, what do they predict the ourcome of the action to be? is it the right action?
- We want to get inside user's head


- Participant - Functionalism, System: Context in broader environment
- Look at the interaction of both above at the larger system
- We look beyond just the user and the interface

![img.png](img.png)

## Designing with three views
- Redesigning Tesla infotainment system

Processor 
- Pros: May use existing data
- Pros: Enables objective comparisons
- Cons: Doesnt find reason for differences
- Cons: Cant differentiate by expertise
- Cons: Help optimize, not redesign

Predictor
- Pros: More complete picture of interaction
- Pros: Targets different levels of expertise
- Cons: Analysis may be expensive, plain text of interviews, surveys (need a lot of effort)
- Cons: Analysis subject to biases
- Cons: Ignore broader Interaction context (test in labs, vs real world)

Participant
- Pros: Evaluates interaction in real world context
- Pros: Captures authentic user attention
- Cons: Expensive to perform and analyze
- Cons: Requires real, functional interfaces
- Cons: Subject to uncontrollable variables

![img_1.png](img_1.png)

## User experience: Sans Design
- UX goes beyond task via interface
- Based on age, sex, culture, prior experience and etc
- Examines emotional response, aesthetics, values and etc
- 3 levels; Individual, Group, and Society
- Make sure user feels represented by the system


## Design Challenge: Morgan 
Morgan loves audiobooks, takes notes and bookmarks and stuff
- As a processor, we might simply look at what information is communicated to Morgan, when, and how.
- As a predictor, we might look instead at how the interface meshes with Morgan’s needs with regard to this task, how easy it is to access, how easy the commands are to perform, and so on. 
- As a participant, we might look at the broader interactions between this interface and Morgan’s other tasks and social activities.

# 2.2: Feedback Cycles

## Feedback cycles are fundamentals
- Intelligence: ability that must be gain thru feedback cycles

## Gulf of Execution
- Two general challanges:
  - Users's interaction with the task thru the interface: gulf of execution
    - How do i know what i can do
  - Task's return to the user of the output via the interface: gulf of evaluation
- First: Identify intention
- Second: Identify actions
- Third: Execute actions
- GoEx: Takes the user from understand their own goal to understand goal in the context of the system to understand the actions necessary to realize the goal to executing those actions


5 tips of GofEx
- Make functions discoverable
  - How they know what they can do? documentation? discoverablke
- Let the user mess around
  - Avoid any button that can cause irreversible damage
- Be consistent with other tools
  - Familiarity
- Know your user
  - Identify intention, identify actions and execute actions
- Feedforward
  - Feedback about what user might want to do
  - Information on what would happen if keep doing what we;re doing

## Gulf of Evaluation
- The output of the actions that the user took
- Interface output -> Interpretation -> Evaluation
- On-demand video shows black, not showing buffering icon to help user understand what's going on, evaluate the situation


Example: Thermostat
- Feeling the heat is good, hearing the heater turn on might not
- Mark the thermostat the heat is on to lower the gulf of evaluation
- 


5 tips of GofEv
- Give feedback constantly
  - Dont wait, give them feedback that the input was received, and what input is received
- Give feedback immediately
  - Tap on app, icon briefly grays out when opening app if there's buffer
- Match feedback to the action
  - Subtle action should result in subtle feedback
- Vary your feedback
  - Think about how auditory or haptic feedback
- Leverage direct manipulation
  - Dragging stuff around, making things large

## Norman's Feedback Cycle Stage
![img_2.png](img_2.png)

Norman ask 7 question when designing these interfaces
- How easily can one
  - determine the function of the device
  - tell what actions are possible
  - determine the mapping from intent to movement
  - actualy perform the physical movement
  - tell what state the system is in
  - tell if the system is in the desired state
  - determine the mapping from state to interpretation


## Conclusion
- Feedback cycles: exchange of input and output between user and system to share some goal
- GoFEx: The distance between making some change in the system and evaluate whether or not the goal was accomplished
- 7 questions to bridge those goals
- Understanding method for crossing the goals

## 

## 

## 

## 

## 

# 3.1 Notes

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 

# 3.2 Notes

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 
