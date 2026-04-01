# Theory of Computation: Interactive Explorations 🕸️🧠

An interactive Theory of Computation suite that visualizes emergent complexity through a randomized, multi-agent Turmite swarm operating on a continuous toroidal canvas. It additionally features a rigorous Busy Beaver module, allowing users to actively explore the mathematical limits of finite state machines and the Halting problem in real-time.

Built entirely in vanilla web technologies (HTML5 Canvas, CSS3, JavaScript) as a submission for the Theory of Computation course competition.

## 🚀 Live Demo
**https://faham-from-nowhere.github.io/Turing-X-Halting/**


## 🧠 Core Modules

### 1. The Multi-Agent Turmite Swarm (Algorithmic Art)
A "Turmite" is a 2D Turing Machine. Instead of a 1D tape, it operates on a grid, possessing an internal state, a reading/writing mechanism, and a directional heading. 

* **Coordinated Initialization Phase:** On boot, the simulation initializes multiple Turmite agents that operate deterministically to draw a specific matrix pattern (`FAHAM`) on the grid, demonstrating programmed, coordinated state execution.
* **Concurrent Randomized Art Phase:** The agents then fracture into a "swarm," each adopting complex, randomly generated transition rules (utilizing up to 8 colors and 5 internal states). 
* **Toroidal Memory Space:** The standard Turing "infinite tape" is simulated using a borderless toroidal canvas. Agents moving off one edge seamlessly wrap around to the opposite side, preventing boundary-halting and allowing continuous emergent patterns.
* **Subset Mutation:** Users can trigger rule mutations for random subsets of the agents, modeling heterogeneous multi-agent systems and concurrent memory access conflicts.

### 2. The Busy Beaver Limit Explorer (Educational Module)
The Busy Beaver game is a classic problem in computability theory that explores the boundaries of the Halting Problem. The challenge: *What is the maximum number of 1s an N-state Turing Machine can print on a blank tape before strictly halting?*

* **Verified Champions:** This module contains the rigorously proven transition tables for the 2-state, 3-state, and 4-state Busy Beaver champions.
* **Live Execution:** Users can step through or auto-play the machines to watch the computational complexity explode. (e.g., The 4-state machine requires 107 discrete state transitions to halt, writing exactly 13 ones).
* **State Tracking:** Features real-time tracking of the Read/Write head, step counts, and active state transitions to demystify how finite rules create massive algorithmic loops.

## 🛠️ Technical Implementation & Architecture
This project was built from scratch to guarantee original work and zero reliance on external rendering or physics libraries.

* **Zero Dependencies:** Pure HTML, CSS, and vanilla JavaScript. 
* **Optimized Render Loops:** * The Turmite Swarm utilizes browser-optimized `requestAnimationFrame` to handle thousands of concurrent cell updates per second without dropping frames.
  * The Busy Beaver educational module uses a decoupled `setInterval` clock, ensuring the high-speed art generation does not interfere with the precise, step-by-step logic rendering of the 1D tape.
* **Bitmapped Matrix Execution:** The initialization sequence uses a custom lightweight 2D array mapping system to translate hardcoded text into specific $x,y$ coordinate commands for the state machines.

## 💻 How to Run Locally
Because this project relies entirely on client-side execution, no build tools, servers, or package managers are required.

1. Clone or download this repository.
2. Double-click the `index.html` file to open it in any modern web browser (Chrome, Firefox, Edge, Safari).
3. The simulation is fully offline-capable.

## 📜 Academic Integrity Statement
This application was developed specifically for the Theory of Computation course fest. The state machine logic, toroidal grid physics, UI architecture, and concurrent agent systems were uniquely engineered for this submission. The Busy Beaver transition tables reflect standard, publicly verified mathematical proofs.
