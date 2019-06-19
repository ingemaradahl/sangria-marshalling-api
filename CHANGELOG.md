## v2.0.0 (2019-06-19)

This is a binary-incompatible release.

 * Target Scala 2.13, and cross-compile for 2.11 and 2.12
 * `InputUnmarshaller.getMapKeys(node: Node)` now returns an `Iterable[String]`

## v1.0.3 (2018-05-11)

The release should be compatible with v1.0.0, so no update to the downstream libraries is necessary. 

* Removed new helpers methods in `ResultMarshaller` (otherwise all downstream libraries need to recompiled, at least for scala 2.11)
* Re-added helpers as a part of `MarshallingUtil` 

## v1.0.2 (2018-05-11) 

* Added several helper methods in `ResultMarshaller` for easy value creation 
* Moved `SimpleResultMarshallerForType` and `SymmetricMarshaller` from sangria

## v1.0.1 (2018-02-20)

The release should be compatible with v1.0.0, so no update to the downstream libraries is necessary. 

* `ArrayMapBuilder` not extends `Iterable[(String, T)]` (#3). Big thanks to @yanns for this contribution! 
* `MarshallingUtil.convert` now has more safe enum value handling

## v1.0.0 (2017-01-16)

* 1.0 release

## v0.2.2 (2016-11-03)

* Cross-compile for scala 2.11 and 2.12
* Updated dependencies

## v0.2.1 (2016-05-01)

* Introduced `ScalarValueInfo` and `MarshallerCapability` marker traits to allow scalar values to coerce output values based on the marshaller capabilities.
* Added a set of standard marshaller capabilities that may be supported by concrete implementations natively: `DateSupport`, `CalendarSupport` and `BlobSupport`.   
* `ResultMarshaller` now only has 2 methods for scalar value marshalling: `scalarNode` and `enumNode`. They get much more info about the value as well.

## v0.2.0 (2016-03-24)

* Introduced map builder which is able to preserve the field order and provides much faster way to build a 
  map (uses mutable data structures to minimize memory footprint)

## v0.1.1 (2016-01-28)

* Added `InputParser` type class which may be implemented by marshalling library in order to provide parsing from string feature 
  (required for default value support in schema materialization)

## v0.1.0 (2016-01-23)

* Initial release
