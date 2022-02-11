# February 10th 2022

[Meeting Recording](https://drive.google.com/file/d/1Q0z7iuUuF9rmiZ47B_gvp5cSjb5Hvrwu/view?usp=sharing)

Date/Time: 10th February 2022 @ 17:00 GMT


## Discussion Points and Recording Timings

* Recap of work since the last meeting: - [1:35](https://drive.google.com/file/d/1Q0z7iuUuF9rmiZ47B_gvp5cSjb5Hvrwu/view?t=95)
* Plugin test harness - call for input: [3:54](https://drive.google.com/file/d/1Q0z7iuUuF9rmiZ47B_gvp5cSjb5Hvrwu/view?t=234)
* Specifications (our hierarchical type system) - call for input: [9:15](https://drive.google.com/file/d/1Q0z7iuUuF9rmiZ47B_gvp5cSjb5Hvrwu/view?t=555)
* AOB: [39:58](https://drive.google.com/file/d/1Q0z7iuUuF9rmiZ47B_gvp5cSjb5Hvrwu/view?t=2398)


## Background Reading

 - Manager test harness [Issue](https://github.com/TheFoundryVisionmongers/OpenAssetIO/issues/95) and [working branch](https://github.com/TheFoundryVisionmongers/OpenAssetIO/tree/feature/96-exampleManager)
 - [Specifications](https://thefoundryvisionmongers.github.io/OpenAssetIO/entities_specifications_and_attributes.html), and how they fit into the system.

## Notes

[see slides](https://github.com/TheFoundryVisionmongers/OpenAssetIO-WG/blob/master/meetings/2022-02-10/Slides-for-Working-Group-002-2022-02-10.md)

Recap of work since the last meeting:
* C, C++, Python strategy decided: C++ but with C as a first class citizen
* String handling approach (UTF-8).

Plugin test harness - call for input
* Quick overview of the system
* What coverage would be most valuable to someone developing a manager plugin?
* There is a public API around test harness, easy to write specific tests that you want to write.

Specifications (our hierarchical type system) - call for input
* Quick overview of what they are/how they work.
* What kind of types would you expect in the core API?
* How to build an extensible system used through C/C++?
* Prior art in this space - usdGenSchema, OTIO SchemaDef, others?
* Action: Sketch out current workflows we understand. Modelling these will help aid the discussion next time

AOB: 
* Suggestions for improvement: Provide more context and realistic examples
* OpenTimelineIO Media Linker is an upcoming example we could discuss
* Investigate BindGen. It takes C++ Bindings and converts to C and Rust. 
* Reach out to rust wg and Scott with any questions
