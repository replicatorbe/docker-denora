1. Pré-requis 

1.1 Avoir un container mysql déjà lancé ou en créer un.  Pour en créer un :

docker run -d -e MYSQL_ROOT_PASSWORD=passworddesire --name mysqldenora mysql    

1.2 Créer une base de donnée et importer le fichier denora.sql + le fichier destiné à votre IRCd (les fichiers sont disponibles dans le répository). 
1.3 Configurez le fichier de configuration denora.conf 

2. Lancer le container denora IRC

docker run -d --name denorairc --link=mysqldenora:mysql --link=unrealircd:unrealircd denorairc

Dans notre exemple, nous allons lier le container avec notre service Denora IRC au serveur Mysql et à notre serveur Unrealircd qui est également géré par Docker. 

A vous d’adapter votre commande.






    
