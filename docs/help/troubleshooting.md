---
icon: bug-slash
---

# Troubleshooting

Most quick fixes live on the [**feature pages**](../learn/features/) under "**Common Issues**". Start here only for global problems or when you're not sure which page to check.

### 30-second checklist

* **Blender version:** **4.2+** (developed and tested on 5.2 LTS)
* **Edition & version:** **Preferences** → **Add-ons** → **AutoCam** → **About**. It names exactly what you're running.
* **Only one edition installed:** Free and Pro **cannot coexist**. If you installed one over the other, uninstall both, restart, and install one. [**More info**](../welcome/editions.md).
* **Updated correctly:** Removed previous install → **Restarted Blender** (important). [**More info**](../welcome/installation.md).
* **Nothing moves:** Select the rig and make sure **Progress has at least two keyframes**; press **Play**. [**More info**](../learn/features/rig.md#progress).
* **Controls vanished:** Read [**UI Overview**](../learn/features/ui-overview.md) to understand contextual panel states.
* **Recording didn't write keys:** Make the camera **Active** (header → **Make Active**), then record again.
* **Blender 5x crash:** Update to AutoCam 2.1 or later.

***

### "A control the docs mention isn't in my panel"

Two likely reasons, in order:

1. **It's a Pro feature.** Anything marked <mark style="color:$warning;">**PRO**</mark> in these docs is absent from a Free install - not greyed out, not labelled, simply not shipped. Check **Preferences → About** for your edition, and see [**Editions**](../welcome/editions.md).
2. **The panel is contextual.** AutoCam shows only what applies to your selection and the stage the rig has reached. The [**stage breadcrumb**](../learn/features/ui-overview.md#the-stage-breadcrumb) at the top tells you which stage you're on.

#### Moved in 2.1.1

| Looking for                                                         | It's now in                                                                            |
| ------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| **Show Path Direction** (was on the Rig panel)                      | **Preferences → Viewport** - and it's global, not per-rig                              |
| **Show Hints** / **Show 'Danger Zone'** (were loose in Preferences) | **Preferences → Interface**                                                            |
| The **LookAt** object                                               | Renamed **Aim**                                                                        |
| The old **Aim** pivot                                               | Renamed **Gimbal**, and no longer drawn (still selectable from the Outliner)           |
| **Show Aim Line**                                                   | Removed - Blender's own **Overlays → Relationship Lines** already draws that sightline |

***

### Installation problems

* _"Both editions seem installed / panels are doubled"_ - Uninstall **both** AutoCam entries, **restart Blender**, then install one ZIP. They register the same operators and cannot run together.
* _"Install failed after uninstalling"_ - You skipped the restart. Blender keeps the old module registered until it restarts.
* _"The add-on list still says just AutoCam"_ - The Free extension was renamed **AutoCam Free** in 2.1.1. It updates in place; the entry refreshes on reinstall. The sidebar tab is still **AutoCam** either way.

***

### Performance Tips

#### While recording:

* Keep the 3D View in **Solid** (or simple MatCap) and **hide shadows/cavity**.
* Temporarily **hide high-poly collections** or set heavy meshes to **Display As: Bounds**.
* Disable or pause **physics/particles** and expensive modifiers during the take.

#### Path editing:

* If the path feels dense, **increase Tolerance** and apply to reduce points before editing.
* Prefer **Bezier** for handle control; **NURBS** for very smooth, long arcs.
* Always **press Apply while still in Edit Mode** (if you've changed the curve points).

#### Tracking:

* In **Match Recording**, use **Simplify** first (sparingly), then a touch of **Smoothing** to reduce jitter.
* <mark style="color:$warning;">**PRO**</mark> In **Smart Auto-Aim**, the scene is raycast once and cached - dragging Smoothing or Simplify re-derives instantly. Only press **Resample Scene** after geometry actually moves.

#### Baking & export:

* **Step** = **1** for final fidelity.
* **Depth of Field** = **Keyframes** for export-safe focus pulls.
* After baking, **hide the original rig collection** so only the baked camera evaluates.

#### General Blender performance:

* Enable **Render Properties** → **Simplify** (lower viewport subdivisions).
* Turn off **Viewport Motion Blur** while iterating.
* Use **Collection Instances** for repeated assets instead of duplicates.

***

### AutoCam Pro specifics <mark style="color:$warning;">**PRO**</mark>

* _"Steer Path won't start"_ - The modal session needs an actual **3D Viewport** in your screen layout.
* _"My loop stutters at the wrap"_ - End the render range **one frame before** the lap end the Loop panel reports. Frame N is a duplicate of frame 1.
* _"Timing drifted after I edited the path"_ - Inherited timing was measured against the old path. Click **Inherit Original Speed** again.
* _"The aim freezes on a later segment"_ - **Match Recording** and **Smart Auto-Aim** are derived from the rig's own recording. Use **Manual Aim**, **Lock to Target**, or **Path Lookahead** across segments.
* _"FBX export fails"_ - Enable Blender's built-in **FBX format** add-on.
* _"The Batch tab isn't showing"_ - It needs two or more rigs, with at least one at the Rig stage.
* _"I reverted a stage by mistake"_ - **Ctrl+Z**. Reverts are undoable, and climbing back up the stage strip restores the stage exactly as it was.

***

### Final Render/Export

* Always export the **baked** camera (not the rig camera).
* When using a render farm or a different PC without AutoCam installed, **Bake the rig**.
* Use **DoF** = **Keyframes** if you want focus pulls outside Blender.
* Sharing a Pro-built file with someone on Free? **Bake first** - a baked camera is plain keyframes and needs no add-on.

***

### Still stuck?

See the [**FAQ**](faq.md) or contact [**Support**](support.md).

&#x20;&#x20;
