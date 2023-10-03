# LES COMMANDES DOCKER

## 1 - Gestion des images

  - creation d'image  :
```
   docker build . 

   NB : cette commande doit être executé dans le repertoire contenant le fichier DockerFile.Si votre
   fichier se trouve à une adresse différente utilisé l'option -f

```
 -  tag d'une image :
```
   docker tag id_image nom_image
```

 - voir la liste des images :
```   
   docker images
```

 - supprimer une image : 
```
   docker rmi nom_image
   NB : IL faudrait qu'aucun conteneur instance de cette image existe
```


## 2 - Gestion des conteneurs
 - creation des conteneurs :
```
   docker container run -p HOST_PORT:CONT_PORT --name [CONT_NAME] IMAGE_NAME

NB : si le nom du conteneur n'est pas renseigné alors docker affectera un nom alétoire au conteneur
-p : spécifie le port hôte sur auquel sera lié le port conteneur
-d : faire tourner notre image en background

```
- se connecter sur un conteneur :
```

docker container exec -it [ID_CONT]/[CONT_NAME]  [shell_type]

```


 - voir la liste des conteneur qui  :
```
   docker container ls ou docker ps

```
    

 - suppression d'un conteneur :
```
  docker container rm [ID_CONT]/[CONT_NAME]
```

 - voir les logs d'un conteneur :
```
 - docker logs [ID_CONT]/[CONT_NAME]
```