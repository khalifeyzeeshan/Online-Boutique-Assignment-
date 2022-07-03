
Troubleshooting pod adservice-78d848d44d-whkd2
1 .  kubectl describe pod adservice-78d848d44d-whkd2 analyzied by reading the logs of the pod
check the last event part to get the error in this case the image was not presnet in the repo

2. changed the image from 0.3.1 to 0.3.4 which is present on open source google platform and edited adservice.yaml 
3. restart the pod 
4. Image is deployed. 

kubectl get pod checkoutservice-79dc4c7fb6-ppctp -o yaml

kubectl get pod adservice-58647f7bc6-9gw5h -o yaml

++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
Reddis Pod yaml has a string which indicate a wrong hostname "Node-Selectors:  kubernetes.io/hostname=test-worker-2"
After Commmenting the node-selector line in yaml and redeploying the pod the pod started with out error
