cat > README.md <<'EOF'
# Project 2 — AWS EKS Deployment

This project deploys a Kubernetes cluster using Amazon EKS, deploys an application with Helm, configures Horizontal Pod Autoscaling, and validates scaling under load.

## Current Status

Phase 1 — Environment Setup

## Tools

- AWS CLI v2
- eksctl
- kubectl
- Helm
- Amazon EKS

## Security

## Phase 2 — EKS Cluster Creation

Phase 2 created and validated an Amazon EKS cluster using a reusable
`eksctl` configuration file.

### Cluster configuration

- Region: `us-east-1`
- Cluster: `project2-eks-cluster`
- Compute: EKS managed node group
- Node group: `project2-managed-nodes`
- Instance type: `t3.medium`
- Desired nodes: 2
- Minimum nodes: 1
- Maximum nodes: 3
- IAM OIDC provider: Enabled
- Availability zones: `us-east-1a` and `us-east-1b`

### Validation performed

- EKS control plane reached `ACTIVE`
- Managed node group reached `ACTIVE`
- Local kubeconfig was configured
- Kubernetes API connectivity was verified
- Both worker nodes reached `Ready`
- Core `kube-system` pods reached `Running`
- Evidence was captured and reviewed for sensitive information

No AWS credentials, private keys, kubeconfig files, or secrets are stored in this repository. All saved terminal evidence is redacted at capture time.
EOF
