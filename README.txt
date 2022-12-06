# k8s Master 
wget https://raw.githubusercontent.com/Jaibw/k8s/master/k8s-master-ubuntu-20.04-docker.sh
sed -i 's/k8s-master/k8s-master-YOURNAME/g' k8s-master-ubuntu-20.04-docker.sh 
sh k8s-master-ubuntu-20.04-docker.sh 


# k8s Worker 
wget https://raw.githubusercontent.com/Jaibw/k8s/master/k8s-worker-ubuntu-20.04-docker.sh
sed -i 's/k8s-node/k8s-worker-YOURNAME/g' k8s-worker-ubuntu-20.04-docker.sh 
sh k8s-worker-ubuntu-20.04-docker.sh 
sudo kubeadm join ## copy it from the outpt of line no. 4 


## In master node 

kubectl get nodes 
kubectl get pods -A 


