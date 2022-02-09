---
marp: true
---

# OpenAssetIO Working Group

### Meeting 2

February 10th 2022

## 🗒 Agenda

- Recap of work since the last meeting
- Plugin test harness
- Specifications (our type system)

---

## 🤚 Meeting guide

- Its a discussion - feel free to jump in with questions
- Raise your hand if you can't get a word in edge-ways 👀
- Side-bar longer discussions

---
---

## 📤 Recent work

- C/C++/Python strategy - DR004 + `feature/181-coreCppBuild`
- String encoding (https://utf8everywhere.org)
- Minimal sample manager and test harness

---

## 🧪 Test harness

https://github.com/TheFoundryVisionmongers/OpenAssetIO/issues/95

🐓🥚

How can you test your manager plugin works?
How do you know if you've implemented the `HostInterface` correctly?

---

```
python -m openassetio.test.manager \
  -f resources/examples/manager/SampleAssetManager/fixtures.py
```

A modular test framework for TDD'ing a `ManagerPlugin` (and later `HostInterface`)

 "have I followed the API contract?"

- ✅ API method fuzzing, canonical publishing workflows
- ❌ Manager-specific responses/business logic checking

### Discussion

- Is this the right balance?
- What else should the harness cover?

---
---

## 🔩 Specifications

- Hierarchical type system for entities (and more)
- Think "glorified mime type"

Used to:

- Describe the "type" of an entity
- Filter browsing and query APIs
- Describe the calling context (with a lowercase 'c')

---

Current core library specifications, used to type-check API methods:

- `EntitySpecification` e.g file, image, shot, etc...
- `RelationshipSpecification`  e.g. parent grouping, pipeline step
- `LocaleSpeciciation` e.g. node in graph, timeline, file menu

### Discussion

Specifications are run-time extensible, what would you like to see in
a "Media & Entertainment specifications" library?

---

## 🔩 Specifications API

- Design goals:
  - Hierarchical (to support upcasting to known types)
  - Decomposable (to simple data types for interop/serialisation)
  - Robust (compile-time checks for programming errors)
  - Discoverable (runtime introspection/help)
  - Out of core (definable by integrations/managers)

---

"schema" + key/value pairs:
```
entity:file.image.texture, { channels: 1 }
```

https://thefoundryvisionmongers.github.io/OpenAssetIO/entities_specifications_and_attributes.html

Looks familiar? USD Prims, OTIO Metadata, Katana Locations, others???

---

- We have a fully working implementation in Python (with some `metaclass` magic)
- We need to port this to `C`/`C++` core API, is the class-based approach sane?


### Discussion
- What similar mechanisms do people know about?
- What is people's experience with the `usdSchemaGen` mechanism or similar mechanisms?

---
---

## ❔ A.O.B / Questions?