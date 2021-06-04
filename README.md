# ModerationBot
Bot discord conçu pour l'animation d'atelier de modération.
## Matériel nééssaire au bon fonctionnnement du bot
- Un serveur discord correctement configuré
![Frame 7](https://user-images.githubusercontent.com/85356491/120828148-79705480-c55c-11eb-8ba6-2c94517e821d.png)
*configuration conseillée : un channel textuel par participant + un channel textuel commun* 


- Une base de donnée en entrée et en sortie (JSON)  
*par défault la base de donnée en sortie est structurée de la manière suivante :*  
`{
    "message": "message",
    "emoji": "👍",
    "participant": "IDduParticipant"
  },`  
*La base de donnée data.json a été constitué à partir de commentaire collectés sur https://www.bodyguard.ai, elle regroupe donc des commentaires pré-modérés issuent de Twitter, Youtube, Twitch... libre à vous de constituer une autre base de donnée*

-Le "ModerationBot" installé sur votre serveur avec tous les droits administrateurs  
*Le bot doit à minima pouvoir écrire et supprimer des messages dans tous les channels. Il doit également pouvoir réagir à des messages et supprimer des réactions*  

## Les commande du bot 
- La variable atelier permet de connaître l'**etapeAtelier** détermine l'étape en cours.
`if(etapeAtelier == 1){
//////////////////// code de la première phase
}else if(etapeAtelier == 2){
//////////////////// code de la phase 2
}else if(etapeAtelier == 3){
//////////////////// code de la phase 2
}`

