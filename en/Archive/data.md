## Data

### Types
#### Numbers
| Icon | Name | Inputs | Outputs |
| -- | -- | -- | -- | -- | -- |-- |
| ![](../images/icons/Dynamo-Nodes-DoubleInput-Large.jpg) | Number | Number Box | double |

Simply put, a number node allows one to add a number to the canvas by typing it in the number box.  This can be an integer, decimal, negative number, etc.  There are other options for adding numbers to the canvas, including sliders, which we'll demonstrate in the exercise at the end of this section.
#### Booleans
| Icon | Name | Inputs | Outputs |
| -- | -- | -- | -- | -- | -- |-- |
| ![](../images/icons/DSCoreNodesUI-BoolSelector-Large.jpg)  | Boolean | True/False | boolean |
Numeric variables can store a whole range of different numbers. Boolean
variables can only store two values referred to as Yes or No, True or False,
1 or 0. Obviously we never use booleans to perform calculations because of their
limited range. We use booleans to evaluate conditions.
#### Strings
| Icon | Name | Inputs | Outputs |
| -- | -- | -- | -- | -- | -- |-- |
| ![](../images/icons/Dynamo-Nodes-StringInput-Large.jpg) | String | Text Box | string |
A string is programming lingo for text.  We know that number can drive parameters, and we can do the same with text, which we demonstrate in section 4.4.
## Geometry
![](images/4-1/CompGeom-01-Dimensionality-01.jpg)
#####Points

| Icon | Name/Syntax | Inputs | Outputs |
| -- | -- | -- | -- | -- | -- |
| ![](../images/icons/Autodesk-DesignScript-Geometry-Point-ByCoordinates-double-double-double-Large.jpg) | Point.ByCoordinates | x,y,z | Point |
| ![](../images/icons/Autodesk-DesignScript-Geometry-Point-ByCylindricalCoordinates-Large.jpg) | Point.ByCylindricalCoordinates | cs,angle,elevation,radius | Point |
| ![](../images/icons/Autodesk-DesignScript-Geometry-Point-BySphericalCoordinates-Large.jpg) | Point.BySphericalCoordinates | cs,phi,theta,radius | Point |

A point is a location in space. For this primer, our coordinate system is X,Y, and Z. A point has a value for X, a value for Y, and a value for Z.


#####Vectors
| Icon | Name/Syntax | Inputs | Outputs |
| -- | -- | -- | -- | -- | -- |
| ![](../images/icons/Autodesk-DesignScript-Geometry-Vector-ByCoordinates-double-double-double-Large.jpg) | Vector.ByCoordinates | x,y,z | Vector |
| ![](../images/icons/Autodesk-DesignScript-Geometry-Vector-ByTwoPoints-Large.jpg) | Vector.ByTwoPoints| start,end | Vector |
| ![](../images/icons/Autodesk-DesignScript-Geometry-Vector-XAxis-Large.jpg) | Vector.XAxis | none | Vector |
| ![](../images/icons/Autodesk-DesignScript-Geometry-Vector-YAxis-Large.jpg) | Vector.YAxis | none | Vector |
| ![](../images/icons/Autodesk-DesignScript-Geometry-Vector-ZAxis-Large.jpg) | Vector.ZAxis | none | Vector |

A vector is a geometric quantity describing Direction and Magnitude. Vectors are abstract; ie. they represent a quantity, not a geometrical element.

#####Planes
| Icon | Name/Syntax | Inputs | Outputs |
| -- | -- | -- | -- | -- | -- |
| ![](../images/icons/Autodesk-DesignScript-Geometry-Plane-ByThreePoints-Large.jpg) | Vector.ByCoordinates | p1,p2,p3 | Plane |
| ![](../images/icons/Autodesk-DesignScript-Geometry-Plane-ByOriginNormal-Large.jpg) | Vector.ByTwoPoints| origin,normal | Plane |
| ![](../images/icons/Autodesk-DesignScript-Geometry-Plane-XY-Large.jpg) | Plane.XY  | none | Plane |
| ![](../images/icons/Autodesk-DesignScript-Geometry-Plane-XZ-Large.jpg) | Plane.XZ | none | Plane |
| ![](../images/icons/Autodesk-DesignScript-Geometry-Plane-YZ-Large.jpg) | Plane.YZ | none | Plane |

Planes are “Flat” and extend infinitely in two directions, defining a local coordinate system.

#####Nurbs
| Icon | Name/Syntax | Inputs | Outputs |
| -- | -- | -- | -- | -- | -- |
| ![](../images/icons/Autodesk-DesignScript-Geometry-NurbsSurface-ControlPoints-Large.jpg) | NurbsSurface.ByControlPoints | ControlVertices,uDegree,vDegree | NurbsSurface |
| ![](../images/icons/Autodesk-DesignScript-Geometry-NurbsCurve-ByControlPoints-Point1-Large.jpg) | NurbsCurve.ByControlPoints | points | NurbsCurve |

NURBS (non-uniform rational B-splines) are mathematical representations that can accurately model any shape from a simple 2D line, circle, arc, or box to the most complex 3D free-form organic surface or solid.  They are created with rational algorithms and are infinitely differentiable.

#####Meshes
| Icon | Name/Syntax | Inputs | Outputs |
| -- | -- | -- | -- | -- | -- |
| ![](../images/icons/Autodesk-DesignScript-Geometry-Mesh-ByPointsFaceIndices-Large.jpg) | Mesh.ByPointsFaceIndices | vertexPositions,indices | Mesh |

A mesh is a collection of vertices, edges and faces which define a polyhedral object.  Meshes are often used for rendering and animation, and are generally 'lighter weight' than nurbs (meaning, they have smaller file sizes and render more quickly).  The tradeoff is that meshes are limited in their resolution.

#####Meshes vs. Nurbs
Generally, we can say that Nurbs are to Meshes as Vectors are to Pixels.  They are significantly different geometry types, and using the propery geometry type for surfaces is critical for parametric modeling and file management.

![nurbs and meshes](images/4-1/4-1-1/4-1-1-Mesh-Nurb.jpg)

#####Surfaces
| Icon | Name/Syntax | Inputs | Outputs |
| -- | -- | -- | -- | -- | -- |
| ![](../images/icons/Autodesk-DesignScript-Geometry-Surface-ByLoft-Curve1-Curve-Large.jpg) | Surface.ByLoft | crossSections | Surface |
| ![](../images/icons/Autodesk-DesignScript-Geometry-Surface-ByPatch-Large.jpg) | Surface.ByPatch| closedCurve | Surface |
| ![](../images/icons/Autodesk-DesignScript-Geometry-Surface-ByPerimeterPoints-Large.jpg) | Surface.ByPerimeterPoints  | points | Surface |
| ![](../images/icons/Autodesk-DesignScript-Geometry-Surface-BySweep-Large.jpg) | Surface.BySweep| profile,path | Surface |
| ![](../images/icons/Autodesk-DesignScript-Geometry-Surface-ByRevolve-Large.jpg) | Surface.ByRevolve | profile,axisOrigin,axisDirection,startAngle,sweepAngle | Surface |

A surface is two-dimensional topological manifold. Rather than deciphering what that means, let's just saw a surface is geometry that does not have thickness.  This is how a surface is different from a solid.

#####Solids
| Icon | Name/Syntax | Inputs | Outputs |
| -- | -- | -- | -- | -- | -- |
| ![](../images/icons/Autodesk-DesignScript-Geometry-Solid-ByUnion-Large.jpg) | Solid.ByUnion | solids | Solid |
| ![](../images/icons/Autodesk-DesignScript-Geometry-Solid-ByJoinedSurfaces-Large.jpg) | Solid.ByJoinedSurfaces| facesOfSolid | Solid |
| ![](../images/icons/Autodesk-DesignScript-Geometry-Solid-ByLoft-Curve1-Large.jpg) | Solid.ByLoft  | crossSections | Solid |
| ![](../images/icons/Autodesk-DesignScript-Geometry-Solid-BySweep-Large.jpg) | Solid.BySweep| profile,path | Solid |
| ![](../images/icons/Autodesk-DesignScript-Geometry-Solid-ByRevolve-Large.jpg) | Solid.ByRevolve | profile,axisOrigin,axisDirection,startAngle,sweepAngle | Solid |

A solid is three-dimensional geometry.  A solid has thickness and can exist in the real world, unlike surfaces, curves, vectors, and points (at least as far as we can see). In Dynamo, a solid can be defined as a collection of surfaces, called a polysurface.

##### "Null"
| Icon | Name/Syntax | Inputs | Outputs |
| -- | -- | -- | -- | -- | -- |
| ![](../images/icons/DSCore-Object-IsNull-Large.jpg) | Object.IsNull | obj | bool |

The 'null' object represents the absense of data. This is abstract, but you will likely come across this while working with visual programming.  Testing for nulls and removing nulls from data structure is a crucial part to creating robust parametric models.
### 4.1.2 Hierarchy
#### Item(s)

| Icon | Name/Syntax | Inputs | Outputs |
| -- | -- | -- | -- | -- | -- |
| ![](../images/icons/DSCore-List-GetItemAtIndex-Large.jpg) | List.GetItemAtIndex | list,index | var[]...[] |

Simply put, an item represents one single value, whether by itself or as part of a list.  This can be any data type.

#### List(s)
| Icon | Name/Syntax | Inputs | Outputs |
| -- | -- | -- | -- | -- | -- |
| ![](../images/icons/DSCore-List-Create-Large.jpg) | List.Create | index0, index1... | list |



