
# Módulo MQ sensor de gases.

Este documento describe el procedimiento para la integración y conexión del **módulo MQ** con la placa de expansión (HUB).

![MQ](/docs/electronica/img/MQ.png)

## 1. Especificaciones del Módulo

Estos sensores son electroquímicos y varían su resistencia cuando se exponen a determinados gases, internamente posee un calentador encargado de aumentar la temperatura interna y con esto el sensor pueda reaccionar con los gases provocando un cambio en el valor de la resistencia. Son sensores con salida analógica pero tambien contienen salida digital integrada con un potenciometro para calibrar el umbral y poder interpretar si hay presencia o no del gas. Costa de **4 pines:**

|PIN |SIGNIFICADO| CONEXIÓN SUGERIDA (HUB)|
|----|---------------------|----|
| **VCC** | Alimentación 3.3v | A cualquier pin rojo (3V).|
| **GND** | Ground (Tierra) | A cualquier pin negro (G).|
| **AO** | Salida Analógica| Al pin P1. |
| **DO** | Salida Digital | Al pin P8. |


## 2. Modelos Comunes y su principal funcion

La diferencia entre los distintos tipos de sensores MQ es la sensibilidad a cierta gama de gases, más sensibles a algunos gases que a otros, pero siempre detectan a más de un gas.

|MODELO |GAS PRINCIPALMENTE  DETECTADO|
|----|---------------------|
| **MQ-2**| GLP, Metano, Hidrógeno, Humo |
| **MQ-3** | Alcohol, Etanol |
| **MQ-4** | Metano |
| **MQ-5** | Gas Natural y GLP, Gas Natural |
| **MQ-6** | GLP (Gas Licuado de Petróleo) |
| **MQ-7** | Monóxido de Carbono |
| **MQ-8** | Hidrógeno |
| **MQ-9** | Monóxido de Carbono y Gases Combustibles |
| **MQ-135** | Calidad del Aire (Amoníaco) |


## 3. Instrucciones de Montaje

1. Asegúrese, antes de realizar alguna conexión, de **apagar el HUB.**
2. **Conecta la Tierra:** Usa un cable para unir el pin **GND** del módulo con cualquier pin de la **fila negra** del HUB.
3. **Conexión de Energía:** Conecte el pin **VCC** del módulo a un pin de la **fila roja** del HUB.
4. **Conexión de Señal:** Conecte el pin **AO** al pin amarillo P1 del HUB y el pin **DO** al pin amarillo P8 del HUB.

**Ojo:** El uso simultáneo de ambas salidas (analógica y digital) es opcional. La elección dependerá exclusivamente de las necesidades específicas de la aplicación.

![MQ_CONEXIONES](/docs/electronica/img/MQ_CONEXIONES.png)

5. **Enciende y Prueba:** Presiona el interruptor del *HUB* para encender la placa. La Micro:bit debe estar insertada correctamente en la ranura superior.

**Nota técnica:** El sensor requiere de 2 a 5 minutos de precalentamiento; al encenderlo, es normal obtener falsas alarmas hasta que se estabilice térmicamente.
Si se alimenta con 3.3V, la estabilización es más lenta y la sensibilidad disminuye. Las lecturas suben rápido al detectar gas, pero bajan despacio.

<sub><sup>En el siguiente ejemplo, utilizamos el MQ2 para detectar la presencia de gas de un encendedor. De igual forma se utiliza el MQ3 para medir gases alcoholicos a traves de un algodon, la cual es su especialidad.</sub><sup>

![MQ_FUNCION](/docs/electronica/img/MQ_FUNCION.png)
