# CliniSys — Mon Journal d’Activité

Interface web responsive en français pour suivre les appels, le support, les analyses, les visites et les actions de suivi.

Prototype autonome : les données sont conservées dans le navigateur utilisé et ne sont pas synchronisées entre appareils. Aucune connexion Supabase n’est active tant que l’accès aux tables `journal_*` n’a pas été sécurisé et vérifié. Les tables historiques `clinisys_*` ne sont pas utilisées ni modifiées.

## Utilisation

- **Planning** (écran d’accueil) : les tâches du jour, avec « Planifier une tâche » et « Saisir mon rapport du jour ». Vues Jour, Semaine et Mois.
- **Journal** : les activités réellement effectuées (appels, support, analyses, interventions, formations…).
- **Clients** : fiche avec potentiel (1 à 4), nombre de visites par semaine, type de suivi et case « Inclure dans la génération automatique ».
- **Rapports** : synthèses et export CSV.

## Propositions automatiques

1. Cocher, dans la fiche de chaque client, ceux à planifier.
2. Planning → « Propositions de visites par client » : choisir le mois de départ et la durée (1 à 4 semaines, du lundi au vendredi), puis « Générer les propositions ».
3. Les tâches générées portent le badge « Proposition ». Les modifier puis enregistrer, les valider (une par une ou toutes), ou les supprimer avec « Effacer les propositions ».

Règles : rien avant aujourd’hui, pas de week-end, aucun chevauchement horaire, heure obligatoire pour toute tâche planifiée. Les tâches existantes ne sont jamais modifiées par la génération.

## Limites

- Données dans le navigateur uniquement (LocalStorage), sans synchronisation entre appareils : exporter une sauvegarde avant de changer d’appareil ou de vider le navigateur.
- Les rappels ne sont fiables que lorsque la page est ouverte et les notifications autorisées.

## Contribution

Récupérer la dernière version du dépôt avant toute modification, modifier uniquement ce qui est nécessaire, vérifier la syntaxe JavaScript, et n’utiliser qu’un seul outil à la fois pour éviter les écrasements.
