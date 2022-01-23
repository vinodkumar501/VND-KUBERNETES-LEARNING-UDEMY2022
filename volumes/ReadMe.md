aws ec2 create-volume --size 10 --region your-region --availability-zone your-zone --volume-type gp2 --tag-specifications 'ResourceType=volume, Tags=[{Key= KubernetesCluster, Value=kubernetes.domain.tld}]'


aws ec2 delte-volume --volume-id _________________



https://kubernetes.io/docs/tasks/configure-pod-container/configure-volume-storage/

https://stackoverflow.com/questions/60533371/how-to-mount-a-persistent-volume-on-a-deployment-pod-using-persistentvolumeclaim

make sure your volume in same zregion of your k8s cluster


Once test to drain a node 

According to the Kubernetes documentation the drain command can be used to “safely evict all of your pods from a node before you perform maintenance on the node,” and “safe evictions allow the pod's containers to gracefully terminate and will respect the PodDisruptionBudgets you have specified”.

Even if node has issue then that pod will place on another node and use same pvc attached to it ( stateful app using pv ) 




