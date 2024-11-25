# **WordPress sur Kubernetes : Création, Automatisation et Surveillance**

Le projet vise à développer une application WordPress intégrée à une base de
données MySQL. Initialement, l'infrastructure est déployée en utilisant Terraform.
Par la suite, on procède à la mise en place d'une machine virtuelle (MV) basée sur
Debian 11, sur laquelle Docker est installé. Ce dernier est essentiel pour
conteneuriser Jenkins. Jenkins, intégré avec GitHub et Git, est utilisé pour
automatiser non seulement l'infrastructure cloud Azure déployée par Terraform,
mais aussi le processus de déploiement de l'application WordPress. Cette synergie
entre Jenkins, GitHub et Git optimise le processus de CI/CD, rendant ainsi le
développement et le déploiement plus rapides et plus fiables..
Pour ce projet, Traefik est utilisé comme reverse proxy et équilibreur de charge,
un choix stratégique qui assure une gestion efficace du trafic entrant. L'installation
a été réalisée via Helm. Le projet intègre également un système de surveillance
avec Grafana et Prometheus, un aspect distinctif qui permet le monitoring continu
des performances et de la santé de l'infrastructure et des applications. Cette
intégration fournit des tableaux de bord intuitifs et des alertes.
