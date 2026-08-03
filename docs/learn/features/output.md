---
icon: file-export
---

# Output

Baking transforms your AutoCam rig into standard keyframes on a Blender camera. This process makes the animation **independent of AutoCam**, ensuring consistent playback across different computers, render farms, or other digital content creation (DCC) tools.

<figure><img src="../../.gitbook/assets/AutoCamBake1.gif" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**Note:** Requires an **AutoCam** [**Rig**](rig.md).
{% endhint %}

***

## Bake the rig

{% hint style="info" %}
**Prerequisites:**

* An **AutoCam** [**Rig**](rig.md) is present.
{% endhint %}

{% stepper %}
{% step %}
In the 3D View, press **N** → open **AutoCam**.

<div align="left"><figure><img src="../../.gitbook/assets/blender_7vLtMsUVBp.png" alt=""><figcaption></figcaption></figure></div>
{% endstep %}

{% step %}
Verify the header displays the correct rig, then click the <i class="fa-gear">:gear:</i> button beside the Bake button.

<div align="left"><figure><img src="../../.gitbook/assets/blender_7vqdoDQrR3.png" alt=""><figcaption></figcaption></figure></div>
{% endstep %}

{% step %}
Configure your **Baking Settings**.

<div align="left"><figure><img src="../../.gitbook/assets/blender_HyL62sT7eN.png" alt=""><figcaption></figcaption></figure></div>

* **Frame Range:** Choose which frames to bake.
  * **Curve Range -** the rig/path span.
  * **Scene Range** - timeline start/end.
  * **Custom** - enter start/end frames.
* **Step:** Write keys every **N** frames.
  * **1** = Every frame (recommended for final).
  * **Higher values** = Fewer keys, but less precise motion/DoF.
* **Depth of Field:** Decide how focus is handled.
  * **Keyframes** - Bake FocusPoint into Focus Distance keys (export-safe).
  * **Use Focus Object** - Uses the original FocusPoint.
  * **Off** - Disable DoF entirely.
* **Set as active scene camera:** Make the newly baked camera the active render camera immediately.
* **Suffix:** Append text to the baked camera’s name (e.g., `_Baked`) for easy identification.
{% endstep %}

{% step %}
Click on the **Bake button** to start the baking process.

<figure><img src="../../.gitbook/assets/ecClAF6DkS.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
A new **baked camera** is created. AutoCam controls hide for that camera.

<figure><img src="../../.gitbook/assets/blender_nuUHkFktbf.png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

{% hint style="success" %}
Baking through AutoCam is **non-destructive** because the original rig collection remains intact. To revert, simply delete the "**\_Baked**" collection and reactivate the original.
{% endhint %}

***

## When to bake <mark style="color:$info;">(quick checklist)</mark>

* You're sending to a **render farm** or sharing the file with someone **without AutoCam**.
* You're **exporting to another DCC** (FBX/Alembic/etc).
* You want a **locked, lightweight** camera you can tweak with vanilla keyframes.
* You want the shot immune to any later edit of the rig or its path.

***

## Re-Bake

<div align="left"><figure><img src="../../.gitbook/assets/blender_kNtDycX1sU.png" alt="" width="351"><figcaption></figcaption></figure></div>

Once a rig has been baked, the **Bake** button becomes **Re-Bake**.

It runs the bake again with your current settings and supersedes the previous baked camera.

Use it when you've changed the Progress timing, adjusted Tracking, or just want a different Step or Depth of Field setting on the output.

***

## Common Issues <mark style="color:$info;">(and quick fixes)</mark>

* _"DoF missing or wrong on the baked camera"_ - You chose **Use Focus Object** or **Off**. Re-bake with **Depth of Field** → **Keyframes** (export-safe).
* _"Controls disappeared"_ - You’re looking at the **baked** camera. Select the **original rig** to show controls.
* _"Export doesn't match preview"_ - Always export the **baked** camera, not the camera inside the rig collection.
* _"I deleted the rig and the baked camera went with it"_ - That's **Clear This Rig** working as intended: it takes the bake down first, then the rig. Bake again from a rebuilt rig, or keep the baked camera by moving it out of its collection first.

{% hint style="success" %}
Learn more about [**Panel States**](ui-overview.md#panel-states) to understand how it changes based on the context.
{% endhint %}

***

## Next steps

* See practical examples → [**Guides**](../guides.md)
* Or jump back to [**Quick Start**](../../welcome/quick-start.md) to see the whole workflow.

&#x20;&#x20;
