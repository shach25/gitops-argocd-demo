1.Kubernetes Cluster Setup:

Installed and configured K3s Kubernetes cluster on an Ubuntu EC2 instance. Verified cluster health using kubectl commands and ensured API connectivity through proper kubeconfig setup.

2.ArgoCD Installation:

Deployed ArgoCD onto the Kubernetes cluster.Then accessed the ArgoCD UI via NodePort.

3.Repository Initialization:

Initialized a new Git repository, organized the project manifests, and pushed the files (namespace, deployment, service) into a structured /app folder on GitHub.

4.Application Deployment Manifests:

Created Kubernetes manifests for a demo Nginx application:

Namespace configuration

Deployment with multiple replicas

Service for cluster-wide exposure

5.ArgoCD GitOps Integration:

Configured an ArgoCD Application that watches the GitHub repository, pointing it to the /app directory. Enabled automated sync, prune, and self-heal to ensure cluster state always matches Git.

6.Automatic Sync & Health Monitoring:

ArgoCD continuously monitored the repository for changes, detected updates in real time, and automatically deployed them to the cluster. Verified resource creation and status through ArgoCD UI and kubectl.

7.GitOps Deployment Testing:

Performed changes (scaling replica count) inside the manifests, committed and pushed them to GitHub. ArgoCD immediately detected the new commit and applied the updated configuration to the cluster.

8.Cluster Validation:

Confirmed successful deployment by checking:

Pod creation and scaling

Deployment status

Service availability
