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
  <summary><strong>Les moteurs DC FIT0186 de chez DFROBOT (JGB37-3530B)</strong></summary>  

Comme le projet consiste à commander le robot le choix d'un moteur DC est pertinent, de plus le modèle choisit présente un encodeur ce qui permet un asservissement en vitesse si nécessaire. Plus de détail dans [Moteur DC](https://github.com/FumesecALPHA/Projet_Gaia_Runner/blob/main/Rover/Moteur_DC).
  
</details>
<details>
  <summary><strong>Les roues omnidirectionnelles</strong></summary>  

Le choix des roues omnidirectionnelles vient du faites qu'il s'agit du moyen le plus adapté pour déplacer notre robot avec une architecture à 4 roues motrices. Plus de détail dans [Roues omnidirectionnelles](https://github.com/FumesecALPHA/Projet_Gaia_Runner/blob/main/Rover/Roues_omnidirectionnelles).
  
</details>
<details>
  <summary><strong>Les PCBs Esclave</strong></summary>  

Le but de ces PCBs est de séparer le contrôle des moteurs DC du PCB Maître, cela permet de s'adapter à un châssis avec 4, 6 ou encore 2 roues motrices. Plus de détail dans [PCB Esclave](https://github.com/FumesecALPHA/Projet_Gaia_Runner/tree/blob/main/Rover/PCB_Slave).
  
</details>
