### Partie 1 : Gestion des utilisateurs
Q.2.1.1 

![Capture d'écran 2025-03-14 115732](https://github.com/user-attachments/assets/178ae2d3-a806-4429-a826-972ed1aa23be)


Q.2.1.2 
Accorder au nouveau compte les droits sudo, pour qu’il puisse exécuter des commandes avec les droits administrateur. 


### Partie 2 : Configuration de SSH


Q.2.2.1
**Nano /etc/ssh/ssh_config** 

![Capture d'écran 2025-03-14 121156](https://github.com/user-attachments/assets/c91c0855-4e53-4d1e-b8e9-53e3cafcd3c1)


Relancer le serveur ssh avec la commande : service ssh restart
Q.2.2.2 

![Capture d'écran 2025-03-14 121640](https://github.com/user-attachments/assets/8a220754-aa91-43e2-ac69-67a60141c4b0)


Q.2.2.3 

![Capture d'écran 2025-03-14 122049](https://github.com/user-attachments/assets/a90c6aba-493d-4071-b2b2-0a60dddc7cdb)



### Partie 3 : Analyse du stockage
Q.2.3.1 
Commande : findmnt

![Capture d'écran 2025-03-14 122558](https://github.com/user-attachments/assets/2af516ce-7b69-4607-826c-3e4051a56331)




Q.2.3.2 

Type de stockage utilisé ext4.


Q.2.3.3 

![Capture d'écran 2025-03-14 124228](https://github.com/user-attachments/assets/9361b0f1-8cc5-470e-83a1-960fa506e825)

![Capture d'écran 2025-03-16 201900](https://github.com/user-attachments/assets/dbb9e356-db17-47ff-be46-7d397c4504be)


mdadm -D –-scan m  
mdadm -D /dev/md0  
partx /dev/sdb1  
fdisk -l  


mdadm -detail /dev/md0  
mdadm –manage /dev/md0 —-add /dev/dsb1  
mdadm -detail /dev/md0  
cat /proc/mdstat

![Capture d'écran 2025-03-17 100429](https://github.com/user-attachments/assets/7b3065ef-d491-43cc-94d0-f39ffa3b554a)


Q.2.3.4 

df -h

![Capture d'écran 2025-03-17 101814](https://github.com/user-attachments/assets/edfd8960-8738-4ffc-81b7-8d7097492c10)

![Capture d'écran 2025-03-17 101836](https://github.com/user-attachments/assets/cd3c5a8e-d9bc-431e-8af1-4ce9c6a905f2)

![Capture d'écran 2025-03-17 101853](https://github.com/user-attachments/assets/1f643576-33b8-4bf6-bbef-8e17a22e72ac)

![Capture d'écran 2025-03-17 102106](https://github.com/user-attachments/assets/445ad85c-6877-4c68-9ade-f370fc4054a9)


Q.2.3.5 Combien d'espace disponible reste-t-il dans le groupe de volume ?

![Capture d'écran 2025-03-19 195305](https://github.com/user-attachments/assets/911422d0-4ac4-43a7-b613-d4d1f7ad3207)


### Partie 4 : Sauvegardes

Q.2.4.1 

Bareos-dir : il est le directeur et contrôle le lancement des tâches de sauvegardes, il permet la connexion avec les clients*

Bareos-sd : permet d'accéder aux stockage et d'écrire les sauvegardes

Bareos-fd : réalise les lectures sur les serveurs au moment de la sauvegarde mais également les ecritures en cas de restauration.

### Partie 5 : Filtrage et analyse réseau

Q.2.5.1 

![Capture d'écran 2025-03-19 202823](https://github.com/user-attachments/assets/c63395e6-d715-44a0-b02f-46aef3227a27)

Q.2.5.2 

![Capture d'écran 2025-03-19 203809](https://github.com/user-attachments/assets/12be9b9a-ffd2-4a6f-82e5-13307dfcf5e6)


Q.2.5.3 


Q.2.5.4 

![Capture d'écran 2025-03-19 211814](https://github.com/user-attachments/assets/ea3d91d5-8883-44de-8c45-e89a1c172120)


### Partie 6 : Analyse de logs

Q.2.6.1 

Tentative de connexion Le 20 DÉC 10:24, par l’adresse ip 10.0.0.199 en ssh.
![Capture d'écran 2025-03-20 155316](https://github.com/user-attachments/assets/a6064179-2738-43a5-a7b9-04b282f19a2d)

Le 03 Janvier 11:06, par l’adresse ip 10.0.0.199 en ssh.
![Capture d'écran 2025-03-20 155525](https://github.com/user-attachments/assets/f47d7558-8e8e-4d55-acb7-c1027f036930)

Le 03 Janvier 11:23, par l’adresse ip 10.0.0.199 en ssh.

Le 03 Janvier 12:09, par l’adresse ip fd26:ba41:c8d6:0:ba92:6393:cc55:8b8b en ssh.

![Capture d'écran 2025-03-20 155826](https://github.com/user-attachments/assets/68e4d706-4ae7-453b-a872-812868b9fd20)


![Capture d'écran 2025-03-20 160033](https://github.com/user-attachments/assets/a97ba5f5-6f4f-453e-b1e9-5a8a829e459f)

