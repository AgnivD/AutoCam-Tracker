---
icon: bug-slash
---

# Troubleshooting

Most quick fixes live on the [**feature pages**](../learn/features/) under "**Common Issues**". Start here only for global problems or when you’re not sure which page to check.

## 30-second checklist

* **Blender version:** **4.0+** (Extensions path supported from **4.2+**).
* **Updated correctly:** Removed previous install → **Restarted Blender** (important). [**More info**](../welcome/installation.md).
* **Nothing moves:** Select the rig and make sure **Speed** ≠ **0**; press **Play**. [**More info**](../learn/features/rig.md#common-issues-and-quick-fixes).
* **Timing mismatch:** If you used **Dynamic**, **Bake** before render/export. [**More info**](../learn/features/bake.md#common-issues-and-quick-fixes).
* **Controls vanished:** Read [**UI Overview**](../learn/features/ui-overview.md) to understand contextual panel states.
* **Record didn’t write keys:** Make the camera **Active** (header → **Make Active**), then record again.

***

## Performance Tips

### While recording:

* Keep the 3D View in **Solid** (or simple MatCap) and **hide shadows/cavity**.
* Temporarily **hide high-poly collections** or set heavy meshes to **Display As: Bounds**.
* Disable or pause **physics/particles** and expensive modifiers during the take.

### Path editing:

* If the path feels dense, **increase Tolerance** and apply to reduce points before editing.
* Prefer **Bezier** for handle control; **NURBS** for very smooth, long arcs.
* Always **press Apply while still in Edit Mode** (if you’ve changed the curve points).

### Tracking:

* In **Match Recording**, use **Simplify** first (sparingly), then a touch of **Smoothing** to reduce jitter.

### Baking & export:

* **Step** = **1** for final fidelity.
* **Depth of Field** = **Keyframes** for export-safe focus pulls.
* After baking, **hide the original rig collection** so only the baked camera evaluates.

### General Blender performance:

* Enable **Render Properties** → **Simplify** (lower viewport subdivisions).
* Turn off **Viewport Motion Blur** while iterating.
* Use **Collection Instances** for repeated assets instead of duplicates.

***

## Final Render/Export

* Always export the **baked** camera (not the rig camera).
* When using a render farm or a different PC without AutoCam installed, use [**Simple Rig Mode**](../learn/features/rig.md#rig-mode) or [**Bake the rig**](../learn/features/bake.md).
* Use **DoF** = **Keyframes** if you want focus pulls outside Blender.

***

## Still stuck?

See the [**FAQ**](faq.md) or contact [**Support**](support.md).

&#x20;&#x20;
