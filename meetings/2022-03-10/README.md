# March 2022

Date/Time: 16th or 17th March 2022 @ 17:00 GMT TBC


## Discussion Points

The main focus of this meeting is to understand the performance characteristics of real world asset management systems that are in use in production.

We are proposing significant structural improvements to the API (see Background Reading). We believe these changes create significant improvements to the API surface area but preclude certain specific optimisations afforded by the current split of "resolving the path" and everything else. We want to ratify this decision, backed by a better understanding based on empirical data. 

To help inform this, we are looking for:
1. Typical ranges encountered in production:
    1. Asset resolution query volumes for typical 2D/3D tasks?
    2. Query latencies? 
2. The bottlenecks encountered during asset resolution in your system
3. How often in the following workflows are you able to take advantage of client-side caching of resolved data to reduce query overhead?
    1. batch render scene expansion
    2. UI sessions
4. Within OpenAssetIO we have the ability to query more data than just paths, 
    1. Does all asset data live in one system, or is it distributed? 
    2. Do you have optimised handling for filepaths specifically. 

We would be extremely grateful for any information people may be able to bring for discussion during the meeting. Please feel free to add any data you have to this discussion [here](https://github.com/TheFoundryVisionmongers/OpenAssetIO/discussions/259), or any other comments about the changes on the respective pull requests below.

After the discussion on performance, we can talk about these two proposals in more detail if there is interest

## Background Reading

There are two changes motivating this discussion which we believe are vital to the consistency of the API and its long term suitability in a variety of asset centric workflows:

* [Trait based identification](https://github.com/TheFoundryVisionmongers/OpenAssetIO/pull/238)
* [Unified entity data model](https://github.com/TheFoundryVisionmongers/OpenAssetIO/pull/253)

## Notes


