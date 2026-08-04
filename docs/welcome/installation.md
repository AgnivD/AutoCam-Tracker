---
icon: gear
---

# Installation

AutoCam is compatible with **Blender 4.2+** across Windows, macOS, and Linux. It is developed and tested on **Blender 5.2 LTS**.

{% hint style="warning" %}
Don't unzip the download. You'll install the `.zip` directly.
{% endhint %}

***

#### Before you start: pick one edition

AutoCam Free and AutoCam Pro **cannot run side by side**. They register the same panels and the same operators, so Blender cannot host both. Whichever you install, make sure the other one is removed first.

| Edition                                                            | File to download         | Where from                                                                                                                       |
| ------------------------------------------------------------------ | ------------------------ | -------------------------------------------------------------------------------------------------------------------------------- |
| **AutoCam Free 2.1.1**                                             | `AutoCam_Free_2-1-1.zip` | [Extensions Platform](https://extensions.blender.org/add-ons/autocam/) (or [Gumroad](https://renderrides.gumroad.com/l/autocam)) |
| **AutoCam Pro 1.0.0** <mark style="color:$warning;">**PRO**</mark> | `AutoCam_Pro_1-0-0.zip`  | [Gumroad](https://renderrides.gumroad.com/l/autocam) · [Superhive](https://superhivemarket.com/products/autocam)                 |

Not sure which you want? See [**Editions**](editions.md).

***

#### Option A: Install as an Extension <mark style="color:$info;">(Blender 4.2+)</mark>

1. **Download** the addon `.zip` file.
2. In Blender:\
   **Edit** → **Preferences** → **Get Extensions** → **Install from Disk**.
3. Select the ZIP file → **Install from Disk**.
4. Enable the extension - it appears as **AutoCam Free** or **AutoCam Pro** in the list.
5. Access AutoCam user preferences from the **Add-ons** menu.
6. Save & close Preferences → in 3D View press **N** → open the **AutoCam** tab.

{% hint style="success" %}
**Tip:** AutoCam **Free** can be installed without downloading anything - search for it directly inside the **Get Extensions** panel (requires internet access). AutoCam **Pro** is a ZIP install from your store account.
{% endhint %}

***

#### Option B: Updating from an older version

**Extensions:**

1. Remove the previous version:\
   **Edit** → **Preferences** → **Get Extensions** → **AutoCam Free** (or **AutoCam Pro**) → **Uninstall.**
2. Restart Blender (important).
3. Follow the installation steps in [Option A](installation.md#option-a-install-as-an-extension-blender-4.2) to reinstall.

{% hint style="success" %}
**Tip:** If you installed AutoCam using the **Blender Extensions Platform** (_Search Extensions_), you can update it by navigating to **Get Extensions** → **AutoCam Free** → **Update** (requires internet access).
{% endhint %}

{% hint style="info" %}
**Coming from 2.1.0 or earlier?** The Free extension was called just "AutoCam" before 2.1.1; the entry in your add-ons list may still read that way until you reinstall. It is the same extension and it updates in place - the sidebar tab is still **AutoCam**.
{% endhint %}

***

#### Option C: Switching between Free and Pro

Because the two editions cannot coexist, switching is an uninstall followed by an install. Your scenes are unaffected - rigs, paths, and bakes are stored in the `.blend`, not in the add-on.

{% stepper %}
{% step %}
**Save your `.blend`** and close it, or start from a fresh file.
{% endstep %}

{% step %}
**Edit** → **Preferences** → **Get Extensions** → find the installed edition → **Uninstall**.
{% endstep %}

{% step %}
**Restart Blender.** This step is not optional - Blender keeps the old module registered until it restarts, and installing the other edition on top of it will fail or double-register the panels.
{% endstep %}

{% step %}
Install the other edition's ZIP via [Option A](installation.md#option-a-install-as-an-extension-blender-4.2), then reopen your file.
{% endstep %}
{% endstepper %}

{% hint style="warning" %}
**Going Pro → Free?** Rigs that use Pro-only features (Loop, Segments, Camera Morph) lose the panels that edit them. **Bake first** if you need the shot to stay editable - a baked camera is plain keyframes and works with AutoCam removed entirely. See [**Output**](../learn/features/output.md).
{% endhint %}

***

#### Verify the install

Open **Edit** → **Preferences** → **Add-ons** → **AutoCam** → **About**. It names the edition and version you're running. If that reads what you expect, you're done.

***

#### Next steps

* **New to AutoCam?** Follow the [**Quick Start**](quick-start.md)**.**
* **Comparing editions?** See [**Editions**](editions.md)**.**
* **Ready to learn more?** Read [**Features**](../learn/features/) & [**Guides**](../learn/guides.md)**.**
* **Having issues?** Start with [**Troubleshooting**](../help/troubleshooting.md), check the [**FAQ**](../help/faq.md), and contact [**Support**](../help/support.md) if necessary.
