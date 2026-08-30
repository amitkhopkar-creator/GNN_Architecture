#  GNN for Datacentre, Telco and Enterprise Infrastructure

## Graphs
A Graph is collection of nodes/vertices and edges denoted as G = (V,E) where V represents a `set of nodes` and E represents a `set of edges` connecting these nodes. Each element/member in V (i.e. individual node v) is tagged with a set of attributes/properties which are called features. These features are encoded as a feature vector X<sub>v</sub>.

In the context of networking infrastructure, network devices, for e.g. routers, can be represented as a set of nodes (V), and links connecting these devices can be represented as a set of edges (E). Together the node/routers and edges/links form the entire network (G).

## Ontology for Networking Infrastructure
A router for e.g. is a sophisticated appliance; a distributed routing system Consists of physical hardware, firmware for data-plane programming, network operating system and applications in the form of networking protocols and management protocols. 

A chassis-based distributed router such as Cisco 8k/ASR9k, Juniper MX/PTX, Nokia SR/IXR, etc. contains Chassis, Fan trays, power supply modules, fabric cards, multiple Route processors, line cards and thousands of logical interfaces, operating systems, network applications, management applications, etc. Similarly a virtual Network function is composed of multiple VMs, Containers, DBs, etc. If we flatten such a distributed systems into a single "Router Node," we lose all the granular relationships, failure modes internal to the router, correlation of events, MELT data (like a single optical transceiver failing on a specific sub-port). 

Therefore in such an application a Heterogeneous Graph is better equipped to represent this modelling using Structural Hierarchy and Composition. 
