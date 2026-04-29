
# Módulo Sensor de nivel de agua.

Este documento describe el procedimiento para la integración y conexión del **módulo sensor de nivel de agua** con la placa de expansión (HUB).

![NivelAgua](/docs/electronica/img/NivelAgua.png)

## 1. Especificaciones del Módulo

El dispositivo está diseñado para detectar la presencia de líquidos, el nivel de llenado de un recipiente o la caída de gotas de lluvia. Funciona mediante un principio de conductividad eléctrica, a través de sus pistas. Cuando el agua entra en contacto con las pistas, actúa como un puente eléctrico (resistor variable). A mayor profundidad de inmersión, mayor es el área de contacto, lo que reduce la resistencia y permite el paso de más corriente. Es un sensor analógico porque entrega datos variables dependiendo del voltaje de alimentación y consta de **3 pines**:

|PIN |SIGNIFICADO| CONEXIÓN SUGERIDA (HUB)|
|----|---------------------|----|
| **+** | Alimentación 3.3v | A cualquier pin rojo (3V).|
| **-** | Ground (Tierra) | A cualquier pin negro (G).|
| **S** | Señal analógica | Al pin P1. |

**Nota Técnica:** Aunque la Micro:bit puede contar de 0 a 1023, este sensor funciona un poco diferente. Al mojarse, el valor cambia inmediatamente a 500 o 600 y, aunque lo sumerjas todo, nunca llega a 1023 porque el agua no conduce la electricidad tan perfectamente como un cable. Además, la placa se protege para no recibir una corriente elevada. Por eso, lo mejor es calibrar el sensor: anotar qué número da cuando está seco y qué número da cuando está lleno, y ajustar la programación con esos valores reales.

## 2. Instrucciones de Montaje

1. Asegúrese, antes de realizar alguna conexión, de **apagar el HUB.**
2. **Conecta la Tierra:** Usa un cable para unir el pin **-** del módulo con cualquier pin de la **fila negra** del HUB.
3. **Conexión de Energía:** Conecte el pin **+** del módulo a un pin de la **fila roja** del HUB.
4. **Conexión de Señal:** Conecte el pin **S** al pin amarillo P1 del HUB.

![nivelagua_esquema](/docs/electronica/img/nivelagua_esquema.png)

5. **Enciende y Prueba:** Presiona el interruptor del *HUB* para encender la placa. La Micro:bit debe estar insertada correctamente en la ranura superior.

**Ojo:** La conductividad de los líquidos varía según su composición, afectando la resistencia eléctrica. Debido a que el rango de los datos analógicos entre un nivel de agua bajo y uno óptimo es muy pequeño (apenas un par de unidades), la precisión en la interpretación de los valores es fundamental.

###### En el ejemplo a continuación se aprecia a través de la pantalla oled, la pequeña variación de los datos, dependiendo de la cantidad de agua del recipiente. Cabe destacar que si el nivel del agua baja rápidamente, el sensor aún quedará húmedo, dando lecturas erróneas del nivel del agua.


![nivelagua_funcionamiento](/docs/electronica/img/nivelagua_funcionamiento.png)