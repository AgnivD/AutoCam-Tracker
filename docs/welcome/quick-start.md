---
icon: forward
---

# Quick Start

Get a working AutoCam rig in under a minute. Follow these steps after [installing](installation.md) AutoCam-

{% hint style="warning" %}
This page is a fast overview to get you moving. Please read [**Features**](../learn/features/) and [**Guides**](../learn/guides.md) for the full breakdowns.
{% endhint %}

***

### Step 1: Record a flythrough

1. In the 3D View, press **N** → open the **AutoCam** tab.
2. Click **Record Flythrough**.
3. Fly like a game: **W/A/S/D** (move), **Q/E** (down/up), **Mouse** (look).
4. Press **Esc** or **Left/Right Mouse Click** to stop.

{% hint style="success" %}
Learn more about [**Recording**](../learn/features/source.md).
{% endhint %}

***

### Step 2: Extract the Camera's Path

1. Select your **Camera** → Click **Generate Curve**.
2. Pick a **Spline Type** (Bezier/Poly/NURBS), and/or tweak the **Tolerance** value.
3. Tweak points in **Edit Mode** if needed and click **Apply** (while still being in Edit mode).

{% hint style="success" %}
Learn more about [**Path Extraction**](../learn/features/path.md).
{% endhint %}

***

### Step 3: Generate the Camera Rig

1. Select the **Curve** (AutoCamPath) → Click **Generate Rig**, then press **Play** on the Timeline.
2. Keyframe **Progress** (0 → 1) on the Rig panel to time the move.

{% hint style="success" %}
Learn more about [**Rig Generation**](../learn/features/rig.md).
{% endhint %}

***

### Step 4: Timing & Tracking <mark style="color:$info;">(Optional for Quick Start)</mark>

#### **Timing (the Progress slider):**

**Progress** runs the camera from the start of the path (**0**) to the end (**1**). Keyframe it to time the shot:

* Frame **1** → Progress **0** → keyframe
* Frame **120** → Progress **1** → keyframe

Hold the same value across two keys to **pause**. Run it backwards to **reverse**.

#### **Tracking settings:**

* **Manual Aim:** Camera tracks the **LookAt** object.\
  <mark style="color:$info;">(Best for single, static subjects, or full control)</mark>
* **Match Recording:** Camera inherits rotation data from the original recording.\
  <mark style="color:$info;">(Best for quick setups with less manual work)</mark>

{% hint style="success" %}
**Tip:** To make the camera finish on an exact frame, drag the last **Progress** keyframe to that frame. That's the whole trick, nothing to sync or recalculate.
{% endhint %}

***

### Step 5: Bake to Keyframes <mark style="color:$info;">(Optional for Quick Start)</mark>

Open the **Output** panel and click **Bake** to convert AutoCam motion to **plain keyframes**. Perfect for exporting to other DCCs or rendering on a PC without AutoCam installed.

Changed your mind? The button becomes **Re-Bake** once a bake exists. Run it again with different settings, no need to rebuild the rig.

{% hint style="success" %}
Learn more about [**Baking**](../learn/features/output.md).
{% endhint %}

***

### Next steps

* **Learn the tools** → [**Features**](../learn/features/)
* **Follow tutorials** → [**Guides**](../learn/guides.md)
* **Having issues?** Start with [**Troubleshooting**](../help/troubleshooting.md), check the [**FAQ**](../help/faq.md), and contact [**Support**](../help/support.md) if necessary.

&#x20;
