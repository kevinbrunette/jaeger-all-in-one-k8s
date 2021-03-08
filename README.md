# jaeger-all-in-one-k8s

Wanted to make a fully k8's version of the "jaeger all in one" application and "hot rods" application which sends traces to the jaeger agent. The yaml I modified from the wonderful folks at these projects who created the docker applications and yamls'..
https://github.com/jaegertracing/jaeger-kubernetes
https://www.jaegertracing.io/docs/1.22/getting-started/

Step 1) Build: 

kubectl create -f /k8s

Step 2) Get the pods:

To see the pods:
kubectl get pods

NAME               TYPE           CLUSTER-IP       EXTERNAL-IP   PORT(S)                               AGE
hot-rod            LoadBalancer   10.96.113.112    <pending>     8080:30010/TCP                        7m27s
jaeger-agent       ClusterIP      None             <none>        5775/UDP,6831/UDP,6832/UDP,5778/TCP   37m
jaeger-collector   ClusterIP      10.100.247.152   <none>        14267/TCP,14268/TCP,9411/TCP          37m
jaeger-query       LoadBalancer   10.100.118.105   <pending>     80:31512/TCP                          37m
kubernetes         ClusterIP      10.96.0.1        <none>        443/TCP                               11d
zipkin             ClusterIP      None             <none>        9411/TCP                              37m
 
Step 3) Next open the hot rod app http://<minikube-ip>:30010. Click buttons to generate traces. 
Step 4) Next open the jaeger trace UI to view the generated traces. http://<minikube-ip>:31512. 


  
