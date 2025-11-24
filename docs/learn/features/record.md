---
icon: video
---

# Record

Fly through your scene like a video game, and AutoCam captures that motion as keyframes on your camera. This rough animation becomes the foundation for the AutoCam path and camera rig.

<figure><img src="../../.gitbook/assets/AutoCamRecord1.gif" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**Note:** Recording is optional. If your camera already has location keyframes, you can skip ahead to [**Path**](path.md)**.**
{% endhint %}

***

## Start a recording

{% hint style="info" %}
**Prerequisites:**

* A **Camera** exists in the scene (**Shift + A** → **Camera**).
* It’s set as the **active scene camera** (AutoCam header → **Make Active**).
{% endhint %}

{% stepper %}
{% step %}
In the 3D View, press **N** → open **AutoCam**.

<div align="left"><figure><img src="../../.gitbook/assets/blender_1cIaaJaFo2.png" alt=""><figcaption></figcaption></figure></div>
{% endstep %}

{% step %}
Click **Start Recording**.

<div align="left"><figure><img src="../../.gitbook/assets/blender_IzUx4LLlZa.png" alt=""><figcaption></figcaption></figure></div>
{% endstep %}

{% step %}
**Fly like a game** ([see controls](record.md#default-controls)).

<figure><img src="../../.gitbook/assets/AutoCamRecord2.gif" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
Press **Esc** or **Left/Right Mouse Click** to stop.

<figure><img src="../../.gitbook/assets/AutoCamRecord3.gif" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

{% hint style="warning" %}
**Note:** Recording always uses the **active scene camera,** regardless of the selected camera.
{% endhint %}

***

## Default controls

| Action                  | Keys/Mouse      |
| ----------------------- | --------------- |
| Forward / Back          | **W / S**       |
| Left / Right            | **A / D**       |
| Down / Up               | **Q / E**       |
| Look / Orbit            | **Mouse**       |
| Accelerate / Decelerate | **Scrollwheel** |
| Stop recording          | **Esc** (twice) |

{% hint style="success" %}
**Tip:** AutoCam utilizes Blender’s built-in **Walk Navigation** mode for recording.

To customize movement key bindings:

1. Go to **Edit** → **Preferences** → **Keymap**.
2. Navigate to **3D View** → **View3D Walk Modal**.
3. Adjust **Forward**, **Backward**, **Left**, **Right**, **Up**, and **Down** controls as needed.
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
* _"Record panel disappeared"_ - Make sure that the selected object does not belong to an already generated AutoCam rig.

{% hint style="info" %}
Learn more about [**Panel States**](ui-overview.md#panel-states) to understand how it changes based on the context.
{% endhint %}

***

## Next steps

* Turn this recording into an editable curve on [**Path**](path.md).
* Or jump back to [**Quick Start**](../../welcome/quick-start.md) to see the whole workflow.

&#x20;&#x20;
