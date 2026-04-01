# De la rareté à la pénurie : la crise d'accès aux médecins spécialistes touche la France entière

*Densité de médecins par département et par spécialité en France métropolitaine (2024)*

## Visualisation

- [Carte choroplèthe interactive avec dropdown par spécialité (Flourish)](https://public.flourish.studio/visualisation/28301643/)

## Méthodologie

Les données sont disponibles en téléchargement direct sur data.ameli.fr, mais ont été volontairement collectées via l'**API Opendatasoft** du portail, avec filtres (`where`, `year()`, `AND`), pagination par offset/limit, et construction programmatique des requêtes. **10 spécialités** ont été retenues : médecins généralistes, chirurgiens-dentistes, cardiologues, dermatologues, ophtalmologues, gynécologues, neurologues, hépato-gastro-entérologues, psychiatres et pneumologues. Les données agrégées au niveau national (code 999) sont exclues.

L'indicateur utilisé est la **densité** (nombre de professionnels pour 100 000 habitants), fourni directement par l'API. Les données sont pivotées pour obtenir un tableau départements × spécialités, utilisé comme source Flourish.

**Limites** :

La densité par département ne reflète pas les disparités infra-départementales, qui peuvent être importantes entre zones urbaines et rurales. L'indicateur ne tient pas compte de l'activité réelle des praticiens (temps partiel, secteur, délais de rendez-vous).

## Organisation du dépôt

```
├── data/
│   ├── raw/            # Données brutes API (toutes spécialités)
│   └── clean/          # Tableau croisé départements × spécialités
├── notebooks/
│   └── deserts_medicaux_departements.ipynb
└── README.md
```

## Outils

Python (pandas, requests) · API data.ameli.fr (Opendatasoft) · Jupyter Notebook · Flourish

---

Projet réalisé par **Timothée Barnaud**.
