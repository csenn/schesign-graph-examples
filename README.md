### Central locations for graphs used for testing
Import graphs are raw graphs that can be uploaded as a design.
Export graphs are what are returned when a design is downloaded.

The 2 will not be identical.

*** Fix, this is not longer true ***
Import graphs can point to nodes
in other designs using a url identifier. An export graph will contain the evaluation of those urls. Also
new nodes in an import graph will not have uids yet.
******

#### propertyVariations
One of every propertySpec constraint
One of every rangeType
One of every rangeConstraint

#### testInhertiance

* 2 different designs are used to test inheritance chain.
* Exclude parent properties should be tested
* Override property should be tested. Property "a" is in parent design and child design, exports should use "a" lowest in the chain. (Boolean instead of Text)


#### testLinking

* Test property refs pointing to internal and external properties
* Test property ranges pointing to internal and external classes
* A class should be able to have a property with range that points to itself