# ModerationBot
Bot discord conçu pour l'animation d'atelier de modération.
## Matériel nééssaire au bon fonctionnnement du bot
- Un serveur discord correctement configuré
![Frame 7](https://user-images.githubusercontent.com/85356491/120825331-93f4fe80-c559-11eb-8bc8-056086c4eb3b.png)
*configuration conseillée : un channel textuel par participant + un channel textuel commun* 
- Une base de donnée en entrée et en sortie (JSON)  
*par défault la base de donnée en sortie est structurée de la manière suivante :*  
`{
    "message": "message",
    "emoji": "👍",
    "participant": "IDduParticipant"
  },`  
*La base de donnée data.json a été constitué à partir de commentaire collectés sur https://www.bodyguard.ai, elle regroupe donc des commentaires pré-modérés issuent de Twitter, Youtube, Twitch... libre à vous de constituer une autre base de donnée*
<img width="1108" alt="Capture d’écran 2021-06-04 à 17 21 05" src="https://user-images.githubusercontent.com/85356491/120827015-4bd6db80-c55b-11eb-92e5-1a11db8ee8ce.png">
