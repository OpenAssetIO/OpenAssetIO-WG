# Assetised OTIO workflows planning

## Attendees

- Joshua Minor (Pixar)
- Eric Desruisseaux (Autodesk)
- Roger Nelson (Autodesk)
- Juan Salazar (Foundry)
- Mathieu Mazerolle (Foundry)
- David Feltell (Foundry)
- Peri Friend (Foundry)
- Tom Cowland (Foundry).

## Notes

- Production media linkers often add specific Clip metadata that
  includes asset-tracking metadata.
  - This may be based on “user metadata” from the upstream EDL/AAF/etc.
- Multi-ref often used for alternate storages, or resolutions
  - Always the same “frame” for any given frame. Just quality or storage
 location variations
  - Not suitable for multiple versions/variations (See below)
- Makes sense to have the asset data on the clip, as when you switch
  versions etc… it may well change timing/offsets and other clip
  metadata.
  - Generally replace the whole clip for versions/etc..
- Raises the Q - does the OTIO just contain one reference and this is
  explored/expanded on the fly in the host (eg: best storage
  location/proxy), or do we expand the OTIO in palace as a cache of this
  data?
  - Could do either! Need a concrete workflow to properly explore this.
- Multicam - how does this fit
- Pixar media linker example, provided for reference:
  - An AAF from Media Composer is converted to OTIO.
  - Each clip's media reference initially points to internal Avid
    storage, not available/suitable for downstream use.
  - Media linker looks at metadata on each clip and media ref to
    determine if it is a managed asset or not. Specifically: some
    studio-specific UserComments fields from the AAF metadata.
  - If a clip is not managed, the media ref and metadata are left as-is.
  - For a managed clip:
    - Media linker moves some metadata from the media ref up to the
      parent clip.
    - Media linker replaces the media ref with new media ref(s) pointing
      to studio managed storage.
    - Media linker adds metadata to each media ref with details of
      codec, resolution, etc.
  - Example OTIOs pre/post media linker sent as ZIP file to ASWF
    `#openassetio` Slack channel [here](https://academysoftwarefdn.slack.com/archives/C03Q36QS8N4/p1661886649632189?thread_ts=1661167406.558319&cid=C03Q36QS8N4)
    (also available [here](./examples)).
  - If you compare these two files, you can see the specifics of the
    transformation explained above.
  - Note: the "pixar" metadata has been redacted, but you can still see
    the general idea.
  - Note: some of the metadata is just plain JSON dictionaries, and some
    metadata is a custom OTIO schemadef object.

## Action items

- Update the media linker to look in clip metadata (OpenAssetIO specific
  schema in the plugin)
- Define traits/specifications for `getRelatedReferences` and `resolve`
  for:
  - Proxy entities
  - Alternate storage locations
- Prototype: `getRelatedReferences` to expand clip to multi
  `ExternalReferences` in OTIO (for proxies or storage, both??)
