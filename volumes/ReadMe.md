aws ec2 create-volume --size 10 --region your-region --availability-zone your-zone --volume-type gp2 --tag-specifications 'ResourceType=volume, Tags=[{Key= KubernetesCluster, Value=kubernetes.domain.tld}]'

https://kubernetes.io/docs/tasks/configure-pod-container/configure-volume-storage/

https://stackoverflow.com/questions/60533371/how-to-mount-a-persistent-volume-on-a-deployment-pod-using-persistentvolumeclaim



