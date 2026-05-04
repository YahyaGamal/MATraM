# MATraM: Multiple-Activity Transport and Mobility agent-based model

Overview
--------

This is a NetLogo model that simulates the movement of vehicles on a road network. The model includes three types of agents: nodes, buildings, and vehicles. Nodes represent intersections in the road network, buildings represent buildings in the environment, and vehicles move along the links between nodes. The model includes features such as speed limits, random maximum speeds for vehicles, and collision avoidance.

Design Concepts
--------------

* **Spatial Extent:** The model is defined on a two-dimensional grid, with nodes, links, and buildings representing intersections, roads, and buildings, respectively.
* **Temporal Extent:** The model operates in discrete time steps, or ticks. At each tick, cars and buses move along the links between nodes and update their speed based on local conditions. Pedestrians move without considering speed limits.
* **Stochasticity:** The model includes randomness in the form of random maximum speeds for cars and buses and the selection of destinations.
* **Collectives:** The model simulates the collective behavior of cars, buses and pedestrians moving on a road network.
* **Observation:** The model includes a visualization of the road network, buildings, and the movement of cars, vehicles and pedestrians.

Details
-------

### Entities, States, and Variables

* **Nodes:** Nodes represent intersections in the road network. They have a position on the grid, a list of links connected to them, and a unique ID.
* **Links:** Links represent roads between intersections. They have a distance to the destination, a speed limit, a color, a thickness, and a unique ID.
* **Buildings:** Buildings represent physical structures in the environment. They have a position on the grid, a unique ID, and a type (e.g. residential, commercial, etc.).
* **Cars:** Cars represent individual agents moving on the road network. They have a position on the grid, a destination, a maximum speed, a current speed, a local speed restriction, a journey distance to their destination, a remaining journey distance, a path to the ultimate destination, and a flag indicating whether they are moving.
* **Buses:** Buses represent public transport agents moving on the road network. They have a position on the grid, a destination (stop point), a maximum speed, a current speed, a local speed restriction, a journey distance to their destination, a remaining journey distance, and a capacity for pedestrians.
* **Pedestrians:** Pedestrians represent individual agents walking on the road network. They have a position on the grid, a destination, a maximum speed, a current speed, a journey distance to their destination, a remaining journey distance, a path to the ultimate destination, and a flag indicating whether they are moving.

### Process Overview and Scheduling

The model operates in two main procedures: `setup` and `go`. `Setup` initializes the nodes, buildings, and cars, buses and pedestrians and `go` advances the simulation by one tick. For a detailed description of the initialisation, input and the run submodels, refer to Yahya Gamal, Ricardo Colasanti, Gary Polhill, Tatsuya Mitomi, Esra Suel, Alison Heppenstall. MATraM: A multi-activity transport and mobility agent-based model for activity modifications. 2026.
