# 📊 Clone Tracker - Suivi des Statistiques GitHub

**Galais Version** *(Version Galaisienne)*

## 🎯 Objectif du Projet

Ce projet permet de suivre les statistiques des dépôts GitHub pour les utilisateurs spécifiés. Il récupère automatiquement les données de clones, étoiles et forks pour chaque repository public.

## 📈 Compteur de Statistiques en Temps Réel

```bash
# Exécution du script pour récupérer les statistiques
./clones

# Résultat attendu :
👤 cadot-eu (repos publics triés par clones)
─────────────────────────────────────────────
  [nombre] 🔄  📦 [nom du repo] ⭐[étoiles] 🔱[forks]
```

### 📊 Statistiques Globales (Exemple)
- **Total des Repositories:** [calculé dynamiquement]
- **Total des Clones:** [calculé dynamiquement] 
- **Total des Étoiles:** [calculé dynamiquement]
- **Total des Forks:** [calculé dynamiquement]
- **Utilisateurs Suivis:** 1 (cadot-eu)

## 🗂️ Tableau d'Affichage des Dépôts

| Clone | Name | Stars | Fork |
|-------|------|-------|------|
| [count] | [repo] | [stars] | [forks] |
| [count] | [repo] | [stars] | [forks] |
| [count] | [repo] | [stars] | [forks] |

*Note: Les données sont triées par nombre de clones (descendant)*

## 🚀 Installation et Utilisation

### Prérequis
- Token d'accès GitHub (avec permissions `repo` et `read:user`)
- Outils: `curl`, `jq`, `bash`

### Configuration
1. Ajoutez votre token GitHub dans le fichier `.github_token`
2. Configurez les utilisateurs à suivre dans `users.yaml`
3. Exécutez le script: `./clones`

### Format du fichier `users.yaml`
```yaml
users:
  - cadot-eu
  # Ajoutez d'autres utilisateurs ici
```

## 🔧 Fonctionnalités

- ✅ Récupération automatique des repositories publics
- ✅ Tri par nombre de clones
- ✅ Affichage formaté avec emojis
- ✅ Support multi-utilisateurs
- ✅ Filtrage des repos inactifs (0 clones, 0 étoiles, 0 forks)

## 📁 Structure du Projet

```
clone/
├── README.md          # Ce fichier (version galais)
├── clones             # Script principal
├── users.yaml         # Configuration des utilisateurs
├── .github_token      # Token d'authentification GitHub
└── .gitignore         # Fichiers ignorés par Git
```

## 🔄 Mise à Jour des Données

Les données sont récupérées en temps réel via l'API GitHub. Pour mettre à jour les statistiques, exécutez simplement le script à nouveau:

```bash
./clones
```

## 📊 Exemple de Sortie

```
👤 cadot-eu (repos publics triés par clones)
─────────────────────────────────────────────
  150 🔄  📦 awesome-project           ⭐42   🔱12
   75 🔄  📦 documentation-tool        ⭐18   🔱5
   30 🔄  📦 utility-scripts           ⭐8    🔱3
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

*Dernière mise à jour: $(date +%d/%m/%Y)*
*Statistiques mises à jour à chaque exécution*# clones
