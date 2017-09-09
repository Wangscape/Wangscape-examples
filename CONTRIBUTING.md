# Contributing to Wangscape-examples

We welcome contributions to this collection, including (in no particular order):
* Improvements and bugfixes for existing examples,
* Improvements to base tiles,
* Language corrections,
* New base tiles,
* New examples,
* Raising and discussing issues.

In addition to the following guidelines, please follow the [contribution guidelines for the main Wangscape repository](https://github.com/Wangscape/Wangscape/blob/master/CONTRIBUTING.md) when contributing to Wangscape-examples.

## Base tiles
* Base tiles should be placed in `base_tiles/<AUTHOR_NAME>/` or a subdirectory.
* Tiles should be in PNG format, and have licensing information clearly provided in the same folder.
* The repository's CI system creates derivative works of the base tiles, and publishes them without attribution. Base tiles must have licenses which are not violated by this process.
* Ideally base tiles should be licensed under CC0 or CC-BY. Share-alike and no-derivs licenses are not suitable for this repository.
* Base tiles with other licenses may be considered, but they should not affect the repository's license ([MIT](./LICENSE))
* Alterations to base tiles must not violate the tiles' license.

## Configurations
* Configurations are code, and all use the repository's [MIT license](./LICENSE).
* Configurations must be placed in the `configurations` folder, and the options file should be `configurations/<CONFIGURATION_NAME>/options.json`.
* They should only use base tiles in the `base_tiles` folder.
* They should use the default output folder and metaoutput filenames.
* They should not require excessive resources to run.
