----Argo Events

Cluster-wide Installation argo-events
1) Create the namespace
    kubectl create namespace <<namespace>>

2) Deploy Argo Events, SA, ClusterRoles, Sensor Controller, EventBus Controller and EventSource Controller. 
    kubectl apply -f install.yaml -n <<namespace>>

3) Deploy the eventbus
    kubectl apply -f event-bus.yaml -n <<namespace>>

4) Setup event-source
    kubectl apply -f event-source/nats-event-src.yaml -n <<namespace>>

5) deploy sensor
    kubectl apply -f sensors/nats-sensor.yaml -n <<namespace>>

-- Argo workflow

Install Argo Workflows
1) Create the namespace \n
    kubectl create namespace <<namespace>>

2) Install Argo Workflow as well as some commonly used components
    kubectl apply  -f https://raw.githubusercontent.com/argoproj/argo-workflows/master/manifests/quick-start-postgres.yaml -n <<namespace>>

3) To start the argo Ui
 kubectl -n argo port-forward deployment/argo-server 2746:2746 &

4) Submit the argo workflows
    kubectl apply  -f  <<workflow yaml>> -n <<namespace>>


	

	
