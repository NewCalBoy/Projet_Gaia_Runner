# Partie 1 : Rover
La partie mobile, dite le Rover, se décompose en 2 partie, les PCBs Esclave c'est-à-dire ceux des roues et le PCB Maître c'est à dire celui qui gère la partie Rover et le bras robotisé.

## Architecture déportée (Avantages et Inconvénients)
L'avantage d'une architecture déportée comme celle choisit pour le Rover est que c'est modulable. En effet chaque PCB Esclave contrôle un moteur et est en liasion I2C avec le PCB Maître, ce qui permet de __passer d'une structure à 4 roues motrices à 6 ou bien 2 roues motrices__.

L'incovénient est que plusieurs PCBs impliquent potentiellement __plus de PCB en panne__.

Voici ci-dessous un schéma du Rover

<img width="404" height="405" alt="image" src="https://github.com/user-attachments/assets/298b60f3-5451-477a-a77e-840785801af8" />

_Figure 1 : Schéma du Rover_

## Détaille du châssis
Les différentes solutions techniques retenues sont :

<details>
  <summary>
    Les moteurs DC FIT0186 de chez DFROBOT (JGB37-3530B)
  </summary>
Comme le projet consiste à commander le robot le choix d'un moteur DC est pertinent, de plus le modèle choisit présente un encodeur ce qui permet un asservissement en vitesse si nécessaire. Plus de détail dans [Moteur DC](https://github.com/FumesecALPHA/Projet_Gaia_Runner/tree/674c549c6b83edb7b40dcca6f1f06973df5d85ec/Rover/Moteur_DC)
  [Moteur DC](url:https://github.com/FumesecALPHA/Projet_Gaia_Runner/tree/674c549c6b83edb7b40dcca6f1f06973df5d85ec/Rover/Moteur_DC)
</details>
