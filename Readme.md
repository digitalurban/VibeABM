# A Collection of Agent-Based Model Simulations

This repository hosts a series of interactive web-based simulations exploring different forms of Agent-Based Models (ABMs). Each simulation is self-contained in a single HTML file and uses JavaScript and Three.js to render dynamic systems where autonomous agents interact with each other and their environment based on a set of rules.

---

### 1. Procedural City & Multi-Agent System

**✨ [View Live Demo: `procedural-city.html`](https://your-username.github.io/your-repository-name/procedural-city.html)**

This simulation generates a complete 3D city procedurally and populates it with several types of autonomous agents, each exhibiting distinct behaviors.

#### Agent Behaviors:

* **Vehicles:** Car agents are generated and navigate the road network. Their behavior is governed by rules for staying in lanes, maintaining a safe distance from cars in front, and obeying traffic light signals at intersections.
* **Pedestrians:** Pedestrian agents navigate the sidewalks of the city blocks. They are assigned target destinations and will move from block to block, creating a sense of a living city.
* **Boids (Bird-like Objects):** A flock of agents simulates bird flight using Craig Reynolds' classic "Boids" algorithm. These agents follow three simple rules:
    1.  **Separation:** Steer to avoid crowding local flockmates.
    2.  **Alignment:** Steer towards the average heading of local flockmates.
    3.  **Cohesion:** Steer to move toward the average position of local flockmates.
    This results in complex, emergent flocking behavior as they fly over the city.

---

### 2. Asteroid Clock - Reactive Agents

**✨ [View Live Demo: `asteroid-clock.html`](https://your-username.github.io/your-repository-name/asteroid-clock.html)**

This project reinterprets the classic arcade game *Asteroids* as a generative agent-based model that visualizes the current time. The simulation resets every minute, creating a perpetual, self-playing game.

#### Agent Behaviors:

* **The Ship:** The central agent is the player's ship, which operates autonomously. Its primary goal is survival.
    * **Threat Assessment:** The ship constantly scans for the nearest threat (asteroids or a UFO).
    * **Reactive Evasion:** If a threat gets within a certain radius, the ship's priority becomes evasion. It will turn away from the threat and engage its thrusters to escape.
    * **Targeted Offense:** When not in immediate danger, the ship will aim directly at the nearest threat and fire its lasers, attempting to clear the screen of asteroids.
* **Asteroids & UFOs:** These are simple agents that move in straight lines. The UFO appears randomly, adding another layer of challenge for the ship agent.

---

### 3. Grand Hall - Crowd & Egress Simulation

**✨ [View Live Demo: `agent-simulation.html`](https://your-username.github.io/your-repository-name/agent-simulation.html)**

This is a large-scale crowd simulation demonstrating how hundreds of agents navigate a complex indoor environment to reach a designated exit. The paths the agents take are visualized as colored trails on the floor.

#### Agent Behaviors:

* **Egress & Pathfinding:** Each agent is given a single goal: move towards the exit of the hall. Their movement is not pre-determined but is calculated in real-time.
* **Obstacle Avoidance:** The hall contains several large pillars. Agents use a look-ahead steering behavior to perceive and navigate around these obstacles smoothly, preventing collisions.
* **Separation:** Agents actively try to maintain a personal space, steering away from other agents that get too close. This prevents unrealistic crowding and creates natural-looking flows of people.
* **Path Visualization:** As each agent moves, it leaves a colored trail on the floor, creating a visual record of the emergent pathways and crowd dynamics over time.