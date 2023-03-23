# Afficher la liste des Deployments
kubectl get deployment [En option DEPLOYMENT NAME]
    -o wide : récupérer en plus, le nom de l'image et le sélecteur

# Créer un Deployment
kubectl create -f template.yaml OR
kubectl apply -f tempyale.yaml

# Supprimer un Deployment
kubectl delete deployment DEPLOYMENT NAME

# Appliquer des nouveaux changements à votre Deployment sans le détruire
kubectl apply -f template.yaml

# Modifier et appliquer les changements de votre Deployment instantanément sans le détruire
kubectl edit deployment DEPLOYMENT NAME

# Afficher les détails d'un Deployment
kubectl describe deployment DEPLOYMENT NAME

# Mettre à jour l'image des Pods de votre Deployment
kubectl set image deployment/DEPLOYMENT NAME CONTAINER NAME=NEW IMAGE NAME

# Afficher le status du rolling update de votre Deployment
kubectl rollout status deployment/DEPLOYMENT NAME

# Afficher l'historique des révisions de votre Deployment
kubectl rollout history deployment/DEPLOYMENT NAME

# Revenir à une version précédente
kubectl rollout undo deployment/nginx-deployment --to-revision=REVISION NUMBER
