
# Módulo Sensor de Humedad del Suelo

Este documento describe el procedimiento para la integración y conexión del **módulo Sensor de Humedad del Suelo** (FC-28) con la placa de expansión (HUB).

![Humedadsuelo](/docs/electronica/img/Humedadsuelo.png)

## 1. Especificaciones del Módulos

El dispositivo consta de dos partes: las sondas y el módulo de control que utiliza un comparador. Su principio se basa en que, cuando el suelo está húmedo, la resistencia eléctrica entre las dos sondas disminuye (permitiendo el paso de más corriente). Por el contrario, cuando el suelo está seco, la resistencia aumenta (pasa menos corriente). Con este mecanismo, podemos obtener una salida digital (0/1) calibrando su sensibilidad mediante el potenciómetro integrado, o bien obtener valores de 0 a 1023 a través de la salida analógica, lo que permite una mejor precisión en su aplicación. Consta de **4 pines** principales:

![Pines_humedadsuelo](/docs/electronica/img/Pines_humedadsuelo.png)  


|PIN |SIGNIFICADO| CONEXIÓN SUGERIDA (HUB)|
|----|---------------------|----|
| **VCC** | Alimentación 3.3V | A cualquier pin rojo |
| **GND** | Ground (Tierra) | A cualquier pin negro. |
| **DO** | Salida de Señal Digital | Pin de señal P8. |
| **AO** | Salida de Señal Analógica | Pin de señal P1. |

## 2. Instrucciones de Montaje

1. Asegúrese, antes de realizar alguna conexión, de **apagar el HUB.**
2. **Conecta la Tierra:** Usa un cable para unir el pin **GND** del módulo con cualquier pin de la **fila negra** del HUB.
3. **Conexión de Energía:** Conecte el pin **VCC** del módulo a un pin de la **fila roja** del HUB.
4. **Conexión de Señal:** Conecte el pin **DO** al pin amarillo 8 del HUB y el pin **AO** al pin amarillo 1.

**Ojo:** Perfectamente se puede utilizar una sola salida, ya sea la analógica o la digital; dependerá de la aplicación que se le dé al módulo.

![esquema_humedadsueldo](/docs/electronica/img/esquema_humedadsueldo.png)

5. **Enciende y Prueba:** Presiona el interruptor del *HUB* para encender la placa. La Micro:bit debe estar insertada correctamente en la ranura superior.
6. **Calibración:** Gire el potenciómetro para ajustar que la cantidad de humedad percibida sea suficiente o no para activar el módulo a través del **DO**, según lo requieras.

###### A continuación se presenta el diagrama de una de sus aplicaciones más comunes, que sirve para saber la "salud" de tu jardín, accionando una bomba de agua cuando lo necesite la planta.


![humedadsuelo_funcionalidad](/docs/electronica/img/humedadsuelo_funcionalidad.png) 

###### Cuando hay mucha resistencia en las sondas (No hay humedad en la tierra) el PIN DO del módulo es = 1