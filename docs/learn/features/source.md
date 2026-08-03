---
icon: video
---

# Source

Fly through your scene like a video game, and AutoCam captures that motion as keyframes on your camera. This rough animation becomes the foundation for the AutoCam path and camera rig.

**Source** is also where AutoCam shows the origin of an existing rig. Select any AutoCam object and the panel names the camera the motion came from.

<figure><img src="../../.gitbook/assets/AutoCamRecord1.gif" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**Note:** Recording is optional. If your camera already has location keyframes, you can skip ahead to [**Path**](path.md)**.**
{% endhint %}

***

## Start a recording

{% hint style="info" %}
**Prerequisites:**

* A **Camera** exists in the scene (**Shift + A** → **Camera**).
* It’s set as the **active scene camera** (**Make Active** in the AutoCam panel header).
{% endhint %}

{% stepper %}
{% step %}
In the 3D View, press **N** → open **AutoCam**.

<div align="left"><figure><img src="../../.gitbook/assets/blender_VnR0vAC9p9.png" alt=""><figcaption></figcaption></figure></div>
{% endstep %}

{% step %}
Click **Record Flythrough**.

<div align="left"><figure><img src="../../.gitbook/assets/blender_QTUK9jVQUO.png" alt=""><figcaption></figcaption></figure></div>
{% endstep %}

{% step %}
**Fly like a game** ([see controls](source.md#default-controls)).

<figure><img src="../../.gitbook/assets/AutoCamRecord2.gif" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
Press **Esc** or **Left/Right Mouse Click** to finish.

<figure><img src="../../.gitbook/assets/AutoCamRecord3.gif" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

{% hint style="warning" %}
**Note:** Recording always uses the **active scene camera,** regardless of the selected camera.
{% endhint %}

***

## Default controls

| Action                  | Keys/Mouse                                  |
| ----------------------- | ------------------------------------------- |
| Forward / Back          | **W / S**                                   |
| Left / Right            | **A / D**                                   |
| Down / Up               | **Q / E**                                   |
| Look / Orbit            | **Mouse**                                   |
| Accelerate / Decelerate | **Scrollwheel**                             |
| Stop recording          | **Esc**, **Left Click**, or **Right Click** |

{% hint style="info" %}
**Note:** These are the defaults. Every movement key is rebindable in Preferences (below).
{% endhint %}

{% hint style="success" %}
**Tip:** AutoCam records using Blender's built-in **Walk Navigation**. You can tune it without leaving AutoCam: **Edit** → **Preferences** → **Add-ons** → **AutoCam** → **Flythrough Controls**.

* **Look Sensitivity** (default 1.0) - Mouse-look speed.
* **Move Speed** (default 2.5) - Base travel speed in Blender units/sec.
* **Fast Multiplier** (default 5.0) - Speed boost while holding the fast modifier.
* **Keyboard Layout** - **QWERTY**, **AZERTY (ZQSD)**, or **Custom**. The six key fields become editable only on **Custom**.
* **Apply** writes the movement keys; **Reset** restores Blender's QWERTY defaults.

**AZERTY preset:** Forward **Z**, Backward **S**, Left **Q**, Right **D**, Up **E**, Down **A**.
{% endhint %}

{% hint style="warning" %}
**Note:** Sensitivity settings are applied only while AutoCam is recording and restored afterwards, so your normal viewport feel is untouched. Movement keys are different: **Apply** rebinds Blender's global _View3D Walk Modal_ keymap, so it changes walk navigation everywhere, not just in AutoCam. Use **Reset** to undo.
{% endhint %}

***

## Tips for clean recordings

* **Plan your move.** Have a rough path in mind before you hit record.
* **Keep it flowing.** Avoid retracing steps to reduce path cleanup later.
* **Control your speed.** Use the scroll wheel to adjust acceleration on the fly.

***

## What exactly gets recorded?

* **Location/Rotation keys** are written to the **active scene camera** from the **frame where you start recording** until you stop.
* The camera's functionality remains unchanged; it continues to function as a regular Blender camera.

***

## Common Issues <mark style="color:$info;">(and quick fixes)</mark>

* _"Nothing recorded"_ - Ensure the camera is **active**, then try again. Keyframes will only appear on the timeline when you select the correct camera where the motion was recorded.
* _"Recording is laggy"_ - Try using minimal viewport shading, simplify the scene, and ensure complex objects remain stationary while recording.
* _"Source panel shows a camera name instead of the Record button"_ - That's expected: you have an AutoCam object selected, so Source is showing where that rig's motion came from. Deselect it (or pick a plain camera) to start a new recording.
* _"Source panel disappeared"_ - You have a **baked** camera selected. AutoCam hides its controls for baked cameras so a finished shot reads clean.
* _"Source removed"_ - The camera this rig was built from is no longer in the file. **The rig is unaffected** (its camera is an independent copy, so the shot still plays and bakes normally).\
  This is rarer than it looks. AutoCam keeps a reference to the source camera, so deleting it with **X**, running **File ▸ Clean Up ▸ Purge**, appending the rig into another file, or saving and reopening all leave it in place. Only a forced datablock delete (Outliner ▸ **Blender File** view ▸ right-click ▸ **Delete**) actually removes it.

{% hint style="info" %}
Learn more about [**Panel States**](ui-overview.md#panel-states) to understand how it changes based on the context. Instructional hint text throughout AutoCam can be hidden via **Preferences** → **Add-ons** → **AutoCam** → **Show Hints**.
{% endhint %}

***

## Next steps

* Turn this recording into an editable curve on [**Path**](path.md).
* Or jump back to [**Quick Start**](../../welcome/quick-start.md) to see the whole workflow.

&#x20;&#x20;
