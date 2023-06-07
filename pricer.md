[⬅ Retour](./README.md)

# Calcul de prix

> Très bon sujet très simple pour débuter en TDD, avec des tests simples (sans mock)

Générer une chaine de caractères avec le prix total à partir des informations suivantes :

- Nombre d'articles
- Prix unitaire
- Taxe en % (voir exemple)

Exemples chiffrées :

- 3 articles à 1,21 € et taxe 0 % → “3.63 €”
- 3 articles à 1,21 € et taxe 5 % → “3.81 €”
- 3 articles à 1,21 € et taxe 20 % → “4.36 €”

Puis on ajoute des réductions si le prix total HT dépasse un seuil :

- 1000 € → Remise 3% :
    - Ex : 5 x 345,00 € + taxe 10% → “1840.58 €”
- 5000 € → Remise 5% :
    - Ex : 5 x 1299,00 € + taxe 10% → “6787.28 €”

⚠️ Pour les remises, il n'y a pas besoin d'ajouter de paramètres d'entrée puisque c'est basé sur le prix total HT !

## Tips si tu débutes en TDD

- Chaque exemple chiffré ci-dessus peut correspondre à un test
- Mettre en place une implémentation la plus simple possible (une fonction, ou une classe et une fonction, devrait
  suffire)
- Toujours implémenter le strict minium ("en toute intelligence" 😉) pour faire passer chaque test

Il vaut mieux essayer et chercher par toi-même, mais tu peux trouver des solutions, ou au moins des contextes et
outillage, [sur ce dépôt xnopre/tdd-demos](https://github.com/xnopre/tdd-demos).
