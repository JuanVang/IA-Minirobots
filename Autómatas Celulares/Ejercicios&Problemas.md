# Ejercicios y Problemas 
### 1. Observe sus comportamientos en la casa, en la universidad y en el medio de transporte que utiliza. Encuentre, para cada uno de estos escenarios sus reglas básicas
Se presenta un diagrama de flujo para ejemplificar el arbol de decisiones y reglas basicas que se tienen a la hora de usar el tranporte publico.

![Ingreso al transporte publico](https://github.com/user-attachments/assets/537b4038-3b07-44e6-b969-034da1fcaea2)


### 2. Suponga una enfermedad, o un incendio forestal, o una moda, desarrolle un modelo de difusión usando ACs probabilísticos. O simule un robot con dos ruedas que evite obstáculos
Se describe un posible modelo de difusion usando AC probabilisticos para incendios forestales , para esto se define un reticulo cuadrado de 2000 celdas donde cada una de estas representa una hectarea de bosque que puede llegar a ser afectada por un incendio forestal.
Primero se definen los estados w ={Hvsi,Hvni,Hvqs,Hvq,Hdty}, donde:
- Hvsi: Hectareas de vegetacion inflamables 
- Hvni: Hectareas de vegetacion no inflamables
- Hvqs: Hectareas de vegetacion quemandose
- Hvq: Hectareas de vegetacion quemadas
- Hdty: Humedad
  
Se usa la vecindad de moore (8 vecinos).
Inicialmente se propone que dentro del reticulo esten distribuidas 20 celdas Hvqs y 480 celdas Hvsi distribuidos aleatoriamente y 1500 celdas Hvni distribuidas uniformemente 

Reglas
---
Regla 1: Transición de vegetación inflamable a quema activa.

Estado actual: Hvsi (vegetación inflamable). 

Nueva transición: Hvsi → Hvqs (comienza a quemarse).

Condiciones:

+ Si la celda tiene 1-2 vecinos en Hvqs y la humedad Hdty es baja (menor al 40%), la probabilidad de transición es alta -> 65%.
+ Si tiene 3 o más vecinos en Hvqs, la probabilidad de transición es mayor -> 90%, independientemente de la humedad.
+ Si Hdty es alta (mayor al 80%) , se reduce la probabilidad de transición un 40% para simular la dificultad de propagación en condiciones de humedad.

---


### 3. Tome el plano de una ciudad pequeña y localice, por ejemplo, las droguerías, o colegios ¿es posible que falte alguno en la ciudad? Utilice diagramas de Voronoi.

Para este ejercicio se tomara los colegios de Paipa, utilizando la herramienta de la pagina de [Frederik Brasz](https://cfbrasz.github.io/Voronoi.html) se crea el siguiente diagrama de boronoi.

![Voronoi](https://raw.githubusercontent.com/JuanVang/IA-Minirobots/d28eed432cb9c767b368bdbb0e564f869f652ce4/Aut%C3%B3matas%20Celulares/Images/Paipa_Voronoi.png?token=GHSAT0AAAAAAC2LRZLILWUTGP22BF36YNVOZZTOSVA)
