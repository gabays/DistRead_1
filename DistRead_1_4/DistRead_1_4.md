Formation Edition numérique

# OCR

Simon Gabay

---
## Colab

Nous avons préparé le cours avec un _notebook_ qui est prévu pour fonctionner avec le service en ligne _Colab_ de Google.

1. Allez à l'adresse suivante: https://colab.research.google.com . (si possible en utilisant le navigateur _Chrome_).

2. Sélectionnez l'onglet `GitHub`

3. Copiez le lien suivant: `https://github.com/gabays/DistRead_1/blob/master/DistRead_1_4/DistRead_1_4.ipynb`

<img src="images/colab.png" width="70%">

4. Supprimez tous les éléments de sortie

<img src="images/colab_2.png" width="70%">

---
## En local

Si vous voulez utiliser _Kraken_ en local, vous devez:
1. Télécharger le cours
```console
git clone https://github.com/gabays/DistRead_1
```
2. Aller au cours 4
```console
cd DistRead_1/DistRead_1_4
```
3. Créer un environnement virtuel
```console
pip install virtualenv
virtualenv env
source env/bin/activate
```
4. Installer Kraken
```console
pip install kraken
```

Vous n'avez ensuite qu'à effectuer une partie des lignes du _notebook_ commençant par `!`. Par exemple:

* Je n'ai pas besoin de créer le dossier `img` est déjà présent dans le `DistRead_1_4`
* J'ai besoin de créer un dossier `results` pour mettre mes résultats donc je lance la commande:

```bash
mkdir results
```

L'image étant déjà dans le dossier `img` du cours, ainsi que le modèle OCR (dossier `material`), vous n'avez qu'à lancer la commande (en adaptant les chemins si besoin) pour OCRiser:

```bash
kraken -i img/10.jpg /content/results/ocr_result.txt binarize segment ocr -m /content/material/OCR17.mlmodel
```
soit (le texte en majuscule doit êtr remplacé par des noms réels):
```bash
kraken -i IMAGE.EXTENSION SORTIE.EXTENSION binarize segment ocr -m MODELE.mlmodel
```

