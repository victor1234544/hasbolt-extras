# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.0.1.9] - 2022-03-14
### Added
- `IsValue` instances for `ToValue` & `NodeLike` via newtypes;
- Add even more `HasCallStack`.

## [0.0.1.8] - 2021-09-07
### Added
- `FromValue` / `ToValue` instances for `NonEmpty`;
- `BoltEnum` wrapper to provide `FromValue` / `ToValue` for enum-like types.

## [0.0.1.7] - 2021-04-28
### Changed
- Add more `HasCallStack`.

## [0.0.1.6] - 2020-12-26
### Fixed
- Fix `makeNodeLike` for `Maybe` fields, bug introduced in previous version.

## [0.0.1.5] - 2020-12-22
### Fixed
- Compatibility of `makeNodeLike` / `makeURelationLike` with `DuplicateRecordFields`, thanks to
  [@oddsome](https://github.com/oddsome), [PR #40](https://github.com/biocad/hasbolt-extras/pull/40).

## [0.0.1.4] - 2020-05-27
### Fixed
- Compatibility with GHC-8.10.

## [0.0.1.3] - 2020-03-04
### Fixed
- https://www.wrike.com/open.htm?id=472936296: fix recursion in `GetTypeFromRecord` type family.
### Added
- Export of `LabelConstraint` to allow users to define wrappers around `lbl`.

## [0.0.1.2] - 2020-01-17
### Added
- `=:` type synonym to avoid ticks in type-level tuples.

## [0.0.1.1] - 2019-12-31
### Added
- `param` combinator to add named parameters to selectors;
- `CypherDSLParams` to control parameters that queries accept.

## [0.0.1.0] - 2019-12-17
### Changed
- Use `hasbolt` 0.1.4.0.
### Added
- Compatibility function `exact` from older `hasbolt`.

## [0.0.0.25] - 2019-12-07
### Added
- `makeNodeLikeWith` and `makeURelationLikeWith` functions.

## [0.0.0.24] - 2019-11-08
### Added
- Support for `Maybe` fields in typed selectors;
- Integration of typed selectors and Graph API.

## [0.0.0.23] - 2019-11-07
### Added
- Type-safe selectors for nodes and relationships.

## [0.0.0.22] - 2019-09-19
### Changed
- Exported `(#)` operator.

## [0.0.0.21] - 2019-09-09
### Added
- `OverloadedLabels` instances and operators for easy selector writing.

## [0.0.0.20] - 2019-09-06
### Added
- `WITH` statement in DSL.

## [0.0.0.19] - 2019-07-09
### Changed
- Directed relationship in graph get dsl instead of undirected.

## [0.0.0.18] - 2019-05-27
### Changed
- Updated dependencies.

## [0.0.0.17] - 2019-05-09
### Changed
- Expanded documentation for `Database.Bolt.Extras.Graph`.

## [0.0.0.16] - 2019-02-01
### Changed
- Optimized query, easy way to extract entities from result graph.

## [0.0.0.15] - 2019-01-22
### Changed
- Ability to choose whether to return entity or not in graphs.

## [0.0.0.14] - 2018-12-25
### Added
- `mergeGraphs`, ability to take not all node properties from DB.
### Changed
- Refactoring.

## [0.0.0.13] - 2018-12-05
### Added
- `ToJSON` and `FromJSON` instances for `Persisted a`.

## [0.0.0.12] - 2018-10-15
### Added
- `REMOVE` query.
### Fixed
- Escaping special characters in text fields.

## [0.0.0.11] - 2018-06-19
### Changed
- Cabal fix.

## [0.0.0.10] - 2018-05-24
### Changed
- Fixed conditions.

## [0.0.0.9] - 2018-05-18
### Added
- New types for conditions in `DSL`.

## [0.0.0.8] - 2018-05-14
### Added
- Added `DSL` for `Cypher`.

## [0.0.0.7] - 2018-04-23
### Added
- Added ability to delete nodes by their `BoltId`s.

## [0.0.0.6] - 2018-04-20
### Added
- Added ability to update properties of the existing node; added ability to choose
if you want to `CREATE` or `MERGE` the relationship.

## [0.0.0.4] - 2018-04-05
### Changed
- More accurate `toNode` on data fields with `Maybe a` type. If the corresponding field in the type is Nothing, this field won't be included to `Node`.

## [0.0.0.3] - 2018-04-05
### Changed
- More accurate `fromNode` on data fields with `Maybe a` type. If there is no such field in Node, data field will be set to Nothing.

## [0.0.0.0] - 2018-02-22
### Added
- Template Haskell code to generate `Node`s and `URelationship`s.
- Simple queries to upload `Node` and `URelationship`.
- Simple query to download `Node`s.
