# StepWise

**StepWise** est une application éducative innovante destinée aux enfants atteints de trisomie 21, conçue pour favoriser leur **autonomie**, leur **intégration sociale** et leur **préparation professionnelle** à travers une expérience assistée par intelligence artificielle.

---

## 🎯 Objectif

Permettre aux enfants trisomiques d’acquérir des compétences essentielles pour leur vie quotidienne, sociale et professionnelle, grâce à une plateforme interactive, personnalisée et accessible.

---

## 🧠 Fonctionnalités Clés

### 🧩 Catégories éducatives adaptées :
- **Spelling** : Apprentissage de la prononciation correcte grâce à la reconnaissance vocale.
- **Études** : Modules simplifiés de Mathématiques, Physique, Sciences.
- **Sport adapté** : Activités physiques simples et accessibles.
- **Pâtisserie & Cuisine** : Développement de l’autonomie culinaire pour des vocations futures.
- **Sensibilisation sociale** : Prévention contre le harcèlement, manipulation et éducation sexuelle.
- **Routines quotidiennes** : Réveil, hygiène, habillage, respiration, repas équilibrés.
- **Badges & Levels** : Système de récompenses motivant l’accomplissement des tâches.

---

## 🧠 Intelligence Artificielle (IA)

### 🧾 Agent AI en temps réel :
- **Reconnaissance vocale et phonétique** via le modèle **Wav2Vec2** pour analyser la prononciation.
- **Analyse d’images** via caméra pour valider les routines (faire le lit, s’habiller, brosser les dents…).
- **Détection de respiration** et validation des exercices de relaxation.
- **Génération audio** via **Speechify** (Text-to-Speech) pour une interaction vocale naturelle.
- **Recommandations de repas** via un module AI santé basé sur des données diététiques adaptées.

---

## 🛠️ Stack Technique

### Frontend
- **Flutter** (Dart) pour une interface responsive et accessible.
- **Push Notifications** intégrées via **WebSockets** pour communication temps réel.

### Backend
- **NestJS (Node.js, TypeScript)** :
  - Architecture modulaire et scalable.
  - Authentification, gestion des tâches, progression utilisateur.
  - WebSockets pour communication bidirectionnelle temps réel.
  - Gestion des événements et des badges utilisateur.

### AI & Traitement temps réel
- **LiveKit** : Streaming vidéo/audio temps réel pour les validations interactives.
- **Wav2Vec2** : Analyse vocale et phonétique via Deep Learning.
- **Speechify** : Conversion texte → voix pour accompagner l'enfant.
- **Gemini AI** : Agent intelligent pour valider, assister et déclencher les tâches.
- **TensorFlow / PyTorch** : Utilisés pour l'entraînement de modèles personnalisés (facultatif).

---

## 🧩 Architecture Générale

```text
[Flutter App]
     |
     | WebSocket (live notifications, data push)
     v
[NestJS Backend] <---> [MongoDB / PostgreSQL]
     |
     | REST + WebSocket + AI Agent Communication
     v
[Gemini AI & Deep Learning Models]
     |
     | Text-to-Speech (Speechify) / Speech-to-Embedding (Wav2Vec2)
     v
[LiveKit] --> [Camera/Mic Stream Analysis in Real-Time]

