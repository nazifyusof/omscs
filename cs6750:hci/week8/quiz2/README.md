- [Notes on \`What Do Prototypes Prototype?\`](#notes-on-what-do-prototypes-prototype)
    - [1\. Core Problem the Authors Are Addressing](#1-core-problem-the-authors-are-addressing)
        - [The Problem with How We Talk About Prototypes](#the-problem-with-how-we-talk-about-prototypes)
    - [2\. Key Definitions \(Memorize These\)](#2-key-definitions-memorize-these)
        - [Artifact](#artifact)
        - [Prototype](#prototype)
        - [Designer](#designer)
    - [3\. The Core Model\: What Do Prototypes Prototype?](#3-the-core-model-what-do-prototypes-prototype)
        - [1\. Role](#1-role)
        - [2\. Look and Feel](#2-look-and-feel)
        - [3\. Implementation](#3-implementation)
    - [4\. The Triangle Model](#4-the-triangle-model)
    - [5\. Four Major Types of Prototypes](#5-four-major-types-of-prototypes)
        - [A\. Role Prototypes](#a-role-prototypes)
        - [B\. Look and Feel Prototypes](#b-look-and-feel-prototypes)
        - [C\. Implementation Prototypes](#c-implementation-prototypes)
        - [D\. Integration Prototypes](#d-integration-prototypes)
    - [6\. Major Conceptual Shifts in the Paper](#6-major-conceptual-shifts-in-the-paper)
        - [Shift 1\: From Fidelity to Purpose](#shift-1-from-fidelity-to-purpose)
        - [Shift 2\: Prototypes Are Communication Tools](#shift-2-prototypes-are-communication-tools)
        - [Shift 3\: Build Multiple Prototypes](#shift-3-build-multiple-prototypes)
    - [7\. Audience Matters \(Very Important Essay Point\)](#7-audience-matters-very-important-essay-point)
    - [8\. Key Warnings from the Authors](#8-key-warnings-from-the-authors)
    - [9\. Practical Takeaways for Essay Answers](#9-practical-takeaways-for-essay-answers)
    - [10\. Short Jargon Glossary](#10-short-jargon-glossary)
    - [11\. One-Sentence Thesis of the Paper](#11-one-sentence-thesis-of-the-paper)
- [Prototyping Tools and Techniques \u2013 Detailed Quiz Notes](#prototyping-tools-and-techniques--detailed-quiz-notes)
    - [1\. What is a Prototype?](#1-what-is-a-prototype-1)
        - [Definition](#definition)
        - [Important Distinction](#important-distinction)
    - [2\. Why Prototypes Matter in HCI](#2-why-prototypes-matter-in-hci-1)
    - [3\. Prototypes as Design Artifacts](#3-prototypes-as-design-artifacts-1)
    - [4\. Four Dimensions of Prototypes \(VERY IMPORTANT FOR ESSAYS\)](#4-four-dimensions-of-prototypes-very-important-for-essays-1)
        - [1\. Representation](#1-representation-1)
            - [Off-line \(Paper Prototypes\)](#off-line-paper-prototypes)
            - [On-line \(Software Prototypes\)](#on-line-software-prototypes)
        - [2\. Precision](#2-precision-1)
        - [3\. Interactivity](#3-interactivity-1)
            - [Levels of Interaction](#levels-of-interaction)
                - [Fixed Prototype](#fixed-prototype)
                - [Fixed-Path Prototype](#fixed-path-prototype)
                - [Open Prototype](#open-prototype)
        - [4\. Evolution](#4-evolution-1)
            - [Rapid Prototypes](#rapid-prototypes)
            - [Iterative Prototypes](#iterative-prototypes)
            - [Evolutionary Prototypes](#evolutionary-prototypes)
    - [5\. Prototypes in the Design Process](#5-prototypes-in-the-design-process-1)
        - [User-Centered Design \(UCD\)](#user-centered-design-ucd)
        - [Participatory Design](#participatory-design)
    - [6\. Design Space \(CRITICAL CONCEPT\)](#6-design-space-critical-concept-1)
        - [What is Design Space?](#what-is-design-space)
    - [7\. Expanding the Design Space](#7-expanding-the-design-space-1)
        - [Brainstorming](#brainstorming)
            - [Video Brainstorming](#video-brainstorming)
    - [8\. Contracting the Design Space](#8-contracting-the-design-space-1)
        - [Video Prototyping \(Different from video brainstorming\)](#video-prototyping-different-from-video-brainstorming)
    - [9\. Prototyping Strategies](#9-prototyping-strategies-1)
        - [1\. Horizontal Prototype](#1-horizontal-prototype-1)
        - [2\. Vertical Prototype](#2-vertical-prototype-1)
        - [3\. Task-Oriented Prototype](#3-task-oriented-prototype-1)
        - [4\. Scenario-Based Prototype](#4-scenario-based-prototype-1)
    - [10\. Rapid Prototyping](#10-rapid-prototyping-1)
    - [11\. Off-line Rapid Prototyping Techniques](#11-off-line-rapid-prototyping-techniques-1)
        - [Paper & Pencil](#paper--pencil)
        - [Mock-ups](#mock-ups)
        - [Wizard of Oz](#wizard-of-oz)
        - [Video Prototyping](#video-prototyping)
    - [12\. On-line Rapid Prototyping](#12-on-line-rapid-prototyping-1)
        - [Non-Interactive Simulations](#non-interactive-simulations)
        - [Interactive Simulations](#interactive-simulations)
        - [Scripting Languages](#scripting-languages)
    - [KEY TERMS \(Simple Definitions\)](#key-terms-simple-definitions)
    - [Essay Advice for Quiz](#essay-advice-for-quiz)

# Notes on “What Do Prototypes Prototype?”
Stephanie Houde & Charles Hill (1997)  
Source: Chapter 16, Handbook of Human-Computer Interaction :contentReference[oaicite:0]{index=0}

---

# 1. Core Problem the Authors Are Addressing

## The Problem with How We Talk About Prototypes

The authors argue that **current terminology about prototypes is misleading**.

Most people describe prototypes based on:
- The **tool used** (e.g., C prototype, paper prototype, Director prototype)
- The **level of detail** (e.g., high-fidelity vs low-fidelity)

But this is problematic because:

- Tools can be used in many different ways.
- A “high-fidelity” prototype does not necessarily mean the design is nearly finished.
- A rough prototype might actually answer very important design questions.
- Different team members (industrial designers, programmers, interaction designers) mean different things when they say “prototype.”

The authors propose shifting the focus away from:
> What is the prototype made of?

And toward:
> What aspect of the design is the prototype exploring?

---

# 2. Key Definitions (Memorize These)

These definitions are foundational to the essay.

## Artifact
**Artifact** = The interactive system being designed.

This can be:
- A real product
- A research concept
- A software system
- A physical-digital hybrid system

It is the *end result* of the design process.

---

## Prototype
**Prototype** = Any representation of a design idea, regardless of medium.

Important:
- A brick can be a prototype (if used to test weight/scale).
- A storyboard can be a prototype.
- A video can be a prototype.
- A program listing can be a prototype.

It is defined by **purpose**, not by tool or polish.

---

## Designer
**Designer** = Anyone who creates a prototype to explore a design idea.

Not limited to:
- Interaction designers
- Programmers
- Industrial designers

Anyone asking and answering design questions through representation is acting as a designer.

---

# 3. The Core Model: What Do Prototypes Prototype?

This is the central contribution of the paper.

The authors introduce a **three-dimensional model**.

Every interactive artifact has three major dimensions:

---

## 1. Role

**Role = What function the artifact serves in the user’s life.**

It answers:
- What problem does it solve?
- What task does it support?
- Why would someone use this?
- What place does it occupy in daily life?

Example:
- Is this device a personal assistant?
- Is it a learning toy?
- Is it a professional design tool?

Role is about **purpose and usefulness**.

---

## 2. Look and Feel

**Look and Feel = The concrete sensory experience of using the artifact.**

It answers:
- What does it look like?
- What does it sound like?
- How does it behave?
- What is interaction like?

Includes:
- Visual design
- Interaction style
- Physical form
- Animation
- Feedback

It is about **user experience**.

---

## 3. Implementation

**Implementation = How the artifact actually works technically.**

It answers:
- What algorithms are used?
- How fast is rendering?
- What programming language?
- What hardware constraints?
- What technical architecture?

It is about:
- Feasibility
- Performance
- Technical viability

---

# 4. The Triangle Model

The authors represent these three dimensions as corners of a triangle:

- Role
- Look & Feel
- Implementation

A prototype can focus on:
- One corner
- Two corners
- All three (integration prototype)

The triangle is NOT hierarchical.
No corner is more important than another.

It is a way to visualize:
- What questions are being explored
- What questions are NOT being explored

---

# 5. Four Major Types of Prototypes

## A. Role Prototypes

Built primarily to explore:
> What should this artifact do?

They:
- Describe functionality
- Show usage scenarios
- Often ignore technical feasibility
- Often ignore polished UI

Examples from the chapter:
- Storyboards
- Vision videos (Knowledge Navigator)
- Appearance models used for market research

Key characteristics:
- Often narrative-based
- Focus on tasks and context of use
- May be non-interactive
- Used to communicate big ideas

Important insight:
Role prototypes are especially useful early in projects when:
- The purpose of the artifact is unclear
- Designers are exploring what value it could bring

---

## B. Look and Feel Prototypes

Built primarily to explore:
> What will it be like to use this?

They:
- Simulate interaction
- Emphasize sensory experience
- May fake functionality
- Often use “Wizard of Oz” techniques

Wizard of Oz technique:
A method where functionality is simulated by a hidden human operator.

Example:
- A toy that “talks” via hidden walkie-talkie
- A ball that “moves autonomously” via hidden remote control

Key idea:
You can simulate advanced technology cheaply to test user experience before building the real system.

Important limitation:
Users may mistakenly believe the system is fully implemented.

---

## C. Implementation Prototypes

Built primarily to explore:
> Can we build this?

They:
- Test algorithms
- Test rendering speed
- Test technical feasibility
- Often have ugly or incidental interfaces

Examples:
- C program testing movie interactivity
- C++ simulation code for fluid dynamics

Key problem:
Audiences may focus on UI flaws instead of technical achievement.

Important insight:
Implementation prototypes often accidentally become part of final systems — which can cause:
- Maintenance problems
- Poorly designed interfaces
- Rushed integration

---

## D. Integration Prototypes

Built to explore:
> What is the complete experience?

They integrate:
- Role
- Look & Feel
- Implementation

These:
- Are closest to final product
- Are most expensive
- Are hardest to build
- Simulate real user experience

Used for:
- User testing
- Organizational buy-in
- Evaluating coherence

Important insight:
Integration prototypes help resolve tensions between:
- What we want it to do
- How it should feel
- What we can technically achieve

---

# 6. Major Conceptual Shifts in the Paper

## Shift 1: From Fidelity to Purpose

Instead of asking:
- Is this low fidelity or high fidelity?

Ask:
- What dimension is this prototype exploring?

Resolution (amount of detail) and fidelity (closeness to final design) do NOT define purpose.

---

## Shift 2: Prototypes Are Communication Tools

Prototypes are not just design tools.
They are communication tools for:

- Design teams
- Users
- Managers
- Organizations
- The public

Different audiences require different levels of:
- Detail
- Realism
- Polish

---

## Shift 3: Build Multiple Prototypes

Because interactive systems are complex, one prototype cannot answer all questions early in design.

The 3D space-planning example shows:
- Role prototype
- Look & feel prototype
- Implementation prototype

Built in parallel.

This is critical:
You do not need one monolithic prototype early.
You need focused experiments.

---

# 7. Audience Matters (Very Important Essay Point)

Prototype effectiveness depends on audience.

Design team:
- Understand abstraction
- Can interpret rough sketches

Managers:
- May expect technical proof

Public:
- Needs high resolution, realistic representations

Example:
Knowledge Navigator video was high-production because audience was broad.

Key idea:
The required “fidelity” depends more on audience than on design stage.

---

# 8. Key Warnings from the Authors

1. Prototypes are not self-explanatory.
2. Audiences misunderstand purpose.
3. Implementation prototypes may distract from real focus.
4. Rough prototypes may be misinterpreted.
5. High-resolution prototypes may be mistaken as finished products.

Designers must:
- Explicitly state what questions are being explored.
- Explicitly state what questions are NOT being explored.

---

# 9. Practical Takeaways for Essay Answers

You should be able to explain:

### 1. Why current terminology (low/high fidelity) is insufficient.
Because it focuses on surface attributes, not design questions.

---

### 2. The three dimensions clearly and distinctly.

Role → function in life  
Look & Feel → sensory experience  
Implementation → technical realization

---

### 3. Why multiple prototypes are often better than one.

Because:
- Design questions are interdependent.
- Early integration is inefficient.
- Focused exploration is more productive.

---

### 4. Why audience awareness is crucial.

Prototype interpretation depends on:
- Organizational culture
- Design literacy
- Expectations

---

### 5. Why purpose-driven prototyping improves design quality.

Because:
- It clarifies what is being tested.
- It reduces wasted effort.
- It improves communication.
- It supports strategic thinking.

---

# 10. Short Jargon Glossary

Fidelity  
→ How closely a prototype resembles the final product.

Resolution  
→ Amount of detail in a prototype.

Wizard of Oz technique  
→ Simulating system intelligence using a hidden human.

Integrated prototype  
→ A prototype that combines role, look & feel, and implementation.

Role prototype  
→ A prototype focused on what the artifact does in a user’s life.

Look and feel prototype  
→ A prototype focused on interaction and sensory experience.

Implementation prototype  
→ A prototype focused on technical feasibility.

Artifact  
→ The system being designed.

---

# 11. One-Sentence Thesis of the Paper

Prototypes should be understood not by how polished they are or what tools were used, but by what aspects of an interactive artifact’s design — role, look and feel, or implementation — they are intended to explore.

---

# Prototyping Tools and Techniques – Detailed Quiz Notes
(Based on Beaudouin-Lafon & Mackay, "Prototype Development and Tools" :contentReference[oaicite:0]{index=0})

---

# 1. What is a Prototype?

## Definition
A **prototype** is a *concrete representation of part or all of an interactive system*.  
It is a **tangible artifact**, not just an abstract description.

It allows:
- Designers
- Developers
- Managers
- Customers
- End-users

to **see, interact with, and reflect on** the future system.

### Important Distinction
Unlike architecture (scaled-down models), interactive system prototypes:
- Must present interaction at **full scale**
- May simulate limited data
- Must show realistic interaction techniques

---

# 2. Why Prototypes Matter in HCI

HCI (Human-Computer Interaction) combines:
- Science
- Engineering
- Design

Prototyping is primarily a **design activity**, but:
- Uses engineering to ensure feasibility
- Uses scientific methods to evaluate usability

---

# 3. Prototypes as Design Artifacts

Successful prototypes:

- Support **creativity**
- Help explore the **design space**
- Encourage **communication**
- Enable **early evaluation**

---

# 4. Four Dimensions of Prototypes (VERY IMPORTANT FOR ESSAYS)

You MUST remember these four:

## 1. Representation
Form of the prototype.

### Off-line (Paper Prototypes)
- No computer required
- Sketches, storyboards, mock-ups
- Cheap and fast
- Usually thrown away

### On-line (Software Prototypes)
- Run on computer
- Animations, simulations, scripted apps
- Higher cost
- Used later in design
- Often evolve into final system

⚠ Important argument:
Programmers often prefer coding early — but authors strongly argue that **off-line prototypes are faster and more creative in early stages**.

---

## 2. Precision

Precision = **Level of detail relevant to evaluation**

Not all details are equally important.

Example:
- Drawing a dialog box layout
- Writing nonsense text for labels
- Showing structure without final wording

Key insight:
A prototype can be detailed but not precise.

Precision increases over iterations.

Precision defines:
- What is fixed
- What is open for discussion

---

## 3. Interactivity

Interactivity = Degree to which users can interact.

Important idea:
Interactivity and precision are **orthogonal (independent)**.

### Levels of Interaction

#### Fixed Prototype
- Non-interactive
- Example: video clip

#### Fixed-Path Prototype
- Limited interaction
- User triggers predefined screens
- Good for scenarios

#### Open Prototype
- Supports many interactions
- Works like real system (partially)
- Often vertical prototypes

---

## 4. Evolution

Life-cycle of prototype.

### Rapid Prototypes
- Created quickly
- Thrown away
- Early design exploration

### Iterative Prototypes
- Evolve through several cycles
- Refine details
- Increase precision

### Evolutionary Prototypes
- Become part of final system
- Require strong architecture
- Used in Extreme Programming

Important Tension:
Exploring new ideas vs. committing to final architecture.

---

# 5. Prototypes in the Design Process

## User-Centered Design (UCD)

User-centered design:
- Users involved throughout
- From requirements → evaluation
- Iterative loops

Prototypes:
- Let users experience system early
- Reveal strengths and weaknesses
- Allow contextual evaluation

---

## Participatory Design

Users are partners, not just evaluators.

Misconception:
Designers give control to users.

Reality:
- Users understand context & real problems
- Designers balance trade-offs and alternatives

Prototypes act as:
- Shared communication tools
- Boundary objects between stakeholders

---

# 6. Design Space (CRITICAL CONCEPT)

## What is Design Space?

Design space =  
Set of possible design ideas + constraints.

Design process is:
- Cyclic
- Expansion (generate ideas)
- Contraction (select ideas)

Designers:
- Add ideas
- Remove ideas
- Sometimes redefine problem

Key insight:
Design is NOT linear refinement.
It is iterative expansion and contraction.

---

# 7. Expanding the Design Space

## Brainstorming

Goal:
- Quantity over quality
- No criticism
- Generate many ideas

Problems found in research:
- Production blocking
- Free-riding
- Evaluation apprehension

### Video Brainstorming

Participants:
- Act out ideas
- Record short clips
- Use mock-ups

Advantages:
- Forces concrete thinking
- Easier to remember
- Encourages participation
- Makes abstract ideas tangible

Purpose:
EXPAND design space.

---

# 8. Contracting the Design Space

After idea generation:

Designers must:
- Evaluate alternatives
- Reject some ideas
- Choose direction

Methods:
- Controlled experiments
- Usability testing
- Heuristic evaluation
- Scenario walkthroughs

### Video Prototyping (Different from video brainstorming)

Goal:
- Refine ONE design
- Show integrated interaction
- Evaluate design choices

Purpose:
CONTRACT design space.

---

# 9. Prototyping Strategies

## 1. Horizontal Prototype

Focus:
Entire interface layer.

Used to test:
- Consistency
- Coverage
- Redundancy

Often:
- UI without backend logic
- Built with interface builders

---

## 2. Vertical Prototype

Focus:
Single feature, full depth (UI → system)

Used to test:
- Technical feasibility
- Performance
- Algorithms

Often thrown away.

---

## 3. Task-Oriented Prototype

Based on:
Task analysis.

Implements:
Only features needed for specific tasks.

Combines:
- Horizontal breadth
- Vertical depth

---

## 4. Scenario-Based Prototype

Based on:
Realistic stories of use.

Includes:
- Typical events
- Errors
- Unusual cases
- Context

Steps:
1. Use scenario (real world)
2. Design scenario (with new system)
3. Prototype scenario

---

# 10. Rapid Prototyping

Goal:
Shorten prototype-evaluation cycle.

Speed depends on:
- Precision
- Interactivity
- Evolution

---

# 11. Off-line Rapid Prototyping Techniques

## Paper & Pencil

- Fastest method
- Use transparencies
- Post-it menus
- Simulate mouse with paper strip

Advantages:
- Very cheap
- Highly flexible
- Great for early stages

---

## Mock-ups

Physical 3D models.

Used for:
- Hardware
- Button placement
- Ergonomics
- Physical integration

Made from:
- Cardboard
- Foamcore

Helps visualize real-world use.

---

## Wizard of Oz

Definition:
Human secretly simulates system behavior.

Used when:
- System not yet implemented
- Natural language interfaces
- Complex AI behaviors

User believes:
They interact with real system.

Important for:
Testing before technical feasibility is solved.

---

## Video Prototyping

Steps:
1. Observe users
2. Create scenario
3. Create storyboard
4. Shoot video

Storyboard:
- Sequence of frames
- Like comic book
- Shows action + dialogue

Benefits:
- Forces detail thinking
- Documents interaction
- Can serve as specification

Advanced technique:
Live Wizard-of-Oz with cameras and projection.

---

# 12. On-line Rapid Prototyping

Used when:
- Dynamic interaction required
- Higher precision needed

---

## Non-Interactive Simulations

Animations only.

Tools:
- Macromedia Director
- Flash
- Photoshop layers
- AfterEffects

Good for:
- Showing visual effects
- Dynamic behavior

---

## Interactive Simulations

Example tools:
- HyperCard
- Director

HyperCard:
- Stack metaphor
- Cards
- Buttons
- Scripted with HyperTalk

Allows:
- Multiple path interaction
- Event-driven behavior

---

## Scripting Languages

Examples:
- Tcl/Tk

Characteristics:
- Interpreted
- Lightweight
- Rapid development
- Good for UI prototypes

Tk Widgets:
- Buttons
- Menus
- Scrollbars
- Canvas
- Text widget

Advantage:
Quick implementation of interactive prototypes.

---

# KEY TERMS (Simple Definitions)

Prototype → Concrete early version of a system  
Representation → Form of the prototype  
Precision → Level of detail relevant to evaluation  
Interactivity → How much user can interact  
Evolution → Prototype life-cycle  
Rapid prototype → Quick, throwaway prototype  
Iterative prototype → Refined through cycles  
Evolutionary prototype → Becomes final system  
Design space → All possible design ideas + constraints  
Horizontal prototype → Full UI layer  
Vertical prototype → One feature, full depth  
Task-oriented prototype → Based on specific tasks  
Scenario-based prototype → Based on realistic story  
Wizard of Oz → Human secretly simulates system  
Storyboard → Visual sequence of interaction  
Video brainstorming → Expanding ideas  
Video prototyping → Refining one design

---

# Essay Advice for Quiz

If asked:
- "Discuss the four dimensions" → Explain representation, precision, interactivity, evolution with examples.
- "Explain design space" → Emphasize expansion vs contraction.
- "Compare horizontal and vertical prototypes" → Breadth vs depth.
- "Discuss rapid prototyping techniques" → Separate off-line and on-line.
- "Explain role of prototypes in user-centered design" → Early evaluation + communication.

Always:
- Use examples (paper, Wizard of Oz, HyperCard)
- Explain WHY each technique is useful
- Mention trade-offs
- Connect to user-centered and participatory design



