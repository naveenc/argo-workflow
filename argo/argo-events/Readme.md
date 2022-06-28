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

	