# EPSIC-LAMP

# Installation
1. Download and install docker
   - Download the docker installer and follow the instructions
     - [Windows install video](https://youtu.be/GIMExUnjzMw?t=97)  
     - [Download docker for windows](https://download.docker.com/win/stable/Docker%20Desktop%20Installer.exe)  
     - [Download docker for mac](https://download.docker.com/mac/stable/Docker.dmg)  

2. Download this file [docker-compose.yml](https://drive.google.com/file/d/1CuoKkH_11AZVbie_Vum10V4K4Ug67Hqe/view?usp=sharing)

3. Paste the [docker-compose.yml](https://drive.google.com/file/d/1CuoKkH_11AZVbie_Vum10V4K4Ug67Hqe/view?usp=sharing) on your project

4. Open your project with pycharm and edit the file docker-compose.yml
   - replace the values of MYSQL_DATABASE, MYSQL_ROOT_PASSWORD, BACKUP_TIME.
   
5. In your project's pycharm terminal run the command `docker-compose up`
   - If you want to run in background (without logs) run `docker-compose up -d` (optional)

6. You can go now to phpmyadmin: http://localhost:5000/
   - You can login using using the user `root` and using the password you add in the docker-compose.yml

8. If you have problems connecting to the database or phpmyadmin:
   - Try using one of the folowing hosts:
     - `localhost` (Recomended)
     - `0.0.0.0`
     - `127.0.0.1`
