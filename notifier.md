[⬅ Retour](./README.md)

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

