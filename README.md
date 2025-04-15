Part I: Deploy and Interact with Your Application
1.	Deploy your Node.js app using Kubernetes manifests (deployment.yaml and service.yaml).
2.	Verify successful deployment by running:
3.	kubectl get pods
4.	kubectl get services
5.	Interact with your app using port forwarding:
6.	kubectl port-forward svc/<your-service-name> <local-port>:<service-port>
Example:
kubectl port-forward svc/node-kube-service 8080:80
7.	Access the application in your browser by navigating to:
http://localhost:8080
8.	(Optional) Use the Kubernetes Dashboard to visually inspect deployments, services, and pod status.

Part II: Update and Redeploy Your Application
1.	Modify your Node.js source code (e.g., update the response message).
2.	Rebuild your Docker image with a new version tag (e.g., v3):
3.	docker build -t kema94/node-kube-app:v3.
4.	docker push kema94/node-kube-app:v3
5.	Update your deployment.yaml file to reflect the new image version.
6.	Apply the updated deployment to the cluster:
7.	kubectl apply -f deployment.yaml
8.	Confirm that the updated version is running by refreshing the web page and checking the output message.



 
