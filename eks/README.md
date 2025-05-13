# Instructions for Running `eksctl` for Hub, Spoc1, and Spoc2

## Prerequisites
- Install `eksctl`: [Installation Guide](https://eksctl.io/introduction/#installation)
- Ensure AWS CLI is configured with appropriate permissions.

## Steps

### 1. Create Hub Cluster
Run the following command:
```bash
eksctl create cluster -f hub-cluster.yaml
```

### 2. Create Spoc1 Cluster
Run the following command:
```bash
eksctl create cluster -f spoc1-cluster.yaml
```

### 3. Create Spoc2 Cluster
Run the following command:
```bash
eksctl create cluster -f spoc2-cluster.yaml
```

## Notes
- Replace `<region>` in the YAML files with your desired AWS region (e.g., `us-west-2`).
- Adjust `desiredCapacity` and `instanceType` in the YAML files based on your workload requirements.
- Use `eksctl delete cluster --name <cluster-name>` to delete clusters when no longer needed.
