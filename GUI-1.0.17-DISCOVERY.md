# Easier discovery in GUI 1.0.17

Proposed patch versions: Aggressive-AI-Behaviour 1.4.1.

- Find these extensions using translated topics in the search box and tag filter.
- Existing saved setups and activation rules keep their package identities and settings.
- Browse related options together in an expandable family. Expand it to choose individual members.

## Maintainer notes

Stable tag IDs use the GUI’s shared translations in all nine supported languages. Capability facts describe this package’s files, parsed configuration demands and options, not its family’s combined behavior. Existing dependencies, required/suggested settings and load-order conflict controls still apply. Family membership does not make members exclusive or install them automatically.

### Family `aggressive-ai-behaviour`

Proposed display root: `Aggressive-AI-Behaviour-Applied`. The creator can choose a different ordinary member as root. Members: `Aggressive-AI-Behaviour`, `Aggressive-AI-Behaviour-Applied`.

Repository consolidation proposal: keep shared assets in `Aggressive-AI-Behaviour` in `Krarilotus/extension-Aggressive-AI-Behaviour` and place the other member manifests/configurations in separate package directories in that repository. The existing Store `contents.source.location` field packages those directories independently. Preserve every member’s technical name, dependency range and resource path. Do not copy the provider’s assets into Applied members. Existing independent asset providers (for example Ascension maps) retain their own files. This PR adds grouping metadata; moving repositories can follow after the maintainers agree on the layout.

Validation: definitions parse; unrelated manifest fields and configuration are preserved, apart from the explicit identity/path corrections above. Shared family roots and tag translations are checked against GUI 1.0.17. No game testing or release publication is claimed.
