# 🔐 Kubernetes RBAC Examples

A collection of Kubernetes Role-Based Access Control (RBAC) manifests that demonstrate how to define and manage role-based permissions and access in a Kubernetes cluster.
This repository includes examples of Role, RoleBinding, ClusterRole, ClusterRoleBinding, and authentication mappings to enforce fine-grained access control for users and service accounts.

# 📌 About

Kubernetes Role-Based Access Control (RBAC) is a security mechanism that regulates access to cluster resources based on roles assigned to users, groups, or service accounts. It lets you define who can do what on which resources within your cluster. RBAC is a fundamental practice for securing Kubernetes environments and enforcing the principle of least privilege. 
Kubernetes
+1

This repository provides example YAML manifests to help you learn and implement RBAC policies for different scenarios.
Use these templates as a starting point for role definitions, permission bindings, and service account access controls.

# 📁 Repository Contents
k8s-rbac/
├── 1-role.yaml                    # Defines a namespaced Role with specific permissions
├── 2-role-binding.yaml            # Binds a Role to a user or service account
├── 3-aws-authentication.yaml      # Example of integrating IAM or AWS authentication
├── 4-admin-role.yaml              # ClusterRole granting administrative permissions
├── 5-admin-binding.yaml           # Binds ClusterRole to an admin identity
├── 6-trainee-role-binding.yaml    # Example limited access policy for trainee
└── README.md


Each manifest illustrates a different aspect of RBAC—from basic role setup in a namespace to cluster-wide permissions and service account access configurations.

# 🛠️ Key Concepts
## 📌 Roles & ClusterRoles

Role — Defines a set of permissions (verbs) within a specific namespace.

ClusterRole — Similar to a Role but applies across the entire cluster. 
Spacelift

## 📌 Bindings

RoleBinding — Grants a Role’s permissions to a user, group, or service account within a namespace.

ClusterRoleBinding — Grants a ClusterRole’s permissions cluster-wide. 
Spacelift

# 🚀 How to Use

Apply any of the example manifests using kubectl:

kubectl apply -f 1-role.yaml


Verify access and RBAC binding results using:

kubectl auth can-i get pods --namespace=<namespace> --as=<user>


Replace <namespace> and <user> to test different permission scenarios.

# 📈 Why This Matters

RBAC helps you:

✔ Enforce security boundaries within the cluster
✔ Limit access according to least privilege
✔ Define scoped permissions for teams, apps, or automation bots
✔ Improve compliance and auditability of access policies 
Kubernetes

# 🤝 Contributing

Contributions are welcome! You can help by:

Adding more RBAC use-cases (e.g., GitOps, CI/CD service accounts)

Including annotated examples or explanations

Adding best-practice tips for RBAC design

Fork the repo

Create a feature branch

Commit changes

Open a Pull Request
