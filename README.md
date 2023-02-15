# ConfigMap_Pod
A ConfigMap provides a way to inject configuration data into pods. The data stored in a ConfigMap can be referenced in a volume of type configMap and then consumed by containerized applications running in a pod.

In this example we are creating ConfigMap with the nginx.conf and then inject this configMap as volume for the nginx pod.
