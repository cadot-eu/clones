# 📊 Clone Tracker - Suivi des Statistiques GitHub

**Galais Version** *(Version Galaisienne)*

## 🎯 Objectif du Projet

Ce projet permet de suivre les statistiques des dépôts GitHub pour les utilisateurs spécifiés. Il récupère automatiquement les données de clones, étoiles et forks pour chaque repository public avec un affichage structuré en tableau.

## 📈 Compteur de Statistiques en Temps Réel avec Étapes de Progression

```bash
# Exécution du script pour récupérer les statistiques
./clones

# Le script affiche maintenant des étapes de progression:
🚀 Démarrage de la récupération des statistiques GitHub...

👤 Traitement de l'utilisateur: cadot-eu
─────────────────────────────────────────────
📡 Étape 1: Récupération des repositories publics...
   ✅ X repositories publics trouvés
📊 Étape 2: Récupération des statistiques de clones...
   🔄 (1/X) Traitement de: [nom du repo]
📈 Étape 3: Tri et affichage des résultats...
```

## 🗂️ Tableau d'Affichage des Dépôts avec Header

Le script génère maintenant un tableau formaté avec les en-têtes:

```
┌─────────────────────────────────────────────────────────────────────┐
│                      TABLEAU DES STATISTIQUES                       │
├─────────┬──────────────────────────────┬──────────┬─────────────────┤
│  Clone  │            Name              │  Stars   │      Fork       │
├─────────┼──────────────────────────────┼──────────┼─────────────────┤
│   150   │ awesome-project              │       42 │              12 │
│    75   │ documentation-tool           │       18 │               5 │
│    30   │ utility-scripts              │        8 │               3 │
└─────────┴──────────────────────────────┴──────────┴─────────────────┘
```

### 📊 Statistiques Globales avec Récapitulatif
- **Total des Repositories:** Calculé dynamiquement pour chaque utilisateur
- **Total des Clones:** Somme de tous les clones
- **Total des Étoiles:** Somme de toutes les étoiles  
- **Total des Forks:** Somme de tous les forks
- **Repositories Actifs:** Nombre de repos avec statistiques > 0
- **Utilisateurs Suivis:** Nombre d'utilisateurs configurés

## 🚀 Installation et Utilisation

### Prérequis
- Token d'accès GitHub (avec permissions `repo` et `read:user`)
- Outils: `curl`, `jq`, `bash`

### Configuration
1. Ajoutez votre token GitHub dans le fichier `.github_token`
2. Configurez les utilisateurs à suivre dans `users.yaml`
3. Donnez les permissions d'exécution: `chmod +x clones`
4. Exécutez le script: `./clones`

### Format du fichier `users.yaml`
```yaml
users:
  - cadot-eu
  # Ajoutez d'autres utilisateurs ici
  # - autre-utilisateur
  # - encore-un-autre
```

## 🔧 Fonctionnalités Améliorées

- ✅ **Header de tableau structuré** avec bordures ASCII
- ✅ **Étapes de progression** détaillées pendant l'exécution
- ✅ **Affichage en temps réel** du traitement de chaque repository
- ✅ **Récapitulatif complet** par utilisateur
- ✅ **Tri automatique** par nombre de clones (descendant)
- ✅ **Filtrage intelligent** des repos inactifs
- ✅ **Support multi-utilisateurs** avec traitement séquentiel
- ✅ **Timestamp de mise à jour** automatique

## 📁 Structure du Projet

```
clone/
├── README.md          # Documentation (version galais)
├── clones             # Script principal amélioré
├── users.yaml         # Configuration des utilisateurs
├── .github_token      # Token d'authentification GitHub
├── .gitignore         # Fichiers ignorés par Git
└── .git/              # Historique Git
```

## 🔄 Mise à Jour des Données

Les données sont récupérées en temps réel via l'API GitHub. Pour mettre à jour les statistiques:

```bash
./clones
```

Le script affiche la date/heure exacte de la dernière mise à jour.

## 📊 Exemple Complet de Sortie

```
🚀 Démarrage de la récupération des statistiques GitHub...

👤 Traitement de l'utilisateur: cadot-eu
─────────────────────────────────────────────
📡 Étape 1: Récupération des repositories publics...
   ✅ 15 repositories publics trouvés
📊 Étape 2: Récupération des statistiques de clones...
   🔄 (1/15) Traitement de: awesome-project
   🔄 (2/15) Traitement de: documentation-tool
   🔄 (3/15) Traitement de: utility-scripts
   ... (traitement des 12 autres repos)
📈 Étape 3: Tri et affichage des résultats...

┌─────────────────────────────────────────────────────────────────────┐
│                      TABLEAU DES STATISTIQUES                       │
├─────────┬──────────────────────────────┬──────────┬─────────────────┤
│  Clone  │            Name              │  Stars   │      Fork       │
├─────────┼──────────────────────────────┼──────────┼─────────────────┤
│   150   │ awesome-project              │       42 │              12 │
│    75   │ documentation-tool           │       18 │               5 │
│    30   │ utility-scripts              │        8 │               3 │
│    12   │ learning-materials           │        5 │               1 │
│     5   │ experimental-code            │        2 │               0 │
└─────────┴──────────────────────────────┴──────────┴─────────────────┘

📊 Récapitulatif pour cadot-eu:
   • Total clones: 272
   • Total étoiles: 75
   • Total forks: 21
   • Repositories actifs: 5

✅ Traitement de cadot-eu terminé avec succès!

🎉 Tous les utilisateurs ont été traités avec succès!
📋 Résumé final:
   • Utilisateurs analysés: 1
   • Données mises à jour: 07/02/2026 12:07:14
```

## 🤝 Contribution

Les contributions sont les bienvenues ! Pour contribuer:

1. Forkez le projet
2. Créez une branche pour votre fonctionnalité
3. Committez vos changements
4. Poussez vers la branche
5. Ouvrez une Pull Request

## 📄 Licence

Ce projet est sous licence MIT. Voir le fichier LICENSE pour plus de détails.

## 🙏 Remerciements

- API GitHub pour l'accès aux données
- Communauté open source
- Tous les contributeurs

---

*Dernière mise à jour du README: 07/02/2026*
*Script amélioré avec header de tableau et étapes de progression*
