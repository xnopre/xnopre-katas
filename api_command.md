[⬅ Retour](./README.md)

# Préparation de commandes

> Mocks et tests asynchrones

# Sujet


Une API **fictive** est accessible via `https://products.com` pour récupérer les différentes 
informations relatives aux produits et au stock (voir détails ci-dessous).

Créer une repository `OrdersManager` pour gérer la préparation des commandes de produits sportifs.
`OrdersManager` doit consommer l’API et fournir les fonctionnalités suivantes :

* Récupérer la liste des descriptions de tous les produits triés par ordre alphabétique
* Récupérer la liste des descriptions des produits disponibles (stock > 0) triés par ordre alphabétique
* Vérifier la disponibilité d'un produit (par référence)
* chercher des produits (description, disponibilité et prix) par mot clé
* Valider un panier de commande en indiquant s'il est valide (disponibilité) et le prix total


# Description de l’API

GET `/products` : retourne la liste des produits, chaque produit est défini ainsi :

```
{
    ref: number,
    description: string,
    stock: number,
    prix: number
}
```

## Exemple de réponse de l'API

```
[
  {
    ref: 1,
    description: ”vélo électrique”,
    stock: 10,
    prix: 1400,
  },
  {
    ref: 2,
    description: ”balle de tennis”,
    stock: 1000,
    prix: 1,5,
  },
]
```