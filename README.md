# Kubernetes_setup

## Lancement du Pod
Le Pod peut être créé avec la commande suivante:

kubectl apply -f whoami.yaml



## Vérification
La commande suivante permet de lister les Pods présent:

kubectl get pods


Note: il est aussi possible de précisez pod (au singulier) ou simplement po au lieu de pods.

## Details du Pod
Les details d'un Pod, dont l'image utilisée par le container whoami, peuvent être obtenus avec la commande suivante:

kubectl describe pod whoami


Note: les commandes suivantes peuvent également être utilisées:

kubectl describe pods whoami
kubectl describe po whoami
kubectl describe pods/whoami
kubectl describe pod/whoami
kubectl describe po/whoami

Il est également possible d'obtenir la spécification du Pod avec la commande suivante dans laquelle -o yaml permet de spécifier le format de sortie.

kubectl get po/whoami -o yaml



## Accès à l'application via un port-forward
Depuis un premier terminal lancez la commande suivante:

kubectl port-forward whoami 8888:80


