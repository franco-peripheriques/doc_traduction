# Procédure (exemple avec le weather:bit)

## Copie (fork)

- Dans le repo GitHub weather:bit original, faire un fork vers l'organisation franco-peripherique
- Cloner le repo GitHub de franco-peripherique vers son ordi avec `git clone ssh/https`; il faut un lien ssh ou https
- Cela crée un nouveau répertoire
    - Ou, dans le terminal créer le répertoire avec `mkdir pxt-weather-bit` pour y sauvegarder les fichiers
    - Bref, organiser les fichiers dans un dossier pxt-weather-bit
- Dans le terminal, aller dans ce nouveau répertoire; lister les fichiers avec `ls`

## Préparation

- Il faut installer pxt???

- Préparer le répertoire pour travailler avec le micro:bit; lancer la commande `pxt target microbit`
- Lancer la commande `pxt install`
- Cela génère de nouveaux fichiers dans le répertoire
- Ajouter les fichiers de traduction avec `pxt gendocs --locs`; pour *localization*
- Lancer `git status` pour voir les ajouts

## Traduction

- Pour la suite, le travail dans le répertoire pxt-weather-bit peut être fait dans le terminal ou dans le sytème GUI
- Dans les fichiers de traduction ou _locales, ajouter un dossier fr
    - Il peut déjà y avoir des dossiers de traduction en d'autres langues que le français
- Copier les fichiers de _locales dans dans le nouveau dossier fr
- Modifier les fichier dans fr
    - Traduire les blocs de code (weatherbit-strings.json) et et l'aide (weatherbit-jsdoc-strings.json)
    - Faire attention aux variables (% |); regarder les cas existants avant de précéder à la traduction, car le français demande d'inverser des expressions et de déplacer les variables
    - Dans le fichier de commentaires weather-jsdoc-strings.json, s'il n'a pas de commentaire (aucun ligne clé:valeur), il faut créer une nouvelle ligne dans weather-jsdoc-strings.json et prendre le nom de la clé dans weather-strings.json pour créer une nouvelle paires clé:valeur ou "nom du bloc": "commentaire" dans weather-jsdoc-strings.json
- Vérifier et sauvegarder
- Enlever les fichiers .bak ou ~ (souvent des fichiers cachés)

## Confirmation

- Retourner dans le dossier principal, aller dans le fichier pxt.json
- Dans ce fichier, dans la catégorie "files", ajouter "_locales/fr/weatherbit-strings.json" et "_locales/fr/weatherbit-jsdoc-strings.json"
    - Faire attention aux virgules
- Vérifier et sauvegarder
- Enlever les fichiers .bak ou ~

## Envoyer

- Revenir au terminal, vérifier le dossier avec `git status` pour voir les ajouts et changements
- Ajouter avec `git add _locales/ pxt.json`; uniquement deux expressions et tout avec un `git add .`
- Vérifier avec `git status`
- Commettre avec `git commit -m "commit the first French translation v1"`
- Insérer la commande `pxt bump` pour gérer la version
- Compléter l'envoie avec `git push`

## Finaliser

- Retourner dans le repo GitHub de l'organisation franco-peripherique, avec le bouton Compare, comparer le clone avec l'original; cela conduit vers le repo orignal
- Déterminer s'il est possible de fusionner les deux repo (merge)
- Du repo original, revenir à la copie (fork) sur l'organisation franco-peripherique
- Dans le fichier pxt.json original, prendre la version en note (clé:valeur, la valeur est la version)
- Dans le fichier pxt.json du fork, dans l'organisation franco-peripherique, la version a tendance à «avancer» avec les changements
- Changer la version dans l'organisation franco-peripherique pour la version notée
- Ajouter un commentaire avant de sauvegarder le changement

## Pull request

- Toujours dans l'organisation franco-peripherique, dans l'onglet Pull requests, appuyer sur le bouton New pull request
- Confirmer avec le bouton Create pull request (seulement si les deux repos peuvent fusionner)
- Commenter le travail: "Hi, We added a French translation to the package (localization files). We will follow up on the matter with someone at Microsoft for approval. Cheers"
demander l'approbation, pull request, écrire un courriel
- Appuer sur le bouton Create pull request

## Approbation

- Copier les liens GitGub: original obligatoire (et copie en plus)
- Écrire un courriel à Microsoft pour demander une approbation (Guillaume, par exemple)
