# Game Engines (GE) — Lecture Notes

* Foundation topic for all future technology lectures (physics, audio simulation, interactive animation, etc.)

---

## 1. What Is a Basic Game Engine? *(GE1)*

* Earliest games (e.g., **Spacewar** on the PDP-1) were low-level, highly optimized programs — none of the "modern" features found in Unity/Unreal existed yet.
* Early engines were just a tight **event-based, frame-based loop**:
    1. Pull user input
    2. Update a simple simulation
    3. Render to an output device
    4. Repeat

> **Computational kernel** — the term used to describe this core loop running an interactive simulation.

* As software engineering matured, engines split into two parts:
    * **Runtime engine (computational kernel)** → stays the same
    * **Data** → can be swapped out (e.g., level data)
* Example: Super Mario Bros. levels stored as arrays of integer references to sprites/tiles — same engine, different data per level.

### The Frame-Based Event Loop
* **Process input → Update simulation state → Render to display**
* User perceives output → makes new decisions/inputs → loop repeats
* **Frame** = a single simulated point in time, rendered to the screen
* This is called a **frame-based simulation / frame-based event loop**

---

## 2. Human Perception & the Event Loop *(GE2)*

* Everything about engine timing/design is driven by **human perception limits**.

### Reaction Times
| Stimulus type | Reaction time |
|---|---|
| Visual stimulus | ~**0.2 s** |
| Self-stimulus (e.g., turning head then reacting) | ~0.2 s |
| Auditory stimulus | ~**0.16 s** (faster — why races use a starter *pistol*, not a flag) |

### Sensory Illusions — Goal: trick the senses into believing a virtual world is real
* **Vision** is the primary focus (most relied-upon human sense).
* Other simulated senses (in decreasing commercial importance): **hearing**, **touch** (force feedback), **smell/taste** (rare — mostly amusement parks).
* Phenomena engines try to fool the user into experiencing:
    * Object representation (persistent objects)
    * Relationships (e.g., spatial constraints — object on top of another)
    * Cause and effect
    * Real-world physics
    * **Immersion** — the feeling of "being there"; a continuum, not all-or-nothing

### Requirements for Perceiving Animation
1. Consecutive images must be **similar enough** to one another
2. Images must be presented **quickly enough**

> **Key threshold:** ~**10 frames per second (fps)** is the bare minimum for the brain to perceive motion instead of a slideshow.

* Historical/typical frame rates:
    * Film: **24 fps**
    * Classic games: **30 fps**
    * Modern games: **60 fps**+ (even higher for VR)

---

## 3. Simulation Concepts, Realism & "Only Simulate What You Need" *(GE3)*

* Game engine advancement = pursuit of **realism** (doesn't have to be "real world," just internally consistent/expected).
* Strategy: build models for different real-world phenomena (animation, light reflection/rendering, audio, **physics** — rigid body collision, friction, etc.) and **weld them together** ("stitched" isolated simulations) rather than one unified emergent low-level simulation (e.g., simulating atoms).

> Video games model the world at a much **higher level of abstraction** than reality (not down to atoms/quarks).

### Twilight Zone Tie-In — *"A Matter of Minutes"*
* Episode depicts a simulation rebuilt in **time slices** (= frames), by "automaton" workers.
* Key idea reflected in the show: **you only build what the observer needs** — don't waste resources building unseen things.
* Side effects shown in the episode (and real games) of only-build-what's-needed:
    * **Glitching** out of the game world
    * Objects **popping in/out** of existence

### Only Simulating What Is Needed
* Each frame is built from **one fixed reference moment in time** → keeps all subsystems (visuals, audio, physics) **synchronized**.
* Techniques to minimize computation:
    * **Surface-based rendering** (don't model object interiors)
    * **Frustum culling** / **occlusion culling** (only render what's in view)
    * **Dynamic level of detail (LOD)** — swap in lower-poly models

### Philosophical Aside
> "If a tree falls in a forest and no one is there to hear it..." — in games, if it's not observed, it's often **not even computed**.

* Examples:
    * *Zelda: Breath of the Wild* — cut down tree, walk away, come back later → tree has respawned.
    * *GTA* — follow an NPC off-screen too long → they're **permanently removed** from the simulation.

### Side Effects of "Bare Minimum" Simulation (real bugs)
* Objects **pop in/out** because computer couldn't finish loading/rendering in time (e.g., a **GTA** issue: vehicles/trains appearing suddenly when driving fast).
* Assets that "wait" to activate (e.g., **Far Cry** waterfall that turns on only once you look at it a certain way).
* Falling through floors / clipping through walls (sometimes exploited intentionally for **speedrunning**).

### Revisiting Frame Rate
* Below **30 fps** → game "feels" slow/broken to most people.
* Most people can notice improvements **up to ~60 fps** for passively observed (synthesized) animation.
* Two different scenarios of frame-rate sensitivity:
    1. **Passive observation** (e.g., watching a video) → mainly notice animation quality, ceiling ~60 fps.
    2. **Interactive animation** (playing a game) → also notice **input latency**; benefits can extend to **~120 Hz**.
* VR commonly targets higher frame rates because of **input latency → simulator/motion sickness**.
* General commercial target: **60 fps** (higher for VR).

---

## 4. Frame Rate Demo Website *(GE4)*

* Demo site: `framesperseconds.appspot.com` (link in course lecture notes PDF).
* Site lets you compare two balls at different fps/speed/motion-blur settings.

### Key Observations
* **Motion blur** can make a lower frame rate (e.g., 25–30 fps) look nearly as good as 60 fps, *especially at low speed*.
* Without motion blur, the frame-rate difference becomes obvious, especially at higher speeds.
* Why motion blur helps: real-world vision **aggregates light continuously over time** (like a camera shutter), whereas a rendered frame captures a **single instant**.
    * Film cameras: shutter open → collects light → 24 fps with natural blur.
    * Games (no motion blur): must use **much higher fps** to compensate for the lack of blur, especially for fast motion.
* Early 3D games (~15 fps) relied on **slow-moving objects**; faster engines (Wolfenstein, Doom) enabled fast-paced 3D gameplay.

> This demo only covers **passive** animation — doesn't test **input latency**, which needs a separate interactive test.

---

## 5. Why Frame-Based Simulation? *(GE5)*

### Reasons We Use Frames
1. **Intuitive** — easy to conceptualize a loop that produces one image after another; easy to build upon.
2. **Built on prior technology/entrenchment**:
    * Celluloid film animation (Disney-style, frame by frame)
    * Digital signal processing / sampling theory
    * Raster displays (pixel-based)
3. **Compatible with human perception** — good enough to "fool" the user (see GE2 thresholds).

### Audio Is *Not* Truly Frame-Based
* Audio plays **continuously**, but audio-*generating* **events** (e.g., a physics collision) are tied to the frame loop.
* Implementation: a small **buffer** is topped off frame-to-frame with new audio data so playback stays continuous as long as the frame rate is sufficient.

### The Canonical Render Pipeline (GPU)
* GPU = dedicated graphics processor; generates a view from a **virtual camera** perspective.
* Rendering is **highly parallelized** for high throughput.
* Per frame: identify **timestamp** + **pose** (camera position + object positions in 3D) → render that snapshot in parallel.

### The Z-Buffer (Depth Buffer)
* Problem solved: with **parallel rendering**, which surface should appear "in front" for a given pixel?
* Each pixel stores **RGB + depth (Z) value**.
* Rule (must be **atomic**, i.e., check + write happen together):
  > "If the new Z value is **closer** than the stored one, write the new RGB + depth. Otherwise, discard."
* This simple atomic check-and-write is what allows massively parallel rendering to resolve visibility correctly.

---

## 6. Could We Avoid Frame-Based Simulation? *(GE6)*

*A thought experiment to better understand **why** we use frames.*

### Alternative 1: Frameless / Best-Effort Ray Tracing
* Instead of locking rendering to a fixed frame rate, **ray tracing** can update pixels on a "best effort" basis.
* Demo styles referenced (SIGGRAPH video):
    * **Traditional frameless** — only a fraction (e.g., ¼) of pixels updated per frame → mix of new/old pixels (visual "speckling"/artifacts when the camera moves).
    * **Reduced pixel count** — lowers resolution so ray-cast rate matches 60 Hz.
    * **Adaptive frameless** — hybrid of approaches for better image quality.
* Trade-off: without locking to frames, movement causes **visual artifacts** unless update rate is extremely high.

### Alternative 2: Move Away From Surface-Based Rendering (Particle Simulation)
* Instead of polygon-mesh surfaces, represent the world with **particles** (closer to atoms).
* Case study: **"Jelly in the Sky"** — a 2D, GPU-based, particle-simulation tank battle game.
    * Every pixel ≈ a particle; particles bond to form solids **unless too hot** (from weapon energy) → melt into liquid, then cool/re-solidify.
    * Numerical/floating-point accuracy issues made **strong, rigid bonds** difficult → objects end up "jelly-like" (embraced as the game's aesthetic/name).
    * Models **object interiors**, not just surfaces — a major departure from standard rendering.
    * Scaling to **3D** would explode data/compute requirements.

> **Conclusion:** Breaking from frame-based simulation isn't impossible, just a **major step back in fidelity** given current computational demands — requires either simpler games or far more powerful hardware.

---

## 7. Time Synchronization & the Main Loop *(GE7)*

### Interactive vs. Non-Interactive Simulation
* Non-interactive (e.g., a **Pixar movie**): frame computation time doesn't matter — some frames can take hours.
* Interactive (video games): simulation time **must stay locked** to real-world time progression — the user has expectations about how fast things should move.

### The Loop (Expanded)
**Process Input → Update State → Render → Sleep/Synchronize → (repeat)**
* All of this must complete within the **target frame period**.

### Grace Hopper's Nanosecond Talk (Reference)
* Famous demonstration: a nanosecond ≈ the length of wire electricity can travel in that time (~11.8 inches); illustrates why computation/communication time really matters.

### Time Budgets
* Target of **60 Hz** → each frame has **16.67 ms** (≈16,666 µs) to complete everything.
* Because of this hard time budget, game development relies heavily on **optimization/efficient algorithms**.

### Why 2D Was Easier Than 3D for Consistent Frame Rate
* **2D (e.g., NES)**: fixed max number of sprites/tiles → **roughly constant computational load** every frame → easy to hit target fps consistently.
* **3D**: scene complexity varies drastically depending on view direction → **frame rate is harder to guarantee**.

### Display Technology & Legacy ("Entrenchment")
* Early **display list / vector graphics** ("Etch-a-Sketch" style) — used by *Spacewar*.
* **Raster display** (CRT) — scans horizontal lines to form pixels; became the dominant approach.
* CRTs use **phosphors** that glow briefly then fade → must be constantly refreshed on a fixed **display schedule**.

### Screen Tearing
* Occurs when the **frame buffer** is updated *while* the display is mid-read from it → part of the screen shows the old frame, part shows the new (visible as a "shearing" effect, e.g., misaligned trees in an FPS).
* Still relevant on **LCDs** because they inherited the CRT-era update-schedule convention.

### V-Sync & Buffering
* **Vertical sync (V-Sync)**: software waits to update the frame buffer until it's safe (matches the display's refresh schedule) → **eliminates tearing**.
* **Double/triple buffering**: render to a secondary buffer, then "flip" (swap reference) to it when safe.
* **Downside of V-Sync**: if you miss the deadline even slightly, you must wait a **full extra frame period** (e.g., entire 1/60 s) → why competitive/professional gamers often **disable V-Sync**.
* **Adaptive V-Sync** (modern NVIDIA/AMD tech): not locked to the old CRT-style fixed schedule — LCDs can update more flexibly, avoiding the "miss = lose a whole frame" penalty while still avoiding tearing.

### Latency
* Frame-based simulation inherently introduces **input latency** — user input is only reflected once rendered/displayed.
* Extra sources of latency: wireless controllers (e.g., Bluetooth transmission + error checking), and rendering based on "old" data as a frame is processed.
* Classic computer-architecture speedup techniques can *hurt* interactivity:
    * **Pipelining** — improves throughput but increases per-item latency (assembly-line analogy).
    * **Cache coalescing** — batches data, adds latency.
* Latency importance depends on **game genre**:
    * **VR**: extremely latency-sensitive (>0.2s → simulator/motion sickness).
    * **First-person shooters / "game feel" games**: latency clearly noticeable.
    * **Turn-based games** (chess, checkers): latency barely matters; can tolerate <10 fps.

### Techniques to Reduce Latency
* Increase frame rate (when possible)
* **Adaptive V-Sync**
* Avoid aggressive pipelining/cache-coalescing where interactivity matters
* **Input prediction**, e.g., the **Kalman filter** (a form of "dead reckoning") — used in VR head tracking
* **Relaxed frustum culling**: do a rough first-pass render prediction early, then a final precise pass using the latest input right before rendering — shrinks the time between input and display.
* Classic hardware speedups: direct memory access, wider memory buses, higher clock speed.

### Why "Sleep" Matters in the Loop
* You want to **finish early** and sleep rather than max out compute, because:
    * Leaves **headroom** for more demanding scenes (e.g., many enemies on screen) to still hit target fps.
    * More **consistent** frame timing = better perceived latency/quality.
    * Saves **power** (important for mobile devices, e.g., Nintendo Switch on battery).

---

## 8. Unity Demo: Frame Rate & Synchronization *(GE8)*

* Demo project: "Roll a Ball" with **3 rotating pills** (blue, red, purple) attached to the ball, each using a different rotation-update strategy.

### Three Rotation Modes (`MyRotate` script)
| Mode | Pill Color | Logic | Behavior when fps drops |
|---|---|---|---|
| **Dumb Mode** | Blue | Rotate a **constant number of degrees** every `Update()` call, regardless of elapsed time | **Slows down** — e.g., at 20 fps (1/3 of 60), rotates only 1/3 as much per real second |
| **Variable Delta Time Mode** | Red | Rotate by `degreesPerSecond × Time.deltaTime` (scales rotation to actual elapsed time) | **Stays correct** — compensates automatically for frame-rate variation |
| **Fixed Update Mode** | Purple | Same constant-degree rotation as Dumb Mode, but runs inside `FixedUpdate()`, a separate update cycle that can run **0, 1, or multiple times** per frame to "catch up" | **Stays correct** — catches up via repeated calls |

* Demonstrated live: turning the camera to a **high-complexity direction** (millions of particles + dense terrain) tanks fps from 60 → ~20.
    * **Blue (dumb) pill visibly falls behind** the other two.
    * Red and purple stay aligned with each other.

> **Takeaway:** `Update()` is called once per frame; `FixedUpdate()` runs on its own schedule, potentially multiple times per frame, to keep time-based logic consistent under variable frame rates.

---

## 9. Implementing Time Synchronization *(GE9)*

### Constant Translation/Rotation — 3 Implementation Options
1. **Dumb Mode**: `new position = old position + constant translation`
    * Assumes the target frame rate is always hit exactly.
    * ✅ Advantage: **low overhead** (no extra computation)
    * ❌ Disadvantage: **oblivious to real-world time** → speeds up/slows down when fps varies; inconsistent across different hardware/scene complexity; works well mainly in **2D** (constant load).
2. **Time-Dependent (Variable Delta Time) Mode**: `new position = old position + velocity × Δt`
    * ✅ Advantage: **normalizes gameplay** across varying scene complexity/hardware.
    * ❌ Disadvantages: extra multiply per object (small overhead, scales with many objects); at **very high fps**, Δt can get so tiny that **floating-point rounding errors** occur (worse for acceleration, which involves *t²*).
3. **Fixed Update Mode**: hybrid — constant translation, but on a separately managed schedule.
    * ✅ Advantage: objects can be **oblivious** to time-sync issues (assume a constant elapsed time between fixed updates); simplifies time-based math; avoids floating-point rounding errors of tiny Δt; needed for **stable physics** (small/controlled increments).
    * ❌ Disadvantages: **runaway computation risk** (frame rate drops → more fixed updates needed → even lower frame rate, potentially spiraling); only suited to a **subset** of game logic; can't easily be tied to responding to user input (since multiple fixed updates can occur before the user ever sees a new frame).

### Common Misconception
> `FixedUpdate()` is **not** run on a separate real-world-clock thread. The engine's main loop is (generally) **single-threaded**; the *Fixed Update Manager* decides how many times to call fixed-update logic **within** the normal frame loop.

### Fixed Update Manager — Pseudocode Logic
1. Compute `total delta time` = `deltaTime since last frame + remaining leftover DT from before`
2. `numFixedUpdates = floor(total delta time / fixed update period)`
3. Run the fixed-update callback that many times
4. Compute and store the **leftover remainder** time for the next frame's bookkeeping
* If fixed-update rate is **higher** than current frame rate → multiple fixed updates run per frame (catch-up).
* If fixed-update rate is **lower** than frame rate → some frames get **zero** fixed updates.

### Advantages of Fixed Update
* Simplifies time-based computation (avoids small-Δt floating point issues)
* Keeps sensitive simulations (esp. **physics**) **stable** with controlled increments
* Can **save power** by running less often than the visual frame rate (interpolate visuals in between)

### Disadvantages / Gotchas of Fixed Update
* **Runaway computational load** — dropping frame rate → more catch-up fixed updates → even lower frame rate (needs a contingency plan, e.g., cap max fixed updates per frame).
* Cannot be used for everything — **rendering** must stay tied to normal `Update()`.
* User **input response** should be handled in normal `Update()`, not `FixedUpdate()` (since multiple fixed updates can run before the next visible frame — no chance for the user to see/react in between).
* Coordinating logic split between `Update()` and `FixedUpdate()` can be tricky (state assumptions can conflict).
* **Jitter**: if fixed-update rate < frame rate, some frames show **no movement** → jerky/staggered motion.
    * Fix: **interpolate/extrapolate** object transforms between fixed updates during normal `Update()` calls (e.g., fixed update at 30, frame rate at 60 → extrapolate motion for the "in-between" frames).

### What Needs Time-Dependency? (assume *everything* does)
* **Velocity/acceleration**-based movement
* **Animation** systems (picking/interpolating frames based on elapsed time)
* **Physics** (usually via fixed update for stability)
* **AI decisions** — frequency of decision-making shouldn't depend on frame rate
* **Probabilistic behavior** (e.g., dice rolls) — must be normalized to time, or higher fps → events triggering more often than intended

---

## 10. The Modern Game Engine *(GE10)*

> Modern engines = **computational kernel (runtime)** + **software framework for creation, development, and deployment** (e.g., Unity, Unreal).

### Historical / Influential Predecessors
* **Sketchpad** (Ivan Sutherland, Lincoln Lab, 1961–63, on the TX-2 computer)
    * Used a **light pen**; could draw lines/circles, apply **constraints** (e.g., horizontal/vertical), and move a point while keeping attached lines connected.
    * Very influential on 3D modeling software, level editors, and CAD-like tools.
* **HyperCard** (Apple Macintosh)
    * One of the first **WYSIWYG live-preview** editors — no compile/link step needed to test.
    * Supported 2D art, event/click callbacks, animation, audio → could build full interactive multimedia experiences and games (e.g., **The Manhole**, a point-and-click adventure).
    * Included a **high-level scripting language**.
* Both were foundational influences on modern engines' **live editing** and **integrated tools** philosophy.

### Early Internal / Genre-Specific Tools
* **Text adventures**: no graphics hardware available → tools like the **Z-machine** (Infocom) provided a **portable virtual machine** so one interpreter could run many games across different computers.
* **Point-and-click adventures**: e.g., LucasArts' **SCUMM engine** (originally for *Monkey Island*, reused for many later games).
* Benefit of these tools: separated **programming** work from **creative/writing** work (different skill sets).
* **id Software** (Wolfenstein, Doom, Quake) was hugely influential:
    * Engines were expensive to license (e.g., ~$1,000,000 for Quake).
    * Fan communities **reverse-engineered** tools (unofficial Doom/Quake level editors), which shaped later mainstream engine tooling.

### Defining Features of Modern Game Engines
* **Declarative creation** — designers configure/define constraints rather than writing lots of procedural code.
* **Extendability** — can add custom procedural code/scripts/menu items/widgets when declarative tools aren't enough.
* **Platform abstraction** — same data/assets deploy across PC, consoles, Mac, etc.
* **Integrated development environment (IDE)** with **live/WYSIWYG editing** (legacy of Sketchpad & HyperCard).
* **Asset management / content pipeline** for organizing media.
* **Standalone** — most work can be done in one tool (occasionally still need external tools like Blender, Photoshop, audio editors).
* **Genre flexibility** — not limited to one type of game.

### Core Subsystems of a Modern Game Engine
* **Computational kernel** (the live simulation loop)
* **Input management** — needs low latency + platform abstraction (multiple controller types)
* **Rendering engine** — GPU-accelerated pipeline, scene graph (spatial relationship management), space/volume partitioning, linear math libraries
* **Physics engine** — essentially a **constraint solver**; runs a "simultaneous simulated world" kept in sync with graphics/audio (own dedicated future lecture)
* **AI** — path planning, behavior planning/implementation, time-scale management
* **Networking** — event synchronization, data prioritization (can't send everything), and **prediction** for responsive multiplayer
* **Event-based architecture** — lets game objects respond to events without needing direct knowledge of the emitter (**loose coupling**) — dedicated future lecture

---

## 11. Summary: What Is a Game Engine? *(GE11)*

> A **game engine** is a **closed-loop sensory simulation** designed to convince a player that a virtual world exists and can be interacted with in real time.

* It runs as a **rapid sequence of frames**, each a "frozen moment in time," presented fast enough that the discreteness is imperceptible (an effective illusion trick on human perception).
* Extended (modern) definition also includes:
    * A **constraint solver**, declaratively defined by the game designer
    * **Extendable** via event-based callbacks/handlers (from constraint solvers, user input, or connected subsystems)
    * A set of **interactive authoring tools** supporting creation, development, and deployment of the game

> So a modern game engine is **not just the runtime** — it's the runtime **plus** the full authoring/tooling ecosystem that supports building the game.