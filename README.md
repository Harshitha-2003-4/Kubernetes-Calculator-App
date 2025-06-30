# Calculator App with Kubernetes (kind)

This is a simple calculator web application built using HTML, CSS, JavaScript, and Node.js. The app is containerized using Docker and deployed to a local Kubernetes cluster using kind.

## Steps to Run

1. Install prerequisites:
   - Node.js
   - Docker
   - kind
   - kubectl

2. Install dependencies:
  
   npm install

3. Build Docker image:

docker build -t calculator-app:latest .


4. Create a kind cluster:

kind create cluster --config kind-config.yaml


5. Load Docker image into kind:

kind load docker-image calculator-app:latest

6. Apply Kubernetes files:

kubectl apply -f deployment.yaml

kubectl apply -f service.yaml


7. Open the app in browser:

http://localhost:30080


To Delete Cluster : kind delete cluster
