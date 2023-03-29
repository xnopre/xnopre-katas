[⬅ Retour](./README.md)

# Calcul du score d'une partie de bowling 🎳

Lors d’une partie de bowling, vous avez 10 **essais** pour faire tomber les 10 **quilles** à chaque fois. Un joueur peut
faire deux **lancers** par essai.

Vos points de l'essai sont la somme des quilles tombées à cet **essai** dans le cas où il vous reste des **quilles** à
faire tomber après vos deux **lancers**. Pour les points de partie il suffit de sommer tous les points de vos 10
**essais**, par exemple :

```
[0, 2], [3, 4], [0, 0], [8, 1], [1, 1], [8, 1], [3, 3], [5, 2], [2, 7], [7, 1] => 59 points
```

> Vous pouvez vérifier les scores via https://www.bowlinggenius.com/

Il y a deux cas spéciaux :

- le *spare*, au deuxième **lancer** vous arrivez à faire tomber toutes les **quilles** restantes : pour cet **essai**
  le score est de `10` (nombre de **quilles** tombées) auquel on ajoute le nombre de **quilles** tombées au prochain
  **lancer**.
  ```
  [0, 2], [3, 4], [5, 5], [8, 1], [1, 1], [8, 1], [3, 3], [5, 2], [2, 7], [7, 1] => 77 points
                  |—> spare
  ```
- le *strike*, au premier **lancer** vous faites tomber les 10 **quilles** : pour cet **essai** le score est de `10`
  (nombre de **quilles** tombées) auquel on ajoute le nombre de **quilles** tombées des **2** prochains **lancers**.
  ```
  [0, 2], [3, 4], [10], [8, 1], [1, 1], [8, 1], [3, 3], [5, 2], [2, 7], [7, 1] => 78 points
                  |—> strike
  ```

Il reste une règle pour avoir un score parfait, si au dernier **lancer** vous arrivez à faire tomber toutes les
**quilles** dans l’un de vos deux lancers, vous pouvez **lancer** un ou deux fois de plus. Ces lancers bonus sont là
pour calculer le score uniquement de votre dernier **essai**. Ainsi si vous faites 3 *strikes* de suite au dernier
lancer, vous ne gagnez que `30` points de plus.

```
[10], [10], [10], [10], [10], [10], [10], [10], [10], [10, 10, 10] => 300 points
```
