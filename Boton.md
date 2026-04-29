
# Módulo Botón Pulsador

Este documento describe el procedimiento para la integración y conexión de las **Módulo Botón Pulsador** con la placa de expansión (HUB).

![boton](/docs/electronica/img/boton.png)

## 1. Especificaciones
Es un sensor digital de entrada. Su función es cerrar un circuito eléctrico cuando se presiona, permitiendo que pase una señal hacia la Micro:bit. Consta de **3 pines:**

|PINES |SIGNIFICADO| CONEXIÓN SUGERIDA (HUB)|
|----|---------------------|----|
| **VCC** | Alimentación 3 a 5V | A cualquier pin rojo (3V)|
| **GND** | Ground (Tierra) | A cualquier pin negro|
| **OUT** | Salida digital | Pin P8.|

## 2. Instrucciones de Montaje

1. Asegúrese, antes de realizar alguna conexión, de **apagar el HUB.**
2. **Conecta la Tierra:** Conecte el pin **GND** del módulo a un pin de la **fila negra** del HUB.
3. **Conexión de Energía:** Conecte el pin **VCC** del módulo a un pin de la **fila roja** del HUB.
4. **Conexión de Señal:** Conecte el pin **OUT** al pin amarillo **P8** del HUB.

**Nota Tecnica:** El pin OUT del módulo presenta un estado lógico bajo (0V) en reposo y conmuta a un estado lógico alto (VCC) mediante la pulsación, enviando la señal de activación al HUB.

![Boton_conexion](/docs/electronica/img/Boton_conexion.png)

5. **Enciende y Prueba:** Presiona el interruptor del *HUB* para encender la placa. La Micro:bit debe estar insertada correctamente en la ranura superior.

###### Es este ejemplo sencillo, controlamos un componente de salida (LED) mediante una señal de entrada (botón), utilizando pines independientes en el microcontrolador.

![bomba_funcion](/docs/electronica/img/boton_funcion.png)