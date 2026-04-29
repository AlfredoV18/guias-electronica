
# Servomotores.

Este documento describe el procedimiento para la integración y conexión de los **Servomotores** con la placa de expansión (HUB).

![servo](img/servo.png)

## 1. Especificaciones

El servomotor es un motor de precision que ademas del motor DC contiene engranajes reductores, un circuito de control y un potenciómetro para posicionamiento preciso. A diferencia de un motor DC estándar, el servo mantiene un torque elevado a bajas velocidades debido a que su electrónica interna utiliza PWM de potencia, aplicando ráfagas de voltaje máximo para vencer la carga.

Se clasifican según su rango de movimiento, **los posicionales (180°/270°)** fijan ángulos exactos mediante retroalimentación, mientras que los de **rotación continua** regulan dirección y velocidad. Aunque su respuesta es inmediata, se puede programar un movimiento suave descomponiendo el trayecto en pequeños pasos angulares con pausas de milisegundos. Consta de **3 cables generalmente de los siguientes colores:**

|COLOR DEL CABLE |SIGNIFICADO| CONEXIÓN SUGERIDA (HUB)|
|----|---------------------|----|
| **ROJO** | Alimentación 3.3v | A cualquier pin rojo (Lado servo).|
| **NEGRO O MARRON** | Ground (Tierra) | A cualquier pin negro (G).|
| **AMARILLO o NARANJA** | Señal de control | A cualquier pin azul S (0-7). |

**Nota Tecnica:** 

## 2. Instrucciones de Montaje

1. Asegúrese, antes de realizar alguna conexión, de **apagar el HUB.**
2. **Conecta la Tierra:** Conecte el **cable negro**  del servo con cualquier pin de la **fila negra** del HUB.
3. **Conexión de Energía:** Conecte el **cable rojo** del servo a un pin de la **fila roja** del HUB.
4. **Conexión de Señal:** Conecte el **cable amarillo** a un pin de la **fila azul** (S0 - S7) del HUB.

**Ojo:** Generalmente, los cables de los servomotores terminan en un conector DuPont hembra de 3 pines. Al estar integrados en una sola pieza, se facilita su conexión directa a los pines en una misma columna de pines de la placa de expansión, evitando errores de polaridad.

![servo_conexion](img/servo_conexion.png)

5. **Enciende y Prueba:** Presiona el interruptor del *HUB* para encender la placa. La Micro:bit debe estar insertada correctamente en la ranura superior.

##### En el siguiente ejemplo, a través de una pantalla oled observamos datos la posición actual en grados del servo.


![servo_funcion](img/servo_funcion.png)