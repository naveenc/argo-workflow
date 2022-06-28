Install Argo Workflows
1) Create the namespace \n
    kubectl create namespace <<namespace>>

2) Install Argo Workflow as well as some commonly used components
    kubectl apply  -f https://raw.githubusercontent.com/argoproj/argo-workflows/master/manifests/quick-start-postgres.yaml -n <<namespace>>

3) To start the argo Ui
 kubectl -n argo port-forward deployment/argo-server 2746:2746 &

4) Submit the argo workflows
    kubectl apply  -f  <<workflow yaml>> -n <<namespace>>


	