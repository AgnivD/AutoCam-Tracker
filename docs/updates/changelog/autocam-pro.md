# AutoCam Pro

Release notes for the **AutoCam Pro** line.

{% hint style="info" %}
AutoCam Pro versions are their own line, separate from AutoCam Free 2.x. This release is built on the shared core of **AutoCam Free 2.1.1** - see the [**Free changelog**](autocam-free.md) for everything in that core, including the rig's renamed aim controls (the target you drag is **Aim**; the pivot behind it is **Gimbal**).
{% endhint %}

***

### 1.0.0 \[Latest Release] <mark style="color:$info;">— 2026-08-04</mark>

First release of AutoCam Pro.

#### Added

* **Inherit Original Speed:** One click preserves the source camera's pacing -\
  pauses, accelerations - on the generated rig; Clear restores your keys.
* **Lock to Target:** Aim the camera at any object in the scene and swap\
  targets live - no rebuild, and animated targets stay tracked.
* **Path Lookahead:** Aim a set distance ahead along the path so the camera\
  steers smoothly through corners, easing out at the path's end.
* **Smart Auto-Aim:** Derive the camera's aim from your recording - surface\
  raycast or focal distance projection, with smoothing and simplify controls.
* **Realtime Path Steering:** Play the shot and bend the path live from the\
  keyboard: proportional falloff around the playhead, hold-to-smooth and\
  hold-to-straighten tools, and the whole session lands as one undo step.
* **Loop:** Close the path into a seamless cycle with a shaped seam (concave\
  to seamless), and repeat laps for endlessly looping moves.
* **Segments:** Chain multiple curves into one camera move with hard cuts,\
  per-segment repeat laps, and color-coded viewport overlays.
* **Camera Morph:** Declare camera poses and let AutoCam build the move\
  through them - marker timing, even or by-distance distribution, and\
  lens/DOF morphing between poses.
* **Pipeline:** Every rig in the scene in one list. Jump between stages from\
  each row's strip - reverts restore exactly what they took when you climb\
  back - plus double-click rename, per-rig delete, and batch bake.
* **Batch Bake:** Bake every rig in the scene in one click, with optional\
  per-rig setting overrides.
* **Export:** Hand a baked camera to other DCCs as Alembic, USD, or FBX -\
  scoped to just the camera, with the bake's own frame range.
* **Path Lookahead as a default:** Preferences → Rig Defaults → Tracking\
  offers it alongside Manual Aim and Match Recording, so a rig can be built\
  already aiming down its path. It is the only Pro aim mode that can be a\
  default - Lock to Target needs a target object and Smart Auto-Aim needs a\
  recording to resample, and neither exists at the moment a rig is built.
* **Priority support** for Pro customers through the store you purchased from.

#### Notes

* The flythrough movement keys also drive **Path Steering**, which the\
  Flythrough Controls box in Preferences now says out loud.
* AutoCam Pro and AutoCam Free **cannot be installed at the same time**.\
  They provide the same panels and operators. See\
  [**Installation**](../../welcome/installation.md).

#### Known limitations in 1.0.0

* Segment transitions are **hard cuts only** - no blended hand-offs.
* **Smart Auto-Aim** needs **Resample Scene** after scene geometry moves; it\
  does not live-track objects (that is Lock to Target's job).
* **Match Recording** and **Smart Auto-Aim** hold their last pose on added\
  segments.
* **Batch export** is not included - exports are one camera at a time.
* **Path Steering** requires an actual 3D Viewport in the screen layout.

***

### **Next steps**

* See what Pro adds over Free → [**Editions**](../../welcome/editions.md)
* Learn each feature → [**Features**](../../learn/features/)
* See the public [**Roadmap**](../roadmap.md) for what's planned.
* Got ideas or feedback? Open an issue in the [**GitHub Tracker**](https://github.com/AgnivD/AutoCam-Tracker/issues/new/choose).
