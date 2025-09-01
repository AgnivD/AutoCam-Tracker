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

## 2.0.0 \[Latest Release] <mark style="color:$info;">— 2025-09-01</mark>

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
