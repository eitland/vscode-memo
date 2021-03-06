# Changelog

All notable changes to this project will be documented in this file. See [standard-version](https://github.com/conventional-changelog/standard-version) for commit guidelines.

### [0.2.2](https://github.com/svsool/vscode-memo/compare/v0.2.1...v0.2.2) (2020-09-27)


### Bug Fixes

* Remove requirement `refUnderCursorExists` when using keyboard shortcut to follow a link [#127](https://github.com/svsool/vscode-memo/issues/127) ([fffb0e3](https://github.com/svsool/vscode-memo/commit/fffb0e3391e07ad4a22f05e01acc80d12040f7dd))

### [0.2.1](https://github.com/svsool/vscode-memo/compare/v0.2.0...v0.2.1) (2020-09-20)


### Bug Fixes

* Infer previous extension on renaming to unknown extension [#120](https://github.com/svsool/vscode-memo/issues/120) ([1aad3f0](https://github.com/svsool/vscode-memo/commit/1aad3f0ee87834db2462e7ec643cbfcab1162cb9))

## [0.2.0](https://github.com/svsool/vscode-memo/compare/v0.1.14...v0.2.0) (2020-09-20)


### ⚠ BREAKING CHANGES

* memo.imagePreviewMaxHeight -> memo.imagePreviewMaxHeight
memo.collapseBacklinksPanelItems -> memo.backlinksPanel.collapseParentItems

### Features

* Take search.exclude and file.exclude settings into account when caching workspace [#116](https://github.com/svsool/vscode-memo/issues/116) ([81643ae](https://github.com/svsool/vscode-memo/commit/81643ae0194ff5093f69a6f422406172a5afbae1))


### Bug Fixes

* Change backlinks panel id namespace to align with settings ([4e9e112](https://github.com/svsool/vscode-memo/commit/4e9e1121f5192179ebc22a757cc4ca5ff32466f9))


* Rename configuration options ([ddfcafd](https://github.com/svsool/vscode-memo/commit/ddfcafd7b19992c4e3ffd7ff330acec1fbba6137))

### [0.1.14](https://github.com/svsool/vscode-memo/compare/v0.1.13...v0.1.14) (2020-08-09)


### Features

* **autocomplete:** Support autocomplete of dangling refs ([1d0fefa](https://github.com/svsool/vscode-memo/commit/1d0fefa33c1b6043dff66e678004401038ab66c9))


### Bug Fixes

* Don't add extra md extension if link has an extension ([4cb7436](https://github.com/svsool/vscode-memo/commit/4cb7436e655e294ebb1462a772b3dc5b3273d4d2))
* Fix findReferences regexp greediness ([c5a976e](https://github.com/svsool/vscode-memo/commit/c5a976eee3643b9b4d9e1223ac8cc0fe4e53f820))
* Fix findUriByRef logic to use relative paths ([a6dbd2c](https://github.com/svsool/vscode-memo/commit/a6dbd2c38af470499e364f29425eb82a0df51b6c))
* Fix path passed to del.sync in cleanWorkspace utility ([f60575c](https://github.com/svsool/vscode-memo/commit/f60575c2d1a749bf9817f0dabfdc16e6d9ee1db8))
* Make links working better with dot files and explicit md extension in the link ([51d65f5](https://github.com/svsool/vscode-memo/commit/51d65f594978d30ee049feda710c3ce52ab64bad))

### [0.1.13](https://github.com/svsool/vscode-memo/compare/v0.1.12...v0.1.13) (2020-08-01)

### [0.1.12](https://github.com/svsool/vscode-memo/compare/v0.1.11...v0.1.12) (2020-07-31)

### Added

- Add `webp` extension support
- Add tooltip about unknown extensions to built-in preview

### Fixed
- Links within code spans and fenced code blocks are not interpreted anymore during links rename and in the backlinks panel
- New [known extensions](https://github.com/svsool/vscode-memo/blob/7643221ae1b8884e02af375af2696c4918fcd285/src/utils/utils.ts#L19) are now recognized on drag and drop to project explorer

### Removed
- Remove `memo.useEnhancedTriggerSuggest` setting in favor of built-in `"[markdown]": { "editor.quickSuggestions": true }`

### [0.1.11](https://github.com/svsool/vscode-memo/compare/v0.1.10...v0.1.11) (2020-07-26)

### Added
- Add new "Open daily note" command

### Removed
- Remove "Open today's note" command in favor of more flexible "Open daily note" command

### [0.1.10](https://github.com/svsool/vscode-memo/compare/v0.1.9...v0.1.10) (2020-07-24)

### Added
- Add new help document "Open link in the default app"
- Add Memo logo for VSCode Marketplace

### Changed
- Better documentation for "Accepted File Formats" in the help
- Added information about links rename via "Rename Symbol" command to "Automatic link synchronization" document in the help

### [0.1.9](https://github.com/svsool/vscode-memo/compare/v0.1.8...v0.1.9) (2020-07-23)

### Added
- Add "Open link in the default app" command. Opening link via context menu is also supported
- Add the possibility to rename links using `F2` or `Rename symbol` command. Renaming via context menu is also supported

### Fixed
- Fix bug when hover was not available for long references in Windows

### [0.1.8](https://github.com/svsool/vscode-memo/compare/v0.1.7...v0.1.8) (2020-07-13)

### Added
- Embedding other notes using `![[Your note]]` syntax
- Support regular links to images `[[image.png]]`, previously it was only possible to refer to an image using embed link `![[image.png]]`
- Add `memo.useEnhancedTriggerSuggest` setting that instructs Memo to continuously trigger suggest after `[[` characters typed, so it makes easier to re-trigger suggest if you made a mistake while typing
- Embed files feature added to help documentation

### Fixed
- Regular and embed links won't be interpreted anymore within code span and fenced code blocks. So you can use it for escaping links and rendering them as is.

### [0.1.7](https://github.com/svsool/vscode-memo/compare/v0.1.6...v0.1.7) (2020-07-08)

### Fixed
- Fix backlinks lookup for filenames with special characters

### [0.1.6](https://github.com/svsool/vscode-memo/compare/v0.1.5...v0.1.6) (2020-07-08)

### Added
- Creating a note from a long link even when folder does not exist

### [0.1.5](https://github.com/svsool/vscode-memo/compare/v0.1.4...v0.1.5) (2020-07-07)

### Fixed
- Fix links resolution in the built-in preview. Sometimes links were not referring to a correct file.

### [0.1.4](https://github.com/svsool/vscode-memo/compare/v0.1.1...v0.1.4) (2020-07-06)

### Added
- Publishing via CI

### Fixed
- Fix opening a note via a short link when note and image share the same name

### [0.1.1](https://github.com/svsool/vscode-memo/compare/v0.1.0...v0.1.1) (2020-07-05)

### Added
- Help docs
- Features demo in README.md
- Hover hint for links referring to nonexistent files

## 0.1.0 (2020-07-04)

### Added
- Links support
  - Creating links
  - Links navigation on `cmd+click` for macOS or `ctrl+click` for Windows
  - Automatic links synchronization on file rename
  - Support for short and full links if filename is not unique in the workspace
- Notes & images preview in the built-in Markdown preview or on hovering a link
- Creating notes on the fly from the links that are not created yet to the filesystem
- Simple backlinks panel
- Two new commands added
  - Open today's note command — creates a note with a title in this format `yyyy-mm-dd` or opens already existing one
  - Open random note — allows you to explore your knowledge base a little bit
