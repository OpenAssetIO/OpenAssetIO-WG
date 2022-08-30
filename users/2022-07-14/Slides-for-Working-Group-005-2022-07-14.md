---
marp: true
---

# OpenAssetIO Working Group

### Meeting 5

July 14th 2022

## 🗒 Agenda

- ASWF Sandbox phase adoption
- Q3 Goals
- Progress update
- Questions/AOB

---

## 🤚 Meeting guide

- Its a discussion - feel free to jump in with questions
- Raise your hand if you can't get a word in edge-ways 👀

---

## 🏡 ASWF Sandbox phase adoption

- We're now part of the ASWF as a Sandbox project
- `#openassetio` Slack channel, mailing lists to follow
- Getting project organisation setup, formation of TAC
- Repos staying in OpenAssetIO GitHub org for now

---

## 🥅 Y22Q3 goals

Initial alpha release:
  https://github.com/OpenAssetIO/OpenAssetIO/milestone/4

- Incomplete API, but structurally stable
- Limited to `resolve` + `preflight`/`register`
- Python: Host or Manager
- C++: Host
- VFX Platform: CY2022

PS. We are hiring! Come help us.

---

---

## 🔩 Progress: Specification/Trait code generation

- Specifications/Traits are how we describe an asset and it's data.

- YAML + JSONSchema validation
- Python module + CLI to generate code
- Generated languages: Python, C++ (for now, will extend)
- Will switch OpenAssetIO-MediaCreation over soon

---

## 🔩 Progress: Specification/Trait code generation

```yaml
package: openassetio-mediacreation

description:
 Traits and Specifications for use in media creation.

traits:
    data:
        description: >
           Traits that describe how to access an entitys data.
        members:
            LocatableContent:
                description: >
                     This trait characterizes an entity whose data is
                     persisted externally to the API through data
                     accessible via a valid URL.
                properties:
                    location:
                        type: string
                        description: The URL of the entities content.
                usage:
                    - entity
```

---

## 🔩 Progress: Specification/Trait code generation

```yaml
specifications:
    managementPolicy:
        description: >
            Specifications that declare common entity management
            policies for media creation tools.
        members:
            ManagedWithThumbnail:
                description: >
                    A specification that declares an entity is managed
                    and the manager desires a thumbnail to be made by
                    the host during publishing.
                usage:
                    - managementPolicy
                traitSet:
                    - package: openassetio
                      namespace: managementPolicy
                      name: Managed

                    - namespace: managementPolicy
                      name: WantsThumbnail
```

---

---

## 🔩 Progress: C++ API signatures

- Batch methods will use callbacks

```cpp
using SuccessCallback = std::function<void(std::size_t, TraitsDataPtr)>;
using ErrorCallback = std::function<void(std::size_t, ErrorCodeAndMessage)>;

void resolve(
             // Inputs
             const std::vector<EntityRef>& entityRefs,
             const TraitsData::TraitSet& traitSet,
             const ContextPtr& context,
             const HostSessionPtr& hostSession,
             // Result callbacks
             const SuccessCallback& successCallback,
             const ErrorCallback& errorCallback);
```

- Can be wrapped to emulate other interfaces
- Avoids complex result types for value or error
- Proved be generally slightly faster than return vector

---

## 🔩 Progress: Pybind shenanigans

- Inheritance slicing(?!)
- The core OpenAssetIO API classes need to be inheritable in python 🤯
- The Python specialisation gets deleted when only C++ has a ref
- Think we have a workaround:

https://github.com/pybind/pybind11/issues/1333#issuecomment-1183537856

---

## ❔ Questions / A.O.B
