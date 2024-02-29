# ReplicaWatcher

Welcome to the official GitHub repository for "ReplicaWatcher: Training-less Anomaly Detection in Containerized Microservices," as presented at the Network and Distributed System Security Symposium (NDSS) 2024.
Our work introduces ReplicaWatcher, a novel approach to anomaly detection in containerized microservices that requires no training. For more details, please check out our paper [here](https://www.ndss-symposium.org/ndss-paper/replicawatcher-training-less-anomaly-detection-in-containerized-microservices/?_sm_au_=iVVZpt77RHn4jNqr41Vp8K0W0RcLq).

## About ReplicaWatcher

ReplicaWatcher leverages the inherent redundancy in microservices architectures to detect anomalies by comparing the behavior of replicas. It does not require training, making it highly adaptable to new and evolving microservices environments.

## Repository Structure

This repository is organized into three main folders:

- **chisel**: Contains the code for Chisel, our custom-built tool for extracting kernel events generated by service replicas. Chisel is crucial for capturing the low-level system calls that ReplicaWatcher analyzes for anomaly detection.

- **replicawatcher**: This folder houses the core logic of ReplicaWatcher. It includes the algorithms and mechanisms for processing the events captured by Chisel, detecting anomalies, and reporting potential security breaches or misconfigurations.

- **normalityshift**: Demonstrates how an upgrade at the base OS level can lead to changes in the executed system calls. 

## Citation

If you use ReplicaWatcher in your research, please consider citing our paper:

```bibtex
@inproceedings{el2024replicawatcher,
  title={{ReplicaWatcher: Training-less Anomaly Detection in Containerized Microservices}},
  author={El Khairi, Asbat and Caselli, Marco and Peter, Andreas and Continella, Andrea},
  booktitle={Proceedings of the ISOC Network and Distributed System Security Symposium (NDSS)},
  year={2024},
}
```
