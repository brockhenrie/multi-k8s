# multi-k8s
minikube start

kubectl create secret generic postgres-password --from-literal PGPASSWORD=passwuhy76t

minikube addons enable ingress

kubectl apply -f k8s 

minikube dashboard

minikube tunnel

may have to run 
kubectl expose deployment client-deployment

then go to 
127.0.0.1

