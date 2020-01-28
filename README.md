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
Ensuite, allé dans l'onglet **action** puis collez y ceci en haut

```actionscript
_global.base = _parent._parent;
```
comme ceci 
[![exemple](https://image.noelshack.com/fichiers/2020/05/2/1580213654-unknown-1.png "exemple")](https://image.noelshack.com/fichiers/2020/05/2/1580213654-unknown-1.png "exemple")

Après avoir fait tout ça nous allons utiliser une fonction d'exemple à modifier. Pour mon cas je vais utiliser la fonction **process** qui se trouve dans **dofus/utils/consoleParsers/** et dans le fichier **consoleParsers.ChatConsoleParser.as**
Pour vous y retrouvez dans les dossier qui ont des noms protéger je vous conseille de télécharger les **sources du client** en forma **ActionScript** [ici](http://https://mega.nz/#!s85SzYrI!4_dHg6Z2rkstukznzleS3-xxuK_6l7toDcP8-ZNNIWc "ici")
ainsi que les sources du client avec l'obfuscation [ici](https://mega.nz/#!04w13CKJ!E4_0ZFyz_GM2ndxef3SzgvitcjQU3b3mKWStSI-eU0Y "ici") vous pouvez utiliser le logiciel JPEX pour décompilé quand il y aura des future maj car le lien ne sera pas maintenanu à jour

Pour notre cas la fonction **process** se trouve dans **ddofus/utils/consoleParsers/** et dans le fichier **ChatConsoleParser** (pour le cas non-obfu)
Maintenant ouvrez le fichier **actionscript** puis copier toute la fonction **process**. 
Ensuite, revenez sur synthesis puis coller toute la fonction comme ceci
[![exemple](https://image.noelshack.com/fichiers/2020/05/2/1580215563-unknown-1.png "exemple")](https://image.noelshack.com/fichiers/2020/05/2/1580215563-unknown-1.png "exemple")


```actionscript
_loc1.process = function (sCmd, oParams, oData, opString)
```

par 

```actionscript
base._global.dofus["\x1e\f\x12"]["\x13\x03"]["\x13\x1a"].prototype.process = function (sCmd, oParams, oData, opString)
```

comme ceci
[![exemple](https://image.noelshack.com/fichiers/2020/05/2/1580215684-unknown-1.png "exemple")](https://image.noelshack.com/fichiers/2020/05/2/1580215684-unknown-1.png "exemple")


## informations 
> De nombreux éditeurs de logiciels propriétaires incluent dans leurs CLUF des clauses interdisant la rétro-ingénierie. Cependant dans de nombreux pays la rétro-ingénierie est autorisée par la loi, notamment à des fins d'interopérabilité. Dans ces pays, les clauses de ces CLUF ne sont pas valables, ou tout au plus dans les limites déterminées par la loi.
Par exemple en France, ce droit est garanti par l'article L122-6-1 du code de la propriété intellectuelle. On trouve des dispositions similaires dans la directive 2009/24/CE du Parlement européen et du Conseil du 23 avril 2009.

merci à **Saphiire** pour l'aide en **p-code**.