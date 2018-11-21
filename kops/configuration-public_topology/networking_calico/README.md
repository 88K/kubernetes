kops create -f cluster_spec_global.yml

kops create secret --name cluster.k8s.example.com sshpublickey admin -i ~/.ssh/id_rsa.pub

kops update cluster cluster.k8s.example.com

kops update cluster cluster.k8s.example.com --yes

kops validate cluster

kubectl get nodes

kubectl get pods --all-namespaces
