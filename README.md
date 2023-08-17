# asp-core-docker-k8s


Step 1: Create a .NET Core Project

Step 2: Dockerize the Application Create a Dockerfile in the project root directory to containerize the application:

Step 3: Build and Test the Docker Image Build and test the Docker image locally:

docker build -t my-dotnet-app . 

-- not requied for k8s  docker run -p 8080:80 my-dotnet-app

Step 4: Deploy to Kubernetes (k8s) Create Kubernetes deployment and service manifests. Create a deployment.yaml file:

Step 5: Create a service.yaml file:

Step 6 : Apply the manifests to your Kubernetes cluster:

kubectl apply -f deployment.yaml
kubectl apply -f service.yaml

-----------useful cmd

Application running on 
localhost : 8080
------------
Useful commends 
kubectl get services
kubectl get pods 
kubectl describe pod <pod_name>
kubectl port-forward pod/<pod_name> 7000:7000 

--- delete 
kubectl delete service service_name
kubectl delete pod <pod-name>
kubectl delete pods -l app=my-aspnet-app
![image](https://github.com/rineshsps/asp-core-docker-k8s/assets/10809494/9750a3ba-4137-4b8e-84d9-89573bbc4a90)
