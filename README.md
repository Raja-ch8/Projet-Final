# **1. WordPress sur Kubernetes : Création, Automatisation et Surveillance**

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

**Développement de l'Infrastructure Cloud avec Terraform sur Azure :**
- Utilisation de Terraform pour l'automatisation de l'infrastructure cloud sur Azure,
incluant le groupe de ressources, localisation, adresse IP, disque, réseau, etc.
- Garantir que l'infrastructure soit adéquate pour supporter l'application
WordPress et la base de données MySQL.

**Mise en Place d'une Machine Virtuelle avec Debian 11 et Docker :**
- Installation et configuration d'une machine virtuelle (MV) basée sur Debian 11.
- Installation de Docker sur la MV pour la conteneurisation de Jenkins.

**Automatisation avec Jenkins Intégré à GitHub et Git :**
- Utilisation de Jenkins, intégré avec GitHub et Git, pour automatiser à la fois
l'infrastructure cloud Azure et le déploiement de l'application WordPress.
- Configuration de Jenkins pour la gestion du processus de CI/CD.

**Orchestration avec Kubernetes :**
- Utilisation de Kubernetes pour l'orchestration et la gestion de l'application
WordPress et de la base de données MySQL en conteneurs.
  
**Traefik comme Reverse Proxy et Load Balancer :**
- Configuration de Traefik en tant que reverse proxy et équilibreur de charge pour
optimiser la gestion du trafic et la sécurité du réseau.
- Installation et configuration de Traefik via Helm dans le cluster Kubernetes.
Surveillance avec Grafana et Prometheus :
- Intégration de Grafana et Prometheus pour le monitoring continu des
performances et de la santé de l'infrastructure et des applications.
- Configuration de tableaux de bord personnalisés et de systèmes d'alarme pour
une gestion proactive des événements.

**Sécurité et Conformité :**
- Mise en œuvre d'un certificat TLS pour permettre l'accès uniquement via
HTTPS, augmentant ainsi la sécurité et la protection des données.
Documentation :
- Fourniture de documentation détaillée sur la configuration et l'utilisation des
technologies mises en œuvre.

**Documentation :**
- Fourniture de documentation détaillée sur la configuration et l'utilisation des
technologies mises en œuvre.

## **1.3 - Exigences Non Fonctionnelles**

**Maintenabilité:**
- Facilité de maintenance et de mise à jour du code source et de l’infrastructure.
- Le code doit être clair, bien documenté et facile à maintenir.

**Sécurité:**
- Implémentation de TLS pour le trafic web, garantissant que toutes les
communications entre le client et le serveur soient sécurisées.
- Chiffrement de bout en bout des données sensibles.

**Disponibilité:**
- Mise en place de stratégies de reprise après sinistre pour assurer une
récupération rapide en cas de défaillance.

1.4 - Contraintes
Contraintes de Sécurité:
Des mesures de sécurité robustes doivent être mises en place pour la gestion des
accès et la protection des données sensibles.
Contraintes de Réseau avec Traefik:
- Utilisation de Traefik comme reverse proxy et load balancer, avec des
configurations spécifiques pour le routage et la sécurité.
- Gestion des certificats SSL/TLS pour le trafic HTTPS via Traefik.

**Contraintes de CI/CD avec Jenkins:**
- Intégration obligatoire avec GitHub pour la gestion du code source.
- Définition de pipelines de déploiement spécifiques dans Jenkins, avec des
étapes de test, de build et de déploiement clairement définies.

**Contraintes de Monitoring avec Grafana et Prometheus:**
- Surveillance obligatoire de l'infrastructure et des applications avec Prometheus.
- Utilisation de Grafana pour la visualisation des données de performance, avec
des tableaux de bord personnalisés.

# **2 - Documentation d’Architecture Technique**

**2.1 Besoins Fonctionnels**
Développement et déploiement de l'application WordPress:
- Capacité de créer, gérer et afficher du contenu via l'interface WordPress.
Gestion de la Base de Données MySQL:
- Stockage, récupération, modification et gestion sécurisée des données de
l'application WordPress.
- Sauvegarde et restauration de la base de données pour garantir la récupération
des données.

**Automatisation de l'Infrastructure avec Terraform:**
- Définition et déploiement automatique de l'infrastructure cloud requise pour
l'application et la base de données.

**Conteneurisation avec Docker:**
- Encapsulation de l'application WordPress, du serveur de base de données
MySQL et d'autres services dans des conteneurs Docker pour la portabilité et
l’isolation.

**Intégration(CI/CD) avec Jenkins:**
- Automatisation des tests, de la construction et du déploiement de l'application à
l'aide de pipelines CI/CD dans Jenkins.
- Intégration avec des systèmes de contrôle de version comme Git pour la gestion
du code source.

**Orchestration avec Kubernetes:**
- Gestion et orchestration des conteneurs Docker dans un environnement de
production.
  
**Gestion du Trafic avec Traefik:**
- Routage et équilibrage de charge du trafic entrant vers l'application WordPress.
Gestion de la sécurité des connexions, notamment avec la mise en place de
HTTPS.

## **2.2 Besoins Non Fonctionnels**

**Performance:**
- Temps de réponse rapide de l’application,
- Capacité à gérer un nombre élevé d'utilisateurs simultanés sans dégradation des
performances.

**Disponibilité et Fiabilité:**
- Haute disponibilité de l’application Wordpress, visant un objectif de minimiser
le temps de fonctionnement.
- Mécanismes de reprise après sinistre pour assurer la continuité des services en
cas de panne.

**Sécurité:**
- Cryptage des données en transit et au repos, en particulier les données sensibles

**Maintenabilité:**
- Code source clair, bien documenté, facile à maintenir et à mettre à jour.


<img width="764" alt="Capture d’écran 2024-11-25 à 14 22 59" src="https://github.com/user-attachments/assets/19dd9566-4452-478e-8033-28abfae82caf">
