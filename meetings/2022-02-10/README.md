# February 10th 2022

Date/Time: 10th February 2022 @ 17:00 GMT

Join: [Zoom link](https://thefoundry.zoom.us/j/97582912679)

This meeting will start with a quick recap of work since the last
meeting. We would then love to get atendees input on the topic of the
plugin test harness and how best to expose our extendable type system to
compiled languages.

## Discussion Points

- Recap of work since the last meeting:
  - `C`, `C++`, `Python` strategy decided.
  - String handling approach (UTF-8).

- Plugin test harness - call for input:
  - Quick overview of the system
  - What coverage would be most valuable to someone developing a manager
	plugin?

- Specifications (our hierarchical type system) - call for input:
  - Quick overview of what they are/how they work.
  - What kind of types would you expect in the core API?
  - How to build an extensible system used through `C`/`C++`?
  - Prior art in this space - `usdGenSchema`, OTIO `SchemaDef`, others?

- A.O.B?


## Background Reading

 - Manager test harness [Issue](https://github.com/TheFoundryVisionmongers/OpenAssetIO/issues/95) and [working branch](https://github.com/TheFoundryVisionmongers/OpenAssetIO/tree/feature/96-exampleManager)
 - [Specifications](https://thefoundryvisionmongers.github.io/OpenAssetIO/entities_specifications_and_attributes.html), and how they fit into the system.
