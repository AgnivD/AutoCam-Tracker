---
icon: code-fork
---

# Editions

AutoCam comes in two editions built on the same core: **AutoCam Free** and **AutoCam Pro**.

They share the same sidebar, the same four stages, and the same rig. Pro adds tools on top of that foundation - it does not change how the foundation works, and a shot built in Free opens in Pro unchanged.

{% hint style="warning" %}
**The two editions cannot be installed at the same time.** They register the same panels and operators. Remove one, restart Blender, then install the other. See [**Installation**](installation.md).
{% endhint %}

***

### Which one am I running?

**Edit** → **Preferences** → **Add-ons** → **AutoCam** → **About**.

The About box names the edition and the version - _AutoCam Free 2.1.1_ or _AutoCam Pro 1.0.0_ - alongside links to these docs, the website, and support. Blender's own add-on list shows the same name.

{% hint style="info" %}
**Version lines are separate.** AutoCam Pro is its own line starting at **1.0.0**; it is not a continuation of Free's 2.x numbering. Pro 1.0.0 is built on the shared core of Free 2.1.1. Both lines are tracked on the [**Changelog**](../updates/changelog/).
{% endhint %}

***

### Feature comparison

<table><thead><tr><th width="270">Feature</th><th width="105" align="center">Free</th><th align="center">Pro</th></tr></thead><tbody><tr><td><strong>Source</strong></td><td align="center"></td><td align="center"></td></tr><tr><td>Record Flythrough</td><td align="center">✅</td><td align="center">✅</td></tr><tr><td>Customizable flythrough controls</td><td align="center">✅</td><td align="center">✅</td></tr><tr><td>Camera Morph (build a move from declared poses)</td><td align="center">—</td><td align="center">✅</td></tr><tr><td><strong>Path</strong></td><td align="center"></td><td align="center"></td></tr><tr><td>Path extraction (Bezier / Poly / NURBS)</td><td align="center">✅</td><td align="center">✅</td></tr><tr><td>Tolerance simplification + Edit Mode reshaping</td><td align="center">✅</td><td align="center">✅</td></tr><tr><td>Loop (seamless cyclic paths, shaped seam)</td><td align="center">—</td><td align="center">✅</td></tr><tr><td>Realtime Path Steering</td><td align="center">—</td><td align="center">✅</td></tr><tr><td><strong>Rig</strong></td><td align="center"></td><td align="center"></td></tr><tr><td>One-click rig + keyframable Progress</td><td align="center">✅</td><td align="center">✅</td></tr><tr><td>Tracking: Manual Aim</td><td align="center">✅</td><td align="center">✅</td></tr><tr><td>Tracking: Match Recording</td><td align="center">✅</td><td align="center">✅</td></tr><tr><td>Tracking: Lock to Target</td><td align="center">—</td><td align="center">✅</td></tr><tr><td>Tracking: Path Lookahead</td><td align="center">—</td><td align="center">✅</td></tr><tr><td>Tracking: Smart Auto-Aim</td><td align="center">—</td><td align="center">✅</td></tr><tr><td>Inherit Original Speed</td><td align="center">—</td><td align="center">✅</td></tr><tr><td>Segments (chain multiple curves)</td><td align="center">—</td><td align="center">✅</td></tr><tr><td><strong>Output</strong></td><td align="center"></td><td align="center"></td></tr><tr><td>Bake to keyframes / Re-Bake</td><td align="center">✅</td><td align="center">✅</td></tr><tr><td>Batch bake, with per-rig setting overrides</td><td align="center">—</td><td align="center">✅</td></tr><tr><td>Export to Alembic / USD / FBX</td><td align="center">—</td><td align="center">✅</td></tr><tr><td><strong>Workspace</strong></td><td align="center"></td><td align="center"></td></tr><tr><td>Stage breadcrumb</td><td align="center">✅</td><td align="center">✅</td></tr><tr><td>Multiple rigs per scene</td><td align="center">✅</td><td align="center">✅</td></tr><tr><td>Pipeline hub (rig list, stage revert &#x26; restore, rename)</td><td align="center">—</td><td align="center">✅</td></tr><tr><td>Clear This Rig / Clear All Rigs</td><td align="center">✅</td><td align="center">✅</td></tr><tr><td><strong>Support</strong></td><td align="center"></td><td align="center"></td></tr><tr><td>Community support (Discord, GitHub Tracker)</td><td align="center">✅</td><td align="center">✅</td></tr><tr><td>Priority email support</td><td align="center">—</td><td align="center">✅</td></tr></tbody></table>

***

### What Free users actually see

Pro features are **absent** from a Free install, not locked. The Pro code is not shipped in the Free build, so:

* Pro-only tracking modes are simply **not in the Mode dropdown**.
* The Loop, Steering, Segments, Batch, and Export tabs **do not exist**.
* There are no "(Pro)" labels, upgrade prompts, or disabled buttons anywhere in the panels.

If you are following a guide and a control isn't where it should be, check the About box - you're probably on Free, and the feature will be marked <mark style="color:$warning;">**PRO**</mark> in these docs.

***

### Moving from Free to Pro

Your work comes with you. Rigs, paths, curve edits, Progress keyframes, tracking settings, and baked cameras all carry over - Pro reads the same scene data.

1. Save your `.blend`.
2. **Edit** → **Preferences** → **Get Extensions** → **AutoCam Free** → **Uninstall**.
3. **Restart Blender** (important).
4. Install `AutoCam_Pro_1-0-0.zip` and enable **AutoCam Pro**.

Full steps on the [**Installation**](installation.md) page.

{% hint style="info" %}
**Going the other way?** A rig built with Pro-only features (Loop, Segments, Camera Morph) will not be editable in Free - those panels aren't there to edit them with. [**Bake**](../learn/features/output.md#bake-the-rig) before you hand a file to someone on Free: a baked camera is plain keyframes and works everywhere, even with AutoCam disabled entirely.
{% endhint %}

***

### Where to get each

| Edition          | Where                                                                                                                                 |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| **AutoCam Free** | [Blender Extensions Platform](https://extensions.blender.org/add-ons/autocam/) · [Gumroad](https://renderrides.gumroad.com/l/autocam) |
| **AutoCam Pro**  | [Gumroad](https://renderrides.gumroad.com/l/autocam) · [Superhive](https://superhivemarket.com/products/autocam)                      |

Both editions are free software under the **GPL-3.0-or-later** license. Purchasing Pro funds continued development and includes updates and priority support through the store you bought it from.

***

### Next steps

* **Install it** → [**Installation**](installation.md)
* **Get moving in 60 seconds** → [**Quick Start**](quick-start.md)
* **See what's in each panel** → [**Features**](../learn/features/)
