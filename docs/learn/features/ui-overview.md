---
icon: objects-column
---

# UI Overview

This page provides a quick overview of the layout, explains the purpose of each panel, and describes how they respond in various contexts.

Think of it as a map- start here to understand where everything lives, then jump into the dedicated pages for each panel.

&#x20;

***

&#x20;

## Introduction

{% columns %}
{% column width="58.333333333333336%" %}
<div align="left"><figure><img src="../../.gitbook/assets/blender_GYHQNtcNy4.png" alt=""><figcaption></figcaption></figure></div>
{% endcolumn %}

{% column width="41.666666666666664%" valign="middle" %}
The AutoCam interface lives in\
**3D View** → **N-panel** → **AutoCam**.
{% endcolumn %}
{% endcolumns %}

&#x20;

***

&#x20;

## Header States

The top of the AutoCam panel is an unlabelled box that always tells you what you're working on.

* **Nothing relevant selected** - "Select a Camera or any AutoCam rig object to begin."
* **A plain camera selected** - Its name and whether it's **active** or **inactive**. If it's inactive, a **Make Active** button appears to make it the scene camera.
* **An AutoCam object selected** - "Selected Rig: _name_", so you always know which rig the panels below are editing.

{% hint style="info" %}
**Make Active** lives here, at the top, not on the Source panel. Recording always uses the **active scene camera**, so this is the button you press before recording.
{% endhint %}

&#x20;

***

&#x20;

## Panel States

Panels within the AutoCam interface dynamically update based on the context, similar to the header.

&#x20;

### **Source** panel:

{% columns %}
{% column width="50%" valign="middle" %}
Shown for everything except a **baked** camera.

With a plain camera or nothing selected, it offers **Record Flythrough**.
{% endcolumn %}

{% column width="50%" valign="middle" %}
<figure><img src="../../.gitbook/assets/blender_YZkUUrzYDE.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

{% hint style="info" %}
[Learn more](source.md) about **Record Flythrough**.
{% endhint %}

{% columns %}
{% column width="50%" valign="middle" %}
With an AutoCam object selected, it switches to naming the camera that rig's motion came from, so Source doubles as "where did this shot come from".
{% endcolumn %}

{% column width="50%" valign="middle" %}
<figure><img src="../../.gitbook/assets/blender_QFmP6kRZLY.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

{% columns %}
{% column width="50%" valign="middle" %}
If that camera is no longer in the file, it reads **Source removed**. The rig still works - its camera is an independent copy.
{% endcolumn %}

{% column width="50%" valign="middle" %}
<figure><img src="../../.gitbook/assets/blender_AlFJrxgjFQ.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

&#x20;

***

&#x20;

### **Path** panel:

{% columns %}
{% column width="50%" valign="middle" %}
When the selected object is a non-camera object, the **Path** panel prompts the user to select an animated camera.
{% endcolumn %}

{% column width="50%" valign="middle" %}
<figure><img src="../../.gitbook/assets/TabTip_mvNGksdEP4.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

***

{% columns %}
{% column valign="middle" %}
If a camera is selected, but it lacks animation data, it updates the prompt.
{% endcolumn %}

{% column valign="middle" %}
<figure><img src="../../.gitbook/assets/TabTip_AR83Nnrvzz.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

***

{% columns %}
{% column valign="middle" %}
When you select an animated camera, **Generate Curve** is enabled and the prompt is hidden.
{% endcolumn %}

{% column valign="middle" %}
<figure><img src="../../.gitbook/assets/TabTip_12VPU35u59.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

***

{% columns %}
{% column valign="middle" %}
When an AutoCam object is selected, **Path Settings** appears instead.

{% hint style="info" %}
[Learn more](path.md) about **Path Settings**.
{% endhint %}
{% endcolumn %}

{% column valign="middle" %}
<figure><img src="../../.gitbook/assets/TabTip_ENvt5QR2wM.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

&#x20;

***

&#x20;

### **Rig Settings** panel:

{% columns %}
{% column valign="middle" %}
Before the rig exists, the **Rig** panel offers **Generate Rig** (an AutoCam curve must be selected).
{% endcolumn %}

{% column valign="middle" %}
<figure><img src="../../.gitbook/assets/TabTip_Cr2qx0dOkc.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

***

{% columns %}
{% column valign="middle" %}
Once built, it becomes the rig's settings: the **Progress** slider with its keyframe decorator, the **Show Path Direction** checkbox, and a collapsible **Tracking** sub-panel.

{% hint style="info" %}
[Learn more](rig.md) about **Rig Settings**.
{% endhint %}
{% endcolumn %}

{% column valign="middle" %}
<figure><img src="../../.gitbook/assets/blender_k5lpGqdTXc.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

***

&#x20;

### **Output** panel:

{% columns %}
{% column valign="middle" %}
Collapsed by default.

Holds **Bake** and its settings popover.
{% endcolumn %}

{% column valign="middle" %}
<div align="center"><figure><img src="../../.gitbook/assets/blender_F7ea0Jh2vw.png" alt=""><figcaption></figcaption></figure></div>
{% endcolumn %}
{% endcolumns %}

{% columns %}
{% column valign="middle" %}
Once a bake exists, the button reads **Re-Bake.**
{% endcolumn %}

{% column valign="middle" %}
<figure><img src="../../.gitbook/assets/blender_kNtDycX1sU.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

{% columns %}
{% column valign="middle" %}
Run it again with different settings without rebuilding the rig.
{% endcolumn %}

{% column valign="middle" %}
<figure><img src="../../.gitbook/assets/blender_XBIo7bSrvb.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

&#x20;

***

&#x20;&#x20;

### **Danger Zone** panel:

{% columns %}
{% column valign="middle" %}
Collapsed by default, and only present when **Show 'Danger Zone'** is on in Preferences.
{% endcolumn %}

{% column valign="middle" %}
<div align="center"><figure><img src="../../.gitbook/assets/blender_XRFLmw4V7O (1).png" alt=""><figcaption></figcaption></figure></div>
{% endcolumn %}
{% endcolumns %}

{% columns %}
{% column valign="middle" %}
**Clear This Rig**: Removes the selected rig and its baked camera, restores the original camera, leaves every other rig alone. Greyed out until a rig is selected.
{% endcolumn %}

{% column valign="middle" %}
<figure><img src="../../.gitbook/assets/blender_OeeFmeq8PT.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

{% columns %}
{% column valign="middle" %}
**Clear All Rigs**: Removes ALL AutoCam rigs; scene-wide.
{% endcolumn %}

{% column valign="middle" %}
<figure><img src="../../.gitbook/assets/blender_wrddTjiAb1.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

&#x20;

***

## User Preferences

Access AutoCam’s user preferences to change the default settings:\
**Edit** → **Preferences** → **Add-ons** → **AutoCam** → expand to see user preferences.

Preferences affect **new** rigs/paths you create; they don’t retroactively change existing ones.

{% hint style="success" %}
**Tip:**

*  **Show 'Danger Zone':** Shows or hides the destructive-tools panel.
* **Show Hints:** Hides the instructional text in the panels once you know the workflow. Warnings, errors, and computed values always stay visible.
* **Flythrough Controls:** Look sensitivity, move speed, fast multiplier, and rebindable movement keys with a one-click AZERTY (ZQSD) preset.
{% endhint %}

***

&#x20;

## Next steps

* **Learn each feature in depth** → [**Source**](source.md) **-** [**Path**](path.md) **-** [**Rig**](rig.md) **-** [**Output**](output.md)
* **See practical examples** → [**Guides**](../guides.md)
* **Having issues?** Start with [**Troubleshooting**](../../help/troubleshooting.md), check the [**FAQ**](../../help/faq.md), and contact [**Support**](../../help/support.md) if necessary.

&#x20;
