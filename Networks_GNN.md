#  GNN for Datacentre, Telco and Enterprise Infrastructure

## Graphs
A Graph is collection of nodes/vertices and edges denoted as G = (V,E) where V represents a `set of nodes` and E represents a `set of edges` connecting these nodes. Each element/member in V (i.e. individual node v) is tagged with a set of attributes/properties which are called features. These features are encoded as a feature vector X<sub>v</sub>.

In the context of networking infrastructure, network devices, for e.g. routers, can be represented as a set of nodes (V), and links connecting these devices can be represented as a set of edges (E). Together the node/routers and edges/links form the entire network (G).

## Ontology for Networking Infrastructure
A router for e.g. is a sophisticated appliance; it is a nested, distributed system of physical hardware, firmware for data-plane programming, network operating system and applications in the form of networking protocols. 

A chassis-based distributed router such as Cisco 8k/ASR9k, Juniper MX/PTX, Nokia SR/IXR, etc. contains multiple Route processors, Fabric cards, Fan Trays, line cards and thousands of logical interfaces, operating systems, network applications. Similarly a virtual Network function is composed a multiple VMs, Containers, DBs, etc. If we flatten such a distributed systems into a single "Router Node," is a single node we lose all the granular MELT data (like a single optical transceiver failing on a specific sub-port). 

In a Heterogeneous Graph, we handle this using Structural Hierarchy and Composition. 
