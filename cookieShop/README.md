1. Configure your `kubectl` to work against the k8s cluster
2. Create `namespace` and name it as your `shortname` / `username` (e.g paveld)
    1. `kubectl crete namespace paveld`

3. Configure your context to work with your `namespace`
    1. `kubectl config set-context cluster.local-context --user=admin --namespace=paveld`

4. Apply the new application configuration.
    1. `kubectl apply -f cookieShop/deployment-v1.yaml`
5. Expose the application
    1. `kubectl expose deployment simple-deployment --type=NodePort`
6. Check out the service
    1. `kubectl get service`
7. Get any `node` IP address.
    1. `kubectl get nodes`
8. Open your browser and go to:
    1. http:\\_nodeIP:nodePort_