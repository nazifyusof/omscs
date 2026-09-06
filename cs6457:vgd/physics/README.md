# Physics Engines — Fundamentals

* Overview of what a physics engine is, common games that pioneered real-time physics, and the core building blocks (bodies, forces, connectors, collision detection) used across engines like Havok, ODE, and PhysX.

![img.png](img.png)

## What Is a Physics Engine

A physics engine provides simulation calculations for a virtual environment.

- **Two flavors**:
    - High-precision offline engines:
        - Used for scientific prediction (e.g. designing structures, automobiles)
    - Real-time physics simulation:
        - Used mainly in video games, but also other interactive simulations
        - Can even be used for near-term prediction (e.g. robotics)
- This lecture focuses on **real-time simulation challenges**, not offline high-precision calculation

> Offline and real-time engines share a lot of algorithm/approach overlap, but are optimized for different goals.

## Influential Physics Games

A brief history of games that pushed real-time physics forward.

- **Bridge Builder** (early 2000s):
    - Gameplay: lay out beams (lines) to form a bridge, goal is getting a train across
    - Popular modern successor: **Poly Bridge**
- **Trials** (originally a grad school project, made in a custom Java engine):
    - Motorcycle game — control driver's weight, throttle, brakes to avoid falling
    - Later became an Xbox 360 game ("Trials," "Trials Fusion," etc.)
- **Trespasser**:
    - One of the earliest games with a very powerful physics engine
- **Half-Life 2**:
    - Used the **Havok** physics engine
- Nearly every modern game has an elaborate physics simulation under the hood

### Popular Real-Time Physics Engines

- **Havok** — commercial engine, used in Half-Life 2
- **ODE (Open Dynamics Engine)** — open source
- **PhysX (Nvidia)**:
    - Integrated into Unity
    - History: started as a university spin-off in Europe → became **Novodex** → bought by **Ageia** (built a dedicated physics accelerator card, similar to a graphics card) → **Ageia bought by Nvidia**
    - Motivation: physics acceleration calculations were similar to GPU parallelization capabilities

## Core Components of a Physics Engine

The main building blocks shared across most physics engines.

- **Bodies**:
    - Usually rigid bodies
    - Common shapes: box/rectangular prism, sphere, capsule (cylinder with half-sphere caps), cylinder, triangle mesh (convex or concave)
- **Connectors**:
    - Ways of attaching bodies together
- **Forces**:
    - How bodies are acted upon / moved within the simulation
- **Constraints**:
    - Sometimes the same concept as connectors depending on the engine
- **Collision detection**:
    - Can be used standalone (just detecting collisions) without full dynamics

## Rigid Body Types & Behaviors

Not all rigid bodies behave the same — key distinctions for performance and gameplay.

- **Dynamic objects**:
    - Affected by gravity, can collide and bounce
- **Static objects**:
    - Infinite mass, fixed in place (e.g. ground, walls)
    - Improves efficiency — fewer constraints need to be solved
- **Kinematic objects**:
    - Programmatically controlled ("puppet" by the programmer)
    - Can still push dynamic objects out of the way
- **Enabling/disabling objects**:
    - Only enable objects that need to be part of the simulation to reduce engine load
- **Sleep / Awake**:
    - Objects that settle can be put to **sleep** to save resources
    - A collision callback can wake a sleeping object back up
- **Layers / Groups**:
    - Like separate "physics universes" superimposed on one another
    - Example: multiplayer shooter — projectiles shouldn't collide with the firing player, and bullet-vs-bullet collisions may be skipped entirely for performance
    - In Unity, called **Physics Layers**

## Body Physical Properties

Properties beyond position/orientation that matter for realistic simulation.

- Position, orientation, linear velocity, angular velocity
- **Mass**:
    - Determines which object gets pushed more in a collision
- **Friction**:
    - Affects sliding behavior (e.g. ice-like vs. high-friction toppling/rolling)
- **Restitution (bounciness)**:
    - Determines how bouncy vs. how "dead" (like lead) an object is on impact
- **Directional/anisotropic friction**:
    - Useful for special cases
- Special-case properties may exist for certain body types (e.g. terrain)

## Collision Detection & Shape Complexity

Why simple shapes are preferred and how complex shapes get approximated.

- Determining collision cost depends heavily on **shape complexity** (polygon count)
- Primitive shapes (sphere, capsule, cylinder) have simple/fast interpenetration formulas
- **The graphics mesh is not what actually collides** — often a simplified collider stands in for the visible mesh (e.g. a capsule for a humanoid character)
- Physics and graphics are synchronized frame to frame; physics engine controls position, graphics "along for the ride"

### Simplifying Complex Shapes

- **Axis-Aligned Bounding Box (AABB)**:
    - Min/max of all vertices along x/y/z
- **Arbitrary (Oriented) Bounding Box (OBB)**:
    - Box can be rotated to find the smallest bounding box
- **Convex Hull**:
    - Smallest convex shape that contains the object (e.g. wraps an asteroid shape)
- **Compound Colliders**:
    - Multiple convex primitive shapes joined together under one parent rigid body (Unity hides implementation details — parent has rigid body, children have colliders)
- **Collision Hierarchies**:
    - Test against a large root bounding box first, then progressively smaller boxes, only testing detailed mesh when truly close (e.g. flight simulator — most planes never collide, so cheap root tests save resources most of the time)

## Collision Geometry: The "Skin" Concept

A key trick used across physics engines to stabilize collision detection.

- **Skin / Contact Offset / Rest Offset**:
    - A slight dilation (expansion) of the true geometry
    - Helps avoid jitteriness from touching/not-touching state flips
- **Layering/filtering** (again) is also considered part of collision geometry efficiency — shown in Unity's collision matrix

## The Tunneling Problem

What happens when discrete collision detection misses fast-moving objects.

- **Discrete collision detection**: only checks geometry intersection at each frame snapshot
- **Tunneling**: a fast-moving object can pass through a thin ("skinny") wall between frames without ever registering an intersection
- Real example: a student's pinball project had a thin "glass" collider that balls tunneled straight through

### Solutions to Tunneling

- **Limit object/wall size**:
    - Enforce minimum wall thickness, minimum object size
- **Ray casting**:
    - Cast a short ray from previous position to current position
    - Limitation: a ray from the center can miss the "shoulders" of an object (edges/corners)
    - More rays (perimeter ray casts) improve accuracy but cost more performance
- **Silhouette extrusion**:
    - Consolidate multiple rays into a single swept shape (e.g. sphere becomes a cylinder along the direction of travel)
    - Hard to generalize beyond simple shapes like spheres
- **Speculative collision detection**:
    - Skin width becomes **dynamic** — grows/shrinks based on object speed and size
    - Problem: under hard acceleration the skin may not grow fast enough, so tunneling can still occur
- **Dynamic sub-stepping**:
    - When objects are近 (close) and might collide, the simulation temporarily runs at a higher rate (e.g. 100Hz → 200Hz) for just that interaction, then returns to normal rate
    - Considered one of the best/most reliable solutions, at the cost of overhead

> Rotating objects at high speed can force a lot of unnecessary dynamic sub-stepping, which is one reason engines cap **maximum angular velocity**.

## Rotating Objects & Angular Velocity

Special issues with fast rotation.

- Rotation between frames is hard to test accurately ("in-between frame" poses)
- Unity/physics engines set a **max angular velocity** cap to avoid these problems
- Anecdote: a student's multiplayer racing game had cars capped at ~10 mph in effect because the default **max angular velocity on wheels** was too low — raising that cap (since wheels are cylindrical and always occupy the same shape in space regardless of spin) solved the issue

## Collision Dynamics (Resolution)

Once a collision is detected, how do you actually respond to it?

### Penalty Force Method

- One of the earliest approaches, used in **Trespasser**
- Concept: find the point of **deepest penetration**, apply a corrective force/vector there
- **Problem — oscillation**:
    - Pushing on one corner causes a "see-saw" around the center of mass, driving the opposite corner into penetration, causing back-and-forth oscillation
    - Compounded by floating point rounding errors
    - Objects often never settle to a stable resting state (great for destructive gameplay, bad for stacking/building/puzzle games)

### Improved Method — Skin-Based, All-Contacts Approach

- Relax the contact constraint: allow interpenetration within a **skin** (rather than the true geometry)
- Consider **all contact points**, not just the deepest one
- Corrective force is **proportional to the degree of interpenetration** in the skin — this removes jitter and allows for smoother stacking/friction behavior
- More overhead: extra bookkeeping and more math (proportional scaling) than the simple penalty method
- If interpenetration reaches the true (non-skin) geometry, a **maximum corrective force** is applied as a last resort — this is what causes objects to go flying (e.g. the Sea of Thieves ship launching into the sky after a kinematic → physics control handoff in shallow water)

### Sequential Impulse Method

- Real-time engines generally can't solve all contacts simultaneously in one exact mathematical step
- Instead, contacts are solved **one at a time in sequence**, iterating a few times to refine the result
- Uses a **Linear Complementary Problem (LCP)** approach at a high level
- Opposing gradients (e.g. an object stuck in a corner) require multiple iterations to reach an acceptable solution

## Forces

Ways to move rigid bodies.

- **Constant forces**:
    - E.g. gravity (can be disabled per-layer, e.g. for ghosts), or continuous thrust/homing missile forces
- **Impulse**:
    - Instant change in velocity applied over a single frame (good for jumping)
- Forces are generally applied at the **center of mass** by default, with a direction and magnitude
- **Force vs. Velocity application**:
    - Force-based application accounts for mass (heavier object = less velocity change for same force)
    - Directly setting **velocity** ignores mass — useful when you want a consistent jump height/behavior even if object mass changes later
- **Torque**:
    - Used for rotational forces
    - Unity (at the time of this lecture) lacked a built-in helper to apply force at an arbitrary point (not center of mass) to derive the correct linear + rotational force combination

## Connectors (Joints)

How rigid bodies attach to one another.

- Implemented using multi-body dynamics with **Jacobian constraints** (similar math to contacts, but distinct)
- Considerations:
    - Can connected sides collide with each other?
    - How much flexibility/freedom is allowed across the joint (to avoid getting numerically "stuck")?
    - Restitution in the joint?
    - Degrees of freedom?
- **Types**: hinge, ball-and-socket, sliding (shower-curtain style), pulley-like connectors
- **Springy joints**: simulate Hooke's law, can add damping (e.g. a door closing smoothly)
- **Joint motors**: torque curves for things like a controllable car engine
- **Breakable joints**: physics engine can detect excess force through a joint and destroy it, separating the objects
- **Soft vs. hard constraints**:
    - Hard constraints never allow violation — but may have no valid solution (object gets "stuck")
    - Soft constraints allow some flexibility — often necessary for playability in real-time simulation

> Example: a wrestling game bug showed soft joint constraints stretching a character's leg/knee mesh in a comical way — an unintended interaction between rigid body ragdoll shapes and skeletal animation.

## Object Activation & Sleep Thresholds

Managing performance by minimizing active calculations.

- Mark static objects clearly
- Let low-energy objects **go to sleep**
- **Sleep/bounce thresholds** control how much movement is "small enough" to count as settled
    - Needs to be tuned: low enough that players don't notice objects stopping early, but not so low that objects rarely sleep
- Example: Half-Life 2's gravity gun kept only ~3 rigid bodies **active** at any given time despite feeling very dynamic, largely due to careful sleep threshold tuning
- Skin-width-related settings also affect how easily sleeping objects wake back up (e.g. from being touched)

## Ragdoll Physics

How rigid-body ragdolls integrate with animated characters.

- Rigid body shapes (simple primitives) approximate the human form and are connected via joints
- These physics bodies are **not rendered directly** — instead their positions drive a **skeletal pose**, which feeds the skeletal mesh rendering
- **Workflow**:
    1. Character normally controlled by animation system (kinematic control)
    2. On impact/trigger: turn off animation control, **disable kinematic control** on the rigid bodies
    3. Physics now drives the rigid bodies (ragdoll falls under gravity/collision/forces)
    4. Rigid body positions drive the skeleton pose in real time
- **Trespasser** was the first game credited with pulling this off ("rag-doll" physics driving mesh deformation via skeletal rigging)
- Handoff between animation control and physics control is complex and error-prone (see Sea of Thieves and wrestling game examples above)

## Physics + Animation Blending (Advanced Topic)

Why pure physics simulation of characters is extremely hard.

- Fully physically-simulated humanoid characters are inherently unstable (a robotics/AI-level challenge) — comparable to Boston Dynamics-style humanoid instability
- Some games (e.g. a boxing/sumo wrestling game) use physics to apply small corrections to animations, resulting in intentionally comical instability
- More advanced approach: **blend animation + physics** (similar to skeletal animation + IK blending), used by third-party Unity plugins to:
    - Slow a kick animation realistically when it contacts an object
    - Let a character lean dynamically under force (e.g. mouse drag)
    - Seamlessly transition between ragdoll and animated control (e.g. recovering from a sniper shot)
- This is beyond the scope of the class, but useful to be aware of

## Common Physics Integration Pitfalls

A checklist of what to watch for when building your own physics integration.

- Apply forces properly — don't just teleport objects around
- Mark static surfaces so objects don't sink or float
- Use realistic **mass, volume, and units** relative to your coordinate system
- Set the physics timestep appropriately — physics usually runs at a higher/fixed rate than graphics for stability
- Choose the right collision detection setting (discrete vs. continuous/higher quality)
- Keep physics and graphics **synchronized** every frame if rolling your own integration
- Have a clear strategy for **deactivating objects** (sleep vs. manual)
- Use **layers** effectively
- Watch for **scale mismatches** between graphics and physics
- Watch for performance slowdowns from an overloaded physics system
- Be aware of realistic density/friction ranges from physics documentation
- Watch for "whip" effects — chains of connected objects can whip an end object to unrealistic speeds

# Unity Physics — Implementation & Demos

* Live walkthrough of Unity physics features (rigid bodies, colliders, joints, layers, materials, ragdolls) demonstrated through a Bridge Builder clone and a "physics playground" project.
  ![img.png](img.png)

## Bridge Builder Demo

A constructive (non-destructive) physics game example shown before diving into Unity specifics.

- Renamed clone of the classic freeware game (original name conflicted with a business-contact-management app called "Bridge Builder")
- **Gameplay**:
    - Left-click and drag to place bridge beams
    - Objective: get a train across a gap within **budget and weight constraints**
    - Real-time **stress visualization** shows structural strain as the bridge is tested
    - Goals can include: surviving the train crossing, making the bridge more robust (no red stress), or making it cheaper
    - Difficulty increases: bigger gaps, tighter budgets, changing weight requirements
- Demonstrates that physics-driven games don't have to be about destruction — they can have a **constructive element**
## Physics Playground Overview

Introduction to the instructor's demo project used to showcase Unity physics features.

- Contains: various robots, compound objects, rigid bodies of different types, joints, physics layers, scripted objects
- Demonstrated behaviors:
    - Some spheres pass through each other (red vs. red), others collide (red vs. blue) — controlled by physics layers
    - A capsule constrained to stay upright vs. one that isn't
    - Crates with collision-triggered sounds
    - Elevators lifting objects up and down
    - Compound objects (e.g. chairs)
## Rigid Bodies & Colliders Basics

The two essential components for any object to participate in physics.

- Every object needs:
    - A **Collider** (added automatically to Unity primitives)
    - A **Rigid Body** (must be added manually via *Add Component*)
- Default rigid body settings: mass = 1 kg, upright, uses gravity
- Can freeze constraints (e.g. keep a capsule locked upright)
- **Kinematic toggle**: switch an object between programmatic control and physics-driven control
- **Static objects**:
    - Mark non-moving environment geometry (e.g. arena/level geometry) as **static** — improves physics performance
    - A purely static collider (no rigid body needed) can be used for objects that should never move
## Audio & Collision Events

How collision-triggered sound works in the demo project.

- Core requirement: implement **OnCollisionEnter**
    - A collision can have **multiple contact points**
    - Simple approach: just play a sound on any collision enter
    - More advanced approach (used in this codebase): loop through contacts, pick the largest **impulse**, and break out of the loop once a "hard enough" hit is found (to avoid redundant sounds)
- **Event-based audio system**:
    - Collision scripts send an **event** (e.g. `AudioManager.BoxAudioEvent`) rather than playing audio directly
    - An **Audio Event Manager** listens for events and centralizes playback (an "audio engine")
    - Benefit: other systems (e.g. particle/spark effects) could also listen to the same event
    - More complex events can attenuate audio level based on impact force and add pitch variation for realism
- **Simplified alternative**: just call something like `PlayClipAtPoint` for basic, 2D-only (stereo panning, no 3D) sound
> Minimum requirement to add sound-on-collision to any object: implement `OnCollisionEnter` and send/play a sound from the contact info (position is usually good enough — you rarely need to dig deeper into the collision data).

## Physics Layers & Collision Matrix

Controlling which objects can collide with each other.

- Demonstrated with **red** and **blue** spheres
- Layers are set per-object in the Inspector; custom layers can be added
- Layers serve multiple purposes in Unity (rendering order, physics, etc.)
- **Project Settings → Physics → Layer Collision Matrix**:
    - Shows intersections between every pair of layers (including self-intersections, e.g. red-vs-red)
    - Unchecking a box disables collisions between those layers/objects
    - Demo: disabled red-vs-red collisions but kept red-vs-blue and blue-vs-blue enabled
## Physics Project Settings

Global settings found under **Project Settings → Physics**.

- **Gravity**: a global vector (default: -9.8 m/s² in the Y direction)
- **Sleep/bounce thresholds**: settings related to objects going to sleep or no longer bouncing
- **Solver iterations**: a cap on the number of iterations the solver runs
- **Contact offset**: related to the collision "skin" concept
- **Fixed Timestep**: found under **Project Settings → Time** — dictates how often the physics engine (and other fixed elements) updates
## Joints

Different joint types demonstrated with a hanging chain.

- **Fixed Joint**: pins an object in place (used for the top of the chain)
- **Configurable Joint**:
    - Has X/Y/Z **motion** and **angular motion**, each of which can be **locked** or **free**
    - Requires a **connected body** (the object it's attached to)
    - Locking translational motion means the object must maintain the same distance from its connected body, but can still be free to rotate
- Both objects in a joint need a **collider** and a **rigid body**
- An anchor point can be non-rigid (e.g. attached to something static/never-moving) if the chain just needs to swing from a fixed point
- Playing the chain in motion shows it swinging as expected once properly configured
## Animating Objects (Elevator Example)

Building a simple kinematic animation without needing physics for the moving part itself.

- **Setup**:
    1. Create an empty parent GameObject
    2. Add the visible geometry (e.g. a cube) as a child — animating in **local coordinates** relative to the parent avoids issues when cloning/moving the whole assembly later
    3. Add a **Rigid Body** + **Animator** to the object that needs to move
- **Creating the animation**:
    - Use the Animation window/tab to create a new animation clip
    - Add a keyframe for **position** at the start, a keyframe partway (e.g. moved up 5 meters), and one back at the end
    - Adjust playback speed on the Animator if the motion is too fast (e.g. slow to a quarter speed)
- Placing a rigid-body object (with gravity) on top of the animated elevator shows it being pushed up and down realistically
## Wobbly Object & Center of Mass Demo

Building a "weeble wobble"-style toy and adjusting its balance point.

- Basic setup: capsule collider, rigid body, increased mass (e.g. 10 kg)
- **Custom center of mass**:
    - Can be set via a script/marker object rather than relying on Unity's automatic calculation
    - Moving the center of mass lower makes the object more stable (harder to tip over)
- **Scaling pitfall**:
    - Scaling an object that has a rigid body directly attached can break physics behavior (a known general problem, sometimes worsened by Unity engine changes over time)
    - **Fix**: keep the object with the rigid body **unscaled**, and put the (scaled) visual/collider geometry on a **child object** instead
## Physics Materials (Friction & Bounciness)

How to control sliding and bouncing behavior per-object.

- Friction/bounciness settings live on the **Collider**, not the rigid body — because compound objects can have different colliders each with different materials
- **Creating a Physics Material**: right-click → Create → Physics Material (commonly organized in a "Physics Materials" folder)
- Key settings: **Dynamic friction**, **Static friction**, **Bounciness**
- **Combine modes** (how two touching materials' values are merged):
    - **Average** (default): averages the two materials' friction — means you can't make something perfectly slippery if it touches a high-friction default surface
    - **Minimum**: uses the smaller of the two friction values — needed to make a truly "slippery" material work as intended
    - **Maximum**: used for bounce combine, e.g. so a bouncy ball (bounciness ~0.9) stays bouncy against less-bouncy surfaces
- Demo: a "slippy" red box slides freely down a ramp; a default-material blue box has high friction and doesn't slide; a yellow sphere with high bounciness combine-maximum bounces repeatedly, losing energy each bounce until it crosses the sleep/bounce threshold and stops
## Ragdoll Creation (Ragdoll Wizard)

Turning a skinned/rigged character into a physics ragdoll.

- **Process**: GameObject → 3D Object → Ragdoll (Wizard)
- Requires assigning each skeleton bone slot (hips, upper leg, lower leg, foot for each side, spine(s), shoulders, arms, forearms, head)
- **Common pitfall**: incorrectly setting the **spine** bones can cause issues/crashes — refer to the assignment write-up for correct mapping
- After creation, colliders (e.g. capsule colliders per limb) may need manual tuning — example: forearm colliders defaulting to an oversized "Popeye forearm" radius that needs shrinking
- Result: a hierarchy of rigid bodies + **character joints** (a specialized joint type) holding the skeleton together
- Turning off the **Animator** lets the ragdoll physics take over and the character collapses/crumples realistically
## Object Deactivation Techniques

Different ways to stop or disable physics objects, demonstrated with a ball on a joint above a ramp.

- **Delete Joint**: destroys a joint via script (e.g. useful for a "boulder chases the player, then gets released" effect)
- **Sleep**:
    - Call `.Sleep()` to force an object to sleep, `.IsSleeping()` to check status, `.WakeUp()` to wake it
    - Sleeping objects wake automatically if touched by something else
    - Useful for a "pile of stuff" that shouldn't move until disturbed
- **Kinematic toggling**:
    - Setting an object to **kinematic** = programmatic control; if nothing moves it programmatically, it's effectively stopped
    - Kinematic objects can have collisions **enabled or disabled** independently — choose based on whether you want it to act like a static collider or be completely ignorable
## Force Application (Impulse vs. Force Mode)

Demonstrating different ways to apply force to a rigid body.

- **Impulse mode**: an instantaneous, one-time push (like a jump) — good for quick, discrete pushes
- **Force mode**: a continuous force applied every frame while active (described as feeling "like a rocket," constantly accelerating while on)
- Toggling between modes on the same object shows very different behavior for the same magnitude value
## Collision Detection Modes & Tunneling Demo

A live demonstration of the tunneling problem and its fix.

- Demo setup: a small, fast-moving collider (a ball) dropped from height
- With **Discrete** collision detection mode: the fast ball can pass straight through geometry (tunneling) — in the demo it flew through a mask/obstacle and got stuck under an elevator instead of landing where expected
- Switching **Collision Detection Mode** to **Continuous** (using something like a ray cast from frame to frame) fixed the issue — the ball now stops correctly instead of tunneling through
- This confirms the benefit of continuous collision detection for small, fast-moving objects
## Interactive Ragdoll Get-Up System

A more advanced demo: a character that can be knocked into a ragdoll state and then get back up automatically.

- **Trigger**: a script event (from a future assignment) turns off the Animator and lets the Ragdoll take over — character "wipes out"
- **The challenge**: getting the character back up again convincingly
- **Approach demonstrated**:
    1. Maintain several possible "get up" animations (e.g. get up from back, from stomach — 4 variations shown)
    2. Use a **pose distance score**: compare the first frame of each get-up animation to the character's current ragdoll pose
    3. Pick the animation with the **lowest (minimizing) score** — the best match to the current pose
    4. Before playing the chosen animation, perform **angular interpolation** on the joints — smoothly moving from the current ragdoll pose to match the animation's starting pose over a short time
    5. Once the pose is corrected, **turn the Animator back on** and let it play the selected get-up animation
- Result: character gets up smoothly from whatever position it landed in, using the best-matching animation
- Instructor notes this "main" (non-fully-automated) approach could be automated further by cycling through all get-up animations, calculating the pose-distance metric for each, and auto-selecting the best one
## Wrap-Up Notes

- This video (Milestone 2 prep) covers rigid bodies, joints, layers, materials, forces, sleep, and ragdolls
- **Not covered here** (left for the next milestone): **Triggers** — rely on the same physics collision detection but use `OnTriggerEnter`-style callbacks instead of `OnCollisionEnter`