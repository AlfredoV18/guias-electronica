
# Módulo Fotorresistor LDR

Este documento describe el procedimiento para la integración y conexión del **módulo fotorresistor LDR** con la placa de expansión (HUB).

![LDR](/docs/electronica/img/LDR.png)

## 1. Especificaciones del Módulo

El dispositivo utiliza una fotorresistencia, un componente cuya resistencia eléctrica varía drásticamente según la cantidad de luz que recibe, a poca luz más resistencia, con mucha luz poca resistencia. Cuenta con un potenciómetro para ajustar manualmente a cuánta intensidad de luz queremos que se active, obteniendo una salida digital (0/1) (Encendido/Apagado). Consta de **3 pines** principales:

![LDR_PINES](/docs/electronica/img/LDR_PINES.png)  


|PIN |SIGNIFICADO| CONEXION SUGERIDA (HUB)|
|----|---------------------|----|
| **VCC** | Alimentación (3.3V-5V) | A cualquier pin rojo |
| **GND** | Ground (Tierra) | A cualquier pin negro. |
| **DO** | Salida de Señal Digital | Pin de señal P8. |



**Nota Técnica:** El diseño de la placa permite medir la variación de resistencia directamente en los bornes de la LDR. Utilice un multímetro para experimentar el cambio de valores entre los estados de oscuridad total e iluminación artificial o natural.
## 2. Instrucciones de Montaje

1. Asegúrese antes de realizar alguna conexión **Apagar el HUB.**
2. **Conecta la Tierra:** Usa un cable para unir el pin **GND** del módulo con cualquier pin de la **fila negra** del HUB.
3. **Conexión de Energía:** Conecte el pin **VCC** del sensor a un pin de la **fila roja** del HUB.
4. **Conexión de Señal:** Conecte el pin **DO** al pin amarillo 8 del HUB.

![LDR_Conexiones](/docs/electronica/img/LDR_Conexiones.png)

 5. **Enciende y Prueba:** Presiona el interruptor del *HUB* para encender la placa . La Micro:bit debe estar insertada correctamente en la ranura superior.
 6. **Calibración:** Gire el potenciómetro para ajustar la cantidad de luz recibida sea suficiente o no para activar el módulo, según lo requieras.

*Este módulo representa la lógica básica de una fotocelda, la cual se utiliza para automatizar el encendido de las luces residenciales al anochecer y su apagado al amanecer, ¡una de sus aplicaciones más comunes!*


![ConLuz](/docs/electronica/img/ConLuz.png) 

<small>PIN DO = 0 </small>

![Aplicando_Sombra](/docs/electronica/img/Aplicando_Sombra.png)

<small>PIN DO = 1 </small>