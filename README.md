# Projet_Kafka

Démarrage de zookeeper:

![zokk_](https://user-images.githubusercontent.com/81563806/173137361-00c8bf87-c9e9-409a-a18c-ec848f63d991.PNG)

Démarrage de kafka:

![D_kafka](https://user-images.githubusercontent.com/81563806/173137434-a30e62b5-c15f-4c57-95a6-f7f3eb3f0ce2.PNG)

On lance le consumer et le producer et on envoie un message depuis le producer vers le consumer pour tester le démarrage de kafka

 ![producer_cons](https://user-images.githubusercontent.com/81563806/173137687-857cc9cf-debd-45ee-86c7-646a9a31d2a4.PNG)
 
On publie un message de type pageEvent vers le topic en utilisant un restcontroller pour qu'un consumer kafka-console-concumer puisse le consumer

 ![3](https://user-images.githubusercontent.com/81563806/173138192-d09554e4-772e-44d2-ab35-9cf5133ca743.PNG)
 
 une fois qu'on actualise le producer le message se transfère vers le consumer
 
 ![4](https://user-images.githubusercontent.com/81563806/173138142-2d7571e0-ec13-4178-aab3-bcce36df93cc.PNG)
 

 ![3](https://user-images.githubusercontent.com/81563806/173138307-ea7497c2-9afd-4bb8-ad14-3a826f21a666.PNG)
 
Maintenant on va créer un consumer dans l'application spring Kafka donc lorsque on actualise le producer le message 
va être consommé par le consumer qu'on a créer et le résultat s'affiche dans le terminal
 
 ![6](https://user-images.githubusercontent.com/81563806/173138602-2c6e16eb-c7eb-4112-b20a-9e803d4b9234.PNG)
 
Dans kafka producer on crée un message au format json qui va être reçu par le consumer

 ![7](https://user-images.githubusercontent.com/81563806/173138924-1236fab2-7f8e-4081-8006-d2c52c171769.PNG)
 
Maintenant on crée une fonction supplier qui permet d'envoyer des messages à chaque seconde vers le consumer

 ![8](https://user-images.githubusercontent.com/81563806/173139622-ff5135cd-c740-4aab-9b71-287d10ec3a11.PNG)
 
  On peut aussi augmenter la vitesse de reçois de messages à l'aide de cette commande  "spring.cloud.stream.poller.fixed-delay=100"

 
 ![9](https://user-images.githubusercontent.com/81563806/173141344-f9e7d3d1-fe69-46c7-80ed-bd950417c0e1.PNG)

 Maintenant on crée une fonction qui gère un input et un output de flux d'enregistrement au même temps,
 c'est à dire un consumer et un producer en utilisant la fonction Function
 
 ![10](https://user-images.githubusercontent.com/81563806/173141395-91789903-4b48-4609-87cf-8c7730e1efe7.PNG)

Kafka Stream :

Pour effectuer un traitement en temps réel on intègre Kafka stream dans l'application

![1_partie2](https://user-images.githubusercontent.com/81563806/173142042-197aafe2-0c36-4237-a10a-194d97dddbce.PNG)

Pour éviter le cumul des résultas on va faire des statistique sur une fenetre de temps de 5 secondes 

![2_p2](https://user-images.githubusercontent.com/81563806/173142204-a52849ce-f7b9-4741-acfc-199ac6eea76a.PNG)

Pour exploiter par la suite les résultats fournit dans ktable dans une application on les stockent dans un store puis on va les interroger avec server sent event

![WhatsApp Image 2022-06-10 at 23 16 18](https://user-images.githubusercontent.com/81563806/173152600-14a1a514-80f2-4608-92a6-eb8c52e608aa.jpeg)

le résultat de client Server Sent Event en utilisant un graphe

![kafka](https://user-images.githubusercontent.com/81563806/173145545-1de471d1-d2fe-43e3-848f-3d52c3161136.png)
