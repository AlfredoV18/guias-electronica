
# Módulo RGB

Este documento describe el procedimiento para la integración y conexión del **módulo RGB** con la placa de expansión (HUB).

![Modulo_RGB](/docs/electronica/img/Modulo_RGB.png)

## 1. Especificaciones del Módulo

El dispositivo integra tres diodos emisores de luz (Rojo, Verde y Azul) en un solo componente, montados sobre una placa de circuito impreso (PCB) que facilita su implementación. La mezcla de estos tres colores primarios mediante señales de intensidad variable permite generar una amplia gama cromática. El módulo cuenta con una interfaz de 4 pines:

![Circulo_Cromatico](/docs/electronica/img/Circulo_Cromatico.png)   


|PIN |SIGNIFICADO| CONEXION SUGERIDA (HUB)|
|----|---------------------|----|
| **R** | Red (Rojo) | Pin de señal P1. |
| **G** | Green (Verde) | Pin de señal P2. |
| **B** | Blue (Azul) | Pin de señal P8. |
| **-** | Ground (Tierra) | A cualquier pin negro.|

**Nota:** Se recomienda el uso de los pines P1 y P2 debido a que son canales dedicados de alta precisión, libres de interferencias, lo que garantiza una señal PWM estable para la mezcla de colores.(En caso de requerir los pines P1 y P2 para otros sensores de lectura analógica crítica, este módulo puede ser reubicado en pines digitales como el P8, P12 o P14, manteniendo la funcionalidad mediante modulación PWM).

## 2. Instrucciones de Montaje

1. Asegurese antes de realizar alguna conexión **Apagar el HUB.**
2. **Conecta la Tierra:** Usa un cable para unir el pin **-** del modulo con cualquier pin de la **fila negra** del HUB.
3. **Conecta las Señales:**     
 * Conecte el pin **R** al pin Amarillo **P1**.
 * Conecte el pin **G** al pin Amarillo **P2**. 
 * Conecte el pin **B** al pin Amarillo **P8**.

![Modulo_RGB_Conexiones](/docs/electronica/img/Modulo_RGB_Conexiones.png)

 4. **Enciende y Prueba:** Presiona el interruptor del *HUB* para encender la placa . La Micro:bit debe estar insertada correctamente en la ranura superior.

![Modulo_RGB_Funcionamiento](/docs/electronica/img/Modulo_RGB_Funcionamiento.png)

###### Para color Morado: R: 512, G:0, B: 512</small>



