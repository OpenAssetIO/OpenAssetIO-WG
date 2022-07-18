# July 14th 2022

**Date/Time**: 14th July 2022 @ 17:00 BST <br>
**Meeting Recording**: [Recording](https://drive.google.com/file/d/1OL559g5qZTZnUQNmXHZ4VAB5GeOSamm4/view?usp=sharing) <br>

## Notes

- ASWF Sandbox adoption (🎉) [00:08](https://drive.google.com/file/d/1OL559g5qZTZnUQNmXHZ4VAB5GeOSamm4/view?t=8)
  - Sandbox phase adoption
  - [`#openassetio`](https://academysoftwarefdn.slack.com/archives/C03Q36QS8N4) slack channel now in ASWF org.
  - Mailing list in progress and will be using as soon as are available.
  - Github will remain in current GitHub org for now. Will move to ASWF further down the line.
- Q3 Goals [03:19](https://drive.google.com/file/d/1OL559g5qZTZnUQNmXHZ4VAB5GeOSamm4/view?t=199)
  - Initial alpha release, not the full API but structurally stable.
  - Limited to resolve+preflight/register
  - C++ host, Python host/manager.
  - VFXplatform 2022
  - We're hiring/contributions welcome!
- Progress with Specification/Trait autogeneration [05:43](https://drive.google.com/file/d/1OL559g5qZTZnUQNmXHZ4VAB5GeOSamm4/view?t=343)
  - Describes the nature of an asset
  - Autogen will help generate required trait code in all supported languages without excessing typing.
  - Will be finished next sprint
- Progress with C++ migration [11:30](https://drive.google.com/file/d/1OL559g5qZTZnUQNmXHZ4VAB5GeOSamm4/view?t=690)
  - Batch API methods using callbacks
  - C++ Host calling through to Python plugins revealed pybind to C++ doesn't keep derived python classes alive!
- AOB
  - When will it be ready to integrate? [16:37](https://drive.google.com/file/d/1OL559g5qZTZnUQNmXHZ4VAB5GeOSamm4/view?t=997)
  - Is it suitable for a multi application interaction solution? [19:54](https://drive.google.com/file/d/1OL559g5qZTZnUQNmXHZ4VAB5GeOSamm4/view?t=1194)

## Background Reading

- [ASWF Project Lifecycle](https://tac.aswf.io/process/lifecycle.html#sandbox-stage).
- [ASWF Sandbox proposal](https://lists.aswf.io/g/tac/message/2209).
- [Decision Record for C++ API signature for batch methods](https://github.com/OpenAssetIO/OpenAssetIO/blob/main/decisions/DR009-Batch-method-result-types.md)
