# HCI Quiz Notes: Distributed Cognition & Information Visualization
**Reading:** Liu, Nersessian & Stasko — *Distributed Cognition as a Theoretical Framework for Information Visualization*

---

## 1. Core Definition of InfoVis

- **Information Visualization (InfoVis):** "The use of computer-supported, interactive, visual representations of abstract data to **amplify cognition**" — Card, Mackinlay & Shneiderman
- Two key dimensions: **Representation** and **Interaction**
- Problem: InfoVis lacks an underlying theory or systematic framework for guiding design

---

## 2. What is Distributed Cognition (DCog)?

- **Distributed Cognition (DCog):** A theoretical framework originating from Edwin Hutchins (UCSD, mid-1980s) that proposes cognition is **not just inside the brain** — it is distributed across individuals, artifacts, and the environment
- **Key claim:** Cognition is an **emergent property of interaction** between humans and their environment, not a property of the isolated mind
- Unit of analysis shifts from **individual human → cognitive system** (humans + artifacts together)

### DCog vs. Traditional Cognitive Science

| Traditional Cognitive Science | Distributed Cognition (DCog) |
|-------------------------------|-------------------------------|
| Cognition = information processing *inside* the brain | Cognition = emergent property of *interaction* with environment |
| Individual human as unit of analysis | Cognitive system (humans + artifacts) as unit of analysis |
| Environment is just input/stimulus | Environment actively shapes cognition |
| Reductionist approach | Environmental/situated perspective |
| "Amplifies cognition" metaphor | Critiques "amplification" — tools transform tasks, not amplify minds |

---

## 3. Key Terms & Definitions

### Representation

- **Internal Representations:** Mental structures inside the brain — frames, schemata, mental models, propositions, mental images
- **External Representations:** Observable representations outside the mind — text on screen, graphs, written notes, visual displays
- **Distributed Representations:** Representations spread across both internal and external media; different distributions produce different cognitive strategies
- **Problem Isomorphs:** Different representations of the *same* problem that share the same problem space but vary in how rules are externalized (e.g., Tower of Hanoi: Orange, Donut, Coffee versions)
    - More externalization = **shorter task time + fewer errors**

### Interaction & Coordination

- **Pragmatic Actions:** Actions whose primary function is to advance the agent toward the physical goal (moving closer to an end state)
- **Epistemic Actions:** Actions taken *not* to advance toward a goal directly, but to change the environment in ways that reduce cognitive effort — e.g., rotating a Tetris piece extra times to make placement easier
    - **Key insight:** Epistemic actions link internal and external representations through coordination
- **Coordination:** The mechanism by which a cognitive system propagates and transforms representations across media; it is an **emergent property**, not a pre-existing rule
- **Cognitive Coupling:** The tight connection between internal and external representations during interaction

### Cognition & Environment

- **Reductionist Approach:** Traditional method of isolating individual minds to study cognition, stripping away environmental context
- **Environmental Perspectives:** Approaches (including DCog) emphasizing that cognition is embodied, enculturated, situated, and distributed
- **Over-attribution Problem:** Mistakenly ascribing to individual minds properties that actually belong to the whole human+artifact system
- **Cognitive Ethnography:** DCog's primary research method — field study of cognitive tasks in real-world settings, including in situ fieldwork, interviews, observations, and video-taping

---

## 4. Representation in InfoVis (DCog Lens)

- All problem solving = changing representations to make solutions transparent (Herbert Simon)
- DCog expands this to include **external** representations, not just internal ones
- **Zhang & Norman's Tower of Hanoi experiments** showed:
    - Externalizing rules → faster completion, fewer errors
    - External representations do more than act as memory aids — they evoke different **situated cognitive strategies**
    - Perceptual processing of external info is more efficient than processing purely internal representations (citing Gibson's ecological approach)

### In Practice (Jigsaw scenario)
The analyst + developer + Jigsaw system + monitors + notepad + mouse = **one cognitive system** performing information foraging. Representations propagated across media:
1. Written note ("butterfly") → verbal instruction → search field text → graph nodes → entity graph → document display → written note ("Osaka smuggler")

---

## 5. Interaction in InfoVis (DCog Lens)

- Interaction is **not one-way** (human → system); external and internal representations reciprocally interact
- A cognitive system accomplishes tasks by **propagating representation states** across representational media through coordination
- InfoVis interaction should be studied for **what users achieve**, not just the techniques provided

### Key Research Questions (Science of Interaction)
- What are the nature and mechanisms of **coordination and cognitive coupling**?
- How do people develop **interaction strategies** during sensemaking?
- How does interaction with visual structures enable turning information into **meaningful understanding**?

---

## 6. Visualization at the Social Level

- DCog argues analysis tasks are **inherently social and embodied in context**, even when done by one person
- The standard **one-person-one-computer InfoVis model is over-simplified**
- **Many Eyes** project (Viegas et al.) is an example of expanding the cognitive system to include multiple users via the WWW
- Social visualization raises questions about **coordinative mechanisms** between people mediated by artifacts

---

## 7. DCog as a Framework (Not a Theory)

- **Framework vs. Theory (Tweney's distinction):**
    - **Theory:** Emphasizes hypothesis formation and testability
    - **Framework:** Reconstructs a model of the world, reduces complexity, anchors to data, and **generates new hypotheses**
- DCog is still developing — it cannot yet fully explain coordination, cognitive coupling, or externalization
- **5 roles of theories in design disciplines (Bederson & Shneiderman):**
    1. **Descriptive** — identify key concepts
    2. **Explanatory** — explain relationships and processes
    3. **Predictive** — predict performance
    4. **Prescriptive** — provide design guidelines
    5. **Generative** — facilitate creativity and future research
- DCog's primary value for InfoVis: **descriptive and explanatory power** for representation and interaction

---

## 8. Implications for InfoVis Research

### Evaluation
- Traditional HCI evaluation: measure usability/utility → find design problems
- Greenberg & Buxton: good usability often happens *after* usefulness, not before → focus on **usefulness**, not just usability
- Problem with pure lab experiments: treats human cognition as a "black box," ignores distribution of internal/external representations
- DCog critique: control variables are hard to pin down because cognition is situated and emergent

### Proposed Approach
- **Make cognition an explicit research agenda** for InfoVis
- Use **cognitive ethnography** (field observation, interviews, video) as primary method
- Controlled experiments still valid — but guided by cognitive ethnography first
- Evaluation goal: understand the nature of **cognitive processes** in human+InfoVis systems, not just validate designs

### Theory Building
- Most InfoVis theory = taxonomies (bottom-up approach)
- DCog adds a **top-down framework** to make bottom-up efforts more directed
- The interplay between **internal and external representations** must be addressed

### Design Warnings
- InfoVis systems might inadvertently **eliminate important epistemic actions** not supported by the system
- May create artificial barriers between digital interfaces and analog media
- Need to support **user customization and appropriation**

---

## 9. Important Quotes to Know

- *"Tools permit us to transform difficult tasks into ones that can be done by pattern matching..."* — Hutchins (on why "amplifying cognition" is misleading)
- *"The study of distributed cognition is very substantially the study of the variety and subtlety of coordination"* — Kirsh
- *"Without interaction, an InfoVis technique or system becomes a static image"* — Yi et al.
- *"The purpose of visualization is insight, not pictures"* — Card et al.

---

## 10. Key People & Works

| Name | Contribution |
|------|-------------|
| **Edwin Hutchins** | Founded DCog; field study on ship navigation; *Cognition in the Wild* |
| **Kirsh & Maglio** | Epistemic vs. pragmatic actions; Tetris study |
| **Zhang & Norman** | Distributed representations; Tower of Hanoi isomorphs |
| **Card, Mackinlay & Shneiderman** | Definition of InfoVis; "amplify cognition" |
| **Shneiderman** | "Overview first, zoom and filter, then details-on-demand" mantra |
| **Gibson** | Ecological approach to visual perception — info can be picked up directly without internal representations |
| **Greenberg & Buxton** | Critique of usability evaluation |

---

## 11. The Jigsaw Scenario (Know This!)

- Context: VAST 2007 contest; analyst + developer working with Jigsaw visual analytics system on a fabricated dataset (~400 news stories)
- Goal: identify threats to endangered species
- **Why it matters for DCog:**
    - Shows cognition distributed across analyst, developer, Jigsaw, monitors, notepad
    - Developer wasn't just an operator — contributed analytical ideas (suggested looking at transaction amounts)
    - Analyst referenced external experts ("I'd call a financial expert") → shows cognition is inherently social
    - Propagation of representations: notepad → search field → graph view → document view → notepad (insight: "Osaka smuggler")

---

*End of Notes*