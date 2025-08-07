# Jackson-Network


A manufacturing company operates a production system composed of three primary workstations: Assembly, Quality Inspection, and Packaging. To better understand the system's performance, the company models this setup as a Jackson queueing network, focusing on the system's steady-state behavior.

Jobs arrive at the Assembly node (Node 1) following a Poisson process. After service, they are probabilistically routed to the Quality Inspection node (Node 2), the Packaging node (Node 3), or exit the system. Each node is modeled as an M/M/1 queue with its own service rate. The routing between nodes is governed by predefined transition probabilities, and some jobs may re-enter the system at earlier nodes.

To analyze system performance, a combination of theoretical and simulation-based approaches is employed. First, balance equations are formulated and solved to determine the effective arrival rates at each node and to verify system stability conditions. A symbolic solver is developed to automate this process for various routing matrices and service rate configurations.

Next, a discrete-event simulation is implemented to mimic the movement of jobs through the network. The simulator processes approximately 10,000 events, tracking metrics such as queue lengths, delays, and throughput at each node after reaching steady state. To validate the simulation model, theoretical performance measures derived from Jackson network theory are compared to the simulated results. Metrics such as average queue length and time in the system (via Little’s Law) are used for validation. 

The project also investigates performance bottlenecks by systematically varying the service rate at each node. These experiments reveal how delays and congestion develop under different capacity scenarios and help identify the nodes that most critically affect system performance. The entire project is developed using Python.

