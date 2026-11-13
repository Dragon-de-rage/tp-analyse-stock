# Verification du projet

Pour chaque cas, coller la commande, sa sortie, et votre explication.

1. Jeu initial de quatre articles.

`entrees/stock.csv` :
```csv
article,quantite,prix_unitaire
Clavier,10,25.00
Souris,4,15.00
Ecran,2,180.00
Cable,0,8.00
```

`resultats/bilan-stock.txt` :
```
References : 4
Unites : 16
Valeur totale : 228.00 EUR
References en stock faible : 3
References en rupture : 1
```

2. CSV modifié sans reconstruction.

`entrees/stock.csv` :
```csv
article,quantite,prix_unitaire
Clavier,15,25.00
Souris,4,5.00
Ecran,2,180.00
Cable,0,8.00
```

`resultats/bilan-stock.txt` :
```
References : 4
Unites : 21
Valeur totale : 218.00 EUR
References en stock faible : 2
References en rupture : 1
```

Le fichier d'entrée est monté à chaque lancement d'un container avec la commande spécifiée dans `README.md`.

Ainsi, pas besoin de re-build l'image à chaque changement de fichier, comme avec COPY.

3. Tentative d'ecriture dans entrees en lecture seule.



4. Rapport relu depuis un autre conteneur avec le meme volume nomme.


5. Entree absente, vide ou invalide.
