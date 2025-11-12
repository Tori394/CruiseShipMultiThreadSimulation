<h1 align="center">🚢 MultiThread Simulation</h1>

<p align="center">
  A simulation of a port where passengers attempt to board a limited-capacity ship via a narrow bridge.
  This project illustrates the problem of process/thread synchronization in a concurrent environment.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Language-C-blue.svg">
  <img src="https://img.shields.io/badge/Status-Finished-brightpurple">
</p>

---

## 🧰 Makefile Instructions

| Command         | Description |
|-----------------|--------------|
| `make`          | Compiles the programs |
| `make testx`    | Runs simulations with predefined test data |
| `make user`     | Runs simulations with user-provided input |
| `make clean`    | Cleans temporary and build files |

---

## 🧩 Project Description

At the dock stands a ship with a capacity of **N passengers**.  
The ship is connected to the land by a bridge with a capacity of **K**, where `K < N`.

Passengers try to board the ship under the following constraints:
- No more than **N** passengers can be on the ship at the same time.  
- No more than **K** passengers can be on the bridge simultaneously.  
- The bridge is narrow — movement can occur in **only one direction at a time**.  

The ship sets sail every **T₁** units of time (e.g., one hour).  
At the moment of departure:
- There must be **no passengers on the bridge**.  
- The number of passengers on the ship must not exceed **N**.  

Additionally, the ship can depart **earlier** upon receiving an order (**signal1**) from the port captain.  
The voyage lasts **T₂**, after which passengers disembark.  
Once the last passenger leaves the ship, new passengers can begin boarding.  

The ship can complete up to **R voyages** per day or stop its operation after receiving a termination order (**signal2**).  
If this signal arrives:
- During boarding — the ship does not depart, and passengers disembark.  
- During a voyage — the ship finishes the current voyage and stops further departures.

---

## ⚙️ Simulation Focus

This simulation models:
- **Concurrent passenger processes** attempting to board/disembark.  
- **Synchronization mechanisms** ensuring bridge and ship capacity limits.  
- **Event-driven triggers** (departure and termination signals).  
- **Mutual exclusion** of movement direction on the bridge.  

It’s an example of how concurrency and inter-process communication can be used to simulate real-world logistics and coordination problems.

---

Pełen raport:

![Dokumentacja PDF](https://github.com/Tori394/CruiseShipSymulation/blob/main/Raport.pdf)
