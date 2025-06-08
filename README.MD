eval $(minikube docker-env)
docker build -t visakh123/my-flask-app:latest .
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
minikube service flask-service