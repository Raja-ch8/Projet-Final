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

## **1.2 - Exigences Fonctionnelles**

Requis Fonctionnels du Projet de Développement de l'Application WordPress
avec Base de Données MySQL
Développement de l'Infrastructure Cloud avec Terraform sur Azure :
- Utilisation de Terraform pour l'automatisation de l'infrastructure cloud sur Azure,
incluant le groupe de ressources, localisation, adresse IP, disque, réseau, etc.
- Garantir que l'infrastructure soit adéquate pour supporter l'application
WordPress et la base de données MySQL.
Mise en Place d'une Machine Virtuelle avec Debian 11 et Docker :
- Installation et configuration d'une machine virtuelle (MV) basée sur Debian 11.
- Installation de Docker sur la MV pour la conteneurisation de Jenkins.
Automatisation avec Jenkins Intégré à GitHub et Git :
- Utilisation de Jenkins, intégré avec GitHub et Git, pour automatiser à la fois
l'infrastructure cloud Azure et le déploiement de l'application WordPress.
- Configuration de Jenkins pour la gestion du processus de CI/CD.
Orchestration avec Kubernetes :
- Utilisation de Kubernetes pour l'orchestration et la gestion de l'application
WordPress et de la base de données MySQL en conteneurs.
  
Traefik comme Reverse Proxy et Load Balancer :
- Configuration de Traefik en tant que reverse proxy et équilibreur de charge pour
optimiser la gestion du trafic et la sécurité du réseau.
- Installation et configuration de Traefik via Helm dans le cluster Kubernetes.
Surveillance avec Grafana et Prometheus :
- Intégration de Grafana et Prometheus pour le monitoring continu des
performances et de la santé de l'infrastructure et des applications.
- Configuration de tableaux de bord personnalisés et de systèmes d'alarme pour
une gestion proactive des événements.
Sécurité et Conformité :
- Mise en œuvre d'un certificat TLS pour permettre l'accès uniquement via
HTTPS, augmentant ainsi la sécurité et la protection des données.
Documentation :
- Fourniture de documentation détaillée sur la configuration et l'utilisation des
technologies mises en œuvre.
