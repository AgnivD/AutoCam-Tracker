---
icon: forward
---

# Quick Start

Get a working AutoCam rig in under a minute. Follow these steps after installing AutoCam-

{% hint style="warning" %}
This page is a fast overview to get you moving. Please read [**Features**](../learn/features/) and [**Guides**](../learn/guides.md) for the full breakdowns.
{% endhint %}

{% hint style="info" %}
Steps marked <mark style="color:$warning;">**PRO**</mark> are **AutoCam Pro** features. Everything unmarked works in Free.
{% endhint %}

***

#### Step 1: Record a flythrough

1. In the 3D View, press **N** → open the **AutoCam** tab.
2. Click **Record Flythrough**.
3. Fly like a game: **W/A/S/D** (move), **Q/E** (down/up), **Mouse** (look).
4. Press **Esc** or **Left/Right Mouse Click** to stop.

{% hint style="success" %}
Learn more about [**Recording**](../learn/features/source.md#start-a-recording).
{% endhint %}

{% hint style="info" %}
<mark style="color:$warning;">**PRO**</mark> **Prefer blocking shots to flying them?** Click **New Camera Morph** instead and declare the poses you want the camera to pass through. AutoCam builds the move - including lens and focus changes - between them. See [**Camera Morph**](../learn/features/source.md#camera-morph-pro).
{% endhint %}

***

#### Step 2: Extract the Camera's Path

1. Select your **Camera** → Click **Generate Curve**.
2. Pick a **Spline Type** (Bezier/Poly/NURBS), and/or tweak the **Tolerance** value.
3. Tweak points in **Edit Mode** if needed and click **Apply** (while still being in Edit mode).

{% hint style="success" %}
Learn more about [**Path Extraction**](../learn/features/path.md#path-extraction).
{% endhint %}

{% hint style="info" %}
<mark style="color:$warning;">**PRO**</mark> Close the path into a seamless cycle with [**Loop**](../learn/features/path.md#loop-pro), or reshape it live while the shot plays with [**Steer Path**](../learn/features/path.md#realtime-path-steering-pro).
{% endhint %}

***

#### Step 3: Generate the Camera Rig

1. Select the **Curve** (AutoCamPath) → Click **Generate Rig**, then press **Play** on the Timeline.
2. Keyframe **Progress** (0 → 1) on the Rig panel to time the move.

AutoCam leaves the **Aim** target selected after building the rig - that's the handle you drag to point the camera.

{% hint style="success" %}
Learn more about [**Rig Generation**](../learn/features/rig.md#rig-generation).
{% endhint %}

***

#### Step 4: Timing & Tracking <mark style="color:$info;">(Optional for Quick Start)</mark>

**Timing (the Progress slider):**

**Progress** runs the camera from the start of the path (**0**) to the end (**1**). Keyframe it to time the shot:

* Frame **1** → Progress **0** → keyframe
* Frame **120** → Progress **1** → keyframe

Hold the same value across two keys to **pause**. Run it backwards to **reverse**.

{% hint style="info" %}
<mark style="color:$warning;">**PRO**</mark> **Want your recorded pacing back?** One click on **Inherit Original Speed** rebuilds the Progress keys from the original recording - every hesitation and acceleration, on a clean path. See [**Inherit Original Speed**](../learn/features/rig.md#inherit-original-speed-pro).
{% endhint %}

**Tracking settings:**

* [**Manual Aim**](../learn/features/rig.md#manual-aim)**:** Camera tracks the **Aim** object. <mark style="color:$info;">(Best for single, static subjects, or full control)</mark>
* [**Match Recording**](../learn/features/rig.md#match-recording)**:** Camera inherits rotation data from the original recording. <mark style="color:$info;">(Best for quick setups with less manual work)</mark>
* <mark style="color:$warning;">**PRO**</mark> [**Lock to Target**](../learn/features/rig.md#lock-to-target-pro)**:** Camera watches any object you pick, every frame, even animated.
* <mark style="color:$warning;">**PRO**</mark> [**Path Lookahead**](../learn/features/rig.md#path-lookahead-pro)**:** Camera aims a set distance ahead along the path, steering through corners.
* <mark style="color:$warning;">**PRO**</mark> [**Smart Auto-Aim**](../learn/features/rig.md#smart-auto-aim-pro)**:** Camera's aim is derived from what your recording was looking at.

{% hint style="success" %}
**Tip:** To make the camera finish on an exact frame, drag the last **Progress** keyframe to that frame. That's the whole trick, nothing to sync or recalculate.
{% endhint %}

***

#### Step 5: Bake to Keyframes <mark style="color:$info;">(Optional for Quick Start)</mark>

Open the [**Output**](../learn/features/output.md) panel and click **Bake** to convert AutoCam motion to **plain keyframes**. Perfect for exporting to other DCCs or rendering on a PC without AutoCam installed.

Changed your mind? The button becomes **Re-Bake** once a bake exists. Run it again with different settings, no need to rebuild the rig.

{% hint style="success" %}
Learn more about [**Baking**](../learn/features/output.md#bake-the-rig).
{% endhint %}

{% hint style="info" %}
<mark style="color:$warning;">**PRO**</mark> Send the baked camera straight to another DCC with the **Export** tab - **Alembic**, **USD**, or **FBX**, scoped to just the camera. See [**Export**](../learn/features/output.md#export-pro).
{% endhint %}

***

#### Next steps

* **Learn the tools** → [**Features**](../learn/features/)
* **Follow tutorials** → [**Guides**](../learn/guides.md)
* **Compare editions** → [**Editions**](editions.md)
* **Having issues?** Start with [**Troubleshooting**](../help/troubleshooting.md), check the [**FAQ**](../help/faq.md), and contact [**Support**](../help/support.md) if necessary.
