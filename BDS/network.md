- A regional subnet is required for Big Data Service
  - If you plan to make your cluster available for access from the public internet, you must use a public subnet
- **Cluster network** is primarily for BDS nodes talking to each other. 
- **Customer network** is for customer connecting to BDS nodes
- Each node at least join 2 subnets (customer network and cluster network) with different vNICs
  - Master nodes will have 3 VNICs (1 more for Service network used for Control Plane talking to BDS nodes)
