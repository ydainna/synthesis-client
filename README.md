# synthesis-client

## synthesis client késako ?

Le module synthesis client est utilisé pour le client de jeu dofus retro. Celui-ci permet des modifications client plus simplifiée en passant outre l'obfuscation du client de base.

## les dossiers

dans le dossier client il y a :

- le **loader** à remplacer par celui de base qui se trouve dans votre dossier retroclient (%appdata%/Appdata/Local/Ankama/zaap/retro/ressources/app/retroclient/) (je vous conseilles de dupliquer le dossier ''retro'' sur votre bureau (copier - coller))
- le module **synthesis** à ajouter dans le dossier modules qui se trouve dans votre dossier retroclient (%appdata%/Appdata/Local/Ankama/zaap/retro/ressources/app/retroclient/)

dans le dossier src :

- le fichier **synthesis** en forma .fla que vous pour pourrez ouvrir avec un IDE comme **Adobe flash cs6** ou **Macromedia flash pro 8**

## le fonctionnement

Pour la modification il suffit d'ouvrir le fichier synthesis.fla dans un IDE comme adobe flash cs6 ou macromedia 8.
Une fois fais vous pouvez créer un nouveau calque comme ceci (**adobe flash cs6 est utiliser pour les exemples**)

[![exemple](https://image.noelshack.com/fichiers/2020/05/2/1580213184-unknown-1.png "exemple")](https://image.noelshack.com/fichiers/2020/05/2/1580213184-unknown-1.png "exemple")

Une fois fais vous pouvez lui donner le nom que vous voulez cela n'a aucune importance pour la suite.
Ensuite, allé dans l'onglet ''action'' puis collez y ceci en haut

```actionscript
_global.base = _parent._parent;
```


## informations 
> De nombreux éditeurs de logiciels propriétaires incluent dans leurs CLUF des clauses interdisant la rétro-ingénierie. Cependant dans de nombreux pays la rétro-ingénierie est autorisée par la loi, notamment à des fins d'interopérabilité. Dans ces pays, les clauses de ces CLUF ne sont pas valables, ou tout au plus dans les limites déterminées par la loi.
Par exemple en France, ce droit est garanti par l'article L122-6-1 du code de la propriété intellectuelle. On trouve des dispositions similaires dans la directive 2009/24/CE du Parlement européen et du Conseil du 23 avril 2009.

merci à **Saphiire** pour l'aide en **p-code**.