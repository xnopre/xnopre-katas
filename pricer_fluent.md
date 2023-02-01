[⬅ Retour](./README.md)

# Calcul de prix avec API fluent

> Mettre en place une API fluent

# Sujet

Générer une chaine de caractères avec le prix total à partir des informations suivantes :

- Nombre d'articles
- Prix unitaire
- Taxe

Exemples chiffrées :

- 3 articles à 1,21 € et taxe 0 % → “3.63 €”
- 3 articles à 1,21 € et taxe 5 % → “3.81 €”
- 3 articles à 1,21 € et taxe 20 % → “4.36 €”

Puis on ajoute des réductions si le prix total dépense un seuil :

- 1000 € → Remise 3% :
    - Ex : 5 x 345,00 € + taxe 10% → “1840.58 €”
- 5000 € → Remise 5% :
    - Ex : 5 x 1299,00 € + taxe 10% → “6787.28 €”

# Objectif 1 : Mettre en place une API fluent

Une "API fluent" est une architecture du code qui permet d'enchainer les appels de méthodes :

```shell
  un_objet_ou_une_classe
    .withQuantity(3)
    .withUnitPrice(1.21)
    .withTax(5)
    ...
```

# Objectif 2 : guider l'utilisateur

Faire en sorte que le développeur utilisateur de ce code n'ait pas de doute et ne 
puisse pas se tromper lors de l'utilisation de cette API :
- Ne pas pouvoir se tromper dans les typages des données
- Ne pas pouvoir appeler n'importe quel enchainement de méthode
- Ne pas pouvoir appeler plusieurs fois une méthode si cela n'a pas de sens
- Pouvoir utiliser certaines méthodes de façon optionnelle (ex : tax)
- ...