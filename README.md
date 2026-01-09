# Déploiement d’une plateforme SIEM & EDR avec Wazuh sur AWS

## 📌 Présentation du projet

Ce projet a été réalisé dans le cadre du module **Virtualisation et Cloud Computing**
(Année universitaire 2025–2026).

Il consiste à déployer une plateforme complète de supervision de la sécurité intégrant
les fonctionnalités **SIEM (Security Information and Event Management)** et
**EDR (Endpoint Detection and Response)** à l’aide de la solution **Wazuh**,
dans un environnement **Cloud AWS**.

---

## 🎯 Objectifs du projet

- Mettre en œuvre une infrastructure Cloud virtualisée sur AWS
- Déployer une solution SIEM & EDR centralisée
- Superviser des endpoints Linux et Windows
- Détecter et analyser des incidents de sécurité
- Appliquer les bonnes pratiques de sécurité Cloud

---

## 🏗️ Architecture du projet

L’architecture repose sur :
- Un **serveur Wazuh** (Ubuntu 22.04 – All-in-One)
- Un **client Linux** (Ubuntu 22.04)
- Un **client Windows** (Windows Server)
- Un **VPC AWS unique** avec des Security Groups sécurisés

📌 Les agents communiquent avec le serveur Wazuh via les ports **1514/TCP** et **1515/TCP**.

📷 Voir les schémas dans le dossier `architecture/`.

---

## ☁️ Infrastructure AWS

- Plateforme : AWS Learner Lab
- Services utilisés :
  - EC2
  - VPC
  - Security Groups
- Accès sécurisés :
  - SSH (Linux)
  - RDP (Windows)
  - HTTPS (Wazuh Dashboard)

---

## 🔧 Installation et déploiement

### 1️⃣ Installation du serveur Wazuh
- OS : Ubuntu 22.04
- Installation via le script officiel Wazuh All-in-One

### 2️⃣ Enrôlement des agents
- Agent Linux installé via le Dashboard Wazuh
- Agent Windows installé via PowerShell

📌 Les étapes détaillées sont disponibles dans le dossier `wazuh/`.

---

## 🧪 Démonstrations SIEM & EDR

### 🔹 Linux
- Tentatives SSH échouées (brute force simulé)
- Élévation de privilèges (sudo)
- Modification de fichiers sensibles (FIM)

### 🔹 Windows
- Échecs de connexion RDP
- Création d’utilisateurs et modification de groupes
- Analyse des événements de sécurité Windows

📷 Captures disponibles dans le dossier `screenshots/`.

---

## 🔍 Analyse & Threat Hunting

- Filtrage des alertes par niveau
- Analyse IAM / PAM
- Investigation des événements FIM
- Corrélation multi-endpoints via le Dashboard Wazuh

---

## 📄 Rapport

Le rapport complet du projet est disponible dans le dossier :

