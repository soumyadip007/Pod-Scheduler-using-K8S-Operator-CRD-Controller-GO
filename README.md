# Pod-Scheduler-using-K8S-Operator-CRD-Controller-GO
Pod Scheduler using K8S Operator CRD Controller

go mod init github.com/soumyadip007/pod-scheduler-using-k8s-operator-crd-controller-go     

 operator-sdk init --plugins go/v3 --domain soumyadip.k8s --owner "Soumyadip Chowdhury" --repo github.com/soumyadip007/pod-scheduler-using-k8s-operator-crd-controller-go

  operator-sdk create api --kind Scaler --group api --version v1alpha1                                                                            

  make manifests

  kubectl apply -f config/crd/bases/api.soumyadip.k8s_scalers.yaml

  kubectl get crd

  kubectl create deploy nginx --image=nginx

  kubectl delete deployment nginx