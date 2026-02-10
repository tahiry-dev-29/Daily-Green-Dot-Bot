# Daily Green Dot Bot

Ce dépôt contient un petit robot GitHub Actions pour maintenir une activité quotidienne (mettre un "point vert" sur ton profil GitHub).

Structure:

```
.
├── .github/
│   └── workflows/
│       └── daily_commit.yml
├── data/
│   └── heartbeat.txt
└── README.md
```

Installation & utilisation:

- Vérifie que tu as poussé ces fichiers sur le dépôt distant (`git push`).
- Dans `Settings > Actions > General`, assure-toi que les workflows ont les permissions en lecture et écriture ("Read and write permissions").
- Le workflow s'exécute quotidiennement à `00:00 UTC`. Tu peux le lancer manuellement via l'onglet "Actions" puis "Run workflow".

Personnalisation:

- Pour changer l'heure, modifie la valeur `cron` dans `.github/workflows/daily_commit.yml`.
- Si tu veux des messages de commit aléatoires, dis-le-moi et j'ajouterai cette option.

Remarque:

GitHub peut désactiver les workflows programmés si le repo reste inactif sans "activité humaine" pendant ~60 jours. Pense à vérifier si le workflow se désactive.
