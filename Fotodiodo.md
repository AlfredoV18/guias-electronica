
# Módulo Fotodiodo

Este documento describe el procedimiento para la integración y conexión del **módulo fotodiodo** (también conocido como sensor de luz) con la placa de expansión (HUB).

![Fotodiodo](/docs/electronica/img/Fotodiodo.png)

## 1. Especificaciones del Módulo

El dispositivo utiliza un fotodiodo, un componente que detecta luz de manera extremadamente rápida y precisa, convirtiendo la energía lumínica directamente en una señal eléctrica, produciendo una corriente proporcional a la intensidad de la luz, obteniendo una salida digital (0/1) (Encendido/Apagado) ajustando su sensibilidad con el potenciómetro integrado, pero también ofrece una salida analógica para saber con exactitud la cantidad de luz recibida. Consta de **4 pines** principales:

![Fotodiodo_Pines](/docs/electronica/img/Fotodiodo_Pines.png)  


|PIN |SIGNIFICADO| CONEXIÓN SUGERIDA (HUB)|
|----|---------------------|----|
| **VCC** | Alimentación (3.3V-5V) | A cualquier pin rojo |
| **GND** | Ground (Tierra) | A cualquier pin negro. |
| **DO** | Salida de Señal Digital | Pin de señal P8. |
| **AO** | Salida de Señal Analógica | Pin de señal P1. |

**Nota Técnica:**  A mayor intensidad de luz, el módulo tiende a entregar una salida de voltaje bajo (0 lógico); por el contrario, a menor intensidad de luz, la salida de voltaje es alta (1 lógico). Cabe destacar que el potenciometro solo es para regular la sensibilidad de la salida digital.
## 2. Instrucciones de Montaje

1. Asegúrese, antes de realizar alguna conexión, de **apagar el HUB.**
2. **Conecta la Tierra:** Usa un cable para unir el pin **GND** del módulo con cualquier pin de la **fila negra** del HUB.
3. **Conexión de Energía:** Conecte el pin **VCC** del sensor a un pin de la **fila roja** del HUB.
4. **Conexión de Señal:** Conecte el pin **DO** al pin amarillo 8 del HUB y el pin **AO** al pin amarillo 1.

**Ojo:** Perfectamente se puede utilizar una sola salida, ya sea la analógica o la digital; dependerá de la aplicación que se le dé al módulo. Para fines educativos, en este caso utilizamos ambas.

![LDR_Conexiones](/docs/electronica/img/Fotodiodo_conexiones.png)

5. **Enciende y Prueba:** Presiona el interruptor del *HUB* para encender la placa. La Micro:bit debe estar insertada correctamente en la ranura superior.
6. **Calibración:** Gire el potenciómetro para ajustar que la cantidad de luz recibida sea suficiente o no para activar el módulo, según lo requieras.

###### Para este ejemplo, la matriz de LEDs de la Micro:bit actúa como barra medidora de intensidad de luz; utilizando las lecturas analógicas se puede saber este valor de intensidad.


![Fotodiodo_Conluz](/docs/electronica/img/Fotodiodo_Conluz.png) 

###### PIN DO = 0

![Fotodiodo_Sinluz](/docs/electronica/img/Fotodiodo_Sinluz.png)

###### PIN DO = 1 </small>
