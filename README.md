# **Contexte du projet**

En tant qu’Administrateur Cloud, on vous demande d’utiliser Terraform afin de pouvoir déployer plusieurs infrastructures.
Il vous est demandé de faire un module qui déploie les composants réseau sur Azure (resource group, vnet, etc), ce module devra être le plus réutilisable possible afin de l’adapter à chaque situation donnée en prenant différentes valeurs en paramètre (par exemple nom des ressources, adresses IP, etc.).
Enfin déployer un cluster aks avec terraform en vous basant sur les valeurs renvoyé par le module qui gère le réseau.
Ecrire un module terraform qui déploie le réseau:

- Resource group

- vnet

- subnet

- nat gateway (bonus)

- route table (bonus)

- subnet privé/public (bonus)

- Dans un autre fichier terraform faite appel a votre module et utilisez les variables renvoyé par le module pour déployer un cluster AKS

- (Bonus) Écrire les pipelines pour déployer automatiquement l’infra sur la validation d’une pull request

- (Bonus) Écrire les pipelines pour rollback automatiquement l’infra si le déploiement a échoué
