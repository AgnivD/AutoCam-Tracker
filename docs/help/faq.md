---
icon: messages-question
---

# FAQ

Most common questions were resolved in **AutoCam 2.0**. Below are the ones that come up after the 2.1 update.

#### - Where did Dynamic mode and the Speed slider go?

**Both were removed in 2.1.** Simple keyframed motion is now the single motion model, and timing is authored by keyframing the **Progress** slider on the Rig panel: 0 at the start of the path, 1 at the end.

Anything Speed did, Progress does more directly: Hold a value to pause, drop it to run backwards, and drag the last key to change how long the move takes. **Sync Speed to Keys** is gone too; you now set the end frame by moving the key itself.

#### - I opened a 2.0 file and the camera's pacing changed. Why?

Rigs built in 2.0.x are migrated automatically the first time you open them in 2.1. Simple rigs carry over unchanged. **Dynamic** rigs are converted to an even-paced traversal of their original frame range. The path and the frame range are preserved, but the performed speed-ups and slow-downs of live Dynamic playback are not.

Re-key the **Progress** slider to restore custom pacing. If you need a Dynamic rig exactly as it was, keep a copy of your 2.0.6 build and the `.blend` before upgrading.

#### - Blender crashed while rendering on 5.x. Is that fixed?

Yes, in 2.1. Versions up to 2.0.6 ran a per-frame handler inside Blender's render job that could crash Blender with an access violation. That handler no longer exists, and any copy left behind by an older install is removed on start-up. **Update to 2.1.**

***

#### **For now:**

* Quick fixes live on [each feature page](../learn/features/) under [**Common issues**](../learn/features/source.md#common-issues-and-quick-fixes).
* If you're stuck, check [**Troubleshooting**](troubleshooting.md) or contact [**Support**](support.md).

&#x20;&#x20;

***

### **Have a question?**

Send it via [**Support**](support.md). We’ll answer and add it here.

&#x20;&#x20;
