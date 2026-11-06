À la racine du projet, si on exécute `tree Wikipedia/Python` dans le shell,
l'affichage est :

```
Wikipedia/Python
├── Mythology
│   ├── Apollo_dan_Pithon.jpg
│   ├── en.txt
│   └── fr.txt
├── ProgrammingLanguage
│   ├── en.txt
│   ├── fr.txt
│   ├── logo.svg.png
│   └── source-code.png
└── Pythonidae
    ├── en.txt
    ├── fr.txt
    ├── molurus_molurus.jpg
    └── royal.JPG

4 directories, 11 files
```

`Scripts/tree.py` implémente le même comportement en Python, en utilisant les
éléments en annexe ci-dessous. Il est possible de modifier le script pour
ajouter le support d'options de la commande `tree` (aide complète accessible par
`man tree`), par exemple pour ne montrer que les répertoires ou limiter la
profondeur d'affichage.

# Annexe

## Entrées/sorties

La fonction [open](https://docs.python.org/3/library/functions.html#open) permet
d'ouvrir un fichier pour lire / écrire son contenu. Sur la valeur retournée,
nommé `file` ci-dessous, on peut appeler :

- `file.read()` pour lire le contenu du fichier sous forme d'octets ;
- `file.readlines()` pour lire le contenu du fichier sous forme une liste
  de lignes (chaînes de caractères) ;
- `file.close()` pour fermer le fichier.


## Conversions

- [chr](https://docs.python.org/3.13/library/functions.html#chr)
  permet de convertir un code de caractère en caractère
- [ord](https://docs.python.org/3.13/library/functions.html#ord)
  permet de convertir un caractère en son code


## Module [glob](https://docs.python.org/3.13/library/glob.html)

- [glob.glob](https://docs.python.org/3.13/library/glob.html#glob.glob)
  renvoie la liste des fichiers et répertoires correspondant au *pattern* passé


## Module [os](https://docs.python.org/3.13/library/os.html)

- [os.chdir](https://docs.python.org/3.13/library/os.html#os-file-dir)
  change le répertoire courant à l'argument passé
- [os.getcwd](https://docs.python.org/3.13/library/os.html#os-file-dir)
  renvoie le répertoire courant
- [os.listdir](https://docs.python.org/3.13/library/os.html#os.listdir)
  renvoie la liste des fichiers et répertoires dans le répertoire passé
  (ou le répertoire courant si aucun argument n'est passé)


## Module [os.path](https://docs.python.org/3.13/library/os.path.html)

- [os.path.abspath](https://docs.python.org/3.13/library/os.path.html#os.path.abspath)
  transforme le chemin passé en chemin absolu
- [os.path.exists](https://docs.python.org/3.13/library/os.path.html#os.path.exists)
  renvoie `True` si le chemin passé existe
- [os.path.isdir](https://docs.python.org/3.13/library/os.path.html#os.path.isdir)
  renvoie `True` si le chemin passé désigne un répertoire
- [os.path.isfile](https://docs.python.org/3.13/library/os.path.html#os.path.isfile)
  renvoie `True` si le chemin passé désigne un fichier
- [os.path.join](https://docs.python.org/3.13/library/os.path.html#os.path.join)
  concatène les portions de chemin passées
- [os.path.splitext](https://docs.python.org/3.13/library/os.path.html#os.path.splitext)
  sépare la partie *principale* du chemin de l'extension


## Module [string](https://docs.python.org/3.13/library/string.html)

- [string.printable](https://docs.python.org/3.13/library/string.html#string.printable)
  contient les caractères *affichables* (essentiellement les caractères alphanumériques,
  la ponctuation et les espaces)


## Module [sys](https://docs.python.org/3.13/library/sys.html)

- [sys.argv](https://docs.python.org/3.13/library/sys.html#sys.argv)
  donne accès aux arguments passés sur la ligne de commandes
