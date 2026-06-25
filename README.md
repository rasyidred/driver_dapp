# DRIVERDAPP

## Abstract

Existing driver distraction detection systems face critical barriers to real-world deployment in safety-critical transportation environments, including the lack of real-time edge inference, explainable artificial intelligence (XAI), trustworthy event logging, and privacy-preserving evidence management. To overcome these challenges, this paper presents an integrated framework, termed *DRIVERDAPP*, that unifies real-time edge-based detection, AI explainability, and secure, auditable event management. RGB in-cabin image frames captured by a dashboard camera are processed locally on an NVIDIA Jetson Nano edge device, where a fine-tuned YOLOv11s model classifies ten driver behavior states and triggers in-vehicle audio alerts for unsafe activities. To suppress transient misclassifications under edge constraints, distraction persistence is verified using a lightweight temporal confirmation strategy. Confirmed distraction events are immutably recorded via Solidity-based smart contracts and submitted through the Web3.py interface to a permissioned Hyperledger Besu consortium blockchain operating under Quorum Byzantine Fault Tolerance (QBFT) consensus. Privacy is preserved by retaining raw visual data off-chain, while only pseudo-anonymous identifiers and event metadata are stored on-chain under controlled access policies. Model interpretability is enabled using Gradient-weighted Class Activation Mapping (Grad-CAM), providing transparent visual explanations of distraction-related predictions. The framework is evaluated using the State Farm Distracted Driver and American University in Cairo datasets, demonstrating stable real-time edge operation, negligible blockchain query latency, and secure smart contract execution. These results confirm the suitability of *DRIVERDAPP* for secure, explainable, and deployable driver monitoring in intelligent transportation systems.

---

## Repositories

| Repository | Purpose |
| --- | --- |
| [driver_dapp_contract](https://github.com/rasyidred/driver_dapp_contract) | Solidity smart contracts (`AccessRegistry`, `DistractionRecorder`), Foundry tests, and deployment scripts |
| [driverdapp_netbench](https://github.com/rasyidred/driverdapp_netbench) | Hyperledger Besu permissioned network configuration and benchmarking |

---

## Authors

- **Odinachi Udemezuo Nwankwo** [![ORCID](https://img.shields.io/badge/ORCID-0009--0008--9595--921X-a6ce39?logo=orcid&logoColor=white)](https://orcid.org/0009-0008-9595-921X) — Department of IT Convergence Engineering, Kumoh National Institute of Technology, Gumi, South Korea

- **Simeon Okechukwu Ajakwe** [![ORCID](https://img.shields.io/badge/ORCID-0000--0002--6973--530X-a6ce39?logo=orcid&logoColor=white)](https://orcid.org/0000-0002-6973-530X) — Smart Computing Department, Kyungdong University Global Campus, Goseong-gun, South Korea

- **Muhammad Rasyid Redha Ansori** [![ORCID](https://img.shields.io/badge/ORCID-0000--0002--5704--9134-a6ce39?logo=orcid&logoColor=white)](https://orcid.org/0000-0002-5704-9134) — NSLab Inc., Gumi, South Korea

- **Gifar Arif Haryadi** [![ORCID](https://img.shields.io/badge/ORCID-0009--0007--1129--0727-a6ce39?logo=orcid&logoColor=white)](https://orcid.org/0009-0007-1129-0727) — Department of IT Convergence Engineering & ICT Convergence Research Center, Kumoh National Institute of Technology, Gumi, South Korea

- **Dong-Seong Kim** [![ORCID](https://img.shields.io/badge/ORCID-0000--0002--2977--5964-a6ce39?logo=orcid&logoColor=white)](https://orcid.org/0000-0002-2977-5964) — Department of IT Convergence Engineering & ICT Convergence Research Center, Kumoh National Institute of Technology, Gumi, South Korea; NSLab Inc., Gumi, South Korea

- **Jae Min Lee** ✉ [![ORCID](https://img.shields.io/badge/ORCID-0000--0001--6885--5185-a6ce39?logo=orcid&logoColor=white)](https://orcid.org/0000-0001-6885-5185) — Department of IT Convergence Engineering, Kumoh National Institute of Technology, Gumi, South Korea *(Corresponding author)*
