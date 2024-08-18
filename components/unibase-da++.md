# Unibase DA++

#### Challenges with DAS

* Data security relies on the consensus protocol of DAS clients, which may reduce security compared to the Ethereum chain.
* High network transmission overhead with large data volumes.

#### Core Features

* **On-Chain Verification**:
  * Encode Proof: Verify RS encoding correctness on-chain.
  * Duality Proof: Ensure data availability within a specific timeframe on-chain.
  * Security assumptions: Relies on one honest validator for security.
* **High Performance**:
  * Supports large data writes with a speed of 100GB/s.
  * Fast proof generation offline, high encoding performance at 100MB/s.
  * Minimal impact on online verification, with challenges and verifications only triggered by false proofs.
* **Infinity scalable:**
  * Supports storage capacity above EB level.
  * Supports expansion to millions of storage nodes.
  * Supports custom private storage pools.

#### Decentralized, On-Chain High-Performance Data Availability Solution

* **Decentralized Storage**:
  * Users submit commitments and RS encoding parameters on-chain.
  * Blob size can be variable, and storage duration is customizable.
  * Data is encoded into multiple blocks based on custom encoding parameters and sent to different storage nodes.
* **Decentralized Verification**:
  * No DAC; storage nodes submit proofs on-chain for validation.
  * Encode Proof indicates that a storage node has stored a data block, which belongs to a specific part of the encoded user data.
  * Duality Proof demonstrates the continuous availability of data on storage nodes throughout its validity period.
* **Cost-Efficient On-Chain Verification**:
  * Aggregated verification with fixed-size Duality Proof reduces verification costs.
    * Proofs of data blocks from a single storage node are aggregated for verification on-chain.
  * Uses optimistic verification to minimize on-chain computational expenses.
    * Anyone can verify proofs offline and initiate on-chain challenges if discrepancies or missing proofs are detected.



