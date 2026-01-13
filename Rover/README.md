# Partie 1 : Rover
La partie mobile, dite le Rover, se décompose en 2 partie, les PCBs Esclave c'est-à-dire ceux des roues et le PCB Maître c'est à dire celui qui gère la partie Rover et le bras robotisé.

## Architecture déportée (Avantages et Inconvénients)
L'avantage d'une architecture déportée comme celle choisit pour le Rover est que c'est modulable. En effet chaque PCB Esclave contrôle un moteur et est en liasion I2C avec le PCB Maître, ce qui permet de passer d'une structure à 4 roues motrices à 6 ou bien 2 roues motrices.

L'incovénient est que plusieurs PCBs impliquent potentiellement plus de PCB en panne.

Voici ci-dessous un schéma du Rover

<img width="808" height="810" alt="image" src="https://github.com/user-attachments/assets/298b60f3-5451-477a-a77e-840785801af8" />
_Figure 1 : Schéma du Rover_
