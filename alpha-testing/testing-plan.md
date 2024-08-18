# Testing plan

**Testing Scale**

* **Number of Nodes**
  * **Storage Nodes**: 50-100 nodes, geographically unrestricted
  * **Stream Nodes**: 5-10 nodes, using public IPs, distributed in different locations

**Testing Method**

* Continuous data uploads by multiple uploaders

**Testing Objectives**

* **Node Functionality Accuracy**
  * **Storage Nodes**: Must be able to store data, generate proof, respond to challenges, and earn rewards
  * **Stream Nodes**: Must be able to correctly process and distribute data
  * **Validator Nodes**: Must be able to verify proofs and initiate challenges upon detecting errors
* **Small-Scale Stability**
  * Assess the stability of the chain and stream nodes under stress conditions
* **Reasonableness of Machine Configuration**
  * Verify if CPU and memory requirements are adequate
  * Determine the appropriate ratio of stream to storage nodes

