# Pasos Previos
Este trabajo será sencillo, nos ayudará a recordar todo desde el verano. El objetivo final será programar una placa Arduino con la idea de hacer que dos diodos leds vayan encendiéndose y apagándose alternativamente cada segundo.


## Montaje


### Componentes
Para este reto necesitamos hacer, primero de todo, el montaje. Para ello necesitaremos:
- Dos diodos led (Componente electrónico que permite pasar corriente solo en una dirección, y cuando suceded, emite luz)
- Una resistencia (Componente electrónico con la única función de aumentar los ohmios del circuito)
- Cables (Filamento normalmente metálico usado en electrónica para conectar camponentes a otros)
- Placa Arduino
- Protoboard (Placa punzada con plaquitas metálicas conectando líneas usada para sostener componentes electrónicos)

Aquí tenemos una imagen del montaje que he realizado.

<p align="center">
<img width="500" height="420" alt="download" src="https://github.com/Alexus8650/Robotica-26-27-4ESO/blob/f391dc155fd1c09848fa7d05da4fc3f63b87ca45/Pasos%20Previos/Im%C3%A1genes/Reto1Montaje.png" />
</p>


### Funcionamiento/Explicación
Para que un circuito funcione necesitamos un polo positivo y otro negativo. El cable negativo siempre se representa con el negro, y el positivo normalmente con el rojo, pero en otros casos (como este) no es así. No es así ya que tenemos más de un positivo, entonces si se ponen los dos rojos no se diferenciarían tan bien.

Este circuito funciona así, empecemos por el polo negativo:
- El circuito empieza en el GND (GROUND) o negativo.
- Este transcurre por el cable negro hasta la protoboard.
- En la protoboard se encuentra una resistencia por la que tendrá que pasar sí o sí.
- De la resistencia se divide en dos.
- Por el cable verde, pasa por un diodo y de ahí un cable al pin 4.
- Y pot último, por el azul, pasa por otro diodo y de ahí al pin 2.

<p align="center">
<img width="500" height="420" alt="download" src="https://github.com/Alexus8650/Robotica-26-27-4ESO/blob/f391dc155fd1c09848fa7d05da4fc3f63b87ca45/Pasos%20Previos/Im%C3%A1genes/Reto1Montaje.png" />
</p>










