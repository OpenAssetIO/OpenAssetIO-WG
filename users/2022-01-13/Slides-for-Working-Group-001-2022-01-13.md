---
marp: true
---

# OpenAssetIO Working Group

### Meeting 1

January 13th 2022

## 🗒 Agenda

- Project overview
- Progress update / Upcoming milestones
- CMake
- C++/Python memory management
- C-based language bindings
- CY2022?

---

## 🤚 Meeting guide

- It should be a discussion - feel free to jump in with questions
- Raise your hand if you can't get a word in edge-ways 👀
- Side-bar longer discussions

---

---

## 🌍 Project overview: origin

- Started cira 2011 when investigating editorial workflows
- Asset Management Systems are an every day part of M&E workflows
- No known existing standard to talk to them
- Facilities shouldn't have to re-code integrations to a new API for each tool

---

## 🥅 Project overview: goals

1. Reduce pipeline integration pain and maintenance overhead
2. Allow DCC tools to design and develop first-class, asset-centric workflows
3. Open source, license free, cross-vendor solution

---

## 📦 Project overview: scope

- Resolution of asset references (URIs) into locatable data (URLs or k/v pairs)
- Publishing of new assets/versions
- Asset relationships
- Replacement/augmentation of in-application UI elements

---

## 🚫 Project overview: scope

By design, OpenAssetIO does not:
 
- Define any standardized data structures for the storage or description of assets or asset hierarchies
- Dictate any aspect of how an asset management system operates, organizes, locates or manages asset data and versions.

---

## 📍 Project overview: resources

http://github.com/TheFoundryVisionmongers/OpenAssetIO

---

---

## ⏳ Progress update

- API design validated through
  - End-to-end workflow prototypes
  - Peer feedback across the industry
- Prototype is pure python implementation
- All development/planning moved to public repository
  - Source code
  - Documentation
  - Issues
  - Discussions (Discord, ASWF Slack?)

---

## 🚧 Upcoming milestones

- C++ core migration
- Sample manager plugin
- Test harness for validating host and manager implementations
- API stability
  - No major changes expected
  - Addressing industry feedback
  - Addressing some questionable past life-choices

---

---

## 🔧 Library build

- `CMake` default variables or custom?

## 🤞 CY2022?

- Python 3.7+
- C++ 17

---

## 🐍 C++/Python memory management topics

- `OpenTimelineIO`/`TfPy`

## 🔩 C-based language bindings

- Target languages
- Best practices to avoid pain later

---

## ❔ A.O.B / Questions?