# ConfigMap_Pod
A ConfigMap provides a way to inject configuration data into pods. The data stored in a ConfigMap can be referenced in a volume of type configMap and then consumed by containerized applications running in a pod.

In this example we are creating ConfigMap with the nginx.conf and then inject this configMap as volume for the nginx pod.

First we need to create create configMap

***kubectl create -f ConfigMap.yaml***

then

***kubectl cretae -f Pod.yaml***

expose the pod using the command:

***kubectl expose pod myapp --type=LoadBalancer --port=80 --target-port=80*** 
(you can expose this using NodePort also by changing the --type=NodePort)

get the external ip of the service:

then hit the : http://external-ip/app ----> it will redirect to the https://google.com as we configured.


***----------------------------------------------------------------------------------------------------------------------***

If you have nginx.conf file then you can also create ConfigMap from the file 

***kubectl create configmap <name of configmap> --from-file=/path/to/conf file***

***kubectl create configmap nginx-conf --from-file=nginx.conf***
