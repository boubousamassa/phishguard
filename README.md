# 🛡️ PhishGuard — Campagne de Sensibilisation Anti-Phishing & Extension de Protection

## 📌 Description
PhishGuard est un projet étudiant développé à l'ECE École d'Ingénieurs, combinant éducation à la cybersécurité et protection technique active contre les attaques de phishing. Il se compose de quatre piliers : une infrastructure réseau sécurisée, une plateforme web ludique, une extension navigateur de détection, et une démonstration réelle de campagne de phishing.

---

## 🎯 Objectifs
- Réduire la vulnérabilité des utilisateurs face au phishing
- Fournir une plateforme d'apprentissage interactive (quiz, mini-jeux, tips)
- Détecter automatiquement les liens malveillants via une extension navigateur
- Démontrer concrètement une attaque de phishing dans un cadre éthique
- Garantir la sécurité de l'ensemble de l'infrastructure réseau du projet

---

## 🏗️ Architecture du Projet

### 🌐 Infrastructure Réseau
Conçue et déployée par Boubou (Moi), l'infrastructure réseau constitue le socle sécurisé sur lequel repose l'ensemble du projet.

- Firewall PfSense — filtrage du trafic entrant et sortant, règles de sécurité personnalisées pour protéger les différentes zones réseau
- Zone DMZ — isolation des serveurs exposés (serveur de simulation GoPhish/Flask) afin de limiter l'impact en cas de compromission
- LAN dédié à l'administration système — réseau séparé réservé à la gestion de l'infrastructure, inaccessible depuis les autres zones
- Communication sécurisée entre l'extension navigateur et le back-end, garantissant l'intégrité des échanges

Technologies : PfSense · Segmentation réseau · Règles de pare-feu

---

### 🖥️ Plateforme Web
Développée par Franck-Arsène, la plateforme permet aux utilisateurs de :
- Jouer à des quiz interactifs sur les bonnes pratiques de cybersécurité
- Consulter des fiches « tips » pour apprendre à reconnaître les tentatives de phishing
- Voir leur score et recevoir des explications pédagogiques à chaque fin de quiz

Technologies : HTML · CSS · JavaScript

---

### 🔌 Extension Navigateur
Développée par Boubou(Moi), l'extension analyse en temps réel les liens présents dans les webmails et alerte l'utilisateur avant tout clic dangereux.

Fonctionnalités :
- Analyse automatique des liens en moins de 2 secondes
- Comparaison avec une base de données d'URLs de phishing connues
- Alerte visuelle informative non intrusive
- Aucune collecte de données personnelles ou d'historique de navigation
- Mise à jour de la liste noire d'URLs via un mécanisme d'import
- Communication sécurisée avec l'infrastructure back-end via l'infra réseau dédiée

Technologies : HTML · CSS · JavaScript · WebExtension API (Manifest V3) · Chrome & Firefox

---

### 🎭 Serveur de Simulation
Développé par Boubou(moi), le serveur simule une attaque de phishing dans un cadre strictement éthique, déployé en zone DMZ.

Fonctionnalités :
- Hébergement d'une fausse page de connexion réaliste
- Capture temporaire des identifiants saisis (supprimés après la session)
- Aucune donnée conservée au-delà de la démonstration
- Isolé du reste de l'infrastructure grâce à la zone DMZ

Technologies : Python (Flask) · PostgreSQL

---

### 🎣 Démonstration Réelle avec GoPhish
Pour aller plus loin, GoPhish (outil open-source de simulation de phishing) a été utilisé pour conduire une démonstration réelle :
- Envoi d'e-mails piégés à un groupe de test
- Suivi en temps réel des ouvertures et des clics
- Collecte temporaire des identifiants saisis sur la fausse page
- Analyse des résultats pour mesurer la vulnérabilité réelle des utilisateurs

> ⚠️ Cette démonstration a été réalisée dans un cadre légal et éthique, avec le consentement des participants, uniquement à des fins pédagogiques.

---

## 📋 Exigences Non-Fonctionnelles

| Catégorie         | Exigence |

| ⚡ Performance    | Analyse d'un lien en < 2 secondes |

| 🔒 Sécurité       | Aucune collecte de données personnelles |

| 🌐 Réseau         | Trafic filtré et segmenté via PfSense |

| 🖱️ Utilisabilité  | Interface responsive et intuitive |

| 🔧 Maintenabilité | Code modulaire et documenté |

---

## 👥 Équipe

| Membre         | Rôle |

| Boubou Samassa | Infrastructure réseau (PfSense, DMZ, LAN admin) · Extension navigateur · Serveur de simulation · Démonstration GoPhish |   
| Franck-Arsène  | Plateforme web (quiz, tips, UI/UX) |

---

## ⚠️ Avertissement Éthique
Ce projet inclut des outils de simulation d'attaque. Leur usage est strictement réservé à des fins pédagogiques, dans un cadre légal, avec le consentement explicite des participants. Toute utilisation malveillante est illégale et contraire à l'éthique.

---

## 📄 Licence
Projet académique — ECE École d'Ingénieurs
