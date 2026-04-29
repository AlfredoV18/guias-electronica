
# Módulo Detector de Objeto Infrarojo

Este documento describe el procedimiento para la integración y conexión del **módulo Detector de Objeto Infrarojo** con la placa de expansión (HUB).

![Detector_ObjetosIR](/docs/electronica/img/Detector_ObjetoIR.png)

## 1. Especificaciones del Módulo

El dispositivo utiliza un par de diodos (emisor y receptor) para detectar el rebote de luz infrarroja. Cuenta con un potenciómetro de precisión para ajustar el rango de detección, obteniendo una salida digital (0/1) (Encendido/Apagado). Consta de **3 pines** principales:

![Detector_ObjetoIR_Pines](/docs/electronica/img/Detector_ObjetoIR_Pines.png)   


|PIN |SIGNIFICADO| CONEXION SUGERIDA (HUB)|
|----|---------------------|----|
| **VCC** | Alimentacion (3.3V-5V) | A cualquier pin rojo |
| **GND** | Ground (Tierra) | A cualquier pin negro. |
| **OUT** | Salida de Señal Digital | Pin de señal P8. |

**Nota Técnica:** Este sensor opera bajo el principio de **Lógica Inversa**. Es decir, en "Estado de Reposo", cuando no detecta ningun objeto cerca de su rango, su salida sera un 1 logico constante. Por el contrario cuando esta en "Estado de Deteccion", conmuta a un 0 logico (0V). 

## 2. Instrucciones de Montaje

1. Asegurese antes de realizar alguna conexión **Apagar el HUB.**
2. **Conecta la Tierra:** Usa un cable para unir el pin **GND** del modulo con cualquier pin de la **fila negra** del HUB.
3. **Conexión de Energía:** Conecte el pin VCC del sensor a un pin de la **fila roja** del HUB.
4. **Conexion de Señal:** Conecte el pin OUT al pin amarillo 8 del HUB.

![Detector_ObjetoIR_Conexiones](/docs/electronica/img/Detector_ObjetoIR_Conexiones.png)

 5. **Enciende y Prueba:** Presiona el interruptor del *HUB* para encender la placa . La Micro:bit debe estar insertada correctamente en la ranura superior.
 6. **Calibracion:** Gira el potenciometro para ajustar el rango de deteccion que sea optimo para ti.

![Objeto_detectado](/docs/electronica/img/Objeto_detectado.png)

###### Salida = 0 (aplicando la logica inversa)

![Objeto_NOdetectado](/docs/electronica/img/Objeto_NOdetectado.png) 

###### Salida = 1 (aplicando la logica inversa)





