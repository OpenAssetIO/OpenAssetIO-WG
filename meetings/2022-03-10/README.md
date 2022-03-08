# March 2022

Date/Time: 16th or 17th March 2022 @ 17:00 GMT TBC


## Discussion Points

The main focus of this meeting is to understand the performance characteristics of real world asset management systems that are in use in production.

We are proposing structural changes to the API (see Background Reading) and believe these changes create significant improvements, but preclude some specific optimisations afforded by the current design.

To ensure we are making a fully informed decision, we are looking for stats about the asset management systems currently used in production - regardless of how they are integrated:

> NOTE: These questions have nothing to do with OpenAssetIO, we are trying to learn about the existing environment.

1. Typical ranges encountered in production scenarios for:
    1. Asset resolution query volumes for typical 2D/3D tasks (assets resolved per task, number of queries)
    2. Query latencies  (overhead of each query)
2. What are the bottlenecks encountered during asset resolution in your system?
3. How often in the following workflows are you able to take advantage of client-side caching of resolved data to reduce query overhead in:
    1. Farm-based renders/scene expansion
    2. Interactive UI sessions
4. Within OpenAssetIO we have the ability to query more data than just paths,  for example, frame ranges, color spaces for images, etc.
    1. Can you query data other than paths from your system?
    2. Does all asset data live in one store, or is it distributed? 
    3. Do you have optimised handling for filepaths specifically?


We would be extremely grateful for any information people may be able to bring for discussion during the meeting. Please feel free to add any data you have to this discussion [here](https://github.com/TheFoundryVisionmongers/OpenAssetIO/discussions/259), or any other comments about the changes on the respective pull requests below.

After the discussion on performance, we can talk about these two proposals in more detail if there is interest

## Background Reading

There are two changes motivating this discussion which we believe are vital to the consistency of the API and its long term suitability in a variety of asset centric workflows:

* [Trait based identification](https://github.com/TheFoundryVisionmongers/OpenAssetIO/pull/238)
* [Unified entity data model](https://github.com/TheFoundryVisionmongers/OpenAssetIO/pull/253)

## Notes


