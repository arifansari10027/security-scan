# Kubernetes Security Scan

## Project Overview
This project involves scanning a local Kubernetes cluster using **Kubescape** and generating a report of the security findings.

---

## How to Reproduce

### 1. Start Kubernetes Cluster
- Start a local Kubernetes cluster using Minikube:
  ```bash
  minikube start
  ```

### 2. Install Kubescape
- Install Kubescape by running:
  ```bash
  curl -s https://raw.githubusercontent.com/kubescape/kubescape/master/install.sh | /bin/bash
  ```

- Add Kubescape to PATH if required:
  ```bash
  export PATH=$PATH:$HOME/.kubescape/bin
  ```

### 3. Run Security Scan
- Perform a scan and output the results to a JSON file:
  ```bash
  kubescape scan framework nsa --format json > results.json
  ```

---

## Output
- The findings are saved in the `results.json` file.
- This file includes vulnerabilities, risks, and compliance details.