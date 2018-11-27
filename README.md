GEDEON Anthony
KHIMOUM Médy
MAHOBAH Erdane

==========================================================================================================================================

Attention : 
   Par manque d'un fichier compile.sh, la hiérarchie des dossiers à quelque peu changer pour parlier les problèmes d'importations des différents fichiers ou packages.

+-- restaurant/
|  +--src/
|  |  +--restaurant/
|  |  |  +--(*.java)
|  |  +--logger/
|  |     +--(*.java)
|  +--bin/
+--logger/
|  +--src/
|     +--logger/
|        +--(*.java)
+--testframework/

Par manque de temps à améliorer le programme, le respect de la taille de chaque fichier en terme de ligne n'a pas été effectué.

La quantité de client n'est pas gérée.

Une fois la note d'un client cloturée, si le vendeur veut rajouter un autre produit sur la note il faudra pour chaque produit aller dans le menu de l'application et selectionner "Enregistrer un produit sur la note".

==========================================================================================================================================

Stratégie de résolution de problème :
   Ici un "produit" n'est pas un objet, comme l'on pourrait penser. Ayant eu quelques mals à manipuler certains attribut de l'objet "produit", nous avons décider de définir les produits comme une énumeration.
   
   L'affichage du prix total n'est pas arrondi et affiche des valeurs comme : 35.970000000000006, pourtant les valeurs entrées pour le calcul sont exprimées en centième. Alors on utilise la méthode setRoundingMode() de la classe DécimalFormat.
