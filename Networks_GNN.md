#  GNN for Datacentre, Telco and Enterprise Infrastructure

## Graphs
A Graph is collection of nodes/vertices and edges denoted as $$G = (V,E)$$ where V represents a `set of nodes` and E represents a `set of edges` connecting these nodes. Each element/member in $$V$$ (i.e. individual node $$v$$ ) and individual edges $$e$$ can be tagged with a set of attributes/properties which are called features. These features are encoded as a feature vector X<sub>v</sub>.

In the context of networking infrastructure, network devices, for e.g. routers, can be represented as a set of nodes ($$V$$), and links connecting these devices can be represented as a set of edges ($$E$$). Together the node/routers and edges/links form the entire network ($$G$$). A simple router could have properties encoded in a feature vector  $$x$$ as follows 

**Router Feature Vector**

Feature vector representation for a simple, consumer-grade home router used for machine learning and classification tasks.

$$x = [4, 1, 128, 1000, 2.4, 5.0, 1200, 1, 0, 12]$$

| Vector Index | Feature Name | Value | Description / Unit |
| :--- | :--- | :--- | :--- |
| $x_1$ | **LAN_Ports** | `4` | Number of Local Area Network ports |
| $x_2$ | **WAN_Ports** | `1` | Number of Wide Area Network (Internet) ports |
| $x_3$ | **RAM_Size** | `128` | System memory in Megabytes (MB) |
| $x_4$ | **Max_Port_Speed** | `1000` | Maximum wired throughput in Megabits per second (Mbps) |
| $x_5$ | **Freq_Band_1** | `2.4` | First supported wireless frequency in Gigahertz (GHz) |
| $x_6$ | **Freq_Band_2** | `5.0` | Second supported wireless frequency in Gigahertz (GHz) |
| $x_7$ | **Max_WiFi_Speed** | `1200` | Combined theoretical wireless speed (Mbps) |
| $x_8$ | **WiFi_6_Support** | `1` | Binary flag for Wi-Fi 6 standard (`1` = Yes, `0` = No) |
| $x_9$ | **PoE_Support** | `0` | Binary flag for Power over Ethernet (`1` = Yes, `0` = No) |
| $x_{10}$ | **Power_Input** | `12` | Required input voltage in Volts (V) |


## Ontology for Networking Infrastructure
A router for e.g. is a sophisticated appliance; a distributed routing system Consists of physical hardware, firmware for data-plane programming, network operating system and applications in the form of networking protocols and management protocols. 

A chassis-based distributed router such as Cisco 8k/ASR9k, Juniper MX/PTX, Nokia SR/IXR, etc. contains Chassis, Fan trays, power supply modules, fabric cards, multiple Route processors, line cards and thousands of logical interfaces, operating systems, network applications, management applications, etc. Similarly a virtual Network function is composed of multiple VMs, Containers, DBs, etc. If we flatten such a distributed systems into a single "Router Node," we lose all the granular relationships, failure modes internal to the router, correlation of events, MELT data (like a single optical transceiver failing on a specific sub-port). 

Therefore in such an application a Heterogeneous Graph is better equipped to represent this modelling using Structural Hierarchy and Composition. 
