
# SAE 1.02 - Déploiement d'une Architecture Réseau d'Entreprise

L'objectif de ce projet est de réalisé l'infrastructure réseau d'une entreprise 
Les tâches consistaient à configurer les VLANs, établir un accès SSH pour l'administration, configurer le routage Inter-VLAN et permettre l'accès extérieur via NAT/ACL

##  Sommaire

* Objectifs du Projet
* Cahier des Charges
* Architecture Réseau
* Structure du Dépôt
* Technologies et Outils

---

##  Objectifs du Projet

Le projet vise à valider les compétences professionnelles liées à l'administration réseau:

**Conception** d'un plan d'adressage IPv4 structuré.

**Configuration** d'équipements actifs (Routeurs et Commutateurs Cisco).

**Segmentation** du réseau via des VLANs pour isoler les différents services.

**Déploiement** de services réseau essentiels (DHCP, DNS, Web Apache).

##  Cahier des Charges

La mission consiste à installer l'infrastructure d'un bureau d'étude disposant de 5 machines physiques par société.

### Configuration Requise

* **Segmentation par VLANs** :
  
**ADMIN** : Accès privilégié pour les administrateurs et hébergement du serveur Web.

**PERSONNEL** : Communication entre les postes de travail des employés.

**PRODUCTION** : Réseau dédié aux machines de l'usine.

**VIDEO** : Flux d'informations internes.

* **Services** :
* Serveur DHCP configuré sur le routeur.


* Accès Internet via le **VLAN 800** existant.


* Hébergement d'une page web statique de présentation via **Apache**.

## Architecture Réseau

Le réseau repose sur une topologie hiérarchique utilisant des équipements Cisco de type **série 800** (routeur) et **2960** (switch).

## 📂 Structure du Dépôt

Le projet est organisé comme suit, reflétant les étapes de mise en place et de simulation :

```text
├── mise en place/
│   ├── Building configuration-switch.txt  # Scripts de conf. du commutateur
│   ├── WU-maquette-réelle.ipynb           # Notebook de suivi de la maquette physique
│   ├── capture-trame-sae12.pcapng         # Analyse Wireshark des flux réseau
│   └── config routeur.txt                 # Scripts de conf. du routeur Cisco
├── simulation du projet/
│   ├── Maquette simulation_finale.pkt     # Fichier Cisco Packet Tracer
│   ├── Préparation.ipynb                  # Documentation de la phase d'étude
│   └── le projet final.ipynb              # Compte-rendu technique final (Markdown)
├── GANTT SAE12.gantt                      # Planification et gestion du temps
└── shema_installation.drawio.png          # Schéma logique du réseau

```

## Technologies et Outils

**Simulateurs** : Cisco Packet Tracer / GNS3.

**Systèmes** : Linux (Debian/Ubuntu) et Windows.

**Services** : Apache (Serveur Web).

**Documentation** : Jupyter Notebook & Markdown.

**Schématisation** : Draw.io.

**Gestion de projet** : Diagramme de GANTT.

---

**Note :** Ce projet a été évalué par l'équipe enseignante lors d'une soutenance orale et d'une démonstration technique de la maquette réelle.
