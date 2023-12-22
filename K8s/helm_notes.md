What is Helm ? 
- Bundle of Yaml Files.
- Create your own Helm Charts with Helm
- Push them to Helm Repository.
- Download and use existing helm charts.

Common Use
Database Apps
Monitoring Apps: Prometheus 


Resume configuration that someone has already made. 

Sharing Helm Charts , 

Deploy Deployment in K8s Cluster, Uisng Helm.

Two ways

# CLI
helm search <keyworld>

# OR Helm Hub

Gui , Search Public available charts. 

nfs-external provisioner. 

# Helm Public and Private Registries(Company Engine)

# Templating Engine
Case : 1. Lets a deploying a microservice using deployment and services are same but only names and some fields varies. 

Create Own Template
-----------------------
1. Define a common blueprint
2. Dynamic values are replaced by placeholders.

apiVersion: v1
kind: Pod
metadata:
  name: {{ .Values.name }}
spec:
  containers:
  - name: {{ .Values.containers.name }}
    image:  {{ .Values.containers.image }}
    ports:
    - containerPort:  {{ .Values.containers.port }}
  ######################################################################
{{.Values }} 


