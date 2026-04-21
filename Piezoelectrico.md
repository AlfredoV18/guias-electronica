
# Módulo Piezoelectrico.

Este documento describe el procedimiento para la integración y conexión del **módulo piezoelectrico** con la placa de expansión (HUB).

![piezoelectrico](/docs/electronica/img/piezoelectrico.png)

## 1. Especificaciones del Módulo

Este sensor detecta golpes y vibraciones físicas para convertirlas en datos eléctricos. Es un componente analógico, lo que permite a la micro:bit medir la intensidad del toque en una escala de 0 a 1023. Una característica interesante es su funcionamiento inverso: si le envías voltaje desde la placa, el sensor puede vibrar o emitir sonidos, aunque su principal funcion es la deteccion antes que la emision. Costa de **3 pines:**

|PIN |SIGNIFICADO| CONEXIÓN SUGERIDA (HUB)|
|----|---------------------|----|
| **+** | Alimentación 3.3v | A cualquier pin rojo (3V).|
| **-** | Ground (Tierra) | A cualquier pin negro (G).|
| **S** | Salida Analógica | Al pin P1. |

**Ojo:** El modulo incluye una bornera para conectar la lamina de latón. El cable rojo (centro de la lamina) va al terminal de **INPUT** y cable negro (exterior de la lamina) al terminal de **GND**.

## 2. Instrucciones de Montaje

1. Asegúrese, antes de realizar alguna conexión, de **apagar el HUB.**
2. **Conecta la Tierra:** Usa un cable para unir el pin **G** del módulo con cualquier pin de la **fila negra** del HUB.
3. **Conexión de Energía:** Conecte el pin **V** del módulo a un pin de la **fila roja** del HUB.
4. **Conexión de Señal:** Conecte el pin **AO** al pin amarillo P1 del HUB.

![piezo_conexion](/docs/electronica/img/piezo_conexion.png)

5. **Enciende y Prueba:** Presiona el interruptor del *HUB* para encender la placa. La Micro:bit debe estar insertada correctamente en la ranura superior.

**Nota técnica:** dentro de sus aplicaciones mas comunes se encuentran: Detección de impactos,  Sensores de vibración, Micrófonos de contacto.

<small>En el siguiente ejemplo, la presion ejercida sobre la lamina determina la intensidad de luz con la que alumbra el led.</small>


![piezo_funcionamiento](/docs/electronica/img/piezo_funcionamiento.png)