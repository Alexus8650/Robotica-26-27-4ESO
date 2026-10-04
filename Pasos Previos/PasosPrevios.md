# PASOS PREVIOS
Este trabajo será sencillo, nos ayudará a recordar todo desde el verano. El objetivo final es programar una placa Arduino con la idea de hacer prácticas con muchos componentes compatibles con Arduino.

> Se organizará en "Retos", un reto es una práctica. Empecemos con el primero.


# Reto 1
Este reto consistirá en hacer que dos diodos leds se enciendan y se apagen alternativamente cada segunodo.


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

*Los pines son los puertos de comunicación de la placa con el propio circuito

<p align="center">
<img width="500" height="420" alt="download" src="https://github.com/Alexus8650/Robotica-26-27-4ESO/blob/f391dc155fd1c09848fa7d05da4fc3f63b87ca45/Pasos%20Previos/Im%C3%A1genes/Reto1Montaje.png" />
</p>


## Programa
Este es el programa que se le implementa a la placa para el funcionamiento del circuito:

<p align="center">
<img width="350" height="350" alt="download" src="https://github.com/Alexus8650/Robotica-26-27-4ESO/blob/9b8c2b577a78e330fa24e7df1841cb440a67d16d/Pasos%20Previos/Im%C3%A1genes/C%C3%B3digoReto1.PNG" />
</p>

Este programa hace que, con el montaje anterior, se vayan encendiéndose y apagándose alternativamente cada segundo los dos diodos leds.

Todos los programas tienen dos partes básicas:
- Void setup
- Void loop

### Void Setup
Todo "Void" se programa entre llaves, todo lo que esté entre ellas se consideran parte del programa. En este caso se llama "setup". Esto significa que se reproducirá una sola vez.

Este te sirve para preparar la placa de Arduino del montaje al que está conectada (Si no usas Arduino servirá para preparar el procesador que se esté usando).

En este caso se usará específicamente para preparar los pines 2 y 4, para ponerlos de dirección de salida. Esto es porque los pines dijitales (1-13) se pueden usar de entrada (Input) o salida (Output), en este caso de salida. De ahí la línea de código: "pinMode(2, OUTPUT);".

Lo primero que lee Arduino, después del "Void Setup" y procesar que todo lo que vendrá a continuación será para realizaarlo una vez, es el "pinMode". Este le dice a Arduino que la línea es para decirle el modo en el que estará ese pin. Después le dicen, entre paréntesis, el pin al que le pondrá el modo, en este caso el 2. Y por último, después de una coma de separación, le dice al modo al que se pondrá el pin, en este caso "OUTPUT", porque se usará para enviar información hacia afuera.

El "Void Setup" tiene dos líneas de código, en este caso con el mismo uso, pero una es para el pin2 y la segunda para el pin4. Los dos en "OUTPUT" porque enviarán información hacia fuera, en este caso a dos leds.


### Void Loop
Este "Void" es igual al anterior, solo que al llamarse "Loop" No se hace solo una vez. Se reproducirá continuamente sin descanso, cuando termina empieza por el principio sin parar.

Entre las llaves nos encontramos los siguientes comantos:

- digitalWrite();
- delay();

El "digitalWrite" le dice al procesador que escriba digitalmente en un pin el estado en el que debe estar, me explico. Al leer la línea, el procesador pone el pin digital indicado en el estado indicado. Ej.: "digitalWrite(2, HIGH);". Traducción: "Dale corriente al pin digital 2.

El "delay" sirve para hacer pausas de tiempo. Al leer este comando, Arduino espera tantos milisegundos como se diga entre los paréntesis. Ej.: "delay(1000);". Traducción: "Esperate 1000 milegundos (1 segundo) antes de leer la siguiente línea".


El resultado final de este void traducido a nuestro idioma sería:
- Dale corriente al pin 2
- Quítale corriente al pin 4
- Espera 1s
- Quítale corriente al pin 2
- Dale corriente al pin 4
- Espera 1s
- Repite todo


En el programa de verdad se pone HIGH o LOW (1 o 0) para dar o quitar corriente. Y por supuesto al final de cada línea un punto y coma ( ; ).


## Resultado
El resultado es el expuesto en el programa se van encendiendo y apagando alternativamente cada segundo los dos diodos leds.

| El Azul Encendido | El Verde Encendido |
|----------|----------|
| <img width="500" height="420" alt="download" src="https://github.com/Alexus8650/Robotica-26-27-4ESO/blob/2e846fe006de81482aa3dcbec59a1d30e59dc0ac/Pasos%20Previos/Im%C3%A1genes/Reto1LedAzul.png" /> | <img width="500" height="420" alt="download" src="https://github.com/Alexus8650/Robotica-26-27-4ESO/blob/2e846fe006de81482aa3dcbec59a1d30e59dc0ac/Pasos%20Previos/Im%C3%A1genes/Reto1LedVerde.png" />   |




















































