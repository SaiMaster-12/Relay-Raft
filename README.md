# Relay-Raft

## Project Description

This project implements a simulated distributed system consisting of three nodes that perform a leader election based on randomized values. The elected leader is responsible for handling client communications, while the other nodes operate as followers.

Each node generates a random number and exchanges it with the other nodes. The node with the highest value is elected as the leader, and the remaining nodes become followers. A client randomly sends messages to one of the three nodes, and the leader node is responsible for responding to these client requests.

## Project Structure

| Filename    | Description                                      |
|-------------|------------------------------------------------|
| `node1.py`  | Implementation of Node 1                         |
| `node2.py`  | Implementation of Node 2                         |
| `node3.py`  | Implementation of Node 3                         |
| `Client.py` | Client that sends requests to the nodes randomly|

## Key Features

- **Randomized Leader Election:** Each node generates a random number to participate in leader election.
- **Leader Selection:** The node with the highest number is elected leader.
- **Follower Role:** Nodes other than the leader assume follower roles.
- **Client Communication:** The client sends messages randomly to any node; the leader node handles all responses.

## Prerequisites

- Python 3.6 or higher
- No external dependencies required (unless otherwise specified in the scripts)

## Usage Instructions

1. Start all three node instances by running `node1.py`, `node2.py`, and `node3.py` concurrently.
2. Run the client script `Client.py` to simulate sending messages to the distributed nodes.
3. Observe the leader election process and how the leader node responds to client requests.

## Notes

- This system is a simulation intended for educational and experimental purposes to demonstrate basic concepts of leader election in distributed systems.
- Communication between nodes and client may use networking or inter-process communication as implemented in the provided scripts.
- The election process occurs at node startup, ensuring a fresh leader election each time the system runs.

---

For questions or contributions, please feel free to open an issue or submit a pull request.
