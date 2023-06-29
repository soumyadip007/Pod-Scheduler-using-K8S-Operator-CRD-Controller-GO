# Pod Scheduler using K8S Operator CRD Controller

This project implements a powerful and flexible Pod Scheduler using Kubernetes (K8S) Operator, Custom Resource Definition (CRD), and Controller in the GO programming language. It provides advanced scheduling capabilities for pods in a Kubernetes cluster, allowing users to define and control pod distribution based on specific requirements.

## Installation

To get started with this project, follow these steps:

1. Initialize the Go module:

go mod init github.com/soumyadip007/pod-scheduler-using-k8s-operator-crd-controller-go

2. Initialize the Operator SDK:

operator-sdk init --plugins go/v3 --domain soumyadip.k8s --owner "Soumyadip Chowdhury" --repo github.com/soumyadip007/pod-scheduler-using-k8s-operator-crd-controller-go


3. Create the API definition:

operator-sdk create api --kind Scaler --group api --version v1alpha1


4. Generate the required manifests:

make manifests

5. Apply the CRD (Custom Resource Definition):

kubectl apply -f config/crd/bases/api.soumyadip.k8s_scalers.yaml

## Usage

Once the installation is complete, you can start using the Pod Scheduler. Here are a few example commands to interact with it:

- List all the available CRDs:

kubectl get crd

- Create a deployment using the Pod Scheduler:

kubectl create deploy nginx --image=nginx

- Delete a deployment:

kubectl delete deployment nginx


Feel free to explore the code and customize the scheduling behavior based on your specific requirements.

## Contributing

Contributions to this project are welcome! If you encounter any issues, have feature requests, or want to contribute improvements, please open an issue or submit a pull request on the GitHub repository.