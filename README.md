# flux
flux

To change grafana admin password, run:
kubectl exec -n monitoring -it $(kubectl get pods -n monitoring -l "app.kubernetes.io/name=grafana" -o jsonpath="{.items[0].metadata.name}") -- grafana cli admin reset-admin-password YOUR_PASSWORD