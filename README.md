
# jaeger-all-in-one-k8s

Wanted to make a fully k8's version of the "jaeger all in one" application and "hot rods" application which sends traces to the jaeger agent. The yaml I modified from the wonderful folks at these projects who created the docker applications and yamls'..
https://github.com/jaegertracing/jaeger-kubernetes
https://www.jaegertracing.io/docs/1.22/getting-started/

Step 1) Build: 

kubectl create -f /k8s

Step 2) Get the services:
<img width="908" alt="Screen Shot 2021-03-08 at 12 44 43 PM" src="https://user-images.githubusercontent.com/29266633/110374480-f51a3e00-800d-11eb-8a8b-c50d9d045b3c.png">

Step 3) Next open the hot rod app http://<minikube-ip>:30010. 
<img width="1850" alt="Screen Shot 2021-03-08 at 12 27 16 PM" src="https://user-images.githubusercontent.com/29266633/110374557-0a8f6800-800e-11eb-9c88-7e9dc418a44b.png">

Step 4) Next open the jaeger trace UI to view the generated traces. http://<minikube-ip>:31512. 
<img width="1847" alt="Screen Shot 2021-03-08 at 12 27 28 PM" src="https://user-images.githubusercontent.com/29266633/110374607-19761a80-800e-11eb-9f98-78cfd3eb39a4.png">
