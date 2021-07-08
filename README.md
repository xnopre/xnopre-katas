Ce dépôt contient quelques sujet de Katas que j'aime bien utiliser dans mes démos de live coding, notamment pour montrer
le TDD en action. Et également des katas en cours d'élaboration ou de test 😉.

N'hésites pas :

- à suivre ("watch") ce dépôt pour suivre les évolutions
- à mettre une étoile ⭐️ si tu aimes bien
- à laisser des commentaires, remarques, suggestions, ...
- à faire des PR pour compléter, améliorer, corriger, ...

# Calcul de prix

> Très bon sujet très simple pour débuter en TDD, avec des tests simples (sans mock)

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

## Tips si tu débutes en TDD

- Chaque exemple chiffré ci-dessus peut correspondre à un test
- Mettre en place une implémentation la plus simple possible (une fonction ou une classe et une fonction devrait
  suffire)
- Toujours implémenter le strict minium ("en toute intelligence" 😉) pour faire passer chaque test

Mieux vaut essayer et chercher par toi même, mais tu peux trouver des solutions, ou au moins des contextes et
outillage, [sur ce dépôt xnopre/tdd-demos](https://github.com/xnopre/tdd-demos).

# Le notificateur par mail

> Ce sujet simple peut permettre de découvrir les mocks

Un notificateur `Notifier` propose une méthode `notifyAllUsers(message)` permettant de :

- Récupérer tous les utilisateurs dans une base de donnée, via un `Dao` et sa méthode `getAllEmails()`
- [Optionnel] Un "helper" génère le contenu du mail contenant le message
- Le mail est envoyé via un 3e collaborateur `MailSender.send(emails, content)`

## Tips si tu débutes en TDD

- Commence par un test pour le cas nominal (= "le" fonctionnement principal) en mockant tous les collaborateurs (Dao,
  générateur de contenu et MailSender) qui peuvent être de simples interfaces à ce stade
- Tu peux ensuite écrire un test pour vérifier ce qui se passe si l'envoi de mail échoue
  (pour cela, le MailSender doit renvoyer une erreur ou exception à la demande d'envoi et le Notifier doit, par exemple,
  générer une exception "maison" avec un texte adapté)

Si tu bloques, tu peux trouver un exemple de test 
[ici](https://github.com/xnopre/tdd-demos/blob/tdd-raise-partner-dec-2019/src/test/java/NotifierTest.java).

# Le "TDD du serpent" ou "Snake TDD" 

> Le but de ce Kata est de pratiquer le TDD mais dans un cadre imposé et en voyant le code
> implémenté donner vie au serpent dans une interface WEB ! 😎

A venir... 😉

(le dépôt est en cours de finalisation...)

En attendant, tu peux retrouver [l'épisode 1](https://www.youtube.com/watch?v=p_FHa0n8whQ)
et [l'épisode 2](https://www.youtube.com/watch?v=TGb34TQSNKk) des live codings réalisés avec 
Benoit.