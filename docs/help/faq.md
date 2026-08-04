---
icon: messages-question
---

# FAQ

Questions that come up most often, grouped by topic.

***

### Editions

**- What's the difference between AutoCam Free and AutoCam Pro?**

Free gives you the whole Record → Path → Rig → Output workflow. Pro adds Camera Morph, Realtime Path Steering, Loop, Segments, three extra tracking modes (Lock to Target, Path Lookahead, Smart Auto-Aim), Inherit Original Speed, the Pipeline hub, batch baking, and Alembic/USD/FBX export.

Full side-by-side on the [**Editions**](../welcome/editions.md) page.

**- Which edition am I running?**

**Edit** → **Preferences** → **Add-ons** → **AutoCam** → **About**. It names the edition and version - _AutoCam Free 2.1.1_ or _AutoCam Pro 1.0.0_.

**- Can I install Free and Pro at the same time?**

**No.** They register the same panels and the same operators, so Blender cannot host both. Remove one, restart Blender, then install the other. See [**Installation**](../welcome/installation.md).

**- Why is Pro version 1.0.0 when Free is on 2.1.1?**

They're separate version lines. AutoCam Pro started its own numbering at 1.0.0; it isn't a continuation of Free's 2.x. Pro 1.0.0 is built on the shared core of Free 2.1.1, which is why the two changelogs cross-reference each other.

**- Do Free users see locked or greyed-out Pro features?**

No. The Pro code isn't shipped in the Free build at all, so Pro-only tracking modes simply aren't in the dropdown and the Loop / Steering / Segments / Batch / Export tabs don't exist. There are no upsell prompts in the panels.

**- If I buy Pro, do I lose my existing work?**

No. Rigs, paths, curve edits, Progress keyframes, tracking settings and baked cameras all live in the `.blend`, not in the add-on. Pro reads them unchanged.

**- Can I open a Pro file in Free?**

The scene opens, but rigs built with Pro-only features (Loop, Segments, Camera Morph) lose the panels that edit them. **Bake before you share** - a baked camera is plain keyframes and plays back with AutoCam removed entirely.

**- Is Pro a subscription?**

No. It's a one-time purchase through [Gumroad](https://renderrides.gumroad.com/l/autocam) or [Superhive](https://superhivemarket.com/products/autocam), and it includes updates and priority support through the store you bought it from. Both editions are GPL-3.0-or-later.

***

### The 2.1.1 update

**- Where did the LookAt object go?**

It's called **Aim** now. And the pivot that used to be called "Aim" is now called **Gimbal**.

The old names were backwards in practice: testers kept dragging the pivot, because it was the one labelled "Aim" - but moving it booms the camera off the dolly rather than changing what the camera points at. The names now match what each object does.

Rigs built in 2.1.0 or earlier keep their old names and keep working; AutoCam recognises both layouts. Rebuild with **Generate Rig** to adopt the new names and shapes.

**- Why can't I see the Gimbal in the viewport?**

It isn't drawn on purpose. It shares a spot with the Dolly and the camera, and a third marker there only ever gave you a wrong thing to grab.

It is still a real, selectable control - pick it from the **Outliner**. Nudging the Gimbal is how you boom the camera off its path while keeping the aim exact, because the Track To is computed from its origin. See [**Rig**](../learn/features/rig.md).

**- The rig handles suddenly got much bigger. Why?**

They're roughly five times their old size, and that's deliberate. The old sizes were inherited constants nobody had measured - in Blender's own default scene they put the Dolly at 1.5% of the shot's size, which reads as dust.

Handles are now sized against the path, and the sizing holds up to kilometre-long paths. If it's wrong for your scene, **Rig Scale** in **Preferences → Viewport** dials it.

**- Where did Show Path Direction go?**

**Preferences → Viewport**. It's a viewport display choice, and the Rig panel is for things that change the shot. Note that it's now **global** rather than per-rig - if you were toggling it per rig, that distinction is gone.

**- Why won't Apply Walk Keys do anything?**

Two flythrough directions are bound to the same key. Walk navigation needs one key per direction - the press starts the move and the release stops it - so a shared key leaves movement that starts and never stops. Preferences names the clash in red, and Apply refuses until you resolve it.

***

### The 2.1 update

**- Where did Dynamic mode and the Speed slider go?**

**Both were removed in 2.1.** Simple keyframed motion is now the single motion model, and timing is authored by keyframing the **Progress** slider on the Rig panel: 0 at the start of the path, 1 at the end.

Anything Speed did, Progress does more directly: Hold a value to pause, drop it to run backwards, and drag the last key to change how long the move takes. **Sync Speed to Keys** is gone too; you now set the end frame by moving the key itself.

**- I opened a 2.0 file and the camera's pacing changed. Why?**

Rigs built in 2.0.x are migrated automatically the first time you open them in 2.1. Simple rigs carry over unchanged. **Dynamic** rigs are converted to an even-paced traversal of their original frame range. The path and the frame range are preserved, but the performed speed-ups and slow-downs of live Dynamic playback are not.

Re-key the **Progress** slider to restore custom pacing. If you need a Dynamic rig exactly as it was, keep a copy of your 2.0.6 build and the `.blend` before upgrading.

**- Blender crashed while rendering on 5.x. Is that fixed?**

Yes, in 2.1. Versions up to 2.0.6 ran a per-frame handler inside Blender's render job that could crash Blender with an access violation. That handler no longer exists, and any copy left behind by an older install is removed on start-up. **Update to 2.1 or later.**

***

**For now:**

* Quick fixes live on each feature page under **Common issues**.
* If you're stuck, check [**Troubleshooting**](troubleshooting.md) or contact [**Support**](support.md).

***

#### **Have a question?**

Send it via [**Support**](support.md). We'll answer and add it here.

&#x20;&#x20;
