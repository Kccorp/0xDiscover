# 0xDiscover
Ce challenge est orienté stegano et osint. Il consiste a trouver le flag grace à une image donnée

## Scénario

Regarde ce que ma femme ma envoyé de ses dernière vacances, ça lui change des vacances anuelle au camping de Tourcoing tu trouves pas ? Elle m'a aussi dit que je serai incapable de trouver le ce qui ce cache DERIERE cette photo. 

Download : image.jpg

## Writ-up
La premiere étape est de comprendre qu'il y a en réalité un fichier caché dans l'image.
On utilise alors steghide avec la commande suivante 

```bash
steghide --extract -sf <fichier image> -xf <fichier output>
```

on récupère alors un fichier zip protégé par un mot de passe. 
Pour obtenir le mot de passe, il faut se rendre sur google map a l'endroit de l'image et tourné la caméra pour y découvrir un code sur le mure dériere.

Pour cela, il suffit de traduire le nom du batiment, d'aller sur google map puis de faire tout le tour du batiment pour trouver l'endroit en le code permettant de dévérouiller le fichier zip 

```bash
Coordonnée gps = 13.731635, 100.527297

code du zip = 089-802-8569
```





