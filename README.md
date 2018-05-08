# Persistance en Java 

Persistence (serialization puis JPA)

suite de https://github.com/ISSAEGITHUB/CycleCTPbesoin0

## Persistance native [Source](http://aisl.cnam.fr/xwiki/wiki/aisl/view/GLG203/TP02)

L'un des fondements de la programmation Orientée Objet réside dans l'idée de réutilisation. La plate-forme Java collecte pour sa part les objets en mémoire afin qu'ils puissent être accédés à partir de n'importe quelle application Java. Cependant, cette réutilisabilité n'est valable que tant que la Java Virtual Machine (JVM) est lancée : si celle-ci est arrêtée, le contenu de la mémoire disparaît.

C'est ici que la sérialisation intervient : elle permet de stocker l'état des objets, ainsi que la manière de les recréer pour plus tard. Un objet peut ainsi exister entre deux exécutions d'un programme, ou entre deux programmes : c'est la persistance objet. La persistance est ainsi le fait « d'exister dans le temps ». Un objet qui reste en l'état lorsqu'il est sauvegardé puis chargé par une autre application, ou à un moment éloigné, possède la propriété de persistance. En conséquence, l'objet n'est plus dépendant de l'application qui l'a créé.

Les objets peuvent être sérialisés sur le disque dur interne, ou sur le réseau disponible (Internet compris). Pour rendre un objet persistant, il faut le sérialiser en implémentant l'interface java.io.Serializable au sein de la classe : Java saura alors comment utiliser l'objet.

Au travers de ce mécanisme de sérialisation, Java fournit une méthode facile, transparente et standard de réaliser cette opération : cela permet facilement de mettre en place un mécanisme de persistance. Il est de ce fait inutile de créer un format particulier pour sauvegarder et relire un objet. Le format utilisé est indépendant du système d'exploitation. Ainsi, un objet sérialisé sur un système peut être réutilisé par un autre système pour récréer l'objet.

Java introduit le mot-clé transient qui précise que l'attribut qu'il qualifie ne doit pas être inclus dans un processus de sérialisation et donc de désérialisation.


## Persistance JSON avec Gson

voir exemple https://github.com/opentrainingcamp/TP-GLG-Cnam-Liban/blob/master/PremierTP/Client.md

## un exemple

Travail demandé

1. Transformer les Hashmap en mémoire des Clients en sauvegarde format GSON dans des fichier du système de fichier (trouver une bijection simple entre une référence SGF et une référence en Mémoire)
3. remplacer vos commandes (TP1) (par menu) par des appels services webs
    1. créer les service web REST
    2. appeler les services ainsi créé
2. Utiliser JPA et mysql pour la présidence 

#Quelques liens

https://www.geeksforgeeks.org/file-handling-java-using-filewriter-filereader/
https://www.mkyong.com/java/how-to-write-to-file-in-java-fileoutputstream-example/
https://java2blog.com/gson-example-read-and-write-json/

