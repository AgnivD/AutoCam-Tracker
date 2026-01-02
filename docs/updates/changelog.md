---
icon: calendar-check
---

# Changelog

This project uses **semantic versioning** - **MAJOR.MINOR.PATCH** <mark style="color:$info;">(</mark>_<mark style="color:$info;">e.g., AutoCam v1.1.2</mark>_<mark style="color:$info;">).</mark>

{% hint style="info" %}
**Note:**

* This documentation contains information on **v2.0.0** onwards.
* For the recommended 2.0 workflow, see [**Record**](../learn/features/record.md) → [**Path**](../learn/features/path.md) → [**Rig**](../learn/features/rig.md) → [**Bake**](../learn/features/bake.md).
{% endhint %}

***

## 2.0.6 \[Latest Release] <mark style="color:$info;">— 2026-01-03</mark>

### Fixed

* **Path Extraction:** Camera animation detection now works reliably with Blender  &#x20;5.x layered actions and NLA-based animation.

### Improved

* **UI Cleanup:** Removed placeholder Pro feature items for a cleaner, more  &#x20;focused Free experience.
* **Bake Settings:** Made the popup more compact without losing functionality.

***

## 2.0.5 <mark style="color:$info;">— 2025-11-24</mark>

### Compatibility

* Now supports **Blender 5.0** while maintaining backwards compatibility back to  &#x20;**Blender 4.2**.

### Fixed

* **Recording Cursor:** The mouse cursor no longer gets stuck or hits a boundary  &#x20;while recording.
* **Recording Exit:** You can now cleanly finish recording by pressing Escape,  &#x20;Left Click, or Right Click.

### Improved

* **Match Recording:** Settings are now more responsive and intuitive to use.

***

## 2.0.4 <mark style="color:$info;">— 2025-10-15</mark>

### Changed

* Dynamic rigs now read speed as distance-per-second, so timing stays consistent  &#x20;when the curve is extended/retracted.
* Simple and Dynamic rigs now keep independent speed values, so keying one mode  &#x20;no longer indicates the other's Speed slider as animated.

### Fixed

* Simple mode path follow preserves its keyframes when you rebuild or toggle  &#x20;modes; animation data is serialized and restored automatically.
* Dynamic mode now supports auto-keying, allowing users to quickly prototype  &#x20;camera animations in real-time.

***

## 2.0.3 <mark style="color:$info;">— 2025-09-25</mark>

### Changed

* Standardized every operator, panel, and helper prefix to `AUTOCAM_`, updating  &#x20;bpy.ops identifiers and helper utilities to the `autocam` namespace for clearer  &#x20;branding.

### Fixed

* Fly Record no longer traps the cursor when canceling; removing the `GRAB_CURSOR`  &#x20;flag lets the pointer return immediately after dismissing confirmation.

***

## 2.0.2 \[Latest Release] <mark style="color:$info;">— 2025-09-16</mark>

### **Fixed**

* Dynamic rigs no longer freeze after reopening a .blend. The rig builder now stamps a persistent ID on new rigs so Dynamic mode resumes correctly on load.

**Note**

* If you built a rig in 2.0.1 or earlier and it still freezes after reopening, rebuild once with **Generate Rig** to stamp the ID. After that, reloads will be stable.

***

## 2.0.1 <mark style="color:$info;">— 2025-09-04</mark>

### **Fixed**

* Aim preset “Recorded Rotations” renamed to **Match Recording**.
* Rig builder now seeds arc table, sets start frame, and refreshes the view layer.
* **Match Recording** starts at frame 1, refreshes the view layer, and runs a safe try/except.

***

## 2.0.0 <mark style="color:$info;">— 2025-09-02</mark>

### Added

* **One-Click Bake**: Convert AutoCam rigs to plain keyframes for rendering/export.
* **Rig Mode switch**: Choose between native Blender constraints (**Simple**) and AutoCam’s realtime evaluator (**Dynamic**).
* **Tracking**: Easier camera aiming with cleaner results and less manual tweaking.
* **UI overhaul**: Context-aware panels, clear tooltips, and smart defaults.

### Changed

* **Path generation** now auto-applies **default Path Settings**.
* Labels, menu order, and tooltips simplified.

### Fixed

* Reduced stutter on newly generated rigs.
* Safer enable/disable and registration; miscellaneous stability fixes.

### Compatibility

* **Blender 4.0+** supported; **Extension** install path available on **4.2+**.
* Scenes from **1.x** should continue to load; if something looks off, regenerate the rig.

***

## 1.1.2 <mark style="color:$info;">— 2025-06-18</mark>

* Consolidated object properties into a single `PropertyGroup`.
* Fixed Preferences registration for 4.x Extension installs.

***

## 1.1.1 <mark style="color:$info;">— 2025-06-15</mark>

* Repackaged as a proper Blender 4.x **Extension**.
* Internal code cleanup.
* No new end-user features (maintenance/stability).

***

## 1.1.0 <mark style="color:$info;">— 2025-05-14</mark>

* Key-framable **negative** and **zero** speed (reverse / pause).
* Removed the **Interpolation** dropdown.
* Removed the older **Sync Speed to Keyframe** button.
* Multiple rigs per scene (independent handlers).
* Arc-length cache for smooth, constant motion on any spline type.
* Stable reload: handler guard, hard speed limits, duplicate-helper cleanup.

***

## 1.0.0 <mark style="color:$info;">— 2025-05-06</mark>

* First public release.

***

## **Next steps**

* See the public [**Roadmap**](roadmap.md) for what’s planned and what’s in progress.
* Got ideas or feedback? Open an issue in the [**GitHub Tracker**](https://github.com/AgnivD/AutoCam-Tracker/issues/new/choose).

&#x20;&#x20;
