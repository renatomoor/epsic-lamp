# EPSIC-LAMP


## Attention
 - Assurez-vous d'avoir désactivé toutes les applications comme WAMP, MAMP, UWAMP...

# Installation
1. Téléchargez et installez docker
   - Téléchargez le programme d'installation de docker et suivez les instructions
     - [Vidéo d'installation de Windows](https://youtu.be/GIMExUnjzMw?t=97)  
     - [Télécharger Docker pour Windows](https://download.docker.com/win/stable/Docker%20Desktop%20Installer.exe)  
     - [Télécharger Docker pour Mac](https://download.docker.com/mac/stable/Docker.dmg)  

2. Téléchargez ce fichier [docker-compose.yml](https://drive.google.com/file/d/1CuoKkH_11AZVbie_Vum10V4K4Ug67Hqe/view?usp=sharing)

3. Collez le fichier [docker-compose.yml](https://drive.google.com/file/d/1CuoKkH_11AZVbie_Vum10V4K4Ug67Hqe/view?usp=sharing) sur votre projet

4. Ouvrez votre projet avec pycharm et éditez le fichier docker-compose.yml
   - remplacer les valeurs de MYSQL_DATABASE, MYSQL_ROOT_PASSWORD, BACKUP_TIME.
   
5. Dans le terminal pycharm de votre projet, exécutez la commande `docker-compose up -d`
Vous devriez voir cette réponse:
```
   Starting xxxxx_db_1         ... done
   Starting xxxxx_phpmyadmin_1 ... done
   Starting xxxxx_backups_1    ... done
```

   - Si vous souhaitez exécuter avec logs, exécutez `docker-compose up` (optionnelle)

6. Vous pouvez maintenant aller sur phpmyadmin: http://localhost:5000/ ou http://0.0.0.0:5000/ ou http://127.0.0.1:5000/
   - Vous pouvez vous connecter en utilisant l'utilisateur `root` et en utilisant le mot de passe que vous avez ajouté dans le docker-compose.yml

8. Si vous rencontrez des problèmes de connexion à la base de données ou à phpmyadmin:
   - Essayez d'utiliser l'un des hosts suivants:
     - `localhost` (Recomended)
     - `0.0.0.0`
     - `127.0.0.1`

### Redémarrer
Pour redémarrer epsic-lapm, accédez à votre console de projet et exécutez ces commandes une par une:
```
docker-compose down
docker-compose up -d
```

