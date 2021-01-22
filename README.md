## Digital Forensics Artifact Repository (*forensicanalysis edition*)

The repository is a fork of ForensicArtifacts/artifacts: [More information](#backgroundhistory)

A free, community-sourced, machine-readable knowledge base of digital forensic
artifacts that the world can use both as an information source and within other
tools.

If you'd like to use the artifacts in your own tools, **all you need to be able
to do is read YAML**. That is it, no other dependencies. The Python code in
this project is just used to validate all the artifacts to make sure they
follow the specification.

## Artifact Definitions

The artifact definition format is described in detail in the [Style Guide](style_guide.md).

As of 2021-07-21 the repository contains:

**Artifact definition by type**

| ARTIFACT GROUP | COMMAND | DIRECTORY | FILE | PATH | REGISTRY KEY | REGISTRY VALUE | WMI |
|----------------|---------|-----------|------|------|--------------|----------------|-----|
|             36 |       9 |        15 |  318 |   20 |           64 |            124 |  26 |

**Artifact definition by OS**

| DARWIN | LINUX | WINDOWS |
|--------|-------|---------|
|    146 |   132 |     326 |


**Artifact definition by label**

| ANTIVIRUS | AUTHENTICATION | BROWSER | CLOUD | CLOUD STORAGE | CONFIGURATION FILES | DOCKER | EXTERNAL MEDIA | EXTERNALACCOUNT | HADOOP | HISTORY FILES | LOGS | MAIL | NETWORK | SOFTWARE | SYSTEM | USERS | IOS |
|-----------|----------------|---------|-------|---------------|---------------------|--------|----------------|-----------------|--------|---------------|------|------|---------|----------|--------|-------|-----|
|         6 |             19 |      28 |     2 |             4 |                  46 |      2 |              2 |               3 |      1 |             3 |   48 |   16 |      18 |       43 |    116 |    77 |   5 |


## Background/History

The repository is a fork of https://github.com/ForensicArtifacts/artifacts with the
following changes:
 - `conditions` are ignored as they have some issues ([#274](https://github.com/ForensicArtifacts/artifacts/issues/274))
 - `provides` on the artifact definition are deprecated, as they do not enable extraction of parameters without further parsing information
 - `provides` on source level are added to enable extraction of parameters
 - All source types are distinctly defined, including the `DIRECTORY` type ([#286](https://github.com/ForensicArtifacts/artifacts/issues/286)).
 - Parameter expansion and globing is defined, including `**` ([#342](https://github.com/ForensicArtifacts/artifacts/issues/342)).
 - Inconsistent trailing `\*` in REGISTRY_KEYs are removed ([#255](https://github.com/ForensicArtifacts/artifacts/issues/255)).
 - Validate path separators ([#265](https://github.com/ForensicArtifacts/artifacts/issues/265)).
 - More validations, smaller documentation fixes ([#23](https://github.com/ForensicArtifacts/artifacts/issues/23#issuecomment-469063370)), ...

See [Updated Style Guide](style_guide.md)

The [ForensicArtifacts.com](http://forensicartifacts.com/) artifact repository
was forked from the [GRR project](https://github.com/google/grr) artifact
collection into a stand-alone repository that is not tool-specific. The GRR
developers have migrated to using this repository and make contributions here. In
addition the ForensicArtifact team will begin backfilling artifacts in the new
format from the [ForensicArtifacts.com](http://forensicartifacts.com/) website.

For some background on the artifacts system and how we expect it to be used see
[this blackhat presentation](https://www.blackhat.com/us-14/archives.html#grr-find-all-the-badness-collect-all-the-things)
and [youtube video](https://www.youtube.com/watch?v=ren6QSvwFvg) from the GRR team.

## Contributing

Please send us your contribution!

## External links

* [GRR Artifacts](https://www.blackhat.com/docs/us-14/materials/us-14-Castle-GRR-Find-All-The-Badness-Collect-All-The-Things-WP.pdf), by Greg Castle, Blackhat 2014

## Contact

* Artifacts channel of [Open Source DFIR Slack](https://github.com/open-source-dfir/slack)
