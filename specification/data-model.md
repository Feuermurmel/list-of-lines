= Data Model

== Overview

//List of Lines// Is a bit of a misnomer as LOL can can specify much more than just lines. An **LOL** file describes a set of [[http://mathworld.wolfram.com/Polyhedron.html|polyhedra]] (generalization of polygons for any number of dimensions). The polyhedra are indexed by a name (think of them as //layers//, like in an image processing application). Each polyhedron built from a set of //points//, //line segments//, //triangles//, //tetrahedra// (called [[https://en.wikipedia.org/wiki/Simplex|simplexes]] if extended to higher dimensions).

The specific type of polyhedra that can be represented are called [[https://en.wikipedia.org/wiki/Nef_polygon|Ned polyhedra]]. These polyhedra allow for example to specify 3-dimensional objects without a volume. Thus we can distinguish the volume inside of a cube from the infinitely thin shell of the cube. We can also represent the lines between the corners or just the corner points, or any combination representable by set operations, with these polyhedra.

The definition of these polyhedra is not constrained by the number of dimensions that are used to represent the coordinates of their vertices and neither does the file format defined by this specification. However, this version of the specification constrains the number of dimensions to any of 0, 1, 2, 3. A 0-dimensional polyhedron can be used to basically specify a boolean value, which sometimes is useful when working with algorithms that work in any number of dimensions. A 1-dimensional polyhedron can be used to specify open and closed intervals on the number line. A 2-dimensional polyhedron can describe one or multiple polygons on the plane. And a 3-dimensional polyhedron is just that, a polyhedron in 3-dimensional space, i.e. any volume or non-volume that can be built up from points, line segments, triangles and tetrahedrons.

An LOL file may contain multiple polyhedra (or even none). All polyhedra in the same file use the same coordinate system (and thus must use the same number of dimensions). These polyhedron have a defined order and each one is given a distinct name, which is just a string. Thus they work much the same as "layers" in most graphics applications. The polyhedra do not need to correlate to each other and may overlap, but are interpreted as occupying the same "canvas" by an application reading such an LOL file.


== 
