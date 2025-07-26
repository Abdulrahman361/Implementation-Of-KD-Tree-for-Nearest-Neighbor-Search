This project implements a KD-Tree (k-dimensional tree) in Python for efficient spatial queries such as nearest neighbor search and point lookup. The KD-Tree is designed to handle 2D spatial data (latitude and longitude), with applications in mapping, GIS systems, and location-based searches.

Features:

KD-Tree Construction
Recursively partitions 2D data points (latitude and longitude) to create a balanced binary tree for efficient querying.

Point Lookup:

Checks whether a specific (latitude, longitude) coordinate exists in the KD-Tree.

Nearest Neighbor Search:

Finds the closest point to a given query coordinate using a recursive backtracking algorithm that prunes unpromising branches.

Utility Methods:

argsort(seq: list[int]) -> list[int] – Returns the indices of a list in ascending order.

distance_to(lat: float, lon: float) -> float – Computes Euclidean distance (rounded to 5 decimals) between a tree node and a query point.



Core Classes and Methods

KDTree Class:

build_tree(data: list[MunicipalTree], depth: int)
Recursively constructs the KD-Tree.

lookup(lat: float, lon: float) -> bool
Checks if a point exists in the tree.

get_nearest(lat: float, lon: float) -> MunicipalTree
Finds the closest tree to a given location.

MunicipalTree Class:

Represents data points (e.g., municipal trees) with methods for distance calculations.

Applications:

Geographic Information Systems (GIS)

Efficient spatial data searches (e.g., finding the closest city landmark)

Robotics (nearest neighbor path planning)

Machine learning (for clustering and classification with spatial data)

How It Works

Tree Construction:

Splits data alternately by latitude (x-axis) and longitude (y-axis) at each tree level using the median to ensure balance.

Querying:

Point Lookup: Performs a binary search through the tree, alternating between x and y comparisons.

Nearest Neighbor: Tracks the closest point during traversal and uses pruning to avoid unnecessary branches.

Future Improvements:

Support for higher-dimensional data (k > 2).

Visualization tools for KD-Tree structure and query results.

Integration with real-world datasets (e.g., municipal or geographic datasets).


