# AutoCam Free

Release notes for the **AutoCam Free** line.

{% hint style="info" %}
**Note:**

* This documentation contains information on **v2.0.0** onwards.
* For the recommended workflow, see [**Source**](../../learn/features/source.md) → [**Path**](../../learn/features/path.md) → [**Rig**](../../learn/features/rig.md) → [**Output**](../../learn/features/output.md).
* Everything here is also in **AutoCam Pro**, which shares this core.
{% endhint %}

***

### 2.1.1 \[Latest Release] <mark style="color:$info;">— 2026-08-03</mark>

#### Changed

* **The add-on is now called "AutoCam Free" in Blender's add-on list,** matching\
  how the Pro edition already read. Nothing else changes: it is the same\
  extension, it updates in place over an earlier install, and the sidebar tab\
  is still "AutoCam".
* **The two aim objects are now named after what they do.** The object you drag\
  to point the camera is called **Aim** (it was "LookAt"), and the pivot that\
  carries the Track To constraint is called **Gimbal** (it was "Aim"). Testers\
  kept dragging the pivot, because it was the one called "Aim" - but moving it\
  booms the camera off the dolly, it does not change what the camera is\
  pointed AT, which is what everyone expected it to do.
* **The Gimbal is no longer drawn.** It shares a spot with the Dolly and the\
  camera, and a third marker there only ever gave you a wrong thing to grab.\
  It is still a real control, though, and still selectable from the outliner:\
  it is where the Track To is computed from, so nudging the Gimbal is how you\
  boom the camera off its path and keep the aim exact. Moving the CAMERA\
  instead only looks similar - the camera then aims parallel to the target\
  rather than at it, drifting several degrees as the offset grows.
* **Rig handles are much bigger - roughly five times their old size.** The old\
  sizes were inherited constants that nobody had measured; in Blender's own\
  default scene they put the Dolly at 1.5% of the shot's size, which reads as\
  dust. Handles are now sized against the path, with the Aim deliberately the\
  largest since it is the one you reach for, and the Dolly sized against the\
  camera it rides with - a collar around the cone, not a hoop. That holds all\
  the way up to kilometre-long paths; previously anything past about 100 m got\
  the same handles as a 100 m shot, so architectural walkthroughs and drone\
  moves ended up with specks again. If the new default is too large or too\
  small for your scene, **Rig Scale** in Preferences dials it.
* **The Aim target is also sized from its distance to the camera,** so a shot\
  that aims at a far wall no longer leaves you hunting for a speck.
* **Generate Rig now leaves the Aim target selected,** so the first move you\
  make is the one that points the camera.
* **The FocusPoint is selectable again.** It was click-through so it would not\
  compete with the aim target for the same click - but the two never did\
  compete, and depth of field is a creative control, not plumbing.
* **The Aim no longer prints its name in the viewport.** The label was there\
  because the old rig was a pile of near-identical gray empties and the text\
  was the only way to tell them apart; the shapes do that now, so it was just\
  a long auto-generated string sitting across the handle.
* **The Aim is a new handle:** a ring with four arrows pointing in at it, so it\
  reads as something you grab. The FocusPoint nested inside it is a focus\
  cross - three axes crossing at the point that is sharp. The Dolly keeps its\
  ring, and the rig camera now draws a little smaller so it stops swallowing\
  that ring.

#### Added

* **A "Rig Scale" preference.** Handle sizes are derived from the path, which\
  suits most shots but cannot suit every one - this multiplies them, and it\
  applies to every rig in the file the moment you move it, not just to rigs\
  you build afterwards.
* **A "Range" default in Preferences → Bake Defaults.** Every other bake\
  setting had a default and this one did not, so anyone who always bakes the\
  scene range was re-picking it in every new file.
* **"Load from Blender"** under the flythrough movement keys. The key fields\
  are what AutoCam will apply; "Apply Walk Keys" is what pushes them into\
  Blender's global walk keymap. If you have rebound walk elsewhere, this reads\
  the real bindings back so the two agree.
* **An "About" box:** which edition and version you are running, plus links to\
  the documentation, the website, and support.

#### Moved

* **"Show Path Direction"** now lives in **Preferences → Viewport**, alongside\
  Rig Scale, instead of on the Rig panel. It is a viewport display choice, and\
  the Rig panel is for things that change the shot. It was per-rig before and\
  is now global; if you were toggling it per rig, that distinction is gone.
* **"Show Hints" and "Show 'Danger Zone'"** now sit in an **Interface** box at\
  the top of Preferences. Same two settings; they were loose above the boxes\
  while everything else was grouped.

#### Fixed

* **Binding two flythrough directions to the same key no longer half-applies.**\
  Walk needs one key per direction - the press item starts the move and the\
  release stops it - so two directions on one key left movement that started\
  and never stopped. Preferences now names the clash and "Apply Walk Keys"\
  refuses until you resolve it.
* **The flythrough key fields no longer misreport your keys.** Picking a layout\
  preset changed the fields but not Blender's keymap until you pressed Apply,\
  and nothing said so; unapplied keys are now called out.
* **A bake suffix longer than 32 characters was silently truncated** on its way\
  from Preferences into a scene's Bake Settings. The preference accepted 64\
  where the setting accepted 32.
* **The default Tracking mode is now applied once the rig is actually on its**\
  **path**, not partway through building it.

#### Compatibility

* **Rigs built in 2.1.0 or earlier keep their old object names and keep**\
  **working** - AutoCam recognizes both layouts. Rebuild with "Generate Rig" to\
  pick up the new names, handle shapes and sizing. Until you do, an old rig\
  still draws its pivot at full size; it is safe to leave alone.

***

### 2.1.0 <mark style="color:$info;">— 2026-07-29</mark>

#### Changed

* **Dynamic rig mode has been REMOVED.** Simple keyframed motion is the single\
  motion model, and speed is authored by keyframing the new "Progress"\
  slider on the Rig panel (forward, hold, or reverse). The "Rig Mode"\
  switch and both Speed sliders are gone, along with their preferences.
* **Rigs saved in 2.0.x are migrated automatically on file open.** Dynamic rigs\
  become an even-paced traversal of their original frame range; performed\
  pacing is not preserved.
* **The sidebar is now organised by stage - Source, Path, Rig, Output.** The\
  "Record" panel is now "Source" and "Bake" is now "Output"; the buttons\
  and the workflow are unchanged.

#### Compatibility

* **Blender 5.x support, including 5.2 LTS.** Minimum is now Blender 4.2 (the\
  add-on install path previously advertised 4.0; the extension has always\
  required 4.2).

#### Added

* **Customizable flythrough controls:** Look sensitivity, movement speed, a\
  fast multiplier, rebindable movement keys, a one-click AZERTY (ZQSD)\
  preset, and reset-to-defaults. Stored in Preferences.
* **Rig visuals:** Rig controls are shaped and colour-coded by role (dolly,\
  aim, look-at, focus) and named in the viewport.
* **"Show Path Direction":** An optional path overlay with direction-of-travel\
  chevrons, toggleable per rig.
* **"Clear This Rig" in the Danger Zone:** Removes one rig and its baked\
  camera, restores the original camera, and leaves other rigs untouched.
* **"Re-Bake":** Re-bake an already-baked camera with different settings\
  without rebuilding the rig.
* "Show Hints" preference to hide the instructional text in the panels.

#### Fixed

* **Blender 5.x:** Rendering an animation with an AutoCam rig in the scene could\
  crash Blender with an access violation (0xc0000005). AutoCam's realtime\
  per-frame handler ran inside Blender's render job and re-entered scene\
  evaluation mid-render. It is gone along with Dynamic mode, and any copy\
  left behind by an older AutoCam is swept on start-up and on every file\
  open. (Tracker issue #35.)
* **Recording:** Cancelling a flythrough now restores your preferences fully\
  and removes the temporary timeline extension; repeated record/discard\
  cycles no longer leave stray handlers behind.
* **Baked cameras now read clean in the viewport** - selecting one no longer\
  draws the rig's path overlay.
* "Make Active" on a baked camera now makes THAT camera the scene camera\
  instead of the rig camera it was baked from.
* The reported add-on version is now taken from the build itself, so the\
  Add-ons list and the extension metadata always agree (2.0.6 reported\
  itself as 2.0.5).

***

### 2.0.6 <mark style="color:$info;">— 2026-01-03</mark>

#### Fixed

* **Path Extraction:** Camera animation detection now works reliably with Blender 5.x layered actions and NLA-based animation.

#### Improved

* **UI Cleanup:** Removed placeholder Pro feature items for a cleaner, more focused Free experience.
* **Bake Settings:** Made the popup more compact without losing functionality.

***

### 2.0.5 <mark style="color:$info;">— 2025-11-24</mark>

#### Compatibility

* Now supports **Blender 5.0** while maintaining backwards compatibility back to **Blender 4.2**.

#### Fixed

* **Recording Cursor:** The mouse cursor no longer gets stuck or hits a boundary while recording.
* **Recording Exit:** You can now cleanly finish recording by pressing Escape, Left Click, or Right Click.

#### Improved

* **Match Recording:** Settings are now more responsive and intuitive to use.

***

### 2.0.4 <mark style="color:$info;">— 2025-10-15</mark>

#### Changed

* Dynamic rigs now read speed as distance-per-second, so timing stays consistent when the curve is extended/retracted.
* Simple and Dynamic rigs now keep independent speed values, so keying one mode no longer indicates the other's Speed slider as animated.

#### Fixed

* Simple mode path follow preserves its keyframes when you rebuild or toggle modes; animation data is serialized and restored automatically.
* Dynamic mode now supports auto-keying, allowing users to quickly prototype camera animations in real-time.

***

### 2.0.3 <mark style="color:$info;">— 2025-09-25</mark>

#### Changed

* Standardized every operator, panel, and helper prefix to `AUTOCAM_`, updating bpy.ops identifiers and helper utilities to the `autocam` namespace for clearer branding.

#### Fixed

* Fly Record no longer traps the cursor when canceling; removing the `GRAB_CURSOR` flag lets the pointer return immediately after dismissing confirmation.

***

### 2.0.2 <mark style="color:$info;">— 2025-09-16</mark>

#### **Fixed**

* Dynamic rigs no longer freeze after reopening a .blend. The rig builder now stamps a persistent ID on new rigs so Dynamic mode resumes correctly on load.

**Note**

* If you built a rig in 2.0.1 or earlier and it still freezes after reopening, rebuild once with **Generate Rig** to stamp the ID. After that, reloads will be stable.

***

### 2.0.1 <mark style="color:$info;">— 2025-09-04</mark>

#### **Fixed**

* Aim preset "Recorded Rotations" renamed to **Match Recording**.
* Rig builder now seeds arc table, sets start frame, and refreshes the view layer.
* **Match Recording** starts at frame 1, refreshes the view layer, and runs a safe try/except.

***

### 2.0.0 <mark style="color:$info;">— 2025-09-02</mark>

#### Added

* **One-Click Bake**: Convert AutoCam rigs to plain keyframes for rendering/export.
* **Rig Mode switch**: Choose between native Blender constraints (**Simple**) and AutoCam's realtime evaluator (**Dynamic**).
* **Tracking**: Easier camera aiming with cleaner results and less manual tweaking.
* **UI overhaul**: Context-aware panels, clear tooltips, and smart defaults.

#### Changed

* **Path generation** now auto-applies **default Path Settings**.
* Labels, menu order, and tooltips simplified.

#### Fixed

* Reduced stutter on newly generated rigs.
* Safer enable/disable and registration; miscellaneous stability fixes.

#### Compatibility

* **Blender 4.0+** supported; **Extension** install path available on **4.2+**.
* Scenes from **1.x** should continue to load; if something looks off, regenerate the rig.

***

### 1.1.2 <mark style="color:$info;">— 2025-06-18</mark>

* Consolidated object properties into a single `PropertyGroup`.
* Fixed Preferences registration for 4.x Extension installs.

***

### 1.1.1 <mark style="color:$info;">— 2025-06-15</mark>

* Repackaged as a proper Blender 4.x **Extension**.
* Internal code cleanup.
* No new end-user features (maintenance/stability).

***

### 1.1.0 <mark style="color:$info;">— 2025-05-14</mark>

* Key-framable **negative** and **zero** speed (reverse / pause).
* Removed the **Interpolation** dropdown.
* Removed the older **Sync Speed to Keyframe** button.
* Multiple rigs per scene (independent handlers).
* Arc-length cache for smooth, constant motion on any spline type.
* Stable reload: handler guard, hard speed limits, duplicate-helper cleanup.

***

### 1.0.0 <mark style="color:$info;">— 2025-05-06</mark>

* First public release.

***

### **Next steps**

* See what AutoCam Pro adds → [**AutoCam Pro changelog**](autocam-pro.md)
* See the public [**Roadmap**](../roadmap.md) for what's planned and what's in progress.
* Got ideas or feedback? Open an issue in the [**GitHub Tracker**](https://github.com/AgnivD/AutoCam-Tracker/issues/new/choose).
