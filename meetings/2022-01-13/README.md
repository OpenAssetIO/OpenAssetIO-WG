# January 13th 2022

[Meeting Recording](https://drive.google.com/file/d/1rIGuFN1VJd_t0UPIoDU0_pPDka7SCx8X/view?usp=sharing)

Date/Time: 13th January 2022 @ 17:00 GMT

## Discussion Points and Recording Timings

* Quick overview for new faces - [0:00](https://drive.google.com/file/d/1rIGuFN1VJd_t0UPIoDU0_pPDka7SCx8X/view?t=0)
* Progress update - [9:25](https://drive.google.com/file/d/1rIGuFN1VJd_t0UPIoDU0_pPDka7SCx8X/view?t=565)
* Upcoming Milestones - [14:58](https://drive.google.com/file/d/1rIGuFN1VJd_t0UPIoDU0_pPDka7SCx8X/view?t=898)
* CY22 or later? - [19:43](https://drive.google.com/file/d/1rIGuFN1VJd_t0UPIoDU0_pPDka7SCx8X/view?t=1183)
* C++/Python bindings and memory management - [25:22](https://drive.google.com/file/d/1rIGuFN1VJd_t0UPIoDU0_pPDka7SCx8X/view?t=1522)
* Considerations when binding to other languages (Nick Porcino) - [27:10](https://drive.google.com/file/d/1rIGuFN1VJd_t0UPIoDU0_pPDka7SCx8X/view?t=1630)

## Notes

Overview of where we are with project (see slides)

Q: Does it contain a resolver?<br>
* No - just specifies how information should be shared

Discussion: Where should communication take place?
* Slack & Discord not open, the more open the better, 
* Conclusion: Discussion on the repo is probably best but it also depends on the type of thing that people need/want to post.

Q: Is there a plan to move to ASWF?
* Plan to move officially to ASWF at some point, currently just with Foundry

CMake Discussion
* Recommend always working default variables rather than custom otherwise huge overheads supporting customers 

CY2022/Python Discussion
* Happy with CY2022 only
* Please not Python 2 - that is going backwards
* 3.9 is the only python version that reliably works on Windows

Nick presentation on OTIO difficulties with languages
* Raymond: Are we trying to optimise the experience of the developers or integrators as that will have a bearing on the route we should take

Which languages feel best for people?
* MovieLabs, PoC in a mix of Python and Javascript in Node. Member studios are all over the map but Python is at the top. 
* Pixar: C++ and Python. C is a good shimming system, great lowest common denominator between the languages.
* Blender is pretty much Python-only when it comes to add-ons / 3rd-party tools. Blender itself is made in C and C++, and uses various libraries in those languages. They precompile those libraries for the major platforms with GCC, it's usually not much of an issue to integrate a new library.
