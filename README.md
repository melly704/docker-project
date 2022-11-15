# DevpOps

Projet final DevOps

PARTICIPANTS DU GROUPE :
-ZEBOUDJ MELISSA 
-BELMIHOUB INES SARAH 
-TAFERRANT WASSIM 
-KOUFI NASSIM 

#PARITE 1 :

1-2) aprés avoir télècharger l'image de base python:3.6-alpine , on doit définir le répertoire /opt comme répertoire  de travail .



![Capture d’écran du 2022-11-15 09-21-25](https://user-images.githubusercontent.com/93126220/201900892-3309be11-e995-4bd2-bedf-e8f178480863.png)
![Capture d’écran du 2022-11-15 09-23-11](https://user-images.githubusercontent.com/93126220/201900970-8311c06b-003a-495c-8485-fe1de3149f14.png)



et comme on le voit dans ces images on a télèchargé les images odoo et pgadmin .


Aprés on devait faire un docker build avec le nom de l'image qui nous a était donné a l'énoncé , et puis on construit un container(test-ic-webapp) a partir de cette image ic-webapp .



   ![Capture d’écran du 2022-11-15 09-24-44](https://user-images.githubusercontent.com/93126220/201902654-7f65f4b5-4776-489e-a16d-d7cf13090918.png)
   
   
   
4) on doit éxposer le port 8080 avec la commande docker run :



![Capture d’écran du 2022-11-15 09-25-19](https://user-images.githubusercontent.com/93126220/201903335-8bf2fe47-703b-47d4-afa2-108f3426a6ea.png)


Création du Dockerfile contenant les variables d'environnements et d'autres informations nécessaires .



![Capture_decran_du_2022-11-15_12-26-39](https://user-images.githubusercontent.com/93126220/201908602-ba741608-0106-43d0-99a3-5387efd01429.png)




5) et pour finir avec cette premiere partie on lance l'application :



![Capture d’écran du 2022-11-15 09-29-30](https://user-images.githubusercontent.com/93126220/201904486-73ef99ed-1355-4d66-9550-2b3a4e1b08b5.png)


#PARTIE 2 :


1) On met en place un registre privé avec docker registry .




![Capture d’écran du 2022-11-15 10-38-49](https://user-images.githubusercontent.com/93126220/201904949-cdbe2b08-15af-4018-8c4c-9405d9e5b8f9.png)
![Capture d’écran du 2022-11-15 10-40-00](https://user-images.githubusercontent.com/93126220/201905351-b0cafeef-9f1b-4c72-a6dc-b82ad5ff2c36.png)



2-3) on rajoute une interface web à ce registre et une fois fait on supprime le container test  et on push notre image sur notre registre privé Docker et sur le registre dockerhub :



![Capture d’écran du 2022-11-15 10-44-20](https://user-images.githubusercontent.com/93126220/201905855-d8566ff4-f3d1-4a72-824a-c75bcd60e1eb.png)
![Capture d’écran du 2022-11-15 10-44-47](https://user-images.githubusercontent.com/93126220/201905877-131ad2ca-7d28-4069-9360-bdd266b1799d.png)

#Partie 3 :

On commencer par rédiger le fichier docker-compose.yml qui nous permet de déployer les quatres services demandés :

1)On crée une base de donnée postgresql


![Capture_decran_du_2022-11-15_11-15-21](https://user-images.githubusercontent.com/93126220/201913808-145d3fb8-e5a9-4fcf-94d4-92a473582fdd.png)




2)On met en place l'application Odoo qui stockes ses informations dans la base postgres 



![Capture_decran_du_2022-11-15_12-55-17](https://user-images.githubusercontent.com/93126220/201914550-bb8e8390-35a1-4a0c-bd76-13019dc49c32.png)




3) Puis on met en place l'application pgadmin permettant visualiser la base postgres dans une IHM



![Capture_decran_du_2022-11-15_11-27-28](https://user-images.githubusercontent.com/93126220/201914690-44027912-d416-4900-a8d0-9a8f02b8e092.png)


![Capture_decran_du_2022-11-15_11-28-35](https://user-images.githubusercontent.com/93126220/201914731-4739820f-46b9-4442-b9e3-0861090d8000.png)




4)Pour finir on met en place l'application ic-webapp qui pointe sur le odoo et le pgadmin déployés localement 



![Capture_decran_du_2022-11-15_12-59-48](https://user-images.githubusercontent.com/93126220/201914797-fea5452c-837d-4c00-ba23-608e749d34d8.png)



![Capture_decran_du_2022-11-15_12-54-49](https://user-images.githubusercontent.com/93126220/201914829-e4c05407-4048-4e1b-a85b-12e39c06ae1b.png)



