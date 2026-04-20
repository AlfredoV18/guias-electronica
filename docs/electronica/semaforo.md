
# Módulo Semáforo

Este documento describe el procedimiento para la integración y conexión del **módulo semáforo** con la placa de expansión (HUB).

![Modulo_Semaforo_Completo](/docs/electronica/img/Modulo_Semaforo_Completo.png)

## 1. Especificaciones del Módulo

El dispositivo integra tres diodos LED (Rojo, Amarillo y Verde) en una PCB común. Para que funcione, necesitamos identificar sus **4 pines**:

![Modulo_Semaforo_Pines](/docs/electronica/img/Modulo_Semaforo_Pines.png)


|PIN |SIGNIFICADO| ¿DONDE SE CONECTA EN EL HUB?|
|----|---------------------|----|
| **G** | Green (Verde) | Al pin de señal P8. |
| **Y** | Yellow (Amarillo) | Al pin de señal P12. |
| **R** | Red (Rojo) | Al pin de señal P14. |
| **GND** | Ground (Tierra) | A cualquier pin negro.|

## 2. Instrucciones de Montaje

1. Asegurate antes de realizar alguna conexión **Apagar el HUB.**
2. **Conecta la Tierra:** Usa un cable para unir el pin **GND** del semáforo con cualquier pin de la **fila negra** del HUB.
3. **Conecta las Señales:** 
 * Conecte el pin **G** al pin Amarillo **8**.
 * Conecte el pin **Y** al pin Amarillo **12**. 
 * Conecte el pin **R** al pin Amarillo **14**.

![Modulo_Semaforo_Conexiones](/docs/electronica/img/Modulo_Semaforo_Conexiones.png)

 4. **Enciende y Prueba:** Presiona el interruptor del *HUB* para encender la placa . La Micro:bit debe estar insertada correctamente en la ranura superior.

![Modulo_Semaforo_Funcionamiento](/docs/electronica/img/Modulo_Semaforo_Funcionamiento.png)


