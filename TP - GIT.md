# TP - GIT
### Qu'est-ce que Git ?
Git est un système de gestion de versions décentralisé qui permet de suivre les modifications apportées à des fichiers et des projets informatiques.
#
### Sommaire :
- [*Lab0*](#Lab0)
- [*Lab1*](#Lab1)
- [*Lab2*](#Lab2)
#
## Lab0
__Mettre à jour__ les fichiers puis __installer Git__.\
Vérifier l'installation de __Git__ ainsi que sa version avec la commande _git -v_.

![alt text](img_git/image.png)\
![alt text](img_git/image(1).png)

__Créer__ le répertoire **siosisr** et se déplacer dedans.

![alt text](img_git/image(2).png)\
![alt text](img_git/image(3).png)

__Renommer__ la branche principale **master** par __main__, initialiser le repository.\
(La commande _git config --global init.defaultBranch main_ permet de changer le nom de la branche par défaut ; pas besoin de retaper la commande à chaque fois car le changement est définitif.)

![alt text](img_git/image(4).png)\
![alt text](img_git/image(5).png)

__Créer__ le fichier __README.md__, __script.sh__ et __index.html__.

![alt text](img_git/image(6).png)

__Ajouter__ les fichiers dans le __staging__ avec la commande _git add ._ puis __commiter__ avec la commande _git commit -m "description du commit"_.\
Pour vérifier le __staging__, taper la commande _git status_ et pour vérifier le __commit__, taper la commande _git log_.

![alt text](img_git/image(7).png)\
![alt text](img_git/image(8).png)

__Créer__ le fichier __.gitignore__ avec la commande _touch nom_du_fichier_ (ce fichier permet d'ignorer les fichiers log) puis __créer__ ensuite le fichier __control.log__ avec cette même commande.\
Ajouter tous les fichiers au __staging__ et vérifier que le fichier __control.log__ n'est pas traqué.

![alt text](img_git/image(9).png)

__Créer la release 1.0.0__ à l'aide de tags.

![alt text](img_git/image(10).png)\
![alt text](img_git/image(33).png)
#

## Lab1
__Créer__ une branche __feature1__  dans laquelle le fichier __index.html__ sera modifié en y ajoutant un _nom_ comme _firstname_ et un _prénom_ comme _lastname_.\
__Commiter__ la modification. 

![alt text](img_git/image(11).png)\
![alt text](img_git/image(12).png)\
![alt text](img_git/image(13).png)

__Merger__ la branche __feature1__ avec la branche __main__. (la branche feature1 sera supprimée par la suite)\
Pour merger la branche feature1, __revenir__ sur la branche __main__ au préalable.\
On peut voir que des modifications ont été prises en compte.

![alt text](img_git/image(14).png)

__Créer__ une branche __fix5__  dans laquelle le fichier __script.sh__ sera modifié.\
__Commiter__ la modification.

![alt text](img_git/image(15).png)

__Revenir__ sur la branche principale (__main__) puis modifier le fichier __script.sh__ avec un contenu différent de celui de la branche __fix5__.\
__Commiter__ la modification.

![alt text](img_git/image(16).png)

__Merger__ la branche __main__ avec la branche __fix5__.\
On peut constater un confilt en rapport avec le contenu du fichier __script.sh__.

![alt text](img_git/image(17).png)

Régler le conflit, __commiter__ la modification finale et enfin __supprimer__ la branche fix5.

![alt text](img_git/image(18).png)
#
## Lab2
Dans __Github__ créer un nouveau __repository__ que l'on nommera __siosisr__.

![alt text](img_git/image(19).png)\
![alt text](img_git/image(20).png)

Sur la machine, __générer__ une clé SSH puis copier la __clé publique__ sur Github. Pour ce faire, aller dans les __settings__ puis __SSH and GPG keys__. Enfin, cliquer sur __New SSH key__ puis coller la clé publique.\
Valider.

(Pour générer une clé SSH : _ssh-keygen -t ed25519_ ; appuyer sur __Entrer__ jusqu'à ce que la clé soit générer. Pour voir la clé publique : _cat ~/.ssh/ed_ed25519.pub_ ; copier toute la clé __SAUF__ le _user@exemple_ à la fin)

![alt text](img_git/image(24).png)\
![alt text](img_git/image(21).png)\
![alt text](img_git/image(22).png)\
![alt text](img_git/image(23).png)\
![alt text](img_git/image(25).png)

Ajouter la __clé SSH__ de Github au fichier __~/.ssh/known_hosts__ sur la machine, sinon la connexion SSH échouera.

![alt text](img_git/image(28).png)

Configurer le __repository local__ pour pouvoir communiquer ensuite avec le __repository distant__.\
Vérifier à l'aide de la commande _git remote -v_.

![alt text](img_git/image(27).png)\
![alt text](img_git/image(26).png)

__Pousser__ le projet sur Github.

![alt text](img_git/image(29).png)\
![alt text](img_git/image(30).png)\
![alt text](img_git/image(31).png)\
![alt text](img_git/image(32).png)