# *Contexte du projet*

En tant qu’Administrateur Cloud, votre client (les formateurs) vous demande de mettre en oeuvre une solution de monitoring complète pour l’application Azure Vote App. Vous devrez déployer un service de collecte des logs pour les containers Kubernetes, un service de collecte des metrics des containers ainsi qu’un service d’affichage des données collecté. Le client vous demande d’utiliser les technologies suivantes:
● Prometheus
● Grafana
● Loki
​
Vous devrez collecter les metrics et les logs des containers faisant tourner l’application mais également ceux de Redis.
Redis étant une base de donnée stocké en mémoire nous devons impérativement être alerté (Warning) si l’utilisation de la mémoire alloué est supérieur à 70% et recevoir une alerte critique (Critical) si l’utilisation de la mémoire alloué est supérieur à 85%. Une alerte devra également être levée si la SWAP (https://fr.wikipedia.org/wiki/Espace_d'%C3%A9change) commence a se remplir. Bien que moins important dans ce cas d’usage l’utilisation CPU doit également lever un Warning au dessus de 75% et une alerte critique au dessus de 85%
Utilisez des seuils similaires pour l’application en Python, mais n’hésitez pas a proposer d’autre seuils s’ils vous semblent plus juste !
Attention nous aimerions que les alertes sont envoyé par mail
​
Sur Grafana, nous souhaitons pouvoir afficher les informations importante sur un Dashboard, comme les dernières metrics et les derniers logs afin de voir en un coup d’oeil si nos services vont bien.
Idéalement nous aimerions projeter les différents Dashboard sur des télévisions controlé a distance. Il nous faudrait un Dashboard pour:
● l’application Python Azure Vote App
● L’application Redis
​
*Bonus :*
● Envoyez des Alertes sur un canal Slack (https://slack.com/intl/fr-fr/)
● Ajouter une rotation des différents Dashboard grafana
● Ajouter le plug-in Azure Monitor à Grafana pour monitorer également la santé du cluster Kubernetes
● Ajouter le Synthetic monitoring pour remonter des informations que le SLA de l’application
● Explorer la solution de monitoring Azure Monitor pour reproduire les demandes ci-dessus
