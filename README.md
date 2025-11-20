# Movhex: Hexagonal Grid Pathfinding 🐝

An optimized pathfinding engine for a logistics company operating on a hexagonal grid map. The system calculates optimal routes in a dynamic environment where "air routes" and terrain costs change in real-time.

## 🧩 The Challenge
The software models a planetary surface using a hexagonal tiling system. It must efficiently handle:
* **Dynamic Graph:** Nodes (hexagons) and Edges (routes) update their weights frequently (`change_cost`, `toggle_air_route`).
* **Constraint Handling:** Max outgoing routes, specific traversal rules, and reachability checks.
* **Query Optimization:** Rapid response to `travel_cost` queries on large grids (up to huge coordinate systems).

## 💡 Solution Overview
* Implemented utilizing **Graph Theory** concepts (Dijkstra/A* adaptations for dynamic weights).
* Efficient memory mapping of hexagonal coordinates to array indices.
* Handling of edge cases like unreachable islands and sudden cost spikes.

## 💻 Usage
```bash
# Initialize a 100x100 grid
init 100 100
# Add an air route
toggle_air_route 0 0 20 0
# Calculate cost
travel_cost 0 0 20 0
