---
marp: true
---

# OpenAssetIO Working Group

### Meeting 3

March 17th 2022

## 🗒 Agenda

- Update on progress.
- A discussion on real-world stats for the use of asset management systems in production.
- Persistence of entity references in metadata such as XMP - @reinecke.
-  Questions/AOB.

---

## 🤚 Meeting guide

- Its a discussion - feel free to jump in with questions.
- Raise your hand if you can't get a word in edge-ways. 👀

---
---

## 📤 Recent work

- OpenTimelineIO PoC
- Improved data model
- Progress with `C++` migration.
- API performance testing

---

## 🎦 OpenTimelineIO PoC

https://github.com/TheFoundryVisionmongers/otio-openassetio

- Resolves an `ExternalReference` `target_url` via OpenAssetIO if it is an entity reference.
- Early days, much more to come.

---

## 🔩 Improved data model

- Switch from hierarchy to traits.
- Removes concept of a "primary string" - much more future proof.

---

## 🔩 Progress with C++ migration

- Implemented `Specification` and `Trait` classes.
- Next steps: "Minimal manager plugin".

---

## ⏱ Performance testing

- Need to ensure API overhead is not significant.
- Data model change could increase this.

```
 Queries: 100000
 Batch size: 1
 Wall-clock time (Total):
   resolveEntityReference: 43 ms
   resolve: 124 ms
 Wall-clock time (Per-call):
   resolveEntityReference: 0.00043ms
   resolve: 0.00124ms
 ```

Change to traits adds less than a tenth of a second when resolving one hundred thousand entities.

---

## 🗣 Discussion

- What volume of assets are present in typical 2D/3D tasks?
- Bottlenecks and Query latencies in AMS queries?
- Does all asset data live in one store, or is it distributed?
- Do you have optimized handling for filepaths specifically?

---

## 🗣 Discussion

- Persisting OpenAssetIO entity references in other metadata schemes like XMP?

---
---

## ❔ A.O.B / Questions?
