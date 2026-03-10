# Exam 1 Readings: 

# 1.1: "The Psychopathology of Everyday Things" — Don Norman

---

## Core Argument

Bad design is the designer's fault, **not** the user's. When people fail to use a product correctly, the machine and its design are to blame. It is the duty of machines and those who design them to understand people — not the other way around.

> Engineers make the mistake of designing for people the way they *wish* people were, not the way they *actually are*.

---

## Two Most Important Characteristics of Good Design

- **Discoverability** — Can users figure out what actions are possible, and where/how to perform them?
- **Understanding** — What does it all mean? How is the product supposed to be used?

---

## Key Design Disciplines

| Discipline | Focus |
|---|---|
| **Industrial Design** | Form, material, function, and appearance of products |
| **Interaction Design** | How people interact with technology; understandability and usability |
| **Experience Design** | Quality and enjoyment of the total experience |
| **Human-Centered Design (HCD)** | A *philosophy/process* that puts human needs, capabilities, and behavior first |

---

## Fundamental Principles of Interaction

Discoverability results from five fundamental psychological concepts, plus one overarching principle:

### 1. **Affordances**

**Definition:** The relationship between the properties of an object and the capabilities of the agent that determines how the object *could possibly* be used.

- An affordance is **not a property** of an object — it is a **relationship** between object and user.
- Example: A chair *affords* sitting; it *affords* lifting (but only for someone strong enough).
- **Anti-affordance** — the prevention of interaction (e.g., glass blocks physical passage).
- Affordances can exist even if they are **not visible**.
- Originated from psychologist **J. J. Gibson** ("Gibsonian psychology").

### 2. **Signifiers**

**Definition:** Any perceivable signal or indicator that communicates appropriate behavior to a person — tells users *where* and *how* to act.

- Signifiers can be **deliberate** (a "Push" sign on a door) or **accidental/incidental** (a worn path through a field).
- More important to designers than affordances, because they directly communicate how to use the design.
- When hand-lettered signs have to be added to a product to explain its use → **bad design**.
- Key distinction:
    - **Affordances** = what actions are *possible*
    - **Signifiers** = *where* and *how* the action should be done

### 3. **Mappings**

**Definition:** The relationship between controls and the results of their actions.

- **Natural mapping** — taking advantage of spatial analogies so controls correspond directly to their effects.
    - Example: Move a control up to move an object up.
    - Example: Mercedes-Benz seat control shaped like the seat itself.
- Good mapping leads to immediate understanding with no need for labels.
- Some "natural" mappings are **culture-specific** — what feels natural in one culture may not in another.

### 4. **Feedback**

**Definition:** Communicating the results of an action back to the user.

- Must be **immediate** — even a tenth-of-a-second delay is disconcerting.
- Must be **informative** — not just a generic beep or light flash.
- **Too little feedback** → confusion (e.g., not knowing if elevator button was pressed).
- **Too much feedback** → annoyance and ignored signals (e.g., excessive alarms in hospital/cockpit).
- **Poor feedback** can be worse than no feedback — it is distracting, uninformative, and anxiety-provoking.
- Feedback must be **planned and prioritized**.

### 5. **Constraints**

Limit the range of possible actions to guide correct use. *(Covered in detail in later chapters.)*

### 6. **Conceptual Models** *(Most Important)*

**Definition:** A simplified explanation of how something works — doesn't need to be complete or accurate, just *useful*.

- Also called **mental models** when they reside in users' minds.
- A good conceptual model allows users to **predict** effects of their actions.
- Without a good model, users operate by rote — they cannot troubleshoot or handle novel situations.
- Example of **bad conceptual model**: The refrigerator with two interdependent controls labeled "Freezer" and "Refrigerator" — implies two independent systems, but they actually share one cooling unit.

---

## The System Image

**Definition:** The combined information available to a user about a product — what the device looks like, manuals, advertising, website, signifiers, etc.

- Forms a **triangle** between:
    1. **Designer's conceptual model** — how the designer intends the product to work
    2. **System image** — the product itself and all its communication
    3. **User's mental model** — developed through interaction with the system image
- Designers *cannot communicate directly* with users — the entire burden of communication falls on the system image.
- If the system image is incoherent or misleading → users build a **wrong mental model** → frustration and errors.

---

## Human-Centered Design (HCD)

**Definition:** A design philosophy that puts human needs, capabilities, and behavior first — then designs to accommodate them.

- Understanding comes primarily through **observation** (people are often unaware of their own needs).
- Core HCD principle: **avoid specifying the problem too early** — instead, iterate through repeated approximations and rapid testing.
- Good design requires good **communication**, especially when things go wrong.
- Designers must focus on cases where things **go wrong**, not just when things work as planned.

---

## The Paradox of Technology

> Technology offers the potential to make life easier, but added complexity increases frustration.

- More features → harder to learn and use.
- Example: The wristwatch evolved from a simple stem-controlled device to a complex multi-function gadget with unintuitive button combinations.
- The same technology that adds value also adds design burden.

---

## The Design Challenge

- Successful products must satisfy **multiple competing stakeholders**: engineers, marketers, manufacturers, support teams, buyers, and end users.
- Disciplines operating **independently** from each other cause major clashes.
- Solution: cross-disciplinary teams with representatives from all constituencies working together.
- The goal: products that are successful *and* that customers love.

---

## Key Examples to Remember

| Example | Concept Illustrated |
|---|---|
| "Norman Doors" — doors you push when you should pull | Poor discoverability, missing signifiers |
| Post office double-door trap | Anti-affordance misread; invisible hinges |
| Refrigerator with two interdependent controls | False conceptual model |
| Digital watch with 5 unlabeled buttons | No conceptual model; poor mapping |
| Scissors | Excellent use of affordances, signifiers, constraints, and mapping |
| Hotel sink stopper (push down to open) | Failed signifier — no way to discover the action |
| Rubber pipes blocking a service road | Misleading signifier / apparent anti-affordance |

---

## Quick-Reference: Affordances vs. Signifiers

| | **Affordances** | **Signifiers** |
|---|---|---|
| What they are | Possible interactions (relationships) | Perceivable signals/clues |
| Visibility required? | No — can be invisible | Yes — must be perceivable to work |
| Designer's concern | Lower priority | **Higher priority** |
| Example | A door can be pushed (the possibility exists) | A flat plate on the door telling you *where* to push |


# 1.1: "Historical Context" — I. Scott MacKenzie

---

## What is HCI?

**Human-Computer Interaction (HCI)** — the field concerned with how people interact with computing technology. It is essentially human factors, but narrowly focused on computing systems.

**Human Factors (Ergonomics)** — both a science and field of engineering concerned with human capabilities, limitations, and performance, and with designing systems that are efficient, safe, comfortable, and enjoyable. HCI is human factors applied specifically to computers.

HCI draws from: psychology (cognitive & experimental), sociology, anthropology, cognitive science, computer science, and linguistics.

**Empirical research** — research based on observation and experience, carried out in a way that allows results to be verified or refuted by other researchers. This book's focus is on **user studies as controlled experiments with human participants**.

---

## Key Terminology

**User study** — in this book's context, a formal experiment with human participants (not just an informal evaluation).

**ACM SIGCHI** — Association for Computing Machinery Special Interest Group on Computer-Human Interaction. The world's largest association of HCI professionals. Its annual conference, **"CHI"** (pronounced with a hard "k"), is the flagship event in HCI.

---

## Historical Timeline of Key Events

| Year | Event |
|---|---|
| 1945 | Vannevar Bush publishes "As We May Think" |
| 1962 | Ivan Sutherland develops *Sketchpad* |
| 1963 | Douglas Engelbart invents the computer mouse |
| 1981 | Xerox *Star* launched — first commercial GUI |
| 1982 | ACM SIGCHI formed |
| 1983 | First ACM SIGCHI (CHI) conference held in Boston |
| 1983 | Card, Moran, and Newell publish *The Psychology of Human-Computer Interaction* |
| 1984 | Apple *Macintosh* launched |

---

## Vannevar Bush — "As We May Think" (1945)

- Published in *The Atlantic Monthly*, July 1945.
- Bush was the U.S. government's Director of the Office of Scientific Research and advisor to President Roosevelt.
- Proposed a device called **memex** — a hypothetical machine for storing and navigating personal knowledge using **associative indexing** (selecting one item automatically leads to another).
- Memex is considered a conceptual precursor to **hyperlinks, bookmarks, and the World Wide Web**.
- Bush's "consequent maze" = today's **information overload**; his "momentarily important item" anticipates blogs and tweets.

---

## Ivan Sutherland — Sketchpad (1962)

- Developed as PhD research at MIT.
- A graphics system allowing users to manipulate geometric shapes on a display using a **light pen** — no typing required.
- **Significance:** Sketchpad was the **first direct manipulation interface** — users acted directly on objects rather than typing commands.

**Direct manipulation** (term coined later by Ben Shneiderman, 1983) — an interface style characterized by:
- Visibility of objects
- Incremental action
- Rapid feedback
- Reversibility
- Exploration
- Syntactic correctness of all actions
- Replacing language with action

---

## Douglas Engelbart — Invention of the Mouse (1963)

- Invented at the **Stanford Research Institute (SRI)**, Menlo Park, California.
- Designed to replace the light pen, which caused fatigue from being held in the air.
- The mouse produced two channels (x-y) of analog positioning data; a **cursor** on screen corresponded to the device's position (**device space** → **display space**).
- The interaction paradigm this enabled: **point-select** (or point-and-click).

### First Mouse User Study (English, Engelbart, and Berman, 1967)
- Arguably **HCI's first user study** — a controlled experiment comparing input devices.
- Devices compared: mouse, light pen, joystick (position-control), joystick (rate-control), knee-controlled lever, Grafacon.
- Measured: **access time** (hand from keyboard to device) and **motion time** (onset of cursor movement to final selection).
- **Result:** The mouse had the lowest error rate — less than half that of any other device. Light pen was slightly faster in motion time, but impractical for extended use.
- Study included an **independent variable** (input method, 6 levels) and two **dependent variables** (task completion time, error rate). Used **counterbalancing** for device order.
- Mouse was not commercialized until 1981 (Xerox Star). Engelbart later won the **ACM Turing Award (1997)** and **ACM SIGCHI Lifetime Achievement Award (1998)**.

---

## Xerox Star (1981)

- First **commercially released** computer system with a **GUI (Graphical User Interface)**.
- Featured **WIMP**: **W**indows, **I**cons, **M**enus, **P**ointing device.
- Supported **direct manipulation** and **WYSIWYG** (What You See Is What You Get) interaction.
- Used a **bit-mapped display** (images formed by mapping bits in memory to pixels) vs. the older character-mapped displays.
- Introduced the **desktop metaphor** — icons representing documents, folders, trays, etc. Users exploit existing knowledge from the office world to understand the interface.
- Designed as an **office automation system** — interaction centered on files, not programs (e.g., "open a document" not "invoke an editor").
- Used **event-driven programming** (not sequential programming) — the system responds to user actions in any order, rather than controlling the sequence.
- Despite its innovation, the Star was **not a commercial success** — it was expensive ($16,000), a closed architecture (only ran Xerox apps), and was a networked workstation, not truly a personal computer.

### Key Concepts from the Star

**Desktop metaphor** — applying real-world office concepts (folders, documents, trashcan) to the GUI to give users an immediate sense of how to interact.

**WYSIWYG** — What you see on screen is exactly what you get in output (e.g., printed document).

**Sequential programming** — commands execute in a fixed order under the system's control (used in command-line interfaces).

**Event-driven programming** — the system responds asynchronously to user actions in any order the user chooses (required for direct manipulation GUIs).

---

## Birth of HCI (1983)

Three key markers for 1983 as the birth year of HCI:

### 1. First ACM SIGCHI Conference (1983)
- Held in Boston; 59 technical papers presented.
- Full name: *ACM SIGCHI Conference on Human Factors in Computing Systems* — known as **"CHI"**.
- Peer-reviewed; overall acceptance rate historically ~24%.
- Brings together researchers (technical program) and practitioners (applying HCI in industry).

### 2. *The Psychology of Human-Computer Interaction* — Card, Moran, and Newell (1983)
- Published from work at **Xerox PARC**.
- Connected low-level human processes (perception, cognition, motor output) with computer interaction.
- Introduced the **Model Human Processor (MHP)** — a framework modeling the human as an information processor with:
    - Perceptual processor
    - Cognitive processor
    - Motor processor
    - Short-term memory and long-term memory
- Featured two key laws (covered more in later chapters):
    - **Hick's Law** — choice reaction time
    - **Fitts' Law** — rapid aimed movement (speed-accuracy tradeoff)
- Introduced the **GOMS model** and **Keystroke-Level Model (KLM)** — tools for predicting task completion times.
- **Recognition vs. recall** principle: menus require recognition; typing requires recall. Recognition is preferred in user interfaces, especially for novices.

**Model Human Processor (MHP)** — a simplified model of human cognition used to predict interaction times; treats human behavior as an information-processing activity with measurable cycle times.

**GOMS** — Goals, Operators, Methods, and Selection Rules. A modeling approach for predicting user interaction with an interface.

**Keystroke-Level Model (KLM)** — a simplified version of GOMS that predicts task time by summing the times for individual keystrokes and motor actions.

### 3. Apple Macintosh (1984)
- Launched January 24, 1984 (pre-announced December 1983).
- Featured a GUI, direct manipulation, point-select interaction, and a one-button mouse (simplicity — no confusion over which button).
- Truly personal and affordable ($2,500) — reached a mass consumer audience.
- Made the GUI mainstream; Microsoft Windows followed (first serious version: Windows 3.1 in 1992).

---

## Growth of HCI Research

- Initial research focused on **quality, effectiveness, and efficiency** of interfaces (e.g., GUI vs. command-line).
- Menu design was a classic early research topic: key question was **breadth vs. depth** in menu hierarchies.
    - **Breadth** — more items per level, fewer levels (e.g., 8×8 = 64 items)
    - **Depth** — fewer items per level, more levels (e.g., 2⁶ = 64 items)
- HCI research grew across computer science, psychology, cognitive science, industrial engineering, and sociology departments.

---

## Other Notable Works Mentioned

- **"Personal Dynamic Media"** — Kay and Goldberg (1977): Described the **Dynabook** concept — a portable personal computer. Never built, but conceptually preceded laptops, tablets, and e-books.
- **"The Computer for the 21st Century"** — Weiser (1991): Introduced **ubiquitous computing** — the idea that the most profound technologies disappear into everyday life.

---

## Quick-Reference: Key People

| Person | Contribution |
|---|---|
| **Vannevar Bush** | "As We May Think" (1945); proposed memex / associative indexing |
| **Ivan Sutherland** | Sketchpad (1962); first direct manipulation interface |
| **Douglas Engelbart** | Invented the mouse (1963); led HCI's first user study |
| **Ben Shneiderman** | Coined the term "direct manipulation" (1983) |
| **Card, Moran, Newell** | *The Psychology of HCI* (1983); MHP, GOMS, KLM, Hick's and Fitts' Laws |
| **Alan Kay** | Dynabook concept; led Smalltalk/MVC development at Xerox PARC |
| **Mark Weiser** | Coined "ubiquitous computing" (1991) |


# 1.2: Chapter 5 — David Joyner: The CHI of Teaching Online"

---

## Core Argument

Online learning environments have transformed the user interface into the classroom itself. This creates a unique intersection where **interface design decisions and learning design decisions are often indistinguishable**. HCI principles can — and should — be directly applied to the design of online courses.

Key tension: Interface design aims to support **immediate interaction**; learning design aims to support **long-term learning gains**. Applying one domain's principles to the other must be done carefully.

---

## Context: The Case Study

- A graduate-level **HCI course** at a major U.S. public university, delivered as part of an online MSCS program.
- Fully **asynchronous** — no required synchronous activities, no in-person attendance.
- ~200–250 students per semester; ~5–6 teaching assistants (1 TA per ~40 students).
- Completion rate: **92%** (program average: ~85%).
- Cost: ~$170/credit hour; full degree ~$6,100–$7,100.
- Proctored exams are open-book, open-note, and open for 3–4 days.

---

## The Four Main HCI Principles Applied to Online Learning

### 1. **Flexibility**

**Source definitions:**
- *Universal Design* (Story, Mueller, Mace): "The design accommodates a wide range of individual preferences and abilities."
- *Nielsen's Heuristic*: "Allow users to tailor frequent actions."

Three types of flexibility in this course:

**Geographic Flexibility** — students can participate from anywhere. Removes barriers unrelated to course content (e.g., needing to commute or relocate). Also supports equity for individuals with disabilities that prevent leaving the home.

**Temporal Flexibility** — students can work whenever they want. The course uses **asynchronous** tools (pre-recorded lectures, forums, peer review) so no live attendance is required. Forums generate 10,000+ posts per semester; ~80% from students, ~20% from instructor.

**Preference Flexibility** — students can watch lectures before or after attempting assignments, re-watch at any pace, or skip around. Participation credit can be earned through multiple routes: forum posts, peer reviews, giving course feedback, or participating in classmates' studies. This accommodates different personalities and schedules.

---

### 2. **Equity**

**Source definition:**
- *Universal Design*: "The design is useful and marketable to people with diverse abilities." Sub-guideline: "Provide the same means of use for all users: identical whenever possible, equivalent when not."

Three applications of equity:

**Equity Through Flexibility** — geographic and temporal flexibility expands the student population to those who cannot relocate, have scheduling constraints, chronic illness, caregiving responsibilities, or cannot afford traditional programs. The requirements are reduced to only those inherent to the content itself.

**Equity Through Admissions** — because the online program has no enrollment cap, any student meeting the minimum requirements is admitted (unlike on-campus programs that reject many qualified applicants due to limited seats). This expands access to students who are qualified but not top-ranked.

**Equity Through Anonymity** — students have considerable control over what they reveal about themselves. This matters because:
- Identity mismatches (gender, race) with computer science are known to reduce performance and engagement.
- **Stereotype threat** — merely being reminded of a stereotype can lessen performance (Good et al., 2003). Online environments reduce inherent signifiers of those stereotypes.
- Students have disclosed to instructors conditions (physical disabilities, speech impediments, behavioral disorders, obesity, transgenderism) that would heavily influence their in-person experience, but have no impact in the online environment.

---

### 3. **Consistency**

**Source definitions:**
- *Norman*: "Consistency in design is virtuous. It means that lessons learned with one system transfer readily to others."
- *Nielsen*: "Users should not have to wonder whether different words, situations, or actions mean the same thing. Follow platform conventions."
- *Constantine and Lockwood's Reuse Principle*: "Reduce the need for users to rethink and remember."

Applied as: set consistent expectations so students spend less cognitive effort on course logistics and more on course content.

**Assignment Cadence** — weekly deliverables directly tied to that week's lecture material. All lectures and assignment descriptions are available from the start of the semester (preserving flexibility), but weekly deadlines force regular engagement. Students know what to expect each week without re-reading the calendar — mirroring the consistency of attending in-person lectures.

**Announcement Cadence** — weekly announcements every **Monday morning** (preview of the week) and **Friday evening** (recap/key points). Replicates the effect of a professor entering the lecture hall. This is the **most praised** element of the course. Note: scheduling them to auto-send was tried but felt impersonal — students preferred knowing the instructor physically sent them.

**Administrative Consistency** — all deadlines fall on **Sunday at 11:59 PM UTC-12** ("Anywhere on Earth" time). Students only need to check once per week whether they've completed work. Few components are time-gated, reducing the cognitive effort of tracking multiple deadlines.

---

### 4. **Distributed Cognition**

**Definition:** Human cognitive tasks (reasoning, remembering, acting) can be offloaded onto an interface, reducing the cognitive load on the user. In an educational context: use the interface to reduce attention paid to course administration, freeing attention for course content.

**"Push" vs. "Pull" structure:**
- Traditional courses = **push** — instructor pushes information to students (announces in class, writes on board).
- Online courses = **pull** — information is available but students must actively retrieve it. This creates cognitive overhead.
- The course uses weekly announcements to **approximate the push dynamic** in an online environment.

**Offloading Through Announcements** — weekly announcements push administrative information (deadlines, what to do, recaps) to students, so students don't have to continuously monitor the course for updates.

**Offloading Through Documentation** — comprehensive course documentation is made available to all students. No single student reads all of it, but the community collectively covers it: if a student has a question answered in the documentation, a classmate will know the answer. Knowledge of course administration is distributed across the student body.

**Offloading Through Assessment Design** — exams are **open-book, open-note, open-video, open-forum**. Students are told in advance and encouraged to organize their resources. The system being assessed is the student + their resources + their environment, not just memory. Distributed cognition is simultaneously a lesson taught, a principle students apply, and a theory used to evaluate the course design.

---

## Additional Principles

### **Structure**
Pre-produced video lectures allow material to be organized around the actual structure of the content, rather than forced into a prescribed lecture schedule.

### **Perceptibility**
Nielsen: "The system should always keep users informed about what is going on, through appropriate feedback within reasonable time." Applied as: students have persistent access to the gradebook for real-time visibility of their standing. This is a **pull** behavior — students access it when relevant rather than being pushed grade updates.

### **Tolerance**
*Universal Design*: "Minimizes hazards and the adverse consequences of accidental or unintended actions." Applied as:
- A **2-hour hidden grace window** after the official deadline for late submissions (accounts for timezone conversion errors, upload issues, etc.).
- Grading workflow designed to accept genuinely late submissions without penalizing the grading team's time.

### **Feedback**
Norman: "Feedback must be immediate… Poor feedback can be worse than no feedback at all, because it is distracting, uninformative, and anxiety-provoking." Applied as:
- Assembly-line grading workflow enables faster return of grades than typical on-campus courses.
- Peer review incentive: **1.5 points** for review within 3 days of deadline; **0.5 points** for review more than a week late. 58% of peer reviews submitted within 3 days as a result.

---

## Key Special Terms

**Desirable difficulties** (Bjork, 2013) — challenges in learning that, while initially frustrating, lead to better long-term retention. Interface designers must not remove all friction, because some friction is pedagogically valuable.

**Stereotype threat** — the phenomenon where reminding someone of a negative stereotype about their group can measurably reduce their performance.

**Asynchronous learning** — education that does not require participants to be online or present at the same time. Contrasts with **synchronous** (real-time/live) learning.

**MOOC** — Massive Open Online Course. Large-scale online education with open access, which inspired elements of this program's design.

---

## Course Evaluation Findings

- Instructor rated highly on enthusiasm (~4.96/5), respect (~4.96/5), and availability (~4.90/5) — notable because online instructors are often perceived as detached.
- Ratings remained stable across semesters even as the course underwent significant revisions.
- Students frequently re-watched lectures (median "occasionally" for full re-watch; "frequently" for partial re-watch) — consistent with supporting attentional or sensory differences.
- A non-trivial minority watched ahead, fell behind, or used flexible viewing behaviors — validating the flexibility design decisions.

---

## Quick Summary: HCI Principle → Course Application

| HCI Principle | Course Application |
|---|---|
| **Flexibility** | Geographic, temporal, and preference flexibility in how/when students engage |
| **Equity** | Open admissions, no required in-person elements, pseudo-anonymity reducing stereotype threat |
| **Consistency** | Weekly assignment cadence, Monday/Friday announcements, single Sunday deadline |
| **Distributed Cognition** | Push announcements, full documentation, open-book exams |
| **Feedback** | Fast grading workflow, early peer review incentives |
| **Tolerance** | Hidden 2-hour grace window, flexible late submission workflow |
| **Perceptibility** | Persistent gradebook access |


# 2.1: Chapter 3: "Cognitive Engineering"
*Donald A. Norman*
*From: User Centered System Design: New Perspectives on Human-Computer Interaction (1986)*

---

## What is Cognitive Engineering?

> "A type of applied Cognitive Science, trying to apply what is known from science to the design and construction of machines."

- NOT Cognitive Psychology, NOT Cognitive Science, NOT Human Factors — a hybrid
- Two major goals:
    1. Understand the fundamental principles behind **human action and performance** relevant to engineering design
    2. Devise systems that are **pleasant to use** — not just efficient, easy, or powerful, but what Laurel calls **"pleasurable engagement"**

---

## Core Problem: Psychological vs. Physical Variables

The central tension in all of Cognitive Engineering:

> **Psychological variables** = what the person *cares about* (goals, intentions) — exist in the mind  
> **Physical variables** = what the system actually *controls* — mechanisms, states, outputs

The person must:
1. Translate **psychological goals → physical actions** (to do something)
2. Translate **physical system state → psychological interpretation** (to understand what happened)

### Key Examples of the Mismatch

**Bathtub faucets**: User wants to control *total flow rate* and *temperature* (psychological). The system controls *hot water rate* and *cold water rate* (physical). Three resulting problems:
1. **Mapping problems** — which control is hot/cold? which way increases/decreases?
2. **Ease of control** — changing temperature while keeping flow constant requires simultaneous manipulation of both faucets
3. **Evaluation** — with two spouts, hard to determine if correct outcome was reached

Solution: single-control faucets that directly vary psychological factors (one dimension = flow rate, another = temperature). Still has a mapping problem but much better overall.

**Refrigerator-freezer controls**: Two psychological variables (freezer temp, fresh food temp) but only *one* cooling mechanism with controls that interact. Four simultaneous problems:
1. Labels don't match actual physical function
2. Strong interaction between the two controls — no simple mapping
3. Very slow feedback (24-hour delay) — can't connect action to result
4. No conceptual model — instructions are opaque

---

## Table 3.1 — Aspects of a Task (Memorize This)

| Aspect | Description |
|---|---|
| **Goals and intentions** | Goal = desired state; Intention = decision to act to achieve the goal |
| **Specification of the action sequence** | The psychological process of determining the actions to be executed on the mechanisms |
| **Mapping from psychological goals/intentions to action sequence** | Translating goals → desired system state → control settings → physical manipulations |
| **Physical state of the system** | Determined by the values of all physical variables |
| **Control mechanisms** | The physical devices that control the physical variables |
| **Mapping between physical mechanisms and system state** | The relationship between mechanism settings and resulting system state |
| **Interpretation of system state** | Translating physical state → psychological states (perception), then interpreting in terms of psychological goals |
| **Evaluating the outcome** | Comparing interpreted system state with desired goals → often leads to new goals/intentions |

---

## The Two Gulfs (Central Framework)

The discrepancy between psychological and physical variables creates two gulfs that must be bridged:

```
         GULF OF EXECUTION
GOALS ─────────────────────────→ PHYSICAL SYSTEM
         GULF OF EVALUATION
PHYSICAL SYSTEM ───────────────→ GOALS
```

Each Gulf is **unidirectional**.

### Gulf of Execution
The gap from **goals → physical system**.  
Bridged in **four segments** (from psychological side):
1. **Intention formation**
2. **Specifying the action sequence**
3. **Executing the action**
4. **Making contact with the input mechanisms of the interface**

Bridged from **system side**: designer builds the **input characteristics** of the interface.

### Gulf of Evaluation
The gap from **physical system → goals**.  
Bridged in **four segments** (from physical side):
1. Starting with **output displays** of the interface
2. **Perceptual processing** of those displays
3. **Interpretation**
4. **Evaluation** — comparing interpreted system state with original goals/intentions

Bridged from **system side**: designer builds the **output characteristics** of the interface.

> Key insight: Both gulfs can be bridged from *either direction*. The designer can move the system closer to the user (better interface design); the user can move closer to the system (training and experience).

---

## Seven Stages of User Activity

A convenient approximation of performing and evaluating an action (Figure 3.3):

**Execution side (3 stages):**
1. Establishing the **Goal** ← central, primary stage
2. Forming the **Intention**
3. Specifying the **Action Sequence**
4. Executing the **Action** ← first physical action

**Evaluation side (3 stages):**
5. Perceiving the **System State**
6. Interpreting the **State**
7. Evaluating the **System State** with respect to Goals and Intentions

> Note: Norman originally proposed 4 stages; this chapter expanded to 7. The stages are a simplification — real activity does not progress as a clean sequence. Stages can appear out of order, be skipped, or repeated. Also, sometimes the person is **reactive** (event/data-driven), not goal-driven.

### Symmetry of the 7 Stages
- Perception ↔ Execution (both physical)
- Interpretation ↔ Action Sequence (both translational)
- Evaluation ↔ Intention formation (both comparative/judgmental)

### Word-Processor Example (Figure 3.4)
Goal: "Improve appearance of letter" → Intention1: improve appearance → Intention2: change to block paragraphs → Intention3: change .pp to .sp → Action Specification → Execution → Perception → Interpretation → Intention4: format the file → Execution 2 → Evaluation

Shows: Even simple-seeming intentions spawn multiple sub-intentions. The stages are not linear.

---

## Conceptual Models and the System Image

Three distinct concepts — two mental, one physical:

| Concept | Description |
|---|---|
| **Design Model** | The designer's conceptualization of the system to be built; ideally based on user's task, requirements, capabilities, and cognitive limitations (especially STM) |
| **User's Model** | The mental model formed by the user; NOT formed from the Design Model directly — it results from the user interpreting the System Image |
| **System Image** | The physical image of the system as built — everything the user interacts with: knobs, dials, keyboards, displays, documentation, instruction manuals, help facilities, error messages |

> **Critical insight**: The User's Model does NOT come from the Design Model. It comes from the System Image. Therefore, the designer's primary task is to construct an appropriate System Image so that the User's Model will be compatible with the Design Model.

### Mental Models
- People form internal mental models of themselves and things they interact with
- They provide **predictive and explanatory power**
- Evolve naturally through interaction
- Are neither **complete nor accurate** — but they function to guide much human behavior
- The conceptual model acts as a **scaffolding** for bridging the gulfs — most important during learning and troubleshooting

### Good Examples Where User's Model Matches Design Model
- **Spreadsheets** (starting with VISICALC) — matched the accountant's conceptualization
- **Hewlett-Packard stack calculator**
- **"Office desk" metaphor** — Xerox Star, Apple Lisa, Macintosh

> Easier to design consistent Design Models for specialized tools. Harder for general-purpose systems with unlimited users.

---

## Quality of Human-Computer Interaction

Norman's design philosophy: not just *correct* and *easy* — but **enjoyable to use**.

This requires:
- Systems that provide a strong sense of **understanding and control**
- Tools that **reveal their underlying conceptual model**
- What Illich (1973) calls **"convivial tools"**

**"Pleasurable engagement"** (Laurel) = complete and full engagement of the person in pursuit of the "end cause" of the activity; the computer should be **invisible** to the user.

### The Power-of-Tools Problem
- Systems that take **too much control** → "overautomation" → user becomes a passive observer, loses feeling of control → serious social/psychological problem
- Systems that are **too primitive** → too large a gap in mappings → user feels out of control from the opposite direction

> The tension: desire for intelligent systems that compensate for our inadequacies vs. the desire to feel in control of the outcome.

### "The Problem of Level"
Tools that are **too primitive** = too much skill required (Turing machine example = "Turing tarpit").  
Tools that are **too high-level** = too specialized (apple-peeler, spelling checker).
> "The level of the tool has to match the level of the intention."

---

## Design Issues

### Tradeoffs
Every design is a series of tradeoffs — benefits in one dimension typically cause deficits in another. There are no correct answers, only tradeoffs. However: there IS a worst solution, and some designs are clearly better than others across all dimensions.

**The prototypical tradeoff: information vs. time**  
Factors that increase informativeness decrease available workspace and system responsiveness. More informative display = more useful for confused users BUT slower to display, uses more space, impedes experienced users. "User friendly" has taken on a negative meaning from badly engineered tradeoffs.

**The beginner vs. expert tradeoff**: Extra information required by beginners is disruptive to experienced users — it can't simply be ignored, it takes screen space and display time.

### First-order vs. Second-order Issues
With limited time and resources, distinguish **big issues (first-order)** from **small issues (second-order)**.

> Norman's position: **Conceptual models are first-order.** The Design Model and System Image are first-order. Get these right first; then worry about second-order issues like command names.

**VISICALC example**: Command structure was cryptic and poorly named. But VISICALC succeeded anyway because:
1. The **conceptual model** (the spreadsheet) was a breakthrough that matched accountants' mental models perfectly
2. The system was **self-contained** (no conflicts with other programs' command conventions)
3. Users were **frequent/practiced** users (cryptic commands become automatic with practice; poor naming only matters when systems are used by beginners or casually)

### The Five-Slot Approximate Model of Short-Term Memory (STM)
Norman's example of a useful approximate model for design:
> STM consists of **5 slots**, each holding one item. Each item decays with a **half-life of 1.5 seconds**. Most information is lost from STM through **interference** (new information taking up available slots).

Even though wrong in its details, this model is practically valuable for design.

---

## Prescriptions for Design Principles

Norman's four prescriptions:

1. **Create a science of user-centered design** — need design principles applicable at design time, before construction; approximate methods suffice

2. **Take interface design seriously as an independent and important problem** — requires three kinds of knowledge:
    - Knowledge of design, programming, and technology (programmers have this)
    - Knowledge of people, cognition, communication, interaction (psychologists have this)
    - Expert knowledge of the task being accomplished (users have this)
      → User-centered design requires collaboration across all three

3. **Separate the design of the interface from the design of the system** — principle of modularization; only the interface module should communicate with the user; enables iterative design without disrupting the rest of the system

4. **Do user-centered system design: Start with the needs of the user** — "From the point of view of the user, the interface IS the system." Let user requirements drive interface design; let interface ideas drive technology.

---

## Key Terms Summary

| Term | Definition |
|---|---|
| **Cognitive Engineering** | Applied cognitive science for designing machines; combines psychology + computer science |
| **Gulf of Execution** | The gap from goals to physical system; the challenge of translating intentions into actions |
| **Gulf of Evaluation** | The gap from physical system to goals; the challenge of interpreting system state in terms of goals |
| **Psychological variables** | What the person cares about; goals and intentions in the person's mind |
| **Physical variables** | What the system actually controls; mechanism states and outputs |
| **Design Model** | Designer's conceptualization of the system |
| **User's Model** | Mental model the user forms from the System Image |
| **System Image** | The physical structure of the system as built, including all documentation and displays |
| **Convivial tools** | Tools that reveal their conceptual model, emphasize comfort, ease, and pleasure of use (Illich, 1973) |
| **Pleasurable engagement** | Complete and full engagement of the person in pursuit of an activity (Laurel) |
| **Overautomation** | When a system takes too much control, making the user a passive observer with no feeling of control |
| **First-order issues** | The primary concerns in design — the conceptual model, Design Model, System Image |

---

## Key Quotes

- "The goal is neither efficiency nor ease nor power... but rather systems that are pleasant, even fun."
- "The correct conceptual model can transform confusing, difficult tasks into simple, straightforward ones."
- "Two variables: two controls. Who could believe that it would be so difficult?" (refrigerator example)
- "Mental models are neither complete nor accurate... but nonetheless they function to guide much human behavior."
- "From the point of view of the user, the interface IS the system."
- "There are no correct answers, only tradeoffs among alternatives."
- "It clearly is possible to design a bad system. Equally, it is possible to avoid bad design."
- "The level of the tool has to match the level of the intention."

# 2.2: The Psychology of Everyday Actions - Don Norman

---

## Key Concept: Blame the Design, Not the User

- When people fail to use everyday objects, they tend to **blame themselves** — this is usually wrong.
- Difficulties with everyday devices typically result from **poor design**, not user incompetence.
- The designer's job is to make objects understandable and usable by people.

---

## The Two Gulfs

### **Gulf of Execution**
> "How do I work this? What can I do?"

The difficulty a user faces in figuring out **how to operate** a device. Bridged through:
- **Signifiers** — perceivable signals of what actions are possible
- **Constraints** — limits that guide correct actions
- **Mappings** — relationship between controls and their effects
- **Conceptual model** — user's mental picture of how the system works

### **Gulf of Evaluation**
> "What happened? Is this what I wanted?"

The difficulty a user faces in **interpreting the state** of a device after an action. Bridged through:
- **Feedback** — information about what happened
- **Conceptual model** — helps user interpret results

---

## The Seven Stages of Action

A framework describing how people perform and evaluate actions. Consists of **1 goal, 3 execution stages, 3 evaluation stages**.

| # | Stage | Description |
|---|-------|-------------|
| 1 | **Goal** | Form the goal — what do I want to accomplish? |
| 2 | **Plan** | Plan the action — what are the alternatives? |
| 3 | **Specify** | Specify an action sequence — what can I do now? |
| 4 | **Perform** | Perform the action sequence — how do I do it? |
| 5 | **Perceive** | Perceive the state of the world — what happened? |
| 6 | **Interpret** | Interpret the perception — what does it mean? |
| 7 | **Compare** | Compare outcome with goal — is this okay? |

### Types of Behavior
- **Goal-driven behavior** — cycle starts from the top (the goal), then moves through execution stages
- **Event-driven / Data-driven behavior** — cycle starts from the bottom (the world), triggered by external events
- **Opportunistic actions** — behavior that takes advantage of circumstances rather than explicit planning; less mental effort but less precise

### Root Cause Analysis
Repeatedly asking **"Why?"** until the ultimate cause of an activity is found. Example: the goal isn't to drill a hole — it's to hang shelves — or ultimately, to store books.

---

## Human Thought: Mostly Subconscious

- Most human behavior is **subconscious** — we are unaware of how we do things.
- **Cognition and emotion cannot be separated** — cognitive thoughts drive emotions; emotions drive cognitive thoughts.
- We often use logic and reasoning **after the fact** to justify decisions already made subconsciously.

### Subconscious vs. Conscious Thought

| Feature | **Subconscious** | **Conscious** |
|--------|-----------------|---------------|
| Speed | Fast | Slow |
| Control | Automatic | Controlled |
| Resources | Multiple | Limited |
| Best for | Skilled/routine behavior | Novel situations, learning, danger |

---

## Three Levels of Processing (Cognition & Emotion)

### **Visceral Level**
- Most basic; sometimes called "the lizard brain"
- Responds to **immediate sensory input** — good/bad, safe/dangerous
- Fast, automatic, **subconscious**
- No context or history considered; just the present moment
- Controls fight-or-flight and physical tension
- Relevant to designers for: **aesthetics, appearance, immediate appeal**

### **Behavioral Level**
- Home of **learned skills** triggered by pattern matching
- Largely **subconscious** — we're aware of actions but not the details
- Driven by **expectations** — positive expected outcomes = positive affect; negative = anxiety/dread
- **Feedback** resolves expectations → leads to satisfaction or frustration
- Relevant to designers for: **usability, interaction, feedback**

### **Reflective Level**
- Home of **conscious cognition** — reasoning, decision-making, deep understanding
- Slow; often occurs *after* events have happened
- Where **highest-level emotions** occur: guilt, pride, blame, praise
- Drives memory of experiences and recommendations of products
- Relevant to designers for: **long-term impressions, brand loyalty, meaning**

> **Design must take place at ALL three levels.**

---

## The Flow State

- Defined by psychologist **Mihaly Csikszentmihalyi**
- Occurs when task difficulty **just slightly exceeds skill level** — requires full attention but doesn't cause frustration
- Person loses track of time; fully immersed in the task
- Too easy → boredom/apathy; Too hard → frustration/anxiety/helplessness

---

## People as Storytellers & Conceptual Models

- Humans are **innately disposed** to find causes and form explanations (stories)
- **Conceptual model** — a person's mental model of how something works, often built from fragmentary evidence
    - Can be accurate or **faulty/folk models**
    - Example: people often believe thermostats work like valves (more = more heat) — this is **wrong**; most thermostats are simply on/off switches

---

## Blaming the Wrong Things

- People assign causality when two events occur in close succession, **even if unrelated**
- When feedback is delayed, users assume their action wasn't registered and **repeat it**, sometimes with more force — can cause unintended results
- Good design provides feedback **within 0.1 second** of any operation
- When delays are unavoidable, progress indicators (loading bars, spinners) reassure users
- **Underpredicting** completion time is preferred — meeting or beating an estimate creates a positive response

---

## Learned Helplessness

- **Learned helplessness** — after repeated failure at a task, a person concludes they are incapable and stops trying
- Can generalize across all similar tasks (e.g., all technology, all math)
- Often caused by poor design, but the **user blames themselves**
- Can be considered **"taught helplessness"** when bad design systematically produces failure

### Positive Psychology Antidote
- Replace "failure" with **"learning experience"**
- Design firm **IDEO** creed: *"Fail often, fail fast"* — failures teach more than successes
- Designers should not blame users; user difficulties are **signifiers of where the product can be improved**

---

## Falsely Blaming Yourself

- When people can't use something, they typically **blame themselves** (not the design)
- This creates a **conspiracy of silence** — nobody reports problems because they feel it's their own fault
- "Human error" is usually **system error / design error**
- Systems should be designed so a single mistake by one person cannot cause catastrophic results

### Designer's Credo
- Eliminate the term **"human error"** — reframe as bad communication or interaction
- Machines should accept **normal human behavior**, not force abnormal precision
- Use **affordances, signifiers, good mapping, and constraints** to prevent mistakes
- Provide **clear feedback and conceptual models** so users can recover from errors

---

## Seven Fundamental Design Principles (from the 7 Stages)

| # | Principle | Description |
|---|-----------|-------------|
| 1 | **Discoverability** | It is possible to determine what actions are possible and the current state |
| 2 | **Feedback** | Full, continuous info about results of actions and current state |
| 3 | **Conceptual model** | Design communicates enough info to build an accurate mental model |
| 4 | **Affordances** | Proper affordances exist to make desired actions possible |
| 5 | **Signifiers** | Effective use of signifiers ensures discoverability and communicates feedback |
| 6 | **Mappings** | Controls and their effects follow good spatial/temporal mapping |
| 7 | **Constraints** | Physical, logical, semantic, and cultural constraints guide actions |

---

## Feedforward vs. Feedback

- **Feedforward** — information that helps the user know **what they can do** (execution side); achieved through signifiers, constraints, mappings, and conceptual models
- **Feedback** — information about **what happened** (evaluation side); achieved through explicit results display and conceptual models

---

## Key Terms Quick Reference

| Term | Definition |
|------|------------|
| **Gulf of Execution** | The gap between a user's goal and knowing how to operate a device |
| **Gulf of Evaluation** | The gap between a device's state and understanding whether the goal was met |
| **Conceptual model** | A user's mental model of how a system works |
| **Feedforward** | Information that tells the user what actions are available |
| **Feedback** | Information that tells the user what happened after an action |
| **Visceral level** | Subconscious, fast, sensory-based processing; immediate reactions |
| **Behavioral level** | Subconscious learned skills; driven by expectations and patterns |
| **Reflective level** | Conscious reasoning, long-term evaluation; highest-level emotions |
| **Flow state** | State of complete immersion in a task at just the right difficulty level |
| **Learned helplessness** | Giving up after repeated failure, believing one is incapable |
| **Root cause analysis** | Repeatedly asking "Why?" to find the true underlying goal/cause |
| **Opportunistic actions** | Unplanned behavior triggered by circumstances rather than explicit goals |
| **Goal-driven behavior** | Action cycle starts from a conscious goal |
| **Event-driven behavior** | Action cycle starts from a world event triggering evaluation |

# 2.3: Direct Manipulation Interfaces
## Hutchins, Hollan & Norman (1985) — HCI Quiz Notes

---

## Overview

This paper seeks a **cognitive account** of why direct manipulation interfaces feel natural (or don't). The core claim: the feeling of **directness** results from committing fewer cognitive resources. More cognitive effort = more indirectness.

> Direct manipulation is not a unitary concept — "directness" is a **feeling or impression** about an interface, not a measurable property.

---

## What is Direct Manipulation?

Term coined by **Shneiderman (1974, 1982, 1983)**. A direct manipulation system has:

1. **Continuous representation** of the object of interest
2. **Physical actions or labeled button presses** instead of complex syntax
3. **Rapid, incremental, reversible operations** whose impact is immediately visible

### Shneiderman's Claimed Virtues
- Novices learn basic functionality quickly (often through demonstration)
- Experts can work rapidly and even define new functions
- Knowledgeable intermittent users can retain operational concepts
- Error messages are rarely needed
- Users can immediately see if actions are furthering their goals
- Users have reduced anxiety because actions are easily reversible

---

## Two Aspects of Directness

### 1. **Distance**
The gap between the user's thoughts/goals and the physical requirements of the system. A **short distance** means thoughts are easily translated into actions and system output is easily interpreted.

- Directness is **inversely proportional** to cognitive effort
- Cognitive effort is a direct result of the **Gulfs of Execution and Evaluation**
- Distance is never a property of the interface alone — it depends on the **relationship between the task and the interface**

### 2. **Direct Engagement**
The qualitative feeling that you are directly manipulating the objects of interest — not the programs or the computer. Also called **"first-personness"** (Laurel, 1986).

Two metaphors for HCI:

| Metaphor | Description |
|----------|-------------|
| **Conversation metaphor** | Interface is a language medium; user and system converse about an implied but not explicitly represented world. Interface acts as **intermediary**. |
| **Model-world metaphor** | Interface **is** the world; the user acts directly upon explicitly represented objects. No intermediary. Supports direct engagement. |

> The model-world metaphor can create the sensation of acting upon task domain objects themselves. This is **direct engagement**.

---

## Two Forms of Distance

Every interaction uses an **interface language** (input and output). These two forms of distance describe how hard it is to bridge the gap between user goals and interface expressions.

### 3.1 **Semantic Distance**
The relationship between the **meaning** of an expression in the interface language and what the user wants to say.

Two key questions:
1. *Is it possible to say what you want to say in this language?* Does the language support the user's conception of the task domain?
2. *Can the thing be said concisely?* Or must the user construct a complicated expression to accomplish a conceptually simple task?

- **Gulf of Execution (semantic):** How much structure must the *user* provide vs. the *system*? More user-provided structure = greater semantic distance.
- **Gulf of Evaluation (semantic):** If output is not in terms of the user's intention, the user must mentally translate it. Example: showing a water level value (not rate of change) forces the user to compute rate mentally — high semantic distance.

### 3.2 **Articulatory Distance**
The relationship between the **physical form** of an expression and its **meaning**.

- Input examples: key presses, mouse movement, speech
- Output examples: character strings, icon changes, audio signals
- Low articulatory distance = the form of the action *resembles* the intended meaning (like **onomatopoeia** in language — "boom", "splash")
- Example of articulatory directness: **moving a mouse to move a cursor** — the action mimics the result

> A moving graphical display has high articulatory directness. A table of numbers showing the same data has low articulatory directness — even if they are semantically equivalent.

### Relationship Between the Two
| Distance Type | Concerns | Bridged By |
|--------------|----------|------------|
| **Semantic** | Meaning of expression ↔ user's intention | Higher-level languages, better output representations |
| **Articulatory** | Physical form of expression ↔ its meaning | Mimetic input (mouse, touch), graphical/visual output |

---

## Reducing Semantic Distance

### From the System Side
- **Higher-level languages** — match the language of the interface to the language of the task domain. Trade-off: **gains specificity but loses generality**. Example: Lisp, UNIX (become massive, hard to learn)
- **WYSIWYG displays** — show semantic concepts directly in output (e.g., screen-oriented text editors, spreadsheets)

### From the User Side
- **Automated behavior** — with practice, users automate mediating structures so they no longer feel the cognitive effort. Important caveat: **automatization does NOT reduce semantic distance** — the gulfs still exist, the user just crosses them faster. The system should not get credit for work the user has done through practice.
- **User adapts to system representation** — users change how they think about a task to match the system's model (related to **linguistic determinism**). Risk: may restrict how users can think about the domain.

### Virtuosity
Expert users sometimes "misuse" limited interfaces to accomplish goals beyond what designers intended. The semantic directness of an interface **changes with the task** — a piano is more semantically direct for producing notes; a violin for expressive performance.

---

## Direct Engagement (Section 4)

Occurs when the user experiences direct interaction with domain objects. The interface and computer become **invisible**.

### Minimum Requirements for Direct Engagement:
1. Execution and evaluation must exhibit both **semantic and articulatory directness**
2. Input and output languages must be **inter-referential** (an input expression can incorporate a previous output expression) — this creates the illusion of directly manipulating the objects
3. System must be **responsive** — no unnatural delays
4. Interface must be **unobtrusive** — if the interface is noticed, it breaks the feeling of engagement

### Inter-Referential I/O (Draper, 1986)
When input and output expressions can refer to each other. Key to creating the illusion that you are directly manipulating the objects, not representations of them.

### Naive Realism (DiSessa, 1985)
The user can assume that the output expressions, in some sense, *are* the things they refer to.

---

## A Space of Interfaces (Section 5)

Interfaces can be mapped on two dimensions:

| Dimension | Range |
|-----------|-------|
| **Distance from user goals** | Large (low-level language) → Small (direct manipulation) |
| **Engagement** | Interface as conversation → Interface as model world |

The **most direct interface** = maximum engagement + minimum semantic and articulatory distance.

| Interface Type | Distance | Engagement |
|----------------|----------|------------|
| Low-level language | Large | Conversation |
| High-level language | Small | Conversation |
| Low-level world | Large | Model world |
| **Direct manipulation** | Small | Model world |

---

## Problems with Direct Manipulation (Section 6)

Direct manipulation is **not a panacea**. Key limitations:

- **Repetitive tasks** are better handled via scripts (symbolic descriptions), not direct manipulation
- Difficulty handling **variables** or distinguishing individual elements from a class/set
- **Accuracy problems** — mimetic actions put precision burden on the user
- **Loss of generality** — matching interface to a specific domain restricts what can be done outside that domain
- **Restricts new thinking** — if the interface only mirrors how we already think, it misses the potential of technology to provide **new ways of thinking** about a domain
- **Directness ≠ ease of use** — if the interface is truly invisible, difficulties in the *task domain* are transferred directly to the user. The system doesn't help users who lack domain knowledge.
- **Some abstractions are easier in language** — certain complex or abstract tasks (e.g., variable scoping in programming) are very difficult to represent in a direct manipulation environment

---

## Key Terms Quick Reference

| Term | Definition |
|------|------------|
| **Direct manipulation** | Interface style with continuous object representation, physical actions instead of syntax, and rapid reversible operations with immediate feedback |
| **Directness** | The *feeling* that results from interacting with an interface; inversely related to cognitive effort |
| **Distance** | The cognitive gap between user goals and the interface; can be semantic or articulatory |
| **Semantic distance** | The gap between the *meaning* of interface expressions and the user's intentions |
| **Articulatory distance** | The gap between the *physical form* of interface expressions and their meaning |
| **Direct engagement** | The feeling of directly interacting with task-domain objects; interface becomes invisible |
| **Conversation metaphor** | Interface as language medium; system is an intermediary between user and a hidden world |
| **Model-world metaphor** | Interface *is* the world; user acts directly on explicitly represented objects |
| **Inter-referential I/O** | Input expressions can incorporate/reference output expressions, creating illusion of direct manipulation |
| **Naive realism** | User treats output representations *as if* they are the actual objects (DiSessa, 1985) |
| **Gulf of Execution** | Gap between user goals and how to specify them to the system |
| **Gulf of Evaluation** | Gap between system state/output and user's ability to interpret whether goals were met |
| **Automatization** | Practice-based reduction of *felt* cognitive effort; does NOT reduce actual semantic distance |
| **WYSIWYG** | "What You See Is What You Get" — output directly mirrors semantic intent; reduces semantic distance |
| **Turing tar-pit** | Interface at bit-manipulation level; everything is technically possible but nothing practical is easy (Perlis, 1982) |

# 2.4: Chapter 2: The Human Factor
*Source: MacKenzie, I.S. — Human-Computer Interaction: An Empirical Research Perspective*

---

## 1. Core Premise of HCI

- The deepest challenges in HCI lie in the **human factor** — humans are complex and variable; computers are comparatively simple.
- Human **variability** (age, ability, language, experience, etc.) means HCI design is always approximate, never perfectly precise.
- Key design precept: **"Know thy user"** (Shneiderman & Plaisant, 2005)
- Empirical HCI research requires **small, narrowly focused questions** — broad "why" questions are too imprecise for empirical inquiry.

---

## 2. Newell's Time Scale of Human Action

A **descriptive model** that categorizes human actions into timeframes. It has **four bands**, each divided into **three levels**, on a **logarithmic scale** (microseconds → months).

| Band | Time Range | HCI Topics | Research Method |
|---|---|---|---|
| **Biological Band** | 100 µs – 10 ms | Neural circuits, neurons, organelles | Quantitative / experimental |
| **Cognitive Band** | 100 ms – 10 sec | Selection techniques, menu design, text entry, gestural input | Primarily quantitative |
| **Rational Band** | Minutes – Hours | Web navigation, user search, collaborative computing | Mixed |
| **Social Band** | Days – Months | Workplace habits, social networking, privacy | Primarily qualitative |

- **Key insight:** The most common dependent variable in HCI experiments is **time** (task completion time).
- Research methodology transitions from **quantitative** (lower bands) to **qualitative** (upper bands).

> Newell also speculated on a **historical band** (years–thousands of years) and an **evolutionary band** (tens of thousands–millions of years), though these are outside the typical scope of HCI.

---

## 3. Human Factors Model

- Human as three components: **sensors**, **responders**, and a **brain**
- The **interface** (dashed vertical line) is where interaction takes place and where researchers measure behavioral events.
- Humans **monitor** the computer through sensors/displays and **control** it through responders/controls.

---

## 4. Sensors

### 4.1 Vision (Sight)
- ~**80%** of human information intake is through **vision**
- The **retina** is a transducer: converts light → neurological signals via the **optic nerve**
- **Fovea**: area near center of retina responsible for sharp central vision (e.g., reading)
    - Spans ~**1 degree of visual angle** (thumb-width at arm's length)
    - Only ~**1% of retina** in size, but engages ~**50% of the visual cortex**
- **Frequency** of light → perception of **color** (visible spectrum: ~390 nm violet to 750 nm red)
- **Luminance**: amount of light per given area; unit = **candela per square meter (cd/m²)**
- **Brightness**: subjective perception of luminance by the brain

#### Fixations and Saccades
- **Fixation**: eyes are stationary, taking in visual detail; typically lasts at least **200 ms**
- **Saccade**: rapid eye repositioning; takes only **30–120 ms**
- Classic research by **Yarbus (1965)** showed that eye-movement patterns differ based on the **task** given to the viewer

### 4.2 Hearing (Auditory)
- The human **auditory system** receives sound waves; converted to neural signals via the **cochlea**
- Properties of sound: **frequency** (perceived as pitch) and **amplitude** (perceived as loudness)
- **Auditory illusions** exist — e.g., the **Shepard scale**: equally spaced sine waves rising in frequency create the illusion of a tone that continually rises yet stays the same

### 4.3 Touch (Haptic/Tactile)
- **Haptic illusions** exist — e.g., the **phantom limb**: amputees sense presence and movement of a missing limb

---

## 5. The Brain

### 5.1 Cognition
- **Cognition**: conscious intellectual activity — thinking, reasoning, deciding
- Difficult to measure directly because cognitive operations occur *inside* the brain
- A cognitive operation is bracketed by a **sensory stimulus** (input) and a **motor response** (output)

#### Reaction Time Components (Bailey, 1996)
| Operation | Typical Time |
|---|---|
| Sensory reception | 1–38 ms |
| Neural transmission to brain | 2–100 ms |
| Cognitive processing | 70–300 ms |
| Neural transmission to muscle | 10–20 ms |
| Muscle latency and activation | 30–70 ms |
| **Total** | **113–528 ms** |

### 5.2 Memory

#### Long-Term Memory
- **Declarative/explicit memory**: stores facts and events (analogous to data space in computers)
- **Implicit/procedural memory**: stores how to do things (analogous to code space)

#### Short-Term (Working) Memory
- **Short-term memory** / **working memory**: active, immediately accessible portion of memory
- Capacity: approximately **7 ± 2 items** (Miller, 1956)
- Classic paper: **"The Magic Number Seven, Plus or Minus Two"** — George A. Miller (1956)
    - At sequence length 7 → ~50% correct recall
    - At length 5 → ~90% correct; at length 9 → ~20% correct

#### Chunking
- **Chunking**: grouping multiple low-level items into a single high-level item to extend memory capacity
- Example: `1000101101110010` → `8, 11, 7, 2` (chunk into decimal digits)
- Example: `BSCBMICRA` → `CBS IBM RCA` (three chunks = easier to remember)

---

## 6. Language

- **Language** (spoken): universally available, learned without conscious effort by children
- **Writing**: a codification of language; requires years of deliberate study and practice
- Quote: *"Humankind is defined by language; but civilization is defined by writing."* (Daniels & Bright, 1996)

### Corpus
- **Corpus**: a large collection of representative text samples used to study a language
- Example: **British National Corpus (BNC)** — 100 million words, British English, late 20th century
- A corpus can be reduced to a **word-frequency list** (unique words + their frequencies)
    - Most frequent English word: *the* (~6.8% of all words)

### Redundancy in Language
- **Redundancy**: the property of language where missing portions can be inferred from context
- Humans can read text with vowels removed and still understand meaning
- **SMS shorthand** exploits language redundancy — e.g., removing ~48.7% of characters while preserving meaning
- **Part-of-Speech (POS) tagging**: tagging words by grammatical category (noun, verb, adjective) — important in predictive text systems

### Entropy
- **Entropy**: in information theory, uncertainty or unpredictability in a system
- Shannon's **letter-guessing experiment** demonstrated redundancy and entropy in English

---

## 7. Human Performance

### 7.1 Reaction Time
- **Simple reaction time**: one stimulus, one response
- **Physical matching**: compare two stimuli for visual identity
- **Name matching**: match words regardless of font/appearance — requires more cognitive processing
- **Class matching**: determine if two symbols belong to the same class (both letters or both digits) — hardest; requires multiple references to long-term memory
- Typical **simple reaction time** ≈ **276 ms** in experiments
- **Auditory reaction time < Visual reaction time**

> **False Start Rule (IAAF):** A false start is declared if an athlete reacts within **100 ms** after the starter's pistol — precariously close to the human lower bound of ~105–113 ms.

### 7.2 Visual Search
- **Visual search**: scanning a set of items to find a target
- Reaction time increases **linearly** with the number of items (N):
    - Formula from experiment: **RT = 498 + 41N ms**
- **No-match trials take longer** than match trials (exhaustive search required)

### 7.3 Skilled Behavior
- **Skilled behavior**: human performance that improves continuously with practice
- Two categories:
    - **Sensory-motor skill**: e.g., darts, gaming
    - **Mental skill**: e.g., chess, programming
- Most tasks involve **both** (e.g., laparoscopic surgery)
- Skill progression is measured in dependent variables: **speed, accuracy, KSPC (keystrokes per character)**

### 7.4 Attention
- **Attention**: limited cognitive resource; attending to one thing can prevent attending to another
- **Divided attention**: concentrating on more than one task simultaneously (e.g., texting while driving)
- **Selected attention** (focused attention): attending to one task while ignoring others (e.g., listening in a noisy room)
- Channels: events in a **single channel** (visual, auditory, motor) are processed in **parallel**; events in **different channels** are processed in **serial**
- Texting while driving = **23-fold increase** in collision risk (Richtel, 2009)
- Attention failure has been implicated in industrial and aviation accidents

### 7.5 Human Error
- **Error**: a discrete event where the task outcome is incorrect (deviated from the desired outcome)
- Errors typically reported as: **error rate = incorrect trials / all trials** (often as %)
- Alternatively, **accuracy = correct trials / all trials**
- Errors can result from:
    - Control problems (device sensitivity, size)
    - Environmental factors (noise, vibration, lighting)
    - Performing secondary tasks / being distracted
- **Design-induced errors**: many serious accidents are caused not purely by the operator, but by **faulty system design** that enables catastrophic outcomes from simple interaction errors (Casey, 1998)
- Safety-critical systems must accommodate human error — such errors are not just possible, they are, in time, **likely**

---

## 8. Key Researchers & References

| Name | Contribution |
|---|---|
| **Newell (1990)** | Time Scale of Human Action |
| **Card, Moran & Newell (1983)** | Model Human Processor; chunking examples |
| **Miller (1956)** | "Magic Number 7 ± 2" — short-term memory capacity |
| **Yarbus (1965)** | Eye movements and vision; fixation/saccade patterns |
| **Bailey (1996)** | Reaction time component breakdown |
| **Casey (1998, 2006)** | Design-induced errors; accident analysis |
| **Shneiderman & Plaisant (2005)** | "Know thy user" |
| **Richtel (2009)** | 23× collision risk when texting while driving |

---

## 9. Key Terms Quick Reference

| Term | Definition |
|---|---|
| **Fovea** | Central retinal area for sharp vision; ~1° visual angle, ~50% of visual cortex |
| **Fixation** | Stationary eye position taking in detail; ≥200 ms |
| **Saccade** | Rapid eye repositioning; 30–120 ms |
| **Luminance** | Amount of light per area (cd/m²) |
| **Cognition** | Conscious intellectual activity (thinking, reasoning, deciding) |
| **Working memory** | Active, accessible short-term memory; ~7±2 items |
| **Chunking** | Grouping low-level items into one high-level unit |
| **Corpus** | Large representative text collection for language analysis |
| **Redundancy** | Property of language where missing content can be inferred |
| **Entropy** | Unpredictability/uncertainty in a system |
| **Divided attention** | Doing two or more tasks simultaneously |
| **Selected/Focused attention** | Concentrating on one task, ignoring others |
| **Skilled behavior** | Performance that improves with practice (sensory-motor or mental) |
| **Error rate** | Ratio of incorrect trials to total trials |
| **Design-induced error** | Error caused by faulty system design rather than pure human fault |
| **Descriptive model** | A tool for thinking/categorizing a problem space (not for predicting) |
| **POS tagging** | Labeling words in a corpus by grammatical category |
| **Saccade** | Fast eye movement to a new fixation point (30–120 ms) |


# 2.5: Human-Centered Design Considered Harmful
*Source: Donald A. Norman, Nielsen Norman Group — Interactions, July + August 2005*

---

## 1. Central Argument

- **Human-Centered Design (HCD)** has become "accepted wisdom" in UI/UX — Norman argues this is **dangerous** because uncritical acceptance prevents improvement.
- Thesis: HCD principles can be **helpful, misleading, or wrong** — and at times, **harmful**.
- Norman's proposed alternative: **Activity-Centered Design (ACD)** may be superior.

---

## 2. The "Know Your User" Principle — Questioned

- The sacred principle of HCI/UI design: **"Know your user"**
- HCD was developed to overcome **poor software design** by emphasizing user needs and abilities — and it *has* improved usability.
- **The Paradox:** Many successful, globally-used products were designed **without** user studies yet work well for nearly everyone (e.g., automobiles, kitchen utensils, musical instruments).
- This paradox challenges the assumption that deep user knowledge is always necessary.

### Examples of Successful Non-HCD Designs
- **The Automobile**: Evolved through trial and error — no systematic user studies. Controls converged through iterative folk design.
- **Everyday Objects**: Kitchen tools, cameras, sporting equipment — vary by culture but universally learnable. Designed from understanding of the *activity*, not the *user*.

---

## 3. Activity-Centered Design (ACD)

### Definition
> **Activity-Centered Design**: Design based on a deep understanding of the **activities** to be performed, rather than the specific users performing them.

- Many successful products evolved via **"slow, evolutionary folk design"** — each generation refined the product based on feedback and experience with the activity.

### Activity Hierarchy (Norman's version of Activity Theory)
Heavily influenced by **Russian and Scandinavian activity theory research**.

| Level | Description |
|---|---|
| **Activity** | Highest level — a coordinated, integrated set of tasks |
| **Task** | A component of an activity |
| **Action** | A component of a task |
| **Operation** | The lowest level — component of an action |

**Example:** A mobile phone supports the *activity* of **communication** through multiple *tasks*: dialing, talking, note-taking, checking calendars, sending texts/photos.

---

## 4. Technology vs. People — Who Adapts?

- HCD tenet: **Technology should adapt to people**, not the other way around.
- Norman challenges this: History shows people **adapt to technology** — often successfully and willingly.

### Examples of People Adapting to Technology
- **The Clock**: Arbitrary division of time (hours, minutes, seconds) now governs when we eat, sleep, and learn — not our biology.
- **Writing Systems**: Printing, handwriting, typing are all **artificial and unnatural** — requiring months/years of practice (e.g., Graffiti stylus input).
- **Musical Instruments**: Complex, physically demanding, cause repetitive stress injuries — would **fail any HCD review** — yet are deeply successful and enduring.

### Key Insight
> *"Learn the tools, and the activity is understood."* — The converse of the HCD mantra.

- In HCD: **the tool should be invisible** (it shouldn't get in the way)
- In ACD: **the tool is the way** (deep tool mastery defines the activity)

---

## 5. Why HCD Can Be Harmful — Norman's Critiques

### 5.1 Over-Tailoring for Specific Users
- Designing for a **specific target population** makes the product *less* appropriate for others.
- **The individual is a moving target**: a design for today's beginner is wrong for tomorrow's expert.
- Successful products create **unanticipated new uses** that the original HCD-focused design doesn't support well.

### 5.2 Focus on Humans Detracts from Activity Support
- Emphasizing the human can cause designers to **neglect the sequential flow** of activities.
- HCD methods are good at static, screen-by-screen evaluation but **fail to support dynamic sequences** of tasks and actions.
- Christine Frederick (1919) noted work consists of "a series of **interrelated processes**" — not independent acts. This is still ignored in HCI.

### 5.3 Too Much Listening to Users → Complexity
- Acceding to every user request leads to **feature bloat and incoherent design**.
- Example: Major software companies that pride themselves on HCD still produce **complex, confusing products** due to over-incorporation of user feedback.
- **Southwest Airlines** example: Ignored its two most-complained-about issues (reserved seating, inter-airline baggage transfer) to maintain strategic advantage (fast turnaround, low cost) — and succeeded.

### 5.4 Personas and Scenarios May Not Actually Help
- Norman challenges whether detailed **personas** (e.g., "37-year-old single mother studying for an MBA") genuinely inform critical design decisions like screen layout or action sequences.

---

## 6. The Case for a "Design Dictator"

- Norman argues that sometimes what is needed is **a strong, authoritative designer** who can:
    - Evaluate user suggestions against the **activity requirements**
    - **Ignore requests** that don't fit the design model
    - Hold a clear **conceptual model** of the product and stick to it

> *"Paradoxically, the best way to satisfy users is sometimes to ignore them."*

- **Apple Computer** example: Replaced its HCD design team with a single authoritative (dictatorial) leader — usability did **not** suffer; products became design prototypes admired worldwide.

### HCD vs. Great Design
- HCD **guarantees good products** — it avoids failures and ensures usability.
- **Great design** comes from breaking rules, ignoring accepted practices, and pushing a clear vision — this is **ego-centric, vision-directed design**.
- Risk: great vision can also lead to **great failures**.

---

## 7. ACD vs. HCD — Key Differences

| Aspect | Human-Centered Design (HCD) | Activity-Centered Design (ACD) |
|---|---|---|
| **Focus** | The individual user | The activity being performed |
| **Adaptation** | Technology adapts to people | People adapt to technology (accepted) |
| **Tool role** | Tool should be invisible | Tool defines the activity |
| **User feedback** | Central to design process | Filtered through activity requirements |
| **Evaluation method** | Personas, scenarios, usability testing | Understanding of activity flow and sequences |
| **Weakness** | Static, screen-level focus; feature bloat | Risk of ignoring legitimate user needs |
| **Strength** | Ensures usability; reduces errors | Cohesion, support for sequential tasks |

---

## 8. Norman's Conclusion

- ACD is **not** a rejection of everything in HCD — it **builds upon** HCD knowledge.
- Activities involve people, so supporting activities necessarily means supporting people.
- ACD also draws on **industrial engineering** and **ergonomics** — fields that have long understood the importance of sequential task support.
- Norman's call: **Reexamine fundamental presuppositions** — the human-focus may be misguided; an activity-focus may bring greater benefits.

---

## 9. Key Terms Quick Reference

| Term | Definition |
|---|---|
| **Human-Centered Design (HCD)** | Design philosophy that prioritizes the needs, abilities, and context of the specific users |
| **Activity-Centered Design (ACD)** | Design philosophy that prioritizes understanding the *activity* to be performed, not just the user |
| **Activity** | A coordinated, integrated set of tasks (highest level in Norman's hierarchy) |
| **Task** | A component of an activity |
| **Action** | A component of a task |
| **Operation** | The lowest-level unit of behavior |
| **Conceptual model** | The designer's clear, overarching vision for what a product is and how it should work |
| **Folk design** | Slow, evolutionary improvement of a product over generations based on practical use and feedback |
| **Persona** | A fictional user archetype used in HCD to represent a target user group |
| **Vision-directed design** | Design driven by a single authoritative designer's clear concept, not user testing |
| **Activity theory** | Theoretical framework (originating in Russian/Scandinavian research) that organizes human behavior into activities, tasks, actions, and operations |

---

## 10. Likely Test Points

- Norman's **main argument**: HCD can be harmful; ACD may be superior
- The **paradox** at the heart of the essay: products designed without user studies still work well globally
- The **activity hierarchy**: Activity → Task → Action → Operation (know the order and definitions)
- **Three examples** of technology where people adapt to tools (Clock, Writing, Musical Instruments)
- **Two main weaknesses** of HCD: (1) static focus misses sequential activity support; (2) over-listening leads to complexity
- **HCD guarantees good design; great design requires breaking rules**
- The **Apple** and **Southwest Airlines** examples as arguments for ignoring users
- Norman's stance: ACD does **not** discard HCD — it expands and refocuses it


# 3.1: Chapter 4: Scientific Foundations

---

## 4.1 What is Research?

Research has **three definitions**:
1. **Careful or diligent search** – e.g., searching files on a computer
2. **Collecting information about a particular subject** – e.g., surveying users or observing interactions
3. **Investigation or experimentation** aimed at the discovery and interpretation of facts, and revision of accepted theories in light of new facts *(most relevant to HCI)*

> Key idea: In HCI research, we don't **prove** things — we **gather facts** and **formulate and test evidence**.

**Theory** – A hypothesis assumed for the sake of argument/investigation; when confirmed through research, becomes a scientifically accepted body of principles.

**Law** – More specific and binding than a theory; a relationship or phenomenon *invariable under given conditions*. Because human behavior is variable, laws are of questionable relevance to HCI.

**Fitts' Law** – Originally a model of human motor behavior (Fitts, 1954); predicts the time to perform rapid aimed movements (e.g., moving a cursor to a target and selecting it). It is technically a **model**, not a law, but was labeled as such by other researchers.

---

### 4.1.1 Research Must Be Published

- Publication in **peer-reviewed journals or conference proceedings** is required.
- **Peer review** – other researchers evaluate the work for integrity, relevance, and contribution.
- Published work is **archived** – added to the global body of knowledge.
- A **patent** also counts as publication (it discloses the invention publicly).

**"Publish or perish"** – researchers, especially in academia, must publish to sustain their careers.

---

### 4.1.2 Citations, References, and Impact

**Citation** – an abbreviated reference in a paper that links to earlier work (like a hyperlink in a webpage).

- Citations support **intellectual honesty** and back up assertions.
- The **number of citations** to a paper is a measure of its **impact**.

**H-index** – A single number measuring both research productivity and impact. A researcher with H-index = *n* has *n* publications each with *n* or more citations. (Proposed by physicist J. Hirsch in 2005.)

---

### 4.1.3 Research Must Be Reproducible

- Research that cannot be **replicated** is useless.
- A standardized methodology ensures enough detail to allow others to reproduce results.
- Example: Louis Pasteur's standardized methodology in microbiology allowed his controversial findings to be verified or refuted by others.

---

### 4.1.4 Research vs. Engineering vs. Design

| | Research | Engineering/Design |
|---|---|---|
| Focus | Small ideas, concepts, questions | Building complete products |
| Prototype | Early mock-up to test an idea | Used later in product development |
| Timeline | Slower, no hard deadlines | Deadline-driven |
| Scope | Narrow and incremental | Broad and integrated |

**Form vs. Function** – A key trade-off in design. *Form trumping function* example: a seamless touchpad (elegant but missing tactile edge feedback) requiring users to add duct tape to know when they've reached the edge.

> Research provides the raw materials (ideas, models) that engineers and designers later build into products.

---

## 4.2 What is Empirical Research?

**Empirical research** – research based on observation or experience; guided by direct observation *without prejudice to existing theories*.

- Must be **verifiable or disprovable** by observation or experiment.
- HCI research is framed as **hypotheses** — assertions that can be verified through observation and measurement.

> Example: Copernicus used empirical observation (not accepted theory) to discover the heliocentric solar system.

---

## 4.3 Research Methods

Three common methods in HCI:

### 4.3.1 Observational Method
- Based on **direct observation** in natural settings.
- Qualitative rather than quantitative → high **relevance**, low **precision**.
- Techniques include: interviews, field studies, contextual inquiries, case studies, focus groups, think-aloud protocols, walkthroughs, cultural probes.
- Focuses on the **why/how** of interaction: thought, attitude, emotion, strategy, etc.
- Cannot establish **cause-and-effect** relationships.

### 4.3.2 Experimental Method (Scientific Method)
- Knowledge acquired through **controlled experiments** in lab settings.
- Low **relevance** (artificial tasks), high **precision** (controlled variables).
- Requires at least:
    - One **independent variable (IV)** – also called the *manipulated variable* or *factor* (what is changed)
    - One **dependent variable (DV)** – also called the *response variable* (what is measured)
- Allows **cause-and-effect conclusions** when properly designed.

> **User study** = controlled experiment. **Usability evaluation** = assessment of a single interface (no manipulated variable — NOT an experiment).

### 4.3.3 Correlational Method
- Looks for **relationships** between variables (not cause and effect).
- Quantitative but data not collected in controlled settings → balance of relevance and precision.
- Results are **circumstantial, not causal**.
- Often accompanies experimental methods (e.g., adding questionnaires to a study).

---

## 4.4 Observe and Measure

### 4.4.1 Observation
Two types of observers:
- **Human observer** (experimenter) – manual measurement, log sheets, timing by hand
- **Apparatus observer** (software/computer) – records keystrokes, timestamps, mouse movements

**Pilot testing** – preliminary testing, often using manual timing, before the full experiment.

---

### 4.4.2–4.4.6 Scales of Measurement

From least to most sophisticated: **Nominal → Ordinal → Interval → Ratio**

| Scale | Description | HCI Example | Math Allowed |
|---|---|---|---|
| **Nominal** | Arbitrary categories/codes | Gender (M/F), scrolling strategy (MW/CD/KB) | None (only frequency counts) |
| **Ordinal** | Ordered ranking, unequal intervals | User preference ranking of GPS devices | Greater than / less than; NO mean |
| **Interval** | Equal spacing, no absolute zero | Likert scale responses | Mean valid; ratios NOT valid |
| **Ratio** | Equal spacing + absolute zero | Task completion time, error rate, age | All math operations valid |

**Likert Scale** – A common interval-scale questionnaire format with symmetric verbal responses around a neutral center (e.g., Strongly Disagree → Strongly Agree).

**Normalization** – Expressing a count *per something* to improve meaning and allow comparison across studies. Example: Instead of "2 errors," report "4% error rate" (2 errors / 50 characters × 100).

> The most common ratio-scale measurement in HCI is **time** (task completion time).

---

## 4.5 Research Questions

- Good research questions move from **broad and informal** to **narrow and testable**.
- A **testable research question** specifies: what is measured, what is compared, and the criterion for comparison.

| Example Question | Quality |
|---|---|
| "Is the new technique any good?" | NOT testable (too vague) |
| "Is measured entry speed (wpm) higher with Technique A than QSK after 1 hour of use?" | Testable ✓ |

- Human **variability** means answers always carry some uncertainty — use **statistical techniques** (covered in Chapter 6) to gauge confidence.

---

## 4.6 Internal Validity and External Validity

**Internal validity** – the extent to which an observed effect is due to the test conditions (not other factors). High internal validity = confidence that the effect is real.

**External validity** – the extent to which results generalize to other people and other situations. High external validity = broad applicability.

> ⚠️ **Key tension**: Improving one often comes at the expense of the other. (e.g., lab settings improve internal validity but reduce external validity.)

**Ecological validity** – closely related to external validity; refers specifically to using materials, tasks, and situations *typical of the real world* in the methodology.

| Term | Refers to... |
|---|---|
| Internal validity | The effect really being due to the test conditions |
| External validity | Results generalizing to other people/situations |
| Ecological validity | The methodology resembling real-world conditions |

---

## 4.7 Comparative Evaluations

- Evaluating a **single** interface has limited research value — it's better to **compare**.
- A **baseline condition** – an established design included for comparison.
    - **Benefit 1**: Acts as a check on the methodology (results should match prior studies).
    - **Benefit 2**: Allows comparison of results across different user studies.

> A comparative evaluation yields more valuable and insightful results than a single-interface evaluation (Tohidi et al., 2006).

---

## 4.8 Relationships: Circumstantial vs. Causal

**Causal relationship** – The manipulated condition *caused* the observed change. Only possible through properly designed **controlled experiments** with random assignment.

**Circumstantial relationship** – A relationship exists and can be measured, but it is NOT causal. Example: Correlational studies on smoking and cancer found a relationship, but the study design could not establish causation.

> Cause-and-effect conclusions are **NOT valid** when the independent variable is a naturally occurring participant attribute (e.g., gender, handedness, personality), because confounding variables cannot be eliminated.

**Confounding variable** – An uncontrolled variable that could explain the observed effect (defined further in Chapter 5).

---

## 4.9 Research Topics

- Most HCI research is **incremental** — small improvements, not big leaps.
- Many "new" features in products (e.g., iPhone's pinch gesture, flick gesture) are rooted in decades-old research.

### Four Tips for Finding a Research Topic

| Tip | Description |
|---|---|
| **#1: Think Small!** | Don't seek a monumental idea. Small, focused ideas lead to testable questions and manageable experiments. |
| **#2: Replicate!** | Replicating an existing experiment builds deep understanding, often sparking a new twist or finding. |
| **#3: Know the Literature!** | Read published research, organize it in a table (rows = papers, columns = methods/results), and patterns/gaps will emerge. |
| **#4: Think Inside the Box!** | Observe your own daily interactions with technology. Notice errors, frustrations, and inefficiencies — these are potential research topics. |

> **"ABD" (All But Dissertation)** – a term for graduate students who complete all requirements but fail to find a dissertation topic.

---

## Key Terms Quick Reference

| Term | Brief Definition |
|---|---|
| **Empirical research** | Research based on observation/experience, verifiable by experiment |
| **Independent variable (IV)** | The manipulated condition in an experiment |
| **Dependent variable (DV)** | The measured human response/behavior |
| **Internal validity** | Confidence that observed effect is due to test conditions |
| **External validity** | Generalizability of results to other people/situations |
| **Ecological validity** | Using real-world tasks and materials in the methodology |
| **Baseline condition** | An established design included for comparison in a study |
| **Causal relationship** | Effect caused by the test condition (requires controlled experiment) |
| **Circumstantial relationship** | Observed relationship that is NOT necessarily causal |
| **Confounding variable** | Uncontrolled variable that may explain an effect |
| **H-index** | Metric of researcher impact: *n* papers each with *n*+ citations |
| **Likert Scale** | Interval-scale questionnaire with symmetric verbal response options |
| **Normalization** | Expressing a count per something (e.g., error rate %) for meaningful comparison |
| **Pilot testing** | Preliminary testing before the main experiment |
| **Fitts' Law** | Predictive model of time for rapid aimed movements (pointing/selecting) |
| **User study** | A controlled experiment with human participants in HCI |
| **Usability evaluation** | Assessment of a single interface; NOT a controlled experiment |

# 3.2: # HCI Study Notes – Reading 3.2: "Unexpected Expectations: Public Reaction to the Facebook Emotional Contagion Study"
**Hallinan, Brubaker & Fiesler (2020) | *New Media & Society*, 22(6), 1076–1094**

---

## Overview

This paper examines why the public reacted so strongly — and negatively — to the **Facebook Emotional Contagion (FEC) study** published in 2014. The researchers analyzed public comments on news articles to understand what people found objectionable. Key finding: **there is no consensus** on what Facebook is, what it should do, or what research on it means — and this lack of consensus is itself the central problem.

---

## What Was the FEC Study?

- **Full citation**: Kramer et al. (2014), "Experimental Evidence of Massive-Scale Emotional Contagion through Social Networks," *PNAS*
- Conducted by Facebook in collaboration with academic researchers
- **~700,000 English-speaking Facebook users** had their News Feeds algorithmically altered
    - Group 1: saw more **positive** emotional content
    - Group 2: saw more **negative** emotional content
    - Group 3: saw **less emotional** content overall
- Used **automated sentiment analysis** to classify posts
- **Findings**: Users exposed to more emotional content were slightly more likely to post similar emotional content for up to 3 days; users exposed to less content posted less frequently
- Conclusion: Evidence of *some* emotional contagion on Facebook; challenged the idea that exposure to positive content makes users unhappy

**The backlash**: Facebook and the lead researcher issued apologies; *PNAS* issued a statement of editorial concern. The researchers, journal, and Facebook were all **surprised** by the negative public reaction.

---

## Theoretical Frameworks

### Controversy Analysis (Science and Technology Studies)
- **Definition**: A method for studying contested issues using mediated controversies to surface beliefs and values that are normally overlooked or taken for granted.
- Mediated controversies reveal larger tensions in how society integrates technology.
- Example: The FEC study brought into the open implicit public expectations about what Facebook *is* and *should be*.

### Expectancy Violation Theory (EVT)
- **Definition**: People have expectations about the communicative behavior of others; when those expectations are violated, people reassess their relationship and knowledge of the other party.
- Originally from face-to-face interpersonal communication; extended to computer-mediated contexts.
- Variables shaping expectations: characteristics of the **communicator**, the **relationship**, and the **context**.
- Applied here: Facebook users had implicit expectations about the platform; the FEC study violated those expectations — but the content of those expectations varied widely across users.

---

## Methods

- **Data**: 2,790 public comments collected from **20 news articles** (published June 2014) about the FEC study
    - Sources: The Atlantic, Slate, Forbes, NYT, The Guardian, Wired, WSJ, Washington Post, etc.
    - All sources were US or UK-based — potential **Western bias**
- **Method**: **Thematic analysis** (Clarke & Braun, 2006) — open coding of comments, then inductive development of themes
- **Research questions**: What were the patterns of public responses? What issues were most important? Why were people upset?

**Why use news comments?**
- Time/resource efficient way to study public reaction
- Captures perspectives of people *unwilling* to participate in formal research (avoids selection bias)
- Surfaces perspectives of **nonusers** of Facebook
- Provides access to reasoning behind opinions
- Limitation: biased toward people with internet access willing to comment; also susceptible to media framing effects

**Ethical considerations in data collection**:
- Comments are "public" data, but context still matters
- Authors included quotes **verbatim but without identification**
- Chose quotes not easily findable via web search and containing no personal/sensitive information

---

## Four Major Themes from Public Comments

### 1. "Living in a Lab"
- Many people **did not know** Facebook conducted experiments or collaborated with researchers at all
- Any announcement of experimentation would be a violation — regardless of the study's specifics
- Key concerns:
    - **Lack of transparency and consent** — no knowledge of participation, no clear start/end to the experiment
    - **Power dynamics** — researchers disconnected from "real world," users treated as "lab rats" or "guinea pigs"
    - Comments compared FEC to Stanford prison experiment and Nazi medical experimentation
    - Almost no recognition of the study's potential **benefits**
- Revealed: Nearly two-thirds of Twitter users didn't know academic researchers use public social media data (Fiesler & Proferes, 2018)

### 2. "Manipulation Anxieties"
- Many users **did not know** the News Feed was algorithmically curated — they assumed it was a "neutral arbiter"
- The experiment exposed that **manipulation is endemic** to how the News Feed operates, not just a one-time experiment
- Key concerns:
    - **Fairness**: manipulation of the feed could cause people to miss important posts (e.g., a friend's call for help)
    - Third-party harm: changes to one user's feed could affect their relationships with others
    - **Emotional manipulation** seen as especially dangerous — could affect identity, politics, mental health
    - Fear of vulnerable populations (e.g., people with depression) being harmed
    - Dystopic extrapolations: political control, "herd of docile consumers"
- **Important note**: The actual effect size was small, but public framing exaggerated the harms dramatically

### 3. "Wake Up, Sheeple"
- These commenters were **unsurprised** — the FEC study confirmed what they already believed about Facebook
- Facebook manipulation was seen as expected, ordinary behavior for corporations
- Key attitudes:
    - Shifted blame onto users for not already knowing/expecting this
    - Many identified as **Facebook nonusers**, framing nonuse as a moral/wise choice
    - Framed Facebook users as **"the product"** sold to advertisers
    - Recommended either opting out entirely or adopting a nihilistic acceptance
- Implication: Researchers cannot assume a baseline of understanding; even nonusers are stakeholders with strong expectations

### 4. "No Big Deal"
- Some commenters found the study **unremarkable** — consistent with their expectations of Facebook, corporations, and advertising-supported media
- Key attitudes:
    - Referenced **A/B testing** as standard industry practice
    - Individuals are "masters of their own minds" and can resist manipulation
    - Facebook, as a company, is entitled to conduct its own research; don't like it → don't use it
    - Manipulation by media is nothing new ("raison d'être for all media")
- Most closely aligned with researchers' and Facebook's perspective
- Saw the problem as a **communication/education gap**, not an ethics failure

---

## Discussion & Key Conclusions

### No shared understanding of Facebook
- There is no consensus on what Facebook *is* — a social space, a commercial platform, a public utility, a product?
- Platform **norms are neither unified nor settled**
- No single answer to what bothered people = no single ethical "fix"

### Relational Approach to Ethical Decision-Making
- **Definition**: An approach to research ethics that begins with understanding the public's *relationship to platforms* and uses that understanding to inform research design and communication.
- Inspired by relational ethics from qualitative research (Ellis, 2007) and extended to human-machine communication contexts.
- Key principles:
    1. **Understand user expectations empirically** before designing research — not just rely on IRB/terms of service compliance
    2. **Include nonusers as ethical stakeholders** — they are affected and have strong opinions
    3. Consider how research may affect **trust in the platform** and in research generally (corrosive effects of negative reactions)
    4. Explore **opt-in or opt-out** mechanisms — even opt-out could address some concerns without requiring users to leave the platform entirely

### Why Terms of Service (ToS) Are Insufficient
- Users rarely read ToS (Martin, 2016a)
- Users interpret ToS through pre-existing expectations, not as formal contracts
- Implicit consent through ToS is **not accepted as legitimate** by the public
- **Folk theories of platforms** — informal, personal mental models users have about how platforms work — are more influential than official policies

### Nonusers as Stakeholders
**Nonusers** – people who do not use a platform but still have expectations about it and are affected by its societal influence. The paper argues nonusers should be included in ethical considerations for platform research because:
- They comment publicly on controversies, shaping other users' views
- Platforms have broad societal effects that extend beyond their user base
- Including nonuser perspectives can help researchers **anticipate controversies**

---

## Key Terms Quick Reference

| Term | Definition |
|---|---|
| **Facebook Emotional Contagion (FEC) Study** | 2014 experiment in which ~700,000 users had their News Feeds altered to test whether emotional content is contagious |
| **Emotional contagion** | The transfer/spread of emotions from one person to another through social exposure |
| **Controversy analysis** | Method from STS for studying contested issues via mediated controversies to surface hidden values and beliefs |
| **Expectancy Violation Theory (EVT)** | Theory that expectation violations cause people to reassess their relationship with the violating party |
| **Thematic analysis** | Qualitative method for identifying and analyzing patterns of meaning (themes) in data |
| **Folk theories of platforms** | Informal mental models users form about how platforms like Facebook work |
| **Nonusers** | People who do not use a platform but still hold expectations about it and are affected by it |
| **Relational approach to ethics** | Ethics framework that centers the relationship between researchers and research populations, especially their relationship to the platform |
| **A/B testing** | Common industry practice of showing different versions of content/features to subsets of users to compare outcomes |
| **Selection bias (in ethics research)** | The problem that studies on research ethics recruit only those *willing* to participate, missing the most critical voices |
| **Contextual integrity** | Principle (Nissenbaum, 2004) that information flows ethically when they match the norms of the context in which data was shared |

---

## Why This Matters for HCI

- HCI research increasingly takes place on online platforms — understanding public expectations is essential
- The FEC controversy illustrates the **gap between researcher/IRB ethics standards and public ethical intuitions**
- Designing research ethically requires not just following formal rules (IRB, ToS) but **empirically studying** the expectations of those affected
- **Transparency, consent, and trust** are central ethical concerns — not just for this study, but for all platform-based HCI research
- The "Living in a Lab" reaction specifically highlights HCI's challenge: **users are often unaware they are research subjects** in online platform studies

---

## Important Stats & Facts for the Quiz

- **~700,000** Facebook users participated (unknowingly) in the FEC study
- **61%** of Guardian poll respondents were surprised to learn about the study
- **84%** lost trust in Facebook after the controversy
- **66%** considered closing their Facebook account
- Nearly **two-thirds of Twitter users** did not know academic researchers use public social media data
- Dataset: **2,790 comments** from **20 news articles** from 10 news outlets
- The study was published **June 2, 2014**; the public controversy erupted **late June 2014**

# 3.3: "Survey Research in HCI"
**Müller, Sedley & Ferrall-Nunge (2014) | Chapter in *Ways of Knowing in HCI***

---

## Overview

A **survey** is a method of gathering information by asking questions to a subset of people (**the sample**), the results of which can be **generalized** to the wider target population. This chapter covers the full survey lifecycle: goals, sampling, questionnaire design, biases, pretesting, launch, and data analysis.

---

## What Surveys Are Good For (Use Cases in HCI)

- Gathering information about habits, behavior, or technology interaction
- Getting demographic or **psychographic** information to characterize a population
- Collecting feedback on experiences with a product, service, or application
- Measuring attitudes and perceptions *in the context of usage*
- Understanding intents and motivations for using an application
- Quantitatively measuring task success
- Capturing awareness of systems or features
- Comparing attitudes/experiences over time or across dimensions

> **Surveys do NOT allow:** observation of context or follow-up questions.

---

## When to Use Surveys vs. When to Avoid Them

### ✅ Use Surveys When:
- You need to **represent an entire population** statistically
- You want to **measure differences between groups**
- You want to **track changes over time** (longitudinal)
- Measuring: **attitudes, intent, task success, user characteristics, awareness, comparisons**

### ❌ Avoid Surveys When:
| Goal | Better Method |
|---|---|
| **Precise behaviors** (exact click sequences, page flows) | Log data, diary study, experience sampling |
| **Underlying motivations** (subconscious reasons) | Ethnography, contextual inquiry |
| **Usability evaluations** (why can't users complete a task?) | Task-based observational study, usability study |

### Using Surveys With Other Methods
- **Survey AFTER qualitative study** → quantifies specific observations from a small sample
- **Survey BEFORE qualitative study** → identifies high-level insights to explore in depth
- **Survey + A/B experiment** → measure satisfaction alongside behavioral log data
- **Survey + physiological data** (EEG, facial muscle activity) → richer picture of experience

---

## Brief History of Surveys

| Date | Event |
|---|---|
| Ancient times | Censuses for food planning, land distribution, taxation |
| 1824 | First US Presidential straw poll |
| 1920s–30s | **Likert** and Thurstone develop reliable attitude scaling methods |
| 1936 & 1948 | Major US polls incorrectly predict election winners → scrutiny of sampling methods |
| 1951 | **Payne** publishes "The Art of Asking Questions" — first study of question wording |
| 1980s | Standardized usability questionnaires developed (SUS, QUIS, SUMI) |
| 1983 | Carnegie Mellon: first survey with a computer interface |
| 1984 | **Tourangeau** identifies **four cognitive steps** for survey response |
| 1989 | **Groves** identifies four types of survey error |
| 1994 | Georgia Tech starts annual online surveys to study Internet usage |
| 2008 | **Couper** publishes on web survey visual design biases |

> **Random sampling** became the gold standard after the 1936 and 1948 polling failures.

---

## The Six Stages of Survey Research

### Stage 1: Research Goals and Constructs

**Construct** – an unidimensional attribute that cannot be directly observed and must be measured indirectly through questions (e.g., "perceived speed," "overall satisfaction").

- Define research goals → identify constructs → write questions to measure each construct
- Validate constructs using correlation, regression, or **factor analysis**
- Use **cognitive pretesting** to verify respondents interpret constructs as intended
- Avoid "nice-to-know" questions — extra questions reduce completion rates

---

### Stage 2: Population and Sampling

| Term | Definition |
|---|---|
| **Population** | The full set of individuals that meet certain criteria and to whom results should generalize |
| **Sampling frame** | The set of people the researcher is actually *able to contact* |
| **Sample** | The people from the sampling frame who are *invited* to take the survey |
| **Respondents** | Those who actually *complete* the survey |

**Coverage error** – When the sampling frame systematically excludes certain types of people (e.g., very dissatisfied users, anonymous users), causing misrepresentation of the population.

#### Probability vs. Non-Probability Sampling

**Probability (random) sampling** – Every person in the sampling frame has an equal, nonzero chance of selection. The **gold standard** because it minimizes **sampling bias (selection bias)**.
- Examples: random digit dialing, intercept pop-up surveys, list-based e-mail samples, pre-recruited panels

**Non-probability sampling** – Not every person has an equal chance. Faster/cheaper but introduces bias. Examples: convenience sampling, snowball sampling.

#### Sample Size
- For a population > 100,000: a sample of **384** achieves **95% confidence level** with **5% margin of error**
- Researchers often use **n = 500** to estimate a single population parameter (yields ~±4.4% margin of error)
- To calculate invitations needed: divide target sample size by expected response rate
    - Example: need 384 responses, expect 30% response rate → invite **~1,280 people**

---

### Stage 3: Questionnaire Design and Biases

**Measurement error** – The deviation of respondents' answers from their true values. Can arise from: respondent (low motivation, comprehension problems, deliberate distortion) or instrument (poor wording, visual design flaws).

#### Types of Survey Questions

**Open-ended questions** – Respondent writes in their own answer.
- Use when: answer universe is unknown, options are too numerous to list, measuring qualitative experience or quantities with natural metrics (age, frequency)

**Closed-ended questions** – Predefined answer choices. Four types:
1. **Single-choice** – Only one answer is possible (e.g., education level)
2. **Multiple-choice** – More than one answer may apply ("select all that apply")
3. **Ranking** – Respondents prioritize options in a real-world situation
4. **Rating** – Judge an object on a continuum; uses a **scale**

#### Rating Scales: Unipolar vs. Bipolar

| Scale Type | Description | Recommended Points | Example Constructs |
|---|---|---|---|
| **Unipolar** | Ranges from zero to an extreme; *no natural midpoint* | **5-point scale** | Importance, interest, usefulness, frequency |
| **Bipolar** | Ranges from extreme negative to extreme positive; *has a natural midpoint* | **7-point scale** | Satisfaction, ease of use, perceived speed, visual appeal |

> **Midpoint inclusion**: Including a midpoint **increases reliability** and does not lower data quality. Omitting it forces truly neutral people to pick randomly, increasing measurement error.

> **Scale labels**: Fully labeled scales are preferred over numbered scales. Each scale point should be of **equal visual width** to avoid bias.

---

#### Five Common Questionnaire Biases

**1. Satisficing**
- **Definition**: Respondents use suboptimal cognitive effort — picking the first acceptable answer rather than the best one.
- Tourangeau's **4 cognitive steps** for survey response (satisficers shortcut these):
    1. Comprehension of the question and answer options
    2. Retrieval of specific memories
    3. Judgement of retrieved information
    4. Mapping of judgement onto answer options
- **Weak satisficing**: Careless but still attempts all 4 steps
- **Strong satisficing**: Skips retrieval and judgement entirely; answers randomly
- Causes: low cognitive ability, low motivation, high question difficulty
- **Minimize by**: avoiding complex questions, avoiding "no opinion" options, avoiding back-to-back same-scale questions (**straight-lining**), keeping surveys short, using **trap questions**

**2. Acquiescence Bias**
- **Definition**: Tendency to agree with statements regardless of content (yes-saying bias)
- Causes: low ability/motivation, social conventions favoring "yes," deferential agreement
- **Minimize by**: Avoiding agree/disagree formats; use construct-specific questions; use **reverse-keyed constructs** (ask same construct positively and negatively, then combine scores)

**3. Social Desirability**
- **Definition**: Respondents answer in a way they feel will be viewed positively by others; sensitive topics are underreported/overreported
- Topics prone to this: voting behavior, religion, sexual activity, illegal acts, charitable acts
- **Minimize by**: allowing anonymous responses; using self-administered (not interviewer-present) surveys

**4. Response Order Bias**
- **Definition**: Tendency to select items at the beginning (**primacy effect**) or end (**recency effect**) of a list
- **Minimize by**: randomly ordering unrelated answer options; ordering rating scales negative-to-positive; randomly reversing ordinal scale order between respondents

**5. Question Order Bias**
- **Definition**: Each question can prime respondents and bias responses to subsequent questions
- **Minimize by**:
    - Order questions **broad → specific** (funnel approach)
    - Start with **easy, topic-related** questions to build rapport
    - Place sensitive/complex/non-critical questions **toward the end**
    - Group **related questions** together to reduce context switching
    - Divide into pages with labeled sections

---

#### Question Types to Avoid

| Question Type | Problem | Example |
|---|---|---|
| **Broad** | Too vague, can be interpreted multiple ways | "Describe the way you use your tablet" |
| **Leading** | Biases respondent toward a specific answer | "This app is ranked #1. How satisfied are you?" |
| **Double-barreled** | Asks about two things at once (detectable by "and") | "How satisfied are you with your smartphone *and* tablet?" |
| **Recall** | Requires remembering past behavior inaccurately | "How many times did you use a search engine in the last 6 months?" |
| **Prediction** | Asks about future behavior (unreliable) | "How often will you use this app next month?" |
| **Hypothetical** | Imaginary scenarios; doesn't predict real behavior | "Would you use this feature if it were added?" |

---

#### Established Usability Questionnaires (Know These!)

| Name | Acronym | What It Measures |
|---|---|---|
| **NASA Task Load Index** | NASA TLX | Workload: mental demand, physical demand, temporal demand, performance, effort, frustration |
| **Questionnaire for User Interface Satisfaction** | QUIS | Overall system reaction: screen, terminology, learnability |
| **Software Usability Measurement Inventory** | SUMI | Perceived software quality: efficiency, affect, helpfulness, control, learnability |
| **Computer System Usability Questionnaire** | CSUQ | User satisfaction with system usability (IBM) |
| **System Usability Scale** | SUS | Effectiveness, efficiency, and satisfaction — 10 questions → single score. Most widely used. |
| **Visual Aesthetics of Website Inventory** | VisAwi | Visual aesthetics: simplicity, diversity, colorfulness, craftsmanship |

---

#### Visual Survey Design Considerations
- **Context-shaping images** can bias respondents (e.g., hospital bed image inflates health self-ratings)
- **Uneven spacing** between horizontal scale options biases toward larger-spaced options → use **evenly spaced** options
- **Drop-down lists** are harder, slower, and cause more accidental selections than radio buttons
- **Larger text fields** increase text entry but may intimidate respondents → higher break-off
- **Progress bars**: helpful for **short surveys**, but can increase break-off in long surveys (slow progress is demoralizing)

---

### Stage 4: Review and Survey Pretesting

#### Cognitive Pretesting
- Small group of potential respondents takes the survey while using the **think-aloud protocol** (like a usability study)
- Assesses: question interpretation, construct validity, comprehension, missing answer options
- Participants are asked for each question:
    1. "Read and describe it in your own words"
    2. "Select an answer while explaining your thought process"
    3. "Describe any confusing terminology or missing answer choices"
- **Limitation**: Lab setting — cannot detect contextual influences on break-off

#### Field Testing
- Pilot the survey with a **small subset of the actual sample**
- Assesses: sampling approach success, break-off points, completion times, open-ended responses
- Can add an explicit feedback question at the end of each page
- May lead to multiple rounds of improvement

---

### Stage 5: Implementation and Launch

**Survey modes**: mail, phone, face-to-face, **Internet** (most common in HCI)

**Internet survey advantages**: wide geographic reach, low cost, speed, anonymity (reduces social desirability bias), **skip logic**

**Internet survey disadvantages**: **coverage error** (excludes people without internet access), lower motivation to respond, minimal respondent info

**Skip logic** – Showing respondents different sets of questions based on their answer to a previous question.

**Piping** – Combining survey responses with behavioral log data for more accurate insights (e.g., merging actual usage frequency from logs with self-reported satisfaction).

#### Survey Paradata (Monitor These After Launch)
**Paradata** – Data collected *about* the survey response process itself.
- **Click-through rate**: Of those invited, how many opened the survey
- **Completion rate**: Of those who opened, how many finished
- **Response rate**: Of those invited, how many finished
- **Break-off rate**: Of those who started, how many dropped off on each page
- **Completion time**: How long it took to finish

> Typical response rates: **30–40%** for e-mail surveys; **15% or lower** for intercept (pop-up) surveys; **40–55%** for mailed surveys

#### Maximizing Response Rates
- **Dillman's Total Design Method**: timed sequence of 4 mailings (initial request, reminder postcard, replacement survey, certified mail) → achieves **70%+** response rates
- Use social exchange theory: personalize invitations, explain importance, assure confidentiality
- **Incentives**: monetary > non-monetary; **non-contingent** (given upfront to all invitees) > contingent (given only upon completion)
- High response rate ≠ low non-response bias (Groves, 2006 meta-analysis finding)

---

### Stage 6: Data Analysis and Reporting

#### Data Cleaning (Do This First)
Signs of poor-quality responses to identify and remove:
- **Duplicate responses** – Same person completed it more than once
- **Speeders** – Completed impossibly fast; likely answered carelessly
- **Straight-liners** – Always pick the same answer option across all questions
- **Missing data/break-offs** – Respondents who skipped questions or dropped out

**Listwise deletion** – Remove the entire respondent's data  
**Pairwise deletion** – Remove only the individual question's data

#### Analysis of Closed-Ended Responses
- **Descriptive statistics**: frequency distribution, central tendency (mean/median/mode), dispersion (standard deviation, variance)
- **Inferential statistics** — two types:
    - **Estimation statistics**: calculate margin of error or confidence interval to generalize from sample to population
    - **Hypothesis testing**: compare groups using t-test, ANOVA, Chi-square
- **Correlational analyses**: bivariate correlations, linear regression, logistic regression, factor analysis, cluster analysis

#### Analysis of Open-Ended Responses
- **Coding** – Assigning words or short phrases (codes) to summarize each comment
- **Deductive coding**: codes defined top-down *before* reading the data
- **Inductive coding**: codes generated bottom-up *from* the data (recommended — captures unexpected categories)
- **Intra-rater reliability**: same coder re-codes a subset to check consistency
- **Inter-rater reliability**: two independent coders code the same data; measured using **Cohen's kappa**

---

## Key Terms Quick Reference

| Term | Definition |
|---|---|
| **Survey** | Method of gathering info from a sample, results generalizable to a population |
| **Construct** | Unidimensional, unobservable attribute measured indirectly through questions |
| **Population** | Full set of individuals to whom results should generalize |
| **Sampling frame** | The set of people the researcher can actually contact |
| **Sample** | People invited to take the survey |
| **Respondents** | People who actually complete the survey |
| **Coverage error** | Sampling frame excludes certain types of people, biasing results |
| **Probability (random) sampling** | Every person has equal chance of selection; minimizes selection bias; gold standard |
| **Non-probability sampling** | Not every person has equal chance; cheaper but introduces bias |
| **Satisficing** | Using suboptimal cognitive effort; picking "good enough" rather than best answer |
| **Straight-lining** | Picking the same scale point across all questions (form of satisficing) |
| **Acquiescence bias** | Tendency to agree with statements regardless of content |
| **Social desirability** | Answering to appear favorable to others; sensitive topics underreported |
| **Response order bias** | Tendency to pick options at beginning (primacy) or end (recency) of a list |
| **Question order bias** | Earlier questions prime and bias responses to later questions |
| **Double-barreled question** | Asks two things at once with one answer option |
| **Leading question** | Biases respondents toward a specific answer |
| **Measurement error** | Deviation of responses from true values |
| **Unipolar scale** | Ranges from zero to extreme; 5-point scale recommended |
| **Bipolar scale** | Ranges from negative extreme to positive extreme; 7-point scale recommended |
| **Skip logic** | Different questions shown based on prior answers |
| **Piping** | Merging survey responses with behavioral log data |
| **Paradata** | Data about the survey response process (completion time, break-off rate, etc.) |
| **Cognitive pretesting** | Small group takes survey with think-aloud to identify confusion before launch |
| **Field testing** | Pilot the survey with a small subset of the actual sample |
| **Inter-rater reliability** | Agreement level between two independent coders; measured by Cohen's kappa |
| **Intra-rater reliability** | Agreement when same coder re-codes the same data |
| **Listwise deletion** | Removing all data from a respondent due to poor quality |
| **Pairwise deletion** | Removing only a specific question's data from a respondent |
| **SUS** | System Usability Scale — 10 questions → 1 score; most widely used usability questionnaire |
| **NASA TLX** | Task Load Index — measures workload on 6 dimensions |
| **Non-contingent incentive** | Incentive given to all invitees upfront; more effective than contingent (completion-based) incentives |


# 3.4 1: "Brainstorm, Chainstorm, Cheatstorm, Tweetstorm: New Ideation Strategies for Distributed HCI Design"
*Faste, Rachmel, Essary, Sheehan — CHI 2013, Carnegie Mellon HCI Institute*

---

## Core Thesis

> Ideation does **not** require the generation of new ideas. The value of brainstorming is less about creating novel ideas than the **cultural influence** of unconventional ideas on the ideating team. Brainstorming = radical redistribution of ideas to "unconventionalize" a context.

---

## Key Term Definitions

| Term | Definition |
|---|---|
| **Ideation** | The generation and elaboration of ideas |
| **Brainstorming** | Generation and elaboration of (usually) language-based ideas following Osborn-like rules |
| **Chainstorming** | Brainstorming performed by passing ideas (and rules) along communication chains; online communication brainstorming |
| **Cheatstorming** | Brainstorming **without** the idea generation component; previously generated ideas are delivered to new contexts in response to a prompt |
| **Tweetstormer** | A digital chainstorming application that leverages cheatstorming; uses Twitter as the transactional medium |
| **Electronic Brainstorming** | Generation and elaboration of (usually) text-based ideas, mediated by computers |
| **Nominal Idea Generation** | Individual brainstorming in which participants are not influenced by others' ideas in real-time |
| **Production Blocking** | A brainstorming limitation where only one person can speak at a time, suppressing others' ideas |
| **Evaluation Apprehension** | Fear of being judged for unusual ideas, inhibiting creative contribution in groups |
| **Free Riding** | Reduced individual motivation in group settings because contributions are not individually attributed |
| **Constructive Strain** | The creative tension produced when unrelated or contradictory ideas are juxtaposed |

---

## Osborn's Brainstorming Framework (1953)

**Source:** Alex Osborn's *Applied Imagination* (1963, 3rd ed.)

### Three Phases of Creative Problem Solving
1. **Fact-finding** — Problem definition and preparation; gathering and analyzing relevant data
2. **Idea-finding** — Idea production and development; thinking of tentative ideas and selecting/combining them *(Osborn said this phase is most neglected)*
3. **Solution-finding** — Evaluation and adoption; verifying and implementing final selected solutions

### Osborn's 4 Rules for Brainstorming
1. **Criticism is ruled out** — Adverse judgment of ideas must be withheld until later ("defer judgment")
2. **"Free-wheeling" is welcomed** — The wilder the idea the better; easier to tame down than think up
3. **Quantity is wanted** — More ideas = greater likelihood of useful ideas
4. **Combination and improvement are sought** — Build on others' ideas; join ideas into new ones

> Note: Osborn himself stated "group brainstorming is recommended solely as a **supplement** to individual ideation."

---

## Limitations of Brainstorming (3 Major Problems)

### 1. Production Blocking
- Only one person speaks at a time → others are inhibited
- Ideas may be suppressed or forgotten while listening to others
- Passive listening disrupts individual thought processes

### 2. Evaluation Apprehension
- Creativity = unconventional act → involves personal risk
- Fear of criticism persists even with "defer judgment" rules
- Study by Collaros & Anderson (1969): Productivity loss observed when groups were told there were "undercover" experts present
- Maginn & Harris (1980): Expert observers through a one-way mirror showed no major productivity difference (control vs. observed)

### 3. Free Riding
- When contributions are not individually identified, motivation decreases
- Lower identifiability → less perceived individual effectiveness
- All generated ideas are pooled together → no personal recognition

---

## Three Configurations of Ideation

| Method | Key Traits |
|---|---|
| **Face-to-face Brainstorming** | Simultaneous, spontaneous, 15–45 min sessions, facilitated, group sizes up to 12 (Osborn), ideas built on in real-time |
| **Nominal Idea Generation** | Done individually, no real-time social influence, research suggests higher quality/quantity due to absence of group inhibitory factors |
| **Computer-Mediated (Electronic)** | Distributed asynchronously, can support nominal and group styles, flexible combinations |

> These three methods are **not mutually exclusive** and can be combined.

---

## Design Research Methodology

The authors used a **design-driven research** approach (based on Fallman's design-oriented HCI) consisting of 4 phases:

1. **Opportunity Finding** — Concept sketches, Post-It notes, 2×2 matrix ("Fun Impact" vs. "Social Impact") → 7 opportunity areas
2. **Electronic Brainstorming** — 7 "How could we…" questions in Google Docs; 30+ interdisciplinary CMU students contributed; goal: 50 ideas per question; 350 total distinct ideas generated
3. **Concept Selection and Refinement** — Impact/Achievability matrix; resulted in two key concepts: **chainstorming** (idea "broken telephone") and **cheatstorming** (creative judgment tasks/voting on existing ideas)
4. **Experimentation** — Two cheatstorming studies (described below)

---

## Cheatstorming — Study 1 (Pilot)

**Premise:** After many brainstorms, thousands of ideas already exist. Given a *new* prompt and 50 *random previous* ideas, skip concept generation entirely and jump to **voting** on which ideas fit.

**Procedure:**
- Team generated random brainstorm questions and random solution concepts on Post-Its
- A random question was paired with 10 random concept Post-Its
- The 4 concepts that best resonated were selected as "winners"
- Repeated 4 times

**Key Finding:** Results were "surprisingly unexpected and fresh." Unexpected combinatory patterns emerged (e.g., screen-based ideas for city illumination also suggested crime safety via kiosks/maps). Process was fast, fun, and required low cognitive effort.

---

## Cheatstorming — Study 2 (Controlled)

**Goal:** Compare different types of "idea input" and compare cheatstorming to traditional brainstorming.

**Input:** 5 previously completed brainstorming sessions from different HCI projects (50+ ideas each, with prior "winners" marked with asterisks).

### Four Experimental Conditions (all used same prompt — Question 5):
| Condition | Description | Expected Result |
|---|---|---|
| **A — Brainstorm Baseline** | Original brainstorm winners for that prompt used as-is | Most familiar/applicable |
| **B — Overlapping Diverse Input** | 17 ideas each from sets 2, 3, 4 (set 4 related to prompt) | Mix of fresh + familiar |
| **C — Unrelated Diverse Input** | 17 ideas each from sets 1, 2, 3 (none related to prompt) | Most random/creative |
| **D — Unrelated Narrow Input** | All 50 ideas from single unrelated set 1 | Most technologically immersive |

**Procedure:** 50 input ideas laid out → worked through one-by-one → grouped into 10 "winning" clusters → each cluster given a new meaningful title.

### Key Findings — Process
- Ideas that were more **familiar** were harder to associate with new meanings
- **Strangeness** is essential: unconventional content must not be familiar to yield creative results
- Diversity of input generally helped broaden scope

### Key Findings — Results
- **Condition A** (baseline): Most immediately useful; not heavily technology-focused
- **Condition B** (overlapping diverse): Most palatable non-baseline; fresh ideas grounded in something familiar
- **Condition C** (unrelated diverse): "Most random" — exciting but out-of-touch with project goals
- **Condition D** (unrelated narrow): Most technologically immersive; compelling but strayed far from project focus
- **All conditions** produced ideas related to the prompt — but ideas reflected the spirit of the brainstorm they originated from

---

## Four-Stage Model of Group Ideation (Authors' Proposed Framework)

The authors propose a **4-stage model** (contrasting earlier models like Jones' "diverge-transform-converge"):

1. **Prompting** — Facilitator presents the challenge to drive ideation
2. **Sharing** — Participants suggest and communicate ideas (orally, whiteboard, sticky notes, database, etc.)
3. **Selecting** — Participants vote / determine their favorite ideas
4. **Committing** — Final criteria set to evaluate, prioritize, and move ideas forward

> Key distinction: This model does **not** view creativity as a "generative" activity. Ideas are **transferred/shared** between people — sharing IS the ideation.

---

## Chainstorming Explained

**Inspired by:** "Broken telephone" / "Chinese whispers" game

**How it works:**
- First person generates prompt + 1–2 ideas → sends to a network
- Each subsequent person sees the prompt + a **subset of prior ideas** → builds on them
- Chain continues → collective creativity embedded in social networks
- Introduces randomness at each stage, reducing cognitive effort

**Tweetstormer** — prototype platform using Twitter as the medium:
- Users post/respond to tweeted prompt questions
- Browse others' replies, vote on favorite ideas
- Enables ideation anytime, anywhere via mobile/computer

**Success factors for chainstorming:**
- Social constitution of the chain
- Level of participant training
- Group's experience with the task
- Criteria used to evaluate outcomes
- Managing: lack of context in passed messages, redundant concepts, dead ends, parallel chains

---

## Core Theoretical Claim

> **"Brainstorming is more than the pooling of 'invented' ideas — it involves the sharing and interpretation of concepts in unintended and (ideally) unanticipated ways."**

- Ideas need **not** be created by the team for ideation to occur
- They simply need to be **interpreted as possibilities** from a collision of shared meanings
- The only requirement: ideas in the sharing stage must be **unconventional** ("strange") to the ideating individual/team/culture
- **Cheatstorming** can "dial in strangeness" — enabling targeted conceptual leaps from an original idea set to a much wider framing of the problem

---

## Comparison to Prior Ideation Models

| Prior Model | Key Concept |
|---|---|
| Jones (1970) | Divergence → Transformation → Convergence |
| Nijstad et al. (2010) | Dual Pathway to Creativity (flexibility + persistence) |
| **This paper's model** | Prompting → Sharing → Selecting → Committing (social/communicative, non-generative) |

---

## Important Quotes / Testable Claims

- Osborn's book: *Applied Imagination* (first published 1953, Scribner)
- First major criticism of brainstorming: Taylor, Berry & Block (1958), Yale University — compared group vs. individual pooled results
- Osborn suggested group sizes up to **12** as effective
- Classic face-to-face brainstorming sessions: **15 to 45 minutes**
- Study 1 electronic brainstorm: **350 total distinct ideas** generated across 7 questions with 30+ students over a 4-day weekend
- Cheatstorming "bypasses the concept generation phase altogether and jumps directly to voting"

# 3.4 2:  Chapter 6: "The Process of Interaction Design"
*From: Interaction Design: Beyond Human-Computer Interaction*

---

## Core Definition

**Design** (Oxford English Dictionary): "a plan or scheme conceived in the mind and intended for subsequent execution."

- Interaction design = developing a plan informed by the product's intended use, target domain, and practical constraints
- Central philosophy: **user-centered design** — users' concerns drive development, not technical concerns
- Design is about **trade-offs** — balancing conflicting requirements
- Key principle: *"To get a good idea, get lots of ideas"* (Marc Rettig, 1994) → generating alternatives is essential

---

## Key Term Definitions

| Term | Definition |
|---|---|
| **User-centered design** | An approach where users' concerns and needs direct the development of a product rather than technical concerns |
| **Stakeholders** | "People or organizations who will be affected by the system and who have a direct or indirect influence on the system requirements" (Kotonya & Sommerville, 1998) |
| **Conceptual design** | A sub-activity of designing; producing the conceptual model — what the product should *do*, *behave*, and *look like* |
| **Physical design** | A sub-activity of designing; considers the detail of the product — colors, sounds, images, menu design, icon design |
| **Prototype / Prototyping** | A limited version of a product built to answer specific questions about design feasibility or appropriateness |
| **Lifecycle model** | A model that captures a set of activities and how they are related; may also describe when/how to move between activities and deliverables |
| **Usability engineering** | An approach involving specifying quantifiable measures of product performance, documenting them in a usability specification, and assessing the product against them |
| **Iteration** | The repeated cycling through design activities to refine a product based on feedback |
| **Time-boxing** | A RAD concept: time-limited cycles (~6 months) at the end of which a system or partial system must be delivered |
| **JAD (Joint Application Development)** | Intensive requirements-gathering workshops in which users and developers come together to determine system requirements; part of RAD |
| **DSDM** | Dynamic Systems Development Method; an industry-standard RAD-based method; first principle: "active user involvement is imperative" |

---

## Four Basic Activities of Interaction Design

These are the core activities — know them well:

1. **Identifying needs and establishing requirements**
    - Understand who the users are and what support an interactive product could usefully provide
    - Forms the basis of the product's requirements; fundamental to user-centered approach

2. **Developing alternative designs**
    - The core activity of designing: suggesting ideas for meeting the requirements
    - Split into two sub-activities:
        - **Conceptual design**: producing the conceptual model (what the product should do, behave, and look like)
        - **Physical design**: detail of the product (colors, sounds, images, menu design, icon design)

3. **Building interactive versions of the designs**
    - Does NOT require working software — paper-based prototypes are valid
    - Role-playing can give users a real sense of what interaction will feel like
    - Interactive versions allow users to actually evaluate designs

4. **Evaluating designs**
    - Determining the **usability and acceptability** of the product
    - Measured by: number of errors, appeal, match to requirements, etc.
    - Does **not** replace quality assurance/testing — it **complements** them

> Activities 2, 3, and 4 are **intertwined**: alternatives are evaluated through interactive versions, and results feed back into further design (iteration).

---

## Three Key Characteristics of Interaction Design

1. **User focus** — users are involved throughout development
2. **Specific usability criteria** — identified, clearly documented, and agreed upon at the start; used to choose between alternatives and check progress
3. **Iteration** — designs are refined based on feedback; "Iteration is inevitable because designers never get the solution right the first time" (Gould and Lewis, 1985)

---

## Practical Issues

### Who Are the Users?

**Eason's (1987) Three Categories of User:**
- **Primary users** — frequent, hands-on users of the system
- **Secondary users** — occasional users or those who use the system through an intermediary
- **Tertiary users** — those affected by the introduction of the system or who will influence its purchase

**Stakeholders** are broader than users — includes the development team, managers, direct users, recipients of output, people who may lose jobs due to the system, etc. Not all stakeholders need to be involved, but all should be identified.

> Key warning (Dix et al., 1993): "It will frequently be the case that the formal 'client' who orders the system falls very low on the list of those affected. Be very wary of changes which take power, influence or control from some stakeholders without returning something tangible in its place."

---

### What Do We Mean by "Needs"?

- You **cannot** simply ask people "What do you need?" — people don't know what's possible
- Must understand: user characteristics, what they're trying to achieve, how they achieve it currently, and whether they'd be better supported differently
- For new/innovative products, there are no prior users — start with **similar existing behavior** as a reference (e.g., standard phones → cell phones)
- Good indication of future behavior = **current or past behavior**
- Dimensions of user characteristics: physical attributes, motor abilities, cultural diversity, experience, workplace norms

---

### How Do You Generate Alternative Designs?

Sources of design alternatives:
- **Individual creativity and flair**
- **Cross-fertilization** of ideas from different applications
- **Evolution** of existing products
- **Copying/adapting** similar products
- **Browsing collections of designs** — inspires alternative perspectives
- **Case-based reasoning** — solving new problems by drawing on knowledge from solving similar previous problems

> "An expert is someone who gets reminded of just the right prior experience to help him in processing his current experiences." — Schank (1982)

**IDEO TechBox** — real-world example: a flatbed filing cabinet with ~200 engineering gizmos in categories (Amazing Materials, Cool Mechanisms, Electronic Technologies, etc.), taken to brainstorming meetings to spark ideas and provide inspiration.

---

### How Do You Choose Among Alternative Designs?

Two categories of design decisions:
1. **Externally visible and measurable** features (what users interact with)
2. **Hidden internal** characteristics (implementation details)

→ Interaction design focuses on **externally visible behavior** since the user interaction is the driving force.

Three ways to choose:
- Let **users and stakeholders interact** with designs and discuss experiences (requires design be in a form users can evaluate)
- **Prototyping** — provides a better impression of user experience than static descriptions
- **Usability criteria** — formal, verifiable, measurable criteria that set benchmarks

> **Usability engineering**: writing down formal, measurable usability criteria in a *usability specification* and assessing the product against them. (Whiteside et al., 1988; Nielsen, 1993)

**Usability goals** (from Chapter 1) — must be measurable and specific:
- **Effectiveness**, **Efficiency**, **Safety**, **Utility**, **Learnability**, **Memorability**

User experience criteria (harder to measure — subjective): satisfaction, enjoyment, motivation, aesthetics

---

## Lifecycle Models

A **lifecycle model** captures a set of activities and how they are related. Used so managers can track progress, allocate resources, specify deliverables, and set targets. Any lifecycle model is a **simplified abstraction** of reality.

---

### The Interaction Design Lifecycle Model (Book's Model)

**Simple four-activity model** (Figure 6.7):

```
Identify needs / establish requirements
        ↓
    (Re)Design
        ↓
Build an interactive version
        ↓
     Evaluate
        ↓
  Final product (when usability criteria met)
```

- **Iterative** — results of evaluation feed back into redesign or re-identifying requirements
- Not prescriptive — represents observed practice
- Ends with an evaluation ensuring the final product meets prescribed usability criteria

---

### Lifecycle Models from Software Engineering

#### 1. Waterfall Model
- Proposed: **1970** (first generally known model in software engineering)
- **Linear** — each step must be completed before the next begins
- Stages: Requirements Analysis → Design → Code → Test → Maintenance
- **Main flaw**: Requirements change over time, but waterfall freezes them for the whole development period
- No built-in opportunity to review/evaluate with users
- Some limited feedback between phases was added later, but not embedded in its philosophy

#### 2. Spiral Model
- Proposed: **Barry Boehm, 1988**
- Key features: **risk analysis** and **prototyping**, in an iterative framework
- Development driven by **risks**, not intended functionality (unlike waterfall)
- Explicitly encourages alternatives and re-addressing problematic steps
- **WinWin Spiral** (Boehm et al., 1998): adds identification of key stakeholders and their "win" conditions; includes stakeholder negotiation for a win-win result

#### 3. RAD (Rapid Applications Development)
- Emerged in the **early 1990s** as a response to inappropriate linear lifecycle models
- Two key features:
    - **Time-boxing**: ~6-month cycles, partial system delivered at the end of each
    - **JAD workshops**: intensive sessions where users and developers jointly define requirements; all stakeholder groups represented
- Basic RAD lifecycle (5 phases): project set-up → JAD workshops → iterative design and build → engineer and test final prototype → implementation review
- **DSDM** (Dynamic Systems Development Method): industry-standard RAD-based method; 5 phases: feasibility study, business study, functional model iteration, design and build iteration, implementation
    - First of nine DSDM principles: "**active user involvement is imperative**"

---

### Lifecycle Models from HCI

#### 1. Star Lifecycle Model
- Proposed: **Hartson and Hix, 1989**
- Derived from **empirical work** on how interface designers actually work
- Two modes of designer activity identified:
    - **Analytic mode**: top-down, organizing, judicial, formal (system view → user view)
    - **Synthetic mode**: bottom-up, free-thinking, creative, ad hoc (user view → system view)
- **No fixed ordering of activities** — you can move from any activity to any other
- **Evaluation is central** — every activity's results must be evaluated before moving on
- Activities: task analysis/functional analysis, requirements/specification, conceptual design/formal design, prototyping, implementation, evaluation
- **Weakness**: Too flexible for large projects — hard to track progress, allocate resources, set targets

#### 2. Usability Engineering Lifecycle
- Proposed: **Deborah Mayhew, 1999**
- Provides a holistic view of usability engineering + detailed guidance on how to perform usability tasks
- Links to software development methods: **rapid prototyping** and **object-oriented software engineering (OOSE)**
- Three main tasks:
    1. **Requirements Analysis** — produces usability goals captured in a *style guide*
    2. **Design/Testing/Development** — largest phase; 3 levels (conceptual model design, screen design standards, detailed UI design), each with iterative evaluation
    3. **Installation** — user feedback collected; issues resolved or enhancements planned
- Difference from book's model: iteration between design and evaluation is **contained within phase 2**; iteration back to requirements analysis only after conceptual model and detailed designs have been developed, prototyped, and evaluated

---

## Summary of Lifecycle Model Comparisons

| Model | Origin | Key Feature | User Involvement |
|---|---|---|---|
| **Waterfall** | Software Eng. (1970) | Linear, sequential | Minimal (not built in) |
| **Spiral** | Software Eng. (Boehm, 1988) | Risk analysis + iteration | Some (through prototyping) |
| **RAD/DSDM** | Software Eng. (1990s) | Time-boxing + JAD | High (JAD workshops) |
| **Star** | HCI (Hartson & Hix, 1989) | Evaluation-centered, no fixed order | High (evaluation central) |
| **Usability Engineering** | HCI (Mayhew, 1999) | Structured, style guide, detailed subtasks | High (usability goals throughout) |
| **Interaction Design (book)** | HCI | Simple 4-activity iterative model | High (user focus is a key characteristic) |

---

## Interview Highlights — Gillian Crampton Smith

Key ideas from the interview (may appear in exam):
- Things should "**work but also delight**" — design is about aesthetics AND function
- Four stages of design (GC's view): (1) research/finding out about people; (2) conceptual design (what should it do?); (3) giving it form (how to represent it?); (4) crafting the interface details
- **Engineers** are trained to focus *in* on a solution from the beginning; **designers** are trained to focus *out* first (explore many alternatives) then focus in — this causes tension in interdisciplinary teams
- Ideal team: people confident in their own field and **open-minded** enough to value different approaches (engineering, design, scientific)
- On users: users should **not** be part of the design team, but should be involved as a source of inspiration and for evaluating proposals
- Design coherence: protecting a design's coherence is both a vice and a virtue

---

## Key Points to Memorize

- Iteration is inevitable: "designers never get the solution right the first time" — Gould and Lewis (1985)
- Waterfall proposed: **1970** | Spiral: **Boehm, 1988** | Star: **Hartson & Hix, 1989** | Usability Engineering Lifecycle: **Mayhew, 1999** | RAD: **early 1990s**
- The Star model has **evaluation at its center** — no fixed ordering of activities
- Usability Engineering = specifying **quantifiable, measurable** criteria in a usability specification
- DSDM's first principle: "**active user involvement is imperative**"
- Conceptual design = what the product *does/behaves/looks like*; Physical design = *details* (color, sound, icons, menus)

# 3.5 1: Chapter 52: "Prototyping Tools and Techniques"
*Beaudouin-Lafon & Mackay*

---

## Core Definition

> **Prototype**: "a concrete representation of part or all of an interactive system." A tangible artifact — not an abstract description that requires interpretation.

Key points:
- Prototypes are used by designers, managers, developers, customers, and end-users to **envision and reflect** upon the final system
- Interactive system prototypes must be **full-scale** (unlike architecture scale models) — you may limit data, but the interface must be presented at full size
- Most successful software prototypes **evolve into the final product**, not thrown away

---

## Key Term Definitions

| Term | Definition |
|---|---|
| **Off-line prototypes** | Paper-based prototypes that do not require a computer (sketches, storyboards, cardboard mock-ups, videos); created quickly, usually thrown away |
| **On-line prototypes** | Software prototypes that run on a computer (animations, scripting languages, interface builders); higher cost, more effective in later stages |
| **Precision** | The relevance of details with respect to the purpose of the prototype; what is stated (subject to evaluation) vs. what is left open (subject to more exploration) |
| **Design space** | The set of ideas and constraints that define possible design directions; expanded by generating ideas, contracted by making design choices |
| **Participatory design** (= Cooperative Design) | A form of user-centered design that actively involves the user in ALL phases of the design process — as partners, not just consultants |
| **Video brainstorming** | Participants act out ideas in front of a video camera; expands the design space by generating many unconnected ideas |
| **Video prototyping** | Uses video to refine a single design; contracts the design space by showing how a specific collection of design choices work together |
| **Wizard of Oz** | A technique where a human (the "wizard") secretly operates a partially-functional system, creating the illusion of a working system to the user |
| **Storyboard** | A sequence of rough sketches of each action/event with annotations — like a comic book; used to plan and shoot video prototypes |
| **Horizontal prototype** | Develops one entire layer of the design (usually the UI) at the same time; gives overall picture from user's perspective |
| **Vertical prototype** | Implements one feature all the way through all layers to test feasibility; usually high precision, often thrown away |
| **Task-oriented prototype** | Organized around specific user tasks; combines breadth of horizontal with depth of vertical |
| **Scenario-based prototype** | Follows a realistic story of how the system would be used in a real-world setting |
| **MVC (Model-View-Controller)** | Software architecture pattern: Model = data/information; View = displays information; Controller = interprets user input and updates model |
| **PAC (Presentation-Abstraction-Control)** | Architecture similar to MVC but abstract; Presentation = input/output; Abstraction = data (like Model); Control = manages communication |
| **Widget** | A software object in a UI toolkit with three facets: presentation (how it looks), behavior (how it responds), and application interface (how it communicates with the rest of the app) |
| **Extreme Programming** | A software development approach that tightly couples design and implementation, building through constant evolution — advocates evolutionary prototyping |

---

## Four Dimensions for Analyzing Prototypes

These are the key framework — know them well:

### 1. Representation
How the prototype is **formed**:
- **Off-line (paper)**: sketches, storyboards, cardboard mock-ups, videos — quick, cheap, no computer required, usually thrown away; best for **early stages**
- **On-line (software)**: animations, scripting languages, interface builders — higher cost, need skilled programmers for advanced techniques; best for **later stages** when basic strategy is decided

> **Why off-line prototypes are better in early stages** (3 reasons):
> 1. **Inexpensive and quick** — rapid iteration; prevents over-attachment to first solution
> 2. **Less constraining** — programming tools impose limits on creativity (e.g., easy to make scrollbars, hard to make zoomable interfaces); paper has no such limits
> 3. **Inclusive** — anyone can contribute (designers, users, managers), not just programmers; improves communication and buy-in

### 2. Precision
The **relevance of details** with respect to the prototype's purpose:
- Imprecise parts are **open for discussion** or further design space exploration
- Precise parts are **subject to evaluation**
- Level of precision typically **increases** with successive prototypes
- Sketches tend to be imprecise; computer simulations are usually precise
- Note: **detailed ≠ precise** — you can have a detailed sketch of a dialog box but still leave label text as squiggles (precise enough to show labels are needed, imprecise about content)

> Authors prefer "precision" over "low/high fidelity" because it refers to the prototype's content, not its relationship to the final system.

### 3. Interactivity
The **extent to which users can interact** with the prototype:
- Three levels:
    - **Fixed prototypes**: non-interactive (video clips, pre-computed animations) — illustrate what interaction *might look like*
    - **Fixed-path prototypes**: limited interaction; pre-specified steps trigger responses — provide *experience of interaction*, but only in pre-specified situations
    - **Open prototypes**: support large sets of interactions, work like the real system with some limitations — allow testing of *wide range of user interactions*
- Interactivity and precision are **orthogonal** — you can have a highly interactive but imprecise prototype (paper-based role-playing), or a precise but non-interactive one (detailed animation)

### 4. Evolution
The **expected life-cycle** of the prototype:
- **Rapid prototypes**: created for a specific purpose and thrown away; especially important in early stages; must be inexpensive and easy to produce
- **Iterative prototypes**: evolve through several design iterations; increasing precision or exploring alternatives; tension between evolving toward final solution and exploring unexpected directions
- **Evolutionary prototypes**: a special case of iterative — prototype **becomes part or all of the final system** (only applies to software prototypes); used in Extreme Programming; requires more planning; harder to explore alternatives

> Recommended approach: **start with rapid prototypes**, then use iterative or evolutionary as needed.

---

## Prototypes as Design Artifacts (Three Characteristics)

Successful prototypes:
1. **Support creativity** — help capture/generate ideas, explore design space, uncover user information
2. **Encourage communication** — help designers, engineers, managers, users discuss options
3. **Permit early evaluation** — can be tested via usability studies or informal user feedback throughout the design process

---

## The Design Space

**Design space** = a set of ideas and constraints. Designers explore it in a **cyclic** process (not linear/reductionist):

- **Expanding** the design space = generating new ideas (brainstorming, video brainstorming)
- **Contracting** the design space = selecting among ideas, making design choices (evaluation, video prototyping)

> Expanding requires **creativity and openness** — avoid criticizing ideas, generate as many as possible (clever, half-finished, silly — all contribute).
> Contracting requires **critical evaluation** — weigh constraints and trade-offs, rejecting ideas is *necessary* to make progress.

Key insight: Choosing a design direction **closes off** part of the design space but **opens up** new dimensions. The designer can also **reframe the design problem** (change constraints) not just generate new ideas within existing constraints.

---

## Participatory Design

- Also called **Cooperative Design**
- Users are treated as **partners throughout** — not just consulted at beginning and end
- Common misconception: designers are expected to abdicate responsibility and leave design to users. **FALSE** — goal is for designers and users to work *together*
- Users are best at: understanding the **context of use** and **subtle aspects of problems**
- Designers are responsible for: considering a wide range of options users may not know, and balancing trade-offs
- Prototypes serve as an effective **shared, concrete medium for communication** in participatory design

---

## Brainstorming (Review / Connection to Reading 3.4)

Simple brainstorming procedure:
- Small group, goal = generate as many ideas as possible (quantity not quality)
- Two phases: (1) generating ideas (no more than 1 hour), (2) reflecting on them
- One **moderator** keeps time, ensures everyone participates, prevents critique
- One person **records all ideas** on a flipchart/transparency
- After a break: each person marks **3 favorite ideas**
- Variant for quiet members: write ideas on individual cards first, then moderator reads aloud

**Video Brainstorming** (Mackay, 2000):
- Participants act out ideas in front of a video camera using paper/cardboard props
- Each idea takes **2–5 minutes** to generate
- Forces designers to seriously consider how a user would interact with the idea
- Video clips = much easier to recall/interpret later than hand-written notes
- Unlike standard brainstorming, encourages even the quietest team members to participate
- Usually run a **standard brainstorm first** to maximize ideas, then develop favorites as video brainstorms

---

## Prototyping Strategies

| Strategy | Description | Key Benefit |
|---|---|---|
| **Horizontal** | One entire layer (usually UI) across the whole system | Overall picture; tests consistency, coverage, redundancy |
| **Vertical** | Full implementation of one feature from UI to underlying system | Tests technical feasibility of a specific feature |
| **Task-oriented** | Covers only functions needed for a set of specified tasks | Combines breadth of horizontal + depth of vertical |
| **Scenario-based** | Follows a realistic story of system use, not independent tasks | Tests realistic user experience; identifies patterns over time |

---

## Off-line Rapid Prototyping Techniques

### Paper & Pencil
- Fastest form — uses paper, transparencies, post-it notes
- Designers play both user and system roles
- Special effects: tiny triangle on transparency strip = mouse pointer; Post-its = pop-up menus; overhead projector on whiteboard = interactive wall display
- Start with quick sketches → progress to more carefully drawn computer-made images

### Mock-ups
- 3D physical prototypes (cardboard, foamcore, found materials)
- Useful for physical device design (button position, screen placement)
- Helps envision how system will be incorporated into physical space

### Wizard of Oz
- Named after the 1939 movie (Kelley, 1993 coined the technique term)
- A hidden human (the "wizard") operates the system, creating the illusion of a working computer for the user
- Originally used for **natural language interfaces**
- Useful when rapid responses are not critical
- Can range from paper prototypes to partially implemented software

### Video Prototyping (Mackay, 1988)
- Process: collect user observations → review video brainstorms → create use scenario → develop **storyboard** → shoot video
- **Storyboard**: sequence of rough sketches + annotations, like a comic book; ~1 paragraph of text = ~1 page of storyboard
- Uses "editing-in-the-camera" technique to create video directly without post-editing
- A second live video camera can be used as a Wizard-of-Oz tool
- Can serve as a **specification for developers**

> **Critical difference**: Video brainstorming **expands** design space (generates many unconnected ideas); video prototyping **contracts** it (shows how specific design choices work together).

---

## On-line Rapid Prototyping Techniques

### Non-interactive simulations
- Computer-generated animations; best created from a storyboard first
- Tools: **Macromedia Director**, Adobe AfterEffects, Macromedia Flash
- Useful when off-line fails to capture a particular aspect of the interaction

### Fixed/Interactive simulations
- Present pre-defined sequences of screens
- Tools: HyperCard, HTML/web authoring tools

### Scripting Languages
- Support open (fully interactive) prototyping
- **Tcl/Tk**: widely used for UI prototyping; Tk provides standard widgets; canvas widget allows custom interaction techniques
- Far fewer lines of code than traditional languages (e.g., 1 line = button widget vs. 5–20 lines in traditional language)

---

## Software Tools for Iterative Prototyping (hierarchy, low to high level)

1. **Graphical libraries** — hardware-independent drawing APIs (Xlib, QuickDraw, Win32 GDI, OpenGL); most flexible but hardest to program
2. **Window systems** — allow multiple apps to share a screen; include window manager
3. **UI toolkits** — provide interactive **widgets** (buttons, menus, scrollbars); most widely used today
4. **UI builders** — interactive graphical editor for creating widget trees without writing layout code; easy to modify and test alternative designs
5. **Application frameworks** — provide a standard shell (e.g., MacApp); developer fills in functional core; assumes stereotyped app (document-based, cut/paste, undo)
6. **Model-based tools** — start from domain objects/functions and auto-generate UI; works toward the interface from the functional core
7. **UIDEs** — integrated collection of all the above tools

> Key tradeoff: **higher-level tools** = easier maintenance, portability, localization but **constrain design space** (limited widget sets, stereotyped apps). Use lower-level tools for novel interaction techniques.

> User interface development costs = **50%–80% of total application development cost** (Myers & Rosson, 1992)

---

## MVC and PAC Architecture Models

### MVC (Model-View-Controller)
- Created for **Smalltalk-80** (Krasner & Pope, 1988)
- Three objects per triplet:
    - **Model**: represents the information/data
    - **View**: displays the model's information
    - **Controller**: interprets user input on the view → changes in the model
- When a model changes, it **notifies its view(s)** to update
- Supports **multiple views** of a single model
- Views and controllers are tightly coupled (sometimes implemented as one object)

### PAC (Presentation-Abstraction-Control)
- Proposed by Coutaz (1987)
- Close to MVC but **abstract** (no reference implementation)
- Three facets of each PAC agent:
    - **Presentation**: captures user input and generates output (like View + Controller)
    - **Abstraction**: holds application data (like Model)
    - **Control**: manages communication between Presentation and Abstraction, and with sub/super-agents

### MVP (Model-View-Presenter)
- Variant of MVC, very close to PAC

---

## Key Quotes / Testable Claims

- "A good design is better than you think" — Rex Heftman (opening quote)
- User interface development cost = **50%–80% of total development cost** (Myers & Rosson, 1992)
- Wizard of Oz coined by **Kelley (1993)**, based on the **1939 movie**
- Brainstorming introduced by **Osborn (1957)**
- Production blocking, free-riding, and evaluation apprehension found to outweigh brainstorming synergy — Collaros & Anderson (1969), Diehl & Stroebe (1987)
- Video Prototyping introduced by **Mackay (1988)**
- MVC created for **Smalltalk-80** by **Krasner & Pope (1988)**
- PAC proposed by **Coutaz (1987)**
- Extreme Programming advocates evolutionary prototyping — **Beck (2000)**
- Participatory Design = "actively involves the user in **all phases** of the design process" (Greenbaum & Kyng, 1991)
- Precision ≠ fidelity: authors deliberately avoid "low/high fidelity" terminology

# 3.5 2:  Chapter 16: "What do Prototypes Prototype?"
*Stephanie Houde & Charles Hill — Apple Computer, Inc.*
*From: Handbook of Human-Computer Interaction, 2nd ed. (1997)*

---

## Core Argument

> Current terminology for prototypes focuses on **attributes of the prototype itself** (what tool was used, how finished it looks). This is misleading. Instead, we should focus on **what the prototype is trying to answer** — its *purpose* with respect to the artifact being designed.

**The shift**: from "what is this prototype made of / how polished is it?" → "what design questions does this prototype explore?"

---

## Key Term Definitions

| Term | Definition |
|---|---|
| **Artifact** | The interactive system being designed — a commercially released product or any end-result of a design activity |
| **Prototype** | "Any representation of a design idea, regardless of medium" — this includes a pre-existing object when used to answer a design question |
| **Designer** | "Anyone who creates a prototype in order to design, regardless of job title" |
| **Resolution** | Amount of detail in a prototype |
| **Fidelity** | Closeness of a prototype to the eventual design |
| **Role** | Questions about the function an artifact serves in a user's life — how it is useful to them |
| **Look and feel** | Questions about the concrete sensory experience of using an artifact — what the user looks at, feels, and hears |
| **Implementation** | Questions about the techniques and components through which an artifact performs its function — the "nuts and bolts" of how it actually works |
| **Integration prototype** | A prototype that explores all three dimensions (role, look and feel, implementation) at once; represents the complete user experience |

---

## The Problem with Current Terminology

Two ways prototypes are currently described — both are problematic:

1. **By tool used**: "C prototype," "Director prototype," "paper prototype"
    - Problem: tools can be used in many different ways; no single tool supports all prototyping needs
    - Even cardboard prototypes are useful for user testing (Ehn & Kyng, 1991)

2. **By level of finish**: "high-fidelity" vs. "low-fidelity"
    - Problem: a finished-looking prototype does NOT necessarily mean the design is near completion
    - A 3D concept model may be made early for market research (high finish, early stage)
    - A rough prototype may be made late to emphasize structure over visual details
    - **Resolution ≠ fidelity ≠ stage of completion**

> "Is a brick a prototype? If used to represent the weight and scale of a future artifact — yes. What matters is not the medium or tool, but **how it is used** to explore or demonstrate some aspect of the future artifact."

> "Looks can be deceiving. Clarifying what aspects of a prototype correspond to the eventual artifact — and what don't — is a key part of successful prototyping."

---

## The Houde & Hill Model — Three Dimensions

The model is a **triangle** with three corners. Any prototype can be placed on this triangle based on which design questions it primarily addresses. The triangle is drawn **askew** to emphasize that no one dimension is inherently more important.

```
           Role
          /    \
         /      \
        /        \
Look & Feel --- Implementation
```

### Dimension 1: Role
- What function does the artifact serve in a user's life?
- How is it useful to them?
- Requires establishing the **context of the artifact's use**
- Example questions: What tasks would users perform? What problem does it solve?

### Dimension 2: Look and Feel
- What is the concrete sensory experience of using the artifact?
- What does the user look at, feel, and hear?
- Requires **simulating or creating the concrete user experience**
- Example questions: What does the interface look like? How does interaction feel?

### Dimension 3: Implementation
- What techniques and components make the artifact actually work?
- Requires **building a working system**
- Example questions: Is this technically feasible? How fast is the rendering? Can we implement this interaction technique?

---

## Four Categories of Prototypes

### 1. Role Prototypes
**Purpose**: Investigate what an artifact could *do* for a user — its functionality and context of use.
- Little attention to how it looks/feels or how it works
- Used to: show design team what the target role might be; communicate to supporting organization; evaluate role in user studies

**Examples from the paper:**
- **Storyboard for portable notebook computer** (Example 4) — paper storyboard showing a student using a pen-and-finger notebook; focused on what functionality should be provided
- **Interactive story for an OS interface** (Example 5) — interactive but single-path; hand-drawn UI elements scanned in; designer play-acted the user role; used for team discussion and manager presentations
    - Notable: some managers became enamored with the sketchy *style* and wanted it in the final product — wrong conclusion from a rough prototype; shows the importance of knowing your audience
- **Knowledge Navigator vision video** (Example 6) — Apple's day-in-the-life video of a professor using a futuristic notebook; high production value because the **audience was very broad** (Apple employees, public); rough storyboard would not have made the idea seem real to a general audience

### 2. Look and Feel Prototypes
**Purpose**: Explore and demonstrate options for the concrete experience of an artifact — what it would be like to look at and interact with.
- Not necessarily investigating role or implementation
- Used to: visualize possibilities for the design team; get user feedback on experience; give supporting org a concrete sense of the artifact

**Examples:**
- **Fashion design workspace animation** (Example 8) — 20-minute animation; confirmed that an engaging look and feel could be designed; shown to managers; issue: inexperienced audiences believed it to be *functional* just because it was on screen — designers had to explain it wasn't implemented
- **GloBall child's toy simulations** (Example 9) — two Wizard of Oz prototypes; one used walkie-talkie to simulate speech, one used radio-controlled car to simulate movement; evaluated how children would respond to toy that seemed to speak and move on its own; both simulated novel technology cheaply
- **Pizza-box architect's computer** (Example 10) — designers weighted a pizza box to the expected weight of a future computer and gave it to an architect on a site visit; observed how he carried it; discovered the rectilinear form was too awkward → led to considering a softer form; a highly efficient look and feel prototype with virtually no build cost

### 3. Implementation Prototypes
**Purpose**: Answer technical questions about how an artifact might actually be made to work.
- Used to: discover methods for meeting technical specs; demonstrate technical feasibility; get user feedback on performance

**Examples:**
- **Digital movie editor** (Example 11) — working prototype in C to test how much interactivity could be added to digital movies; the incidental user interface got in the way of productive discussion → audience critiqued the UI rather than evaluating the implementation; lesson: communicate clearly that look/feel is *not* the focus
- **Fluid dynamics simulation** (Example 12) — C++ program to prove object-oriented programming was viable alternative to FORTRAN for engine simulations; purely an implementation test (performance, memory); eventually became the deployable system

> **Key warning**: Implementation prototypes can find their way into the final system with their temporary UIs never properly redesigned. Treat even implementation prototypes as disposable; migrate successful implementation designs into a new integrated prototype.

### 4. Integration Prototypes
**Purpose**: Represent the **complete user experience** of an artifact — role, look and feel, and implementation together.
- Most accurately simulate the final artifact
- Most **difficult and time-consuming** to build (may be as complex as the final artifact)
- Used to: understand the design as a whole; show organization a close approximation of the final artifact; get user feedback on the overall design

**Examples:**
- **SoundBrowser** (Example 13) — integrated prototype right in the center of the model; role well thought-out from user observations; look and feel iterated many times; implementation redesigned for performance; shows that even near the end of project, quick pixel-painting tools were used alongside the C code for visual exploration
- **Pile metaphor** (Example 14) — brought together role, look and feel, and implementation from separate prior prototypes; shown to designers, managers, and developers as proof of concept for novel technology
- **Garment history browser** (Example 15) — two months of intensive work; highly motivating to users with real data; designers felt they invested too much time to support only a narrow role compared to what the animation (Example 8) had shown earlier; shows the cost-benefit tension of integration prototypes

---

## The 3D Space-Planning Example — Three Prototypes of One System

**Best demonstration of how the model works in practice:**

| Prototype | Type | Purpose |
|---|---|---|
| **Example 1** — interactive slide show of furniture selection | Role | Show how users might select furniture and try it in their room; convey role to design team |
| **Example 2** — Macromedia Director prototype with handle-box UI | Look & Feel | Test the direct manipulation handle-box interface with users; only worked with one chair |
| **Example 3** — working C program with 3D rendering | Implementation | Test rendering performance on a Macintosh IIfx; determine what complexity of 3D scenes was feasible |

> **Key insight**: These three prototypes were developed **almost in parallel** by different team members. No single prototype could have represented the design at that time. Answers from each informed the others:
> - Implementation constraints (how many objects could render) → informed role design (how many furniture objects to show)
> - Role constraints (only a few manipulations needed for space-planning) → simplified the implementation and UI
    > Eventually, Example 3 evolved into an integrated prototype incorporating the UI from Example 2.

---

## Audiences of Prototypes

Three distinct audiences designers discuss prototypes with (Erickson, 1995):
1. **Intended users** — evaluate options and provide feedback on evolving designs
2. **Design teams** — critique prototypes of alternate design directions
3. **Supporting organizations** (project managers, business clients, professors) — indicate progress and direction

> The required **resolution and fidelity** of a prototype depends most on its **audience**:
> - A rough role prototype may work well for the design team but NOT for the supporting organization
> - Broader audiences require higher-resolution representations
> - Some organizations have their own "**prototyping cultures**" and may only respect certain kinds of prototypes (Shrage, 1996)

---

## Practical Implications (Summary Section)

Four key takeaways from the chapter:

1. **Define "prototype" broadly** — Efficient prototypes answer the most important design questions in the least time. Even a pizza box or paper storyboard counts.

2. **Build multiple prototypes** — Interactive artifacts are too complex to capture in one prototype early on. Choosing the right focused prototypes is "an art in itself." Be prepared to throw some away and use different tools for different types.

3. **Know your audience** — Resolution and fidelity requirements depend on the audience. Engineering audiences may expect implementation prototypes; visual design environments may expect look and feel prototypes.

4. **Know your prototype; prepare your audience** — Be clear about what design questions ARE being explored and what are NOT. "Prototypes themselves do not necessarily communicate their purpose." It is the designer's job to prepare the audience.

---

## Comparison: This Model vs. Other Terminology

| Current (problematic) term | Houde & Hill alternative |
|---|---|
| "Paper prototype" | Off-line, often a Role or Look & Feel prototype |
| "High-fidelity prototype" | Could be any type; resolution depends on audience, not stage |
| "Low-fidelity prototype" | Could still be useful for all three dimensions |
| "Working prototype" | Often an Implementation or Integration prototype |

---

## Key Quotes for the Test

- "Is a brick a prototype? The answer depends on how it is used."
- "Prototypes are not self-explanatory: looks can be deceiving."
- "The degree of visual and behavioral refinement of a prototype does not necessarily correspond to the solidity of the design, or to a particular stage in the process."
- "No one tool supports iterative design work in all of the important areas of investigation." (citing Ehn & Kyng, 1991)
- "Even prototypes made of cardboard are very useful for user testing." — Ehn & Kyng (1991)
- Integration prototypes are "the most difficult and time consuming kinds of prototypes to build."
- The triangle is drawn askew to emphasize "no one dimension is inherently more important than any other."










