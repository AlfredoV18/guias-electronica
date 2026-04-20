
# Módulo Sensor de Lluvia.

Este documento describe el procedimiento para la integración y conexión del **módulo sensor de Lluvia** con la placa de expansión (HUB).

![Lluvia](/docs/electronica/img/Lluvia.png)

## 1. Especificaciones del Módulo

Gracias a su salida analógica, este módulo puede detectar desde gotas de lluvia hasta niveles de llenado en recipientes, e incluso responder al tacto humano. El sensor mide la humedad en su superficie; mientras más mojado esté, más alto será el valor de voltaje que enviará a la placa, facilitando la interpretación del nivel de agua. Consta de **3 pines**:

|PIN |SIGNIFICADO| CONEXIÓN SUGERIDA (HUB)|
|----|---------------------|----|
| **V** | Alimentación 3.3v | A cualquier pin rojo (3V).|
| **G** | Ground (Tierra) | A cualquier pin negro (G).|
| **S** | Señal analógica | Al pin P1. |

**Nota Técnica:**  Ten cuidado de no mojar sus componentes electronicos, solo puedes mojar las pistas que tienen forma de estrella.

## 2. Instrucciones de Montaje

1. Asegúrese, antes de realizar alguna conexión, de **apagar el HUB.**
2. **Conecta la Tierra:** Usa un cable para unir el pin **G** del módulo con cualquier pin de la **fila negra** del HUB.
3. **Conexión de Energía:** Conecte el pin **V** del módulo a un pin de la **fila roja** del HUB.
4. **Conexión de Señal:** Conecte el pin **S** al pin amarillo P1 del HUB.

![lluvia_conexion](/docs/electronica/img/lluvia_conexion.png)

5. **Enciende y Prueba:** Presiona el interruptor del *HUB* para encender la placa. La Micro:bit debe estar insertada correctamente en la ranura superior.

**Ojo:** El conversor analogico-digital transforma los niveles de voltaje en datos de 0(0V) a 1023(3.3v), estos datos son utiles para definir actuadores.

<small>Debido a su principio de funcionamiento basado en la conductividad, este módulo puede emplearse como un sensor táctil, ya que el dedo actúa como un puente eléctrico entre las pistas de la misma forma que lo hace el agua. Al producirse este contacto, el sensor genera un incremento en el voltaje de salida (nivel alto), lo cual puede monitorearse en tiempo real mediante la pantalla OLED. En esta aplicación práctica, el sensor se configura como un interruptor para activar un LED.</small>


![lluvia_funcionamiento](/docs/electronica/img/lluvia_funcionamiento.png)