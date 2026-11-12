# Analyse de stock avec Docker

## A compléter.
Elven BOSC--CHARLÈS, B2

## Construction
Indiquer votre commande et expliquer votre Dockerfile.

- Dockerfile :

`FROM ubuntu:24.04`             -> version de l'image utilisée

`RUN ...`                       -> commande d'installation de python3 pour ubuntu

`WORKDIR /app`                  -> spécification du répertoire de travail dans le container (créé si inexistant)

`COPY stock.py .` 			    -> copie du script à faire exécuter au container dans son espace de travail

`CMD ["python3", "stock.py"]`   -> commande exécutée par le container : script stock.py avec la commande python3

- Commande de build :

`docker build -t analyse-stock:v1 .` -> build d'une image appelée 'analyse-stock:v1' avec le Dockerfile du répertoire courant '.'

## Exécution avec montages
Sur mon terminal Gnome :
```bash
docker run --rm -v "$(pwd)/entrees:/entrees:ro" -v "$(pwd)/resultats:/resultats" analyse-stock:v1
```

## Tests et résultats
Renvoyer vers preuves/vérification.md et décrire le résultat attendu.

## Reproduction après git clone
Dans le répertoire du projet :

```bash
docker build -t analyse-stock:v1 .
```

puis, pour Linux/MacOS :

```bash
docker run --rm -v "$(pwd)/entrees:/entrees:ro" -v "$(pwd)/resultats:/resultats" analyse-stock:v1
```

ou pour Windows :

```bash
docker run --rm -v "${PWD}/entrees:/entrees:ro" -v "${PWD}/resultats:/resultats" analyse-stock:v1
```

Les résultats doivent avoir été créés dans `/resultats/` et s'être affichés dans le terminal.

