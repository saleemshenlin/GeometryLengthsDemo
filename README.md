# GeometryLengthsDemo
Gets the lengths for a Geometry[] when the geometry type is Polyline.

<String> calculationType
Defines the type of calculation for the geometry. The type can be one of the following:
planar: Planar measurements use 2D Cartesian mathematics to calculate length. Use this type if the length needs to be calculated in the input spatial reference otherwise use preserveShape.
geodesic: Use this type to calculate an area or length using only the vertices of the polygon to define the lines connecting the vertices as geodesic segments independent of the actual shape of the polygon. Note: a geodesic segment is the shortest path between two points on an ellipsoid.
preserveShape: Calculate the area or length of the geometry on the surface of the Earth ellipsoid, for geometries defined in a projected or geographic coordinate system. This method preserves the shape of the geometry in its coordinate system which means the true area or length will be calculated for the geometry that is displayed on the map.

<Boolean> geodesic
If polylines are in geographic coordinate system, then geodesic needs to be set to true in order to calculate the ellipsoidal shortest path distance between each pair of the vertices in the polylines. The output if lengthUnit if not specified is returned in meters.
Note:If you are using an ArcGIS Server 10.1 or greater then use the calculationType property instead.
