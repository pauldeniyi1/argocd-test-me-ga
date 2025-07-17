install argocd in minukeube using helm or kubectl apply 
configure it to use application set to deploy simple yaml file nginx app from the git repo below
connect it to this repo git@github.com:pauldeniyi1/argocd-test-me-ga.git
run the script ./apply.sh




update your argocd application-server replica to 3 
provide the values file used 
then show the command you used to upgrade it 


COMMAND TO UPGRADE
helm upgrade argocd argo/argo-cd \
  --namespace argocd \
  --set server.replicas=3

COMMAND -> TO OUTPUT the Values.yaml
helm show values argo/argo-cd > values.yaml


helm pull argocd --untar
create application set and point it to argocd folder that wads pulled in the application