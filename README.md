### Central locations for graphs used for testing
Import graphs can be uploaded as a design.
Export graphs are returned when a design is downloaded. They include defaults, external node resolution, validation, etc.

*** Fix, this is not longer true ***
Import graphs can point to nodes
in other designs using a url identifier. An export graph will contain the evaluation of those urls. Also
new nodes in an import graph will not have uids yet.
******

#### propertyVariations
One of every propertySpec constraint
One of every rangeType
One of every rangeConstraint

#### recursion
Simple case to ensure nestedObjects can have children that reference themselves

#### testInhertiance
* 2 different designs are used to test inheritance chain.
* Exclude parent properties should be tested
class1 "a1", "a2", "a3" should all be overwritten and not make it to class5 in inheritance_chain_2
* Override property should be tested.
Property "a" is in parent design and child design. Class 5 should use the lowest in the chain, "a" type Boolean

#### testLinking
* Test propertySpecs pointing to internal and external properties
* Test LinkedClass ranges pointing to internal and external classes
* Test more then one class pointing to same property (linked_nodes_1 property a)
* Test a class should be able to have a property with range that points to itself (linked_nodes_1 class2 property a)
* An imported NestedObject should be able to point to classes and and properties in parent design (linked_node_1 property b) and these should be resolved
* Should be able to import classes and properties into version and their dependencies should resolve (Linked Nodes 2)
* Class 2 should be a direct import
* Property f should be a direct import
* Property d should be imported through Class 3 through Property f