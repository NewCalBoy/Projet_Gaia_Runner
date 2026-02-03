# PCB Esclave

## Description
Voici le PCB Esclave qui a pour but de gérer la commande des moteurs DC.
<p align="center">
<img src="pcb_slave_3d.png"  width="300">
</p>

Il y a 4 composants principaux : le microcontrolleur, le pont H, le LDO et l'optocoupleur.
Nous avons également 4 connecteurs JST : deux JST pour  l'I2C, un jst pour l'alimentation et un pour le moteur.

## Fonctionnement
### Etape 1
Le PCB Maître communique un octet avec le PCB Esclave via I2C. 
En fonction de la combinaisons des jumpers, l'adresse I2C du PCB Esclave est différente plus de détails dans la section [Adressage I2C]().
### Etape 2
En fonction de l'octet reçu, le PCB Esclave sait s'il doit avancer ou reculer et la vitesse attendue.
