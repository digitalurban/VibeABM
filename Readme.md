# A Collection of Vibe Coded Agent-Based Model Simulations

This repository hosts a series of interactive web-based simulations exploring different forms of Agent Based Models (ABMs). Each simulation is self-contained in a single HTML file and uses JavaScript and Three.js to render dynamic systems where autonomous agents interact with each other and their environment based on a set of rules.

---

### 1. Procedural City & Multi-Agent System (Created with Gemini 2.5 Pro)

![Procedural City Demo](https://github.com/digitalurban/VibeABM/blob/main/images/procedural.png)

**✨ [View Live Demo: `proceduralcity.html`](https://digitalurban.github.io/VibeABM/proceduralcity.html)**

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

### 2. Asteroid Clock - Reactive Agents (Created with Gemini 2.5 Pro)

![Asteroid Clock Demo](https://github.com/digitalurban/VibeABM/blob/main/images/asteroids.png)

**✨ [View Live Demo: `asteroidsclock.html`](https://digitalurban.github.io/VibeABM/asteroidsclock.html)**

This project reinterprets the classic arcade game *Asteroids* as a generative agent-based model that visualizes the current time. The simulation resets every minute, creating a perpetual, self-playing game.

#### Agent Behaviors:

* **The Ship:** The central agent is the player's ship, which operates autonomously. Its primary goal is survival.
    * **Threat Assessment:** The ship constantly scans for the nearest threat (asteroids or a UFO).
    * **Reactive Evasion:** If a threat gets within a certain radius, the ship's priority becomes evasion. It will turn away from the threat and engage its thrusters to escape.
    * **Targeted Offense:** When not in immediate danger, the ship will aim directly at the nearest threat and fire its lasers, attempting to clear the screen of asteroids.
* **Asteroids & UFOs:** These are simple agents that move in straight lines. The UFO appears randomly, adding another layer of challenge for the ship agent.

---

### 3. Grand Hall - Crowd & Egress Simulation (Created with Gemini 2.5 Pro)

![Grand Hall Demo](https://github.com/digitalurban/VibeABM/blob/main/images/grandhall.png)

**✨ [View Live Demo: `agent-simulation.html`](https://digitalurban.github.io/VibeABM/agent-simulation.html)**

This is a large-scale crowd simulation demonstrating how hundreds of agents navigate a complex indoor environment to reach a designated exit. The paths the agents take are visualized as colored trails on the floor.

#### Agent Behaviors:

* **Egress & Pathfinding:** Each agent is given a single goal: move towards the exit of the hall. Their movement is not pre-determined but is calculated in real-time.
* **Obstacle Avoidance:** The hall contains several large pillars. Agents use a look-ahead steering behavior to perceive and navigate around these obstacles smoothly, preventing collisions.
* **Separation:** Agents actively try to maintain a personal space, steering away from other agents that get too close. This prevents unrealistic crowding and creates natural-looking flows of people.
* **Path Visualization:** As each agent moves, it leaves a colored trail on the floor, creating a visual record of the emergent pathways and crowd dynamics over time.

---

### 4. Space Invaders Clock - (Created with Gemini 2.5 Pro)

![Space Invaders Clock](https://github.com/digitalurban/VibeABM/blob/main/images/invaders.png)

**✨ [View Live Demo: `spaceinvadersclock.html`](https://digitalurban.github.io/VibeABM/spaceinvadersclock.html)**

A generative, self-playing recreation of the 1978 arcade classic *Space Invaders*, framed as an agent-based model that also functions as a clock. The system showcases how simple rules governing individual agents can lead to complex, emergent group behavior.

#### Agent Behaviors:

* **The Player Ship (AI Agent):** A reactive agent focused on survival and clearing the board.

  * **Defensive Logic:** It perceives incoming invader bullets as threats and its primary rule is to dodge the most immediate danger.

  * **Offensive Logic:** When not dodging, it targets the lowest-ranked living invader to clear the path most efficiently.

  * **Strategic Firing:** It will only fire when it has a clear shot, avoiding its own destructible shields.

* **The Invader Swarm (Collective Agent):** The invaders act as a collective, governed by group rules.

  * **Group Movement:** The swarm marches in unison, dropping down and reversing direction when an edge is reached.

  * **Emergent Speed:** The speed of the entire swarm is inversely proportional to the number of living invader agents. As invaders are destroyed, the swarm accelerates, faithfully recreating the emergent behavior caused by the hardware limitations of the original game.

  * **Individual Firing:** Each invader agent has a small, random chance to fire a bullet.

* **The Mystery Ship (UFO):** A simple agent with a single rule: appear at random, infrequent intervals and travel horizontally across the top of the screen.

* **Shields (Environmental Objects):** While not agents, the shields are a key part of the environment that can be dynamically altered. They erode realistically at the point of impact from bullet agents, affecting the strategic options for both the player and invader agents.

---
  
### 5. Generative Slime Mold Simulation

![Slime Mold Simulation](https://github.com/digitalurban/VibeABM/blob/main/images/slime.png)

**✨ [View Live Demo: `slimemold.html`](https://digitalurban.github.io/VibeABM/slimemold.html)**

This simulation models the emergent foraging behavior of slime mold (*Physarum polycephalum*). It demonstrates how thousands of simple, autonomous agents following basic rules can create complex, efficient, and organic-looking networks.

#### Agent Behaviors:

* **Exploration & Scent-Following:** Each agent wanders the space randomly. However, its primary rule is to "sniff" the area in front of it and steer towards the direction with the strongest chemical (pheromone) trail.

* **Pheromone Deposition:** As an agent moves, it leaves behind its own pheromone trail, reinforcing the path for other agents.

* **Emergent Intelligence:** This simple feedback loop—where agents both follow and reinforce trails—is the core of the model. It causes agents to abandon inefficient paths in favor of the most-traveled routes, leading to the spontaneous formation of vein-like structures connecting the food sources.

#### Environmental Factors & Interaction:

* **Food Sources:** The green dots act as permanent, powerful scent beacons. They emit a constant "scent aura" that attracts agents from a distance, anchoring the network.

* **Trail Decay:** To ensure the network can adapt, the pheromone trails slowly decay and diffuse over time, allowing old, unused paths to fade away.

* **Interactive Controls:** The simulation allows you to directly influence the model's parameters by clicking to add new food sources or using the slider to change the agent population density in real-time.
