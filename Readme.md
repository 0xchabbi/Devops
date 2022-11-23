[![Board Status](https://dev.azure.com/bchabbi/d026da45-80e3-4dfb-8c29-5f92c60d9a7b/fa76cfdd-9bf5-4183-86dc-c526268c3093/_apis/work/boardbadge/48595284-74f2-4bc7-b0e0-a0bd14cf4d53)](https://dev.azure.com/bchabbi/d026da45-80e3-4dfb-8c29-5f92c60d9a7b/_boards/board/t/fa76cfdd-9bf5-4183-86dc-c526268c3093/Microsoft.RequirementCategory)
# K8s-Demo
K8s-Demo ist eine Beispiel-Kubernetes-Applikation und bildet den Standard für weitere Kubernetes-Applikationen.

## Deploy 
Nach dem Schreiben von yaml Datein kann man das Verzeichnis angeben um das Setup zu deployen und schließlich kontrolliert werden ob die Pods auch erstellt wurden und ob das Deployment auf dem jeweiligen Port funktioniert oder nicht.

```bash
kubectl apply -f mongodb/

# check if pods are running
kubectl get pod

# check if all config are running correctly
kubectl get all

# Take Internal-Ip and Port and try it on your browser, webapp with image should start.
192.168.49.2:30100 
```

# Caution

Immer drauf schauen das die Paths zusammenpassen und nichts von selbst auf dem Desktop verschoben wird. Wenn es mal nicht funktioniert, destroy and rebuild, in den meisten funktioniert das auch. Auch drauf schauen ob die Ip-Adresse richtig gewählt wurde und das image keine zusätzlichen requirments hat. 
