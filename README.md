# Auto-Research Agent — Agent de recherche itératif IA

Agent IA autonome qui reçoit une question, effectue plusieurs cycles de 
recherche et d'analyse avec Mistral, et produit une réponse synthétisée 
et approfondie.

## Concept

Au lieu de poser une question et obtenir une seule réponse, l'agent :
1. Décompose la question en sous-questions
2. Recherche et analyse chaque sous-question
3. Évalue si la réponse est suffisante
4. Si non, génère de nouvelles questions et recommence
5. Synthétise tout en une réponse finale structurée

## Structure du projet

- `index.php` — interface utilisateur (formulaire + affichage résultats)
- `config.php` — configuration clé API Mistral via .env
- `agent.php` — moteur de l'agent (boucle d'itération)
- `mistral.php` — client API Mistral (appels HTTP)
- `logger.php` — journal de chaque étape de recherche
- `.env` — clé API (jamais publiée)
- `.gitignore` — protection des fichiers sensibles

## Fonctionnalités

- Boucle de recherche automatique (max 5 itérations)
- Décomposition automatique de questions complexes
- Évaluation de la complétude des réponses
- Journal détaillé de chaque étape visible en temps réel
- Synthèse finale structurée en markdown
- Interface web simple et lisible

## Stack technique

- PHP 8.3
- Apache (Laragon)
- API Mistral AI (mistral-small-latest)
- JavaScript vanilla (affichage temps réel)

## Paramètres configurables

- Nombre max d'itérations : 5 (modifiable dans agent.php)
- Modèle Mistral : mistral-small-latest
- Température : 0.7
- Max tokens par appel : 1024

## Utilisation

1. Entrer une question complexe
