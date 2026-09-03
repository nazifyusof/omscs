# Animation — Lecture Notes

* Compiled from 4 lecture recordings: **(1) History of Animation**, **(2) Animation in Video Games**, **(3) Animation in Unity — Milestone 1**, **(4) Hybrid Root Motion + Programmatic Turning**
* "An" = **Animation**

---

# Lecture 1: History of Animation (Pre-Interactive → Early Interactive)

* Goal: trace animation history from earliest non-interactive forms → early interactive (pre-computer) examples → sets up transition to video games

## Earliest / Speculative Origins

* **Cave art** (archaeological speculation)
    * Animals (e.g., a boar) painted with **multiple/extra legs** in different positions, as if mid-stride
    * Theory: firelight flickering unevenly lit different leg positions → created illusion of primitive motion
* **Shadow play**
    * Human actors or **puppets** moved in front of a light source, casting shadows on a screen/backdrop
    * Often combined with puppetry
* **Puppetry**
    * At least ~4,000 years of history (possibly older)
    * Controlled via strings, sticks, or performer inside the puppet (e.g., sock puppet)
    * Mostly **3D form** animation (though shadow puppets are 2D)

## The Magic Lantern (~1600s)
* Early image projector: light source → painted/stained glass slide → lens → projected image on wall
* Later versions added **mechanical components** (levers, dials) to move layers of glass — a primitive form of animation
* Evidence: a 1659 sketch of a skeleton believed to show animation frames made for a magic lantern slide

## Automata
* Puppet concepts **without a human operator** — replaced by mechanical automation (clockwork: gears, levers, springs)
* Found in music boxes; elaborate examples exist (e.g., automaton that writes a signature)
* Famous example: recreation of a **Da Vinci mechanical lion** design
* Modern descendant: **Disney animatronics** (Hall of Presidents, Pirates of the Caribbean) — computerized, latex skin, facial features

## Toward Film: Frame-Based Devices

| Device | Year | Mechanism |
|---|---|---|
| **Phenakistoscope** | 1833 | Spinning pinwheel disc with radial slits; viewed through a slit reflected in a mirror; each spin-position briefly reveals one frame |
| **Zoetrope** | shortly after | Refinement — cylinder with slits, no mirror needed; viewer looks through slits at an angle |
| **Flip book / Kineograph** | later (exact date unclear) | Simplest form — sequential drawn/photographed pages flipped by hand |

* Phenakistoscope/zoetrope images were framed in irregular/curved shapes, limited to simple repeating motion (e.g., horse running, bird flying)

## Early Film
* **"Arrival of a Train at La Ciotat"** — one of the earliest well-known films; famous for allegedly scaring early audiences (train appeared to move toward them)
* **Film camera mechanics**: film advances rapidly, stops abruptly, shutter opens/exposes, shutter closes, film advances again — very fast start-stop cycle (source of classic camera/projector "clatter" sound)
* Minimum ~10 fps needed for the appearance of motion (revisited later re: Quake)

## Early Animated Film / Cartoons
* **Phantasmagoria (1908)** — one of the first cartoons; very primitive, frame-by-frame hand-drawn art
* **Rotoscope** — patented by **Max Fleischer, 1915**
    * Projects one frame of live-action film at a time onto frosted glass
    * Artist traces over the projected image (often silhouette/edges) on paper
    * Traced frames are then photographed in sequence like a normal cartoon
    * Fleischer Studios used this for **Koko the Clown**; later also **Betty Boop**
    * Benefit: correct human proportions/perspective; allows blending rotoscoped motion with pure artistic embellishment (impossible moves)

### Disney and Rotoscoping
* Disney used rotoscoping early on (e.g., **Snow White** — dance reference footage of actress **Marge Champion**)
* Disney transitioned away from strict rotoscoping to **"live action reference"**
    * Actors filmed for inspiration/guidance, but animators interpret artistically rather than tracing precisely
    * Allowed more expressive/exaggerated results (facial expressions, physical performance)
    * Example: **Alice in Wonderland** — actress performed "live action reference" for scenes (e.g., talking doorknob scene)
* **Comparison**: Snow White (rotoscoped) appears less expressive/flat vs. the Dwarfs (live-action-reference / freely animated) who appear more lively

## Disney's 12 Principles of Animation (book, early 1980s)
* Two singled out as **most important**:
    * **Squash and Stretch**
        * Version A (realistic bouncing ball): maintains form
        * Version B (Disney-style): ball **stretches** in direction of travel while accelerating (approximates motion blur), and **squashes** dramatically on collision
        * Applies beyond objects: facial expressions (e.g., Three Little Pigs), body movement (e.g., a person crouching/balling up before a jump, then stretching out mid-leap)
    * **Exaggeration**
* Others mentioned but not detailed: anticipation, staging, etc.

## Early Interactive Animation (Pre-Computer)
* Far fewer examples than non-interactive animation
* Two main categories: **interactive automata (mechanical games)** and **simulators**

### Interactive Automata / Penny Arcades
* Late 1800s–early 1900s, evolved over time
* Mechanical, sometimes basic analog circuits (relays)
* Examples: mechanical fighting-figure games, bowling games, baseball machines (coin → ball → hit for home run), **Rock 'Em Sock 'Em Robots** (human-powered), hockey/foosball-type toys

### Simulators
* **Link Trainer** (WWII)
    * Simulated instrument panel readings (elevation, speed, angle) via gears/simple electrical signals — **not** external visuals (no terrain/aircraft rendering)
    * Responded to user controls; tactile feedback (resistance), lights, fuel gauge
    * Used a **state machine** to coordinate behavior
    * Later also used for Air Force pilot training, airline pilots, anti-submarine pilots, submariners
* **Aetna Drivotrainer** (driver's ed simulator, used into ~early 1990s)
    * Classroom setup: students at simulated driving stations (steering wheel, gas pedal, gear shift) watching a shared film
    * **Quick-Time-Event-like mechanic**: correct response required within a time window; scored via **card punches**, tallied by a card reader → pass/fail
    * **Key feature**: in a single-projector, single-student configuration, the **student's control input could pause/advance the actual film reel** — the film would not continue until the correct input was given
    * → This is a genuine example of **on-screen animation directly controlled by user input**, prior to computers

> **Transition point:** This wraps up the pre-video-game history. Lecture 2 moves into actual video games.

---

# Lecture 2: Animation in Video Games

## Vector Graphics Era

* **Dispute over "first video game":**
    * **Tennis for Two (1958)** — built with **analog circuits** (mechanical relays); no CPU. Player controls: angle knob + fire button. Debate: does non-digital = not a "real" computer/video game?
    * **Spacewar! (1962)** — ran on a **PDP-1** with an actual CPU → generally credited as the first true video game due to general-purpose processing
        * Vector-drawn spaceships with arbitrary rotation, central black hole affecting physics, simple orbital/inertial simulation
* **Vector display mechanics** (like an oscilloscope/CRT):
    * CRT: electron beam (magnetic yoke) strikes phosphor-coated glass in a vacuum tube; phosphors glow then decay — beam must re-scan to persist an image
    * **Raster display**: scans horizontal lines top to bottom, then vertical sync/refresh
    * **Vector display**: beam has arbitrary aim (two voltages control X/Y deflection) + on/off toggle → draws **smooth arbitrary lines**, no aliasing, but can't fill/raster-scan like a normal screen

## Discrete Logic Era
* **Pong (1972)** — first major **raster** display game
    * No CPU — used **discrete logic** (individual logic gates wired together)
    * Discrete logic was cheaper than processors at the time but extremely hard to develop with
    * Severe graphics limitations: basically lines / axis-aligned filled boxes only (e.g., paddles, ball)

## Sprites
* **Taito Basketball (1974)** — first game to use **sprites**; also first to depict a human form
    * Sprite = small 2D pixel array copied ("blitted") to screen locations
    * Decouples **art** (pixel data) from **program logic** — artists could contribute independently
* **Text mode games**: earliest PCs (e.g., IBM) often only supported text
    * Used extended character sets (line segments, fill patterns) to fake graphics; swapping similar characters created crude animation
    * Example: **Castle Adventure (1984)**
* **8-bit/16-bit sprite era** (e.g., Super Mario Bros., Street Fighter II)
    * Introduced color + **animated sprites** (swap through a small set of poses per frame count)
    * Sprites used a **palette/color lookup table** per pixel (not full RGB) due to memory limits — special hardware paths for sprite rendering; limits on sprites-per-frame
    * Sprites were **always axis-aligned** — no rotation (rotation illusions were done by swapping pre-drawn angled sprites, e.g., Bionic Commando)
    * **Aesthetic association**: sprite look = 8/16-bit limitations (no rotation, palette-based color) — modern games can technically rotate/recolor sprites freely but avoid it for stylistic authenticity

### Palette Color Cycling
* A creative trick for animating **backgrounds** (waterfalls, rain, snow) without redrawing pixels
* A subset of the palette (e.g., indices 200–230) treated as a **circular buffer**; colors shift by one slot per frame (wrap around)
* Since pixels reference palette indices (not RGB directly), shifting the palette animates the on-screen colors

## Dragon's Lair & Laser Disc Games
* **Dragon's Lair** — used **LaserDisc** (analog, high-quality, non-contact/no wear, but had **digital indexing/table of contents** for fast scene jumps)
* Gameplay = **early Quick-Time Events**: correct joystick/button input → jump to correct clip; wrong input → jump to death scene
* Disc layout had to be physically optimized (clips placed near each other) for fast seeking
* Made by **Don Bluth** (traditional animator: Secret of NIMH, American Tail, Land Before Time), followed by **Space Ace**
* Sacrificed interactivity for animation quality — fell out of favor as real-time tech improved
* *(Note: Don Bluth ≠ Don Knuth — different people)*

## Rotoscoped Games
* **Karateka (1984)** — Jordan Mechner's early work; limited memory meant less-fluid animation than his later game
* **Prince of Persia** — rotoscoped from footage of Mechner's little brother running (movement) and friends (cutscenes); fight scenes rotoscoped from **Errol Flynn's *Adventures of Robin Hood***
    * Much more fluid than Karateka due to more frames of memory
    * Animation **tightly coupled to movement** (foreshadows **root motion** discussion later) — avoids foot-sliding
* **Flashback (1992)** — also rotoscoped, later ported/remade for Switch
* **The Last Express** — also Mechner, adventure game elements
* **Dragon's Lair (Amiga port)** — laser disc footage impossible to fit on floppies, so developers **vectorized** the rotoscoped frames (foreground) and overlaid on scanned original background art → fit onto 8 floppy disks
* **Another World / Out of This World** — Éric Chahi filmed himself with a home video camera and rotoscoped frame-by-frame using his own custom software (inspired by the Amiga Dragon's Lair)

## Early 3D & Vector 3D
* **Battlezone (1980)** — vector display, **wireframe 3D**; wireframe avoided occlusion/hidden-surface problems, simplifying processing

## 2D Sprite Scaling/Rotation
* **Super Nintendo Mode 7** — specialized hardware for scaling/rotating a **background** texture
    * Used for parallax, pseudo-3D effects (e.g., Mario Kart track "driving into the distance" via uneven scaling)
    * Example: Super Mario World Bowser fight — background itself rotates/scales to simulate Bowser rotating
    * Limited to backgrounds, not individual sprites (hardware constraint)
* Modern example: **Terraria mod** — shows sprite rotation is now trivial computationally, just historically infeasible on 8-bit hardware

## Raycasting & Billboards (Pseudo-3D)
* **Wolfenstein 3D, Doom** — **raycasting** for real-time indoor wall rendering
* Enemies/objects rendered as **billboards** (2D textures) — scaled for distance, but **rotation faked by swapping pre-rendered angle sprites** (front/left/right/behind, etc.)
* **Wing Commander** — same billboard approach for 3D space combat (more angles needed since no up/down constraint)
* This complexity (needing many discrete angle sprites) **motivated the move to true 3D**

## True 3D & Vertex Animation
* **Quake (id Software)** — first to pull off real-time 3D with acceptable performance
    * **Animation ran at a fixed 10 fps**, regardless of overall game frame rate — no interpolation → clunky, obvious "stepping" motion
    * **MDL format**: each keyframe stores an entire array of **updated vertex positions** for the whole triangle mesh (no skeleton — brute-force per-vertex animation)
    * Triangles reference vertex indices → indexed into the current frame's vertex table
    * **Major storage problem**: memory cost scales with vertex count × number of frames — not scalable for detailed meshes

### In-Betweening (Interpolation)
* **Quake 2** — added **linear interpolation** between two keyframes' vertex tables (weighted average based on time elapsed between frames)
    * Same storage approach as Quake 1, but interpolates for smooth motion at any frame rate
    * Non-linear/curved interpolation possible but computationally costlier
* **Alone in the Dark (1992)** — one of the first games to use interpolated keyframe animation; fixed camera, Resident-Evil-like

## Procedural Animation
* Writing an **algorithm** to animate an object directly (no keyframes/authoring tool needed)
* Best for simple/cyclic motion: clocks, machinery, hovercraft bobbing (sinusoidal motion), etc.
* Example: Uncharted 4 clock tower gears (likely procedural)

## Physically-Based Animation
* Animation driven by **physics simulation** integration
* Example: **Just Cause 3** (grappling hook + exploding propane tanks, rockets attached to objects)

## Motion Capture (Mocap)
* Maps real performances to game objects/characters — evolution of rotoscoping but with **full 3D data**
* Example: Naughty Dog (Uncharted, The Last of Us) — full body + facial capture
* **4D Boxing** — early mocap-like example (possibly done via multi-angle rotoscoping); fluid animation and good control for its time
* **Teddy** (~1999–2000) — sketch-based 3D modeling tool; drew shapes on screen, software inferred symmetric 3D volume — noted as a potential concept for future ML-assisted animation tools

## Skeletal Animation
* Solves the **storage problem** of per-vertex (MDL-style) animation
* **Skeleton** = abstract "wireframe" hierarchy (tree structure) used to **deform** an arbitrarily complex mesh
* **Root bone** = typically the **hip**; has 3 DOF (rotation) or 6 DOF (rotation + translation, needed for **root motion**)
* Other bones have 1–3 DOF depending on joint type
* Storage per keyframe = compact array of floats (much smaller than full vertex tables)
* **Mesh binding**: each mesh vertex has a **weighted list of bones** (commonly max 2–4 bones per vertex) determining how much each bone's transform affects that vertex — critical near joints (e.g., elbow) for proper deformation
* **Rigging** = process of aligning the skeleton within the mesh + painting bone weights (typically done from a **T-pose**)
    * Iterative process: pose-test extreme movements, fix problem areas (e.g., stiff armor stretching like rubber) with weight painting tools

### Skeletal Animation — Pros/Cons
* **Pros:** major memory savings vs. per-vertex animation; works well with **blending**, **IK**; animations are **portable/reusable** across compatible skeletons; simpler authoring
* **Cons:** implementation complexity, computational overhead (though vertex deformation can run on GPU); potential **self-intersection** problems at joints (e.g., elbow) without extra correction

### Squash & Stretch on Skeletons
* Achieved by adding extra DOF: **scaling** on bones, extra bones for deformable parts (e.g., tail)
* Example discussed: **Jak and Daxter** run/jump animation — torso compression/extension while running, dramatic stretch at jump apex, compression at landing

### Early Skeletal Animation in Games
* **Half-Life (1998)** — early effective use; enabled complex creatures (e.g., tentacle monster) and in-game cutscenes that would be impossible with per-vertex storage

## Root Motion
* Embeds **translation** (not just rotation) in the root bone's animation data
* All child bones follow via **forward kinematics** (hierarchical transform propagation)
* Solves the **foot-sliding problem**: real human movement isn't constant-speed (accelerates while falling forward, decelerates on foot-plant) — very hard to fake programmatically; root motion captures this naturally from mocap
* **Unity specifics**: the "root" is not literally the hip bone — it's the **hip bone projected onto the Y=0 plane**, computed each frame, so it aligns better with a capsule collider's base
* **Benefits beyond footfall accuracy:**
    * Physics interaction: engine can **restrict** root motion translation if blocked by a collider (e.g., can't fully punch through a wall)
    * **Authoring power**: animators control movement without programmer intervention (declarative)
* **Selective root motion**: can restrict root motion to certain axes only (e.g., XZ only, not Y) — Y left to physics/gravity so characters can fall off ledges properly; rotation root motion can also be toggled off (e.g., to avoid chase-camera shake)

## Animation Blending
* Instead of authoring/mocapping **every possible movement variation**, blend between a small set of animations
* **Blend tree** (Unity term; aka blend map) — maps input parameters (e.g., joystick X/Y) to weighted combination of animations
* Works with **root motion** too (blends translation + rotation, not just pose)
* Enables continuous, declarative movement definition — minimal/no code required
* **Bunny hop problem**: blending dissimilar animations (mismatched footfall count/order) causes both legs to move together / hopping artifacts
    * Fix: ensure blended animations share the same number of foot-falls, same loop starting point/order (clip **length** can differ; blending uses normalized timeline)
* **Animation masks / layers**: allow blending only part of the skeleton (e.g., upper body rifle-firing blended over independent leg locomotion) to avoid needing every leg-state × arm-state combination mocapped

## Match Targets (Unity term)
* Real-time correction utility: linearly interpolates ("LERPs") a bone's position to align with a **world-space target** by a specific point in the animation timeline
* Example use: character jumping to grab a ledge — corrects hand position over time so animation lines up despite imprecise player input/positioning
* If correction distance is too large, looks unnatural (visible "gliding"); works best for small corrections

## Kinematics
* **Forward Kinematics (FK)**: parent transform propagates down to children (standard scene graph / matrix stack multiplication) — most common default in games
* **Inverse Kinematics (IK)**: solve backward from a desired **end position** (e.g., hand touching a button) to determine necessary parent joint rotations
    * **Non-trivial & often ambiguous** — many valid joint configurations can satisfy the same end position (e.g., elbow can bend multiple ways)
    * Some third-party IK solvers show visible **wobbling** between valid solutions; better frameworks minimize this using solution history
    * **Unity's built-in IK** (Humanoid rig): limited to hands, feet (position + rotation goals) and a **head "look at"** target; each goal has a **weight** (0 = pure animation, 1 = full IK override) — allows blending IK correction smoothly into an existing animation
    * Also useful for **animation authoring** (grab-and-drag posing tools)
* **Real-game examples:**
    * **Uncharted 4** — feet IK-adapted to sloped rooftop terrain, head-turn cues toward objectives, match targets + IK combined for hand-to-ledge precision
    * **Terra Nova** — one of the first games with real-time IK; torso hovers via capsule collider, feet corrected with IK for varied terrain
    * **Trespasser** (Jurassic Park, dev: Seamus Blackley) — box colliders for dinosaur torsos slide along ground; per-foot raycast detects ground contact and overrides animation (bends joints more if ground hit early, extends leg if not touching expected ground) — imperfect but effective

## Animation Retargeting
* Reusing a **humanoid skeleton's animation** on a different rigged model
* Requires more than rescaling limb lengths — needs **joint limits**, handled in Unity via **"muscle space"** (part of the **Avatar** system) — normalizes joint movement so it maps across different skeletons
* Works ~80–90% of the time; can still get **self-intersection** issues (e.g., Street Fighter IV's Rufus — tight-to-body arm swing animation may clip through his body on a different skeleton) — may require manual correction tools

## Rotations & Interpolation
* **Euler angles (XYZ rotation)** are intuitive but suffer from **gimbal lock** — certain configurations lock out some rotational freedom (e.g., looking straight up in an FPS can "lock" left/right turning)
* **Quaternions** avoid gimbal lock and support reliable **linear interpolation** between rotation poses — this is why game engines (e.g., Unity) primarily use quaternions internally (convertible to/from Euler angles for display, but not for interpolation)

---

# Lecture 3: Animation in Unity — Milestone 1 (Project Walkthrough)

## Project Setup
* Git-based Unity milestone project; must open the correct **scene** under Project → Scenes (opening incorrectly creates a blank default scene)
* **4 default characters**: 2 humans (skeletal, rigged mesh) + 2 "minions" (built from Unity primitive shapes)
* Each character type has **2 versions**:
    * **Programmatic movement** version (no root motion)
    * **Root motion** version
* Press **T** to switch between characters at runtime

## Programmatic (Non-Root-Motion) Movement — Observations
* Visible **foot sliding** ("skating on ice") — worse at certain speeds; a throttle (keys 1–9, 0) simulates joystick deflection amounts
* Turning quality is also poor with programmatic control
* For the **minion** (no visible feet), programmatic movement actually looks **fine** — foot-sliding issue is irrelevant without visible feet

## Root Motion Movement — Observations
* Feet appear firmly planted at all speeds — much more convincing
* Root motion is **projected root bone position** onto the Y-plane (as discussed in Lecture 2)
* Minions can also use root motion (baked into their animations) for translation & turning — assignment includes **adding a missing hop animation**

## Required Editor Windows
* **Window → Animation** and **Window → Animator** — both usually need to be manually opened and docked

## Key Scripts (Assets → Scripts → Character Control)
* `CharacterInputController` — common input polling (forward, turn, action)
    * Reads **raw** input values (author prefers filtering outside Unity's Input Manager for portability across projects)
    * **Circular vs. square joystick deflection**: circular controllers normalize diagonal input to a unit vector; square/uncircularized input can give **diagonal movement a higher effective speed** (this is the classic **"speedrunner zig-zag" exploit**) — good practice: map input to circular
    * Includes **half-speed turn** controls for testing (Q/E) alongside WASD
    * Includes a **throttle** (speed cap) and simple **input smoothing/filtering**
    * **Script execution order matters**: input-polling script must run **before** any script that consumes its values, or you introduce **1 frame of input latency** — configured under Project Settings → Script Execution Order
* `CharacterCommon` — shared helpers, e.g. **jump reliability**: raycast downward from capsule collider base to detect "close enough to ground" (handles rolling terrain where character is technically airborne by a small margin) — common in most platformers
* `BasicControlScript` (non-root-motion humanoid)
    * `animator.applyRootMotion` explicitly set to **false/default** at Start (since the same Animator Controller can be shared between root-motion and non-root-motion setups)
    * Movement: `transform.forward * inputForward * Time.deltaTime * maxSpeed`, applied via **`rigidbody.MovePosition`** (never set `transform.position` directly when a Rigidbody is attached — Unity recommends Rigidbody-based movement for stable physics)
    * Rotation applied similarly via `Quaternion.AngleAxis` + **`rigidbody.MoveRotation`**
    * Sends animator parameters: `VelX` (turn axis), `VelY` (forward axis), plus a bool for falling (currently unused, could trigger a falling animation)

## Animator / Blend Trees (Non-Root-Motion Character)
* **Idle Turn** state = **1D blend tree** — single parameter (VelX): −1 = 100% left turn, +1 = 100% right turn, 0 = idle
* **Transitions**: e.g., idle→forward triggers when `VelY > 0.05` (a **dead zone** to allow turning in place without accidentally triggering forward locomotion)
    * Transition settings: **fixed duration**, no **exit time** = immediate crossfade begin (chosen here for responsiveness); exit time would instead wait for a specific point in the current animation before transitioning
* **Forward blend tree** = **2D blend tree** — parameters VelX & VelY define a 2D map; animations (idle, walk-forward, walk-forward-turn-left/right, turn-left/right-90) are placed at coordinates in this space; a draggable marker (simulating joystick deflection) shows live blending
* **Parameters** (Float / Int / Bool / Trigger) created manually in the Animator's Parameters tab
    * **Triggers are discouraged** — they can queue up and cause a backlog of unintended activations; prefer Bools

## Root-Motion Character — Blend Tree Notes
* Very similar Animator setup, but the visualized **red disc** on the ground shows Unity's projected root position moving as blending occurs — confirms both **pose and root translation** are blending together
* **Trick — double-entry of walk animation at two speeds**: same walk clip placed twice in the blend tree — once near idle (speed multiplier ~1.0) and once further out (speed multiplier ~1.4)
    * Purpose: shrinks the "dead zone" near idle where blending idle (no leg movement) with walking causes visible foot-dragging; adds a small "creeping" walk close to idle, then scales walking speed further out — smoother feel overall
* **Bunny Hop demo**: two similar-looking run animations with **mismatched footfall order** blended together produce a visibly broken "hopscotch"-like movement — confirms the Lecture 2 concept in practice
* Importing new animations: must set **Animation Type = Humanoid**, assign/create an **Avatar**; **Bake Into Pose** checkboxes control which axes get root motion baked in on import

## Exaggerating / Tuning Mocap Animations (assignment technique)
* Two script parameters added to `RootMotionControlScript`:
    * **`animationSpeed`** — sets `animator.speed` every frame (1.0 = normal); >1 speeds up playback overall
    * **`rootMovementSpeed`** (a scaling/extrapolation factor) — applied via `Vector3.LerpUnclamped(oldRootPosition, newRootPosition, rootMovementSpeed)`
        * At 1.0 = no change from default
        * >1.0 = **extrapolates** beyond the raw root motion delta → exaggerates stride length (scales proportionally with the animation's natural speed variation, so it still "looks right," unlike simply adding a flat constant translation)
* Combining a modest **animationSpeed boost (~1.1)** with a modest **rootMovementSpeed boost** produces a convincing "elite athlete" feel from average mocap, without redoing motion capture

## Minion Animation Authoring (Animation window direct keyframing)
* Minion (no-root-motion) uses a simple **1D blend tree**
* Animations were **hand-keyframed directly in the Animation window** (not mocap) — demonstrates manual keyframing workflow:
    * **Add Property** to select which fields to animate (position, rotation, or any public/serializable field, incl. colors)
    * **Dope sheet** view shows keyframe timing (diamonds)
    * Animate a **child object** (e.g., "Minion Model") separately from the parent game object — **critical**: keep physics collider/rigidbody on the *unanimated* parent, only animate the visual child, so collision detection isn't broken by bouncing colliders
    * **Animation Events**: add a marker at a specific time (the small pencil/plus icon) that calls a **public method** on any attached script (e.g., `ExecuteFootstep()` to play footstep audio)
* **Root-motion minion**: keyframes exist on both the **child model** (visual hop/rotation) *and* the **root game object** (position/rotation = actual root motion)
    * Unity does **not preview world-space root translation/rotation** in the Scene view for root-level keyframes (must preview via the Animation asset directly with a model reference dragged in)
    * **Curve editor / tangents**: precise curve shaping (Free, Smooth, Flat, Broken tangent modes) allows fine control of root translation/rotation using only a couple of keyframes — useful for root-motion turning on non-humanoid or custom-rigged characters
    * Alternative for non-humanoid characters: keep animation to forward-only root motion, and apply **rotation programmatically** (e.g., `rigidbody.MoveRotation`) instead of authoring root-motion turning

## Match Targets + IK — Button-Press Example (assignment feature)
* Goal: character approaches a button, corrects position/orientation, and presses it precisely regardless of imprecise player positioning
* **Two entry paths** in the Animator:
    * If close enough & correctly facing the button spot → transition directly to **Button Press** state
    * If not close enough → transition to **"Match to Button Press"** state first (a corrective single walking step), then transition (with an **exit time of 0.75**, i.e., 75% through) into the Button Press animation
* **Match Targets code** (in `OnAnimatorMove`-adjacent update logic):
    * Checks: is Animator in the "match button press" state, not mid-transition, not already matching?
    * If a valid button-standing-spot target exists: call **`animator.MatchTarget`** with
        * target position/rotation = the button-standing-spot transform
        * a mask restricting correction to **rotation + X/Z position only** (not Y — leave Y to gravity/physics collision)
        * start time = current normalized animation time; end time = `0.75` (matches the transition's exit time)
    * Result: by 75% through the corrective step animation, character's root is aligned to the target spot
* **IK for the button press hand position** (`OnAnimatorIK` callback):
    * Must be explicitly enabled per Animator layer: **Layer settings (gear icon) → "IK Pass"** — without this, no IK code executes even if written
    * Naive version: IK weight forced to **1** whenever Button Press animation is playing → causes the hand to **"teleport"/snap** into position rather than moving smoothly
    * **Fix**: use an **imported animation curve** (custom curve authored on the button-press clip's import settings, e.g., named `"buttonClose"`) read via `animator.GetFloat("buttonClose")` each frame, and use that as the **IK weight** instead of a constant 1
        * Curve shaped to ramp IK weight up as the animated hand nears the button (in the original generic animation), hold high while at the button, then ramp back down — smooth, natural hand correction to varying button heights
* This chain — **match targets (body) + curve-weighted IK (hand)** — lets one generic button-press mocap clip work correctly for buttons at many different world positions/heights.

---

# Lecture 4: Hybrid Root Motion Translation + Programmatic Turning

## Motivation
* **Pure root motion turning** (relying on mocap turn animations) can look **sluggish/disorienting** — mocap turning often requires the character to **lean into the turn**, adding a "rubbery"/delayed feel, especially noticeable at a run
* Goal: combine
    * **Root motion translation** (for natural, non-sliding footfalls / forward movement)
    * **Programmatic (code-driven) rotation** (for **snappy, responsive turning**, independent of any turn animation)

## Setup Steps
1. **Add a "run" motion field** to the forward blend tree (in addition to existing walk speeds) to create a fuller idle→walk→jog→run feel across the joystick's forward deflection range
2. In the **root motion control script**, **stop passing the turn parameter** to the Animator (comment it out) — this disables root-motion-driven turning in the animation state machine
3. Also **disable the `MoveRotation` call** tied to root motion rotation in `OnAnimatorMove`

## Implementing Programmatic Turning
* Add a **public `turnRate` field** (default ~100, meaning ~100°/sec)
* In **`Update()`** (not `FixedUpdate`) — because the **legacy Input Manager only reads new input values during the Update cycle**, not FixedUpdate
* Build the turn rotation:
  ```
  Quaternion rot = Quaternion.AngleAxis(turnRate * inputTurn * Time.deltaTime, Vector3.up);
  rigidbody.rotation = rot * rigidbody.rotation; // apply additively
  ```
    * `Quaternion.AngleAxis` builds a rotation around the Y-axis (`Vector3.up`)
    * Must be applied **additively/multiplicatively** to the current pose (quaternion multiplication), not replacing it outright
    * `rigidbody.rotation` used (equivalent effect to `MoveRotation` here) so the rotation is applied to the **current physics pose**

## Fixing "Slowdown While Turning"
* Symptom: character visibly **slows down** while turning
* Cause: **circular joystick coordinate mapping** setting in the Input Map — turning "eats into" the forward magnitude when clamped to a unit circle
* Fix: **turn off circular mapping** in the Input settings → turning becomes independent of forward speed, much more responsive

## `Time.deltaTime` vs `Time.fixedDeltaTime` — Animate Physics Trick
* Animator **Update Mode = "Animate Physics"** means `OnAnimatorMove` runs during the **FixedUpdate** cycle (even though it's not literally named `FixedUpdate`)
* **Key Unity behavior**: inside the fixed-update cycle, calling `Time.deltaTime` **automatically returns `Time.fixedDeltaTime`**
* **Debug technique**: `Debug.Assert(Time.fixedDeltaTime == Time.deltaTime)` inside `OnAnimatorMove`
    * If Update Mode = **Animate Physics** → assertion **passes** (no console error) — confirms you're truly running in the physics/fixed cycle
    * If switched to **Normal** update mode → assertion **fails** — confirms you're in the regular Update cycle instead
* **Why use "Animate Physics"?** Needed when interacting with objects that are part of the physics simulation (e.g., pushing something) — avoids jittery, unsynchronized-looking interactions between animation and physics

## Why "Animate Physics" Makes the `Time.deltaTime` Multiply Technically Redundant
* Since `turnRate * Time.deltaTime` under Animate Physics is really `turnRate * Time.fixedDeltaTime` — a **constant** every frame
* Could simplify to just using `turnRate` directly (no multiply) **if** the fixed timestep never changes
* Keeping the multiply is still good practice: if the physics **simulation step size** (fixed delta time) is ever changed in Project Settings, the turn rate would automatically stay correct without further code changes

## Advanced Idea (mentioned, not implemented in the demo)
* You might want **root motion turning** for some animations (e.g., an **idle turn-in-place** animation) but **programmatic turning** for others (e.g., fast running)
* Possible approach: **dynamically toggle root motion rotation on/off** based on which animation state is currently playing (inspect current Animator state at runtime) — described as a more advanced technique left for further exploration