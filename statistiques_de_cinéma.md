[⬅ Retour](./README.md)

# Statistiques de cinéma

> Intéressant pour faire de la manipulation de données, notamment avec le triptyque `filter / map / reduce`

Le fichier [Meilleures_audiences_en_salles_depuis_1945.json](./Meilleures_audiences_en_salles_depuis_1945.json)
contient des données relatives au cinéma de cette forme :

```
{
"films":[
 {
  "rang": 1,
  "titre": "Titanic",
  "réalisateur": "J. Cameron",
  "année de sortie": 1998,
  "nationalité": "US",
  "entrées (millions)": 21798906
 },
 ...
}
```

Ecrire du code pour lire ce fichier et en tirer les statistiques suivantes (ou d'autres) :
- Top 5 des films
- Top 5 des réalisateurs par nombre de films
- Top 5 des réalisateurs par nombre de films, et leurs films par ordre de rang
- Top 5 des réalisateurs par nombre d'entrées (et le nombre d'entrées)
- Top 5 des pays
- Top 5 des années avec le plus de films
- Top 5 des années avec le plus d'entrées
- etc...