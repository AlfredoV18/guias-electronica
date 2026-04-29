
# Módulo sensor de Turbidez.

Este documento describe el procedimiento para la integración y conexión del **módulo sensor de turbidez** con la placa de expansión (HUB).

![Turbidez](/docs/electronica/img/Turbidez.png)

## 1. Especificaciones del Módulo

Este dispositivo permite evaluar la pureza de un líquido mediante la medición de su turbidez, utilizando un sistema de detección óptica basado en un diodo infrarrojo y un fototransistor. El principio de funcionamiento consiste en analizar la transmitancia y dispersión de la luz: al haber partículas suspendidas o Sólidos Suspendidos, el haz de luz se interrumpe o desvía, permitiendo cuantificar el nivel de suciedad. Costa de **3 pines:**

|PIN |SIGNIFICADO| CONEXIÓN SUGERIDA (HUB)|
|----|---------------------|----|
| **V** | Alimentación 3.3v | A cualquier pin rojo (3V).|
| **G** | Ground (Tierra) | A cualquier pin negro (G).|
| **S** | Salida Analógica o Digital | Al pin P1. |

**Nota Tecnica:**  El modulo tiene un pequeño selector para configurar si quieres que el Pin S tenga una salida Analogica o Digital (La salida digital incluye un potenciometro para calibrar su activacion).

![turbidez_info](/docs/electronica/img/turbidez_info.png)

## 2. Instrucciones de Montaje

1. Asegúrese, antes de Xrealizar alguna conexión, de **apagar el HUB.**
2. **Conecta la Tierra:** Usa un cable para unir el pin **G** del módulo con cualquier pin de la **fila negra** del HUB.
3. **Conexión de Energía:** Conecte el pin **V** del módulo a un pin de la **fila roja** del HUB.
4. **Conexión de Señal:** Conecte el pin **S** al pin amarillo P1 del HUB.

![turbidez_conexiones](/docs/electronica/img/turbidez_conexiones.png)

5. **Enciende y Prueba:** Presiona el interruptor del *HUB* para encender la placa. La Micro:bit debe estar insertada correctamente en la ranura superior.

**Recomendaciones:**
* Lógica de Señal: La lectura es inversamente proporcional, a mayor turbidez, menor es el voltaje y el valor analógico. Calibra los umbrales en tu código según tus necesidades.

* Interferencias: Factores externos como la luz ambiental pueden alterar ligeramente los valores; se recomienda medir en entornos de luz controlada.

* Nivel de Agua: Mantén el líquido al menos a la altura indicada en la siguiente imagen para lecturas estables, recuerda que no es impermeable, no lo sumerjas completamente.

![turbidez_nivel](/docs/electronica/img/turbidez_nivel.png)


###### En el siguiente ejemplo, a través de una pantalla OLED observamos datos obtenidos del sensor de turbidez; estableciendo un umbral, podemos declarar el estado del agua.


![turbidez_funcion](/docs/electronica/img/turbidez_funcion.png)