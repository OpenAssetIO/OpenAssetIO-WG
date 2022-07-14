---
marp: true
---

# OpenAssetIO Working Group

### Meeting 4

May 19th 2022

## 🗒 Agenda

- New GitHub Org, ASWF
- Entity Traits
- Published Packages
- Questions/AOB

---

## 🤚 Meeting guide

- Its a discussion - feel free to jump in with questions.
- Raise your hand if you can't get a word in edge-ways. 👀

---

## 📤 Recent work

- Move to traits nearly complete merge to `main` soon.
- Minimal Manager now possible in `C`.
- `ext-openassetio` Slack channel open to all (Foundry org).

---

## 🏡 Project home

https://github.com/OpenAssetIO

- Moved repositories from `TheFoundryVisionmongers` org to `OpenAssetIO`.
- Applied to ASWF to join the new Sandbox phase:
  - Vote penciled in for June 1 TAC meeting.
  - Could then move Slack to ASWF org to reduce friction.

---

## 🔩 Entity Traits

- https://github.com/OpenAssetIO/OpenAssetIO-MediaCreation
- A working space for collaboration on defining traits for digital media.
- 🗣 PYPE.club collaboration.
- 🗣 MovieLabs ontology collaboration.
- *Q: How do we make progress here - its not an easy task?*

---

## 🔩 Entity Traits

```
trait blob {
    properties: { url: { type: str, desc: "A Valid RFC 3986 URL" } }
}

trait image {
    properties: { colorSpace: { type: str, doc: "OCIO Colorspace name" } }
}

specification image {
    traits: { blob, image }
}
```

- We want to auto-generate the `C`, `C++` and `Python` boilerplate.
- Currently thinking JSON schemas?
- *Q: Recommendations for tool chains for variable structures?*

---

## 🔩 Packages and publishing

- OpenAssetIO will be `C`/`C++` libs + `Python` package (bound libs).
- Currently envisioning `PyPi` and `ConanCenter` releases.
- *Q: What is a useful distribution form for you, and requests?*
- *Q: How urgent are these vs building your own as needed?*
- *Q: Any tips? (We currently rely on Python for majority of C++ test coverage)*

---

## ❔ A.O.B / Questions?
