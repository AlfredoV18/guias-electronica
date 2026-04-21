
# Módulo Sensor de Ruido.

Este documento describe el procedimiento para la integración y conexión del **módulo sensor de ruido o sonido** con la placa de expansión (HUB).

![Sonido](/docs/electronica/img/Sonido.png)

## 1. Especificaciones del Módulo

Este módulo emplea un micrófono de condensador para transformar las vibraciones del aire en señales eléctricas. Ofrece una salida analógica (0-1023) y una digital (0 o 1). Incluye un potenciómetro para calibrar la sensibilidad de la respuesta digital, el cual influye directamente en el comportamiento de la señal analógica. Posee una interfaz de conexión de **4 pines:**

![sonido_pines](/docs/electronica/img/sonido_pines.png)

|PIN |SIGNIFICADO| CONEXIÓN SUGERIDA (HUB)|
|----|---------------------|----|
| **+** | Alimentación 3.3v | A cualquier pin rojo (3V).|
| **GND** | Ground (Tierra) | A cualquier pin negro (G).|
| **AO** | Salida Analógica | Al pin P1. |
| **DO** | Salida Digital  | Al pin P8. |

## 2. Instrucciones de Montaje

1. Asegúrese, antes de realizar alguna conexión, de **apagar el HUB.**
2. **Conecta la Tierra:** Usa un cable para unir el pin **GND** del módulo con cualquier pin de la **fila negra** del HUB.
3. **Conexión de Energía:** Conecte el pin **+** del módulo a un pin de la **fila roja** del HUB.
4. **Conexión de Señal:** Conecte el pin **DO** al pin amarillo P8 y el pin **AO** al pin amarillo P1 del HUB.

**Ojo:** El uso simultáneo de ambas salidas (analógica y digital) es opcional. Debido a su versatilidad, la salida analógica suele ser suficiente para cubrir los requerimientos de la mayoría de los proyectos, permitiendo procesar el umbral de activación directamente por software. La elección dependerá exclusivamente de las necesidades específicas de la aplicación.

![sonido_conexiones](/docs/electronica/img/sonido_conexiones.png)

5. **Enciende y Prueba:** Presiona el interruptor del *HUB* para encender la placa. La Micro:bit debe estar insertada correctamente en la ranura superior.


**Nota técnica:** Dada la baja ganancia del preamplificador integrado, la variación detectada por el microcontrolador es mínima ante ruidos distantes. Se recomienda ajustar la lógica del programa para responder a incrementos leves sobre el valor de reposo y situar el sensor lo más cerca posible de la fuente emisora para maximizar la tasa de éxito en la detección.


<small>En el siguiente ejemplo, configuramos el sistema para que el LED conmute su estado (encendido/apagado) cada vez que el módulo detecte un estímulo acústico (un aplauso) que genere un flanco de subida en la salida digital (estado lógico 1).</small>


![Sonido_funcionamiento](/docs/electronica/img/Sonido_funcionamiento.png)