# ModerationBot
Bot discord conçu pour l'animation d'ateliers de modération.
## Matériel nécéssaire au bon fonctionnnement du bot
- Un serveur discord correctement configuré
![Frame 7](https://user-images.githubusercontent.com/85356491/120828148-79705480-c55c-11eb-8ba6-2c94517e821d.png)
*configuration conseillée : un channel textuel par participant + un channel textuel commun + un channel de configuration* 


- Une base de données en entrée et en sortie (JSON)  
*par défaut la base de donnée en sortie est structurée de la manière suivante :*  
`{
    "message": "message",
    "emoji": "👍",
    "participant": "IDduParticipant"
  },`  
*La base de données data.json a été constituée à partir de commentaires collectés sur https://www.bodyguard.ai, elle regroupe donc des commentaires pré-modérés issus de Twitter, Youtube, Twitch... libre à vous de constituer une autre base de données*

-Le "ModerationBot" installé sur votre serveur avec tous les droits administrateurs  
*Le bot doit à minima pouvoir écrire et supprimer des messages dans tous les channels. Il doit également pouvoir réagir à des messages et supprimer des réactions*  

## Structure type d'un atelier
- Phase de découverte  
![schéma-1](https://user-images.githubusercontent.com/85356491/120850826-420fa100-c578-11eb-80e2-27971af7d67d.png)
- Modération semi-collective
![schéma-2](https://user-images.githubusercontent.com/85356491/120850916-63708d00-c578-11eb-86a0-be281f88f3a6.png)
- Modération collégiale
![schéma-3](https://user-images.githubusercontent.com/85356491/120851818-a717c680-c579-11eb-9f00-15e6beffa4a0.png)



- Modération collective sans concertations
![schéma-4](https://user-images.githubusercontent.com/85356491/120851141-bb0ef880-c578-11eb-99f5-f9c1f789aeb5.png)


## Interface de modération
Chaque commentaire est transmi aux participants de la manière suivante : 
Ils doivent utiliser une des trois réactions proposées pour transmettre leurs décisions. Seul ces trois emojis sont pris en compte. Une fois le message traité il est supprimé et remplacé par un autre commentaire. Une fois la liste de commentaire en cache épuisée, le participant reçoit un message de mise en attente.


## Les commandes du bot 
*les commandes doivent être écrites et envoyées dans le channel paramétrage*
- la commande **start**,lance l'étape sélectionnée.
- La variable **etapeAtelier** détermine l'étape sélectionnée.  
`if(etapeAtelier == 1){
//////////////////// code de la première phase
}else if(etapeAtelier == 2){
//////////////////// code de la phase 2
}else if(etapeAtelier == 3){
//////////////////// code de la phase 3
}`  
A tout moment la commande **atelier1 / atelier2....** permet de changer la valeur de cette variable et donc de sélectionner une autre étape de l'atelier.
- la commande **end**, clôture l'atelier et assigne à la varible etapeAtelier la valeur "1".
