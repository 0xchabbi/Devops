# K8s-Demo
K8s-Demo ist eine Beispiel-Kubernetes-Applikation und bildet den Standard für weitere Kubernetes-Applikationen.

## Deploy 
Nach dem Schreiben von yaml Datein muss jede einzelne Datei deployed werden und schließlich kontrolliert werden ob die Pods auch erstellt wurden und ob das Deployment auf dem jeweiligen Port funktioniert oder nicht.

```bash
kubectl apply -f mongo-config.yaml
kubectl apply -f mongo-secret.yaml
kubectl apply -f mongo.yaml
kubectl apply -f webapp.yaml

# check if pods are running
kubectl get pod

# check if all config are running correctly
kubectl get all

# Take Internal-Ip and Port and try it on your browser, webapp with image should start.
192.168.49.2:30100 
```
# Caution

Immer drauf schauen das die Paths zusammenpassen und nichts von selbst auf dem Desktop verschoben wird. Wenn es mal nicht funktioniert, destroy and rebuild, in den meisten funktioniert das auch. Auch drauf schauen ob die Ip-Adresse richtig gewählt wurde und das image keine zusätzlichen requirments hat. 
