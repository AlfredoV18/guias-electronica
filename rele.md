
# Módulo Relé

Este documento describe el procedimiento para la integración y conexión del **módulo Relé** con la placa de expansión (HUB).

![rele](/docs/electronica/img/rele.png)

## 1. Especificaciones del Módulo

Este módulo utiliza un relé: un interruptor controlado eléctricamente que permite abrir o cerrar circuitos de potencia mucho mayor a la que puede manejar directamente la placa de expansión con la Micro:bit. Consta de **3 pines** de control (entrada) y un bloque de **3 terminales** para conectar la carga (salida):


|PIN |SIGNIFICADO| CONEXIÓN SUGERIDA (HUB)|
|----|---------------------|----|
| **VCC** | Alimentación (3.3V-5V) | A cualquier pin rojo |
| **GND** | Ground (Tierra) | A cualquier pin negro. |
| **IN** | Señal de Control | Pin de señal P8. |

**Nota Técnica:** El bloque de terminales azul funciona como un desvío eléctrico. El pin central es siempre el Común (COM), mientras que los laterales son Normalmente Abierto (NO) y Normalmente Cerrado (NC). Puedes identificarlos por el diagrama en el reverso de la placa o usando un multímetro en modo continuidad. Este módulo se activa por nivel bajo (*Low Level Trigger*):

* **0 Lógico:** Activa la bobina, el relé hace "click" y la energía pasa del COM al terminal NO.
* **1 Lógico:** El relé vuelve a su estado de reposo y la energía vuelve al terminal NC. 

En esta imagen, la flecha roja representa el camino de la corriente:

![Accionar_rele](/docs/electronica/img/Accionar_rele.png)

## 2. Instrucciones de Montaje

1. **Seguridad:** Antes de realizar cualquier conexión, asegúrese de **apagar el HUB.**
2. **Conexión de Tierra:** Use un cable para unir el pin **GND** del módulo con cualquier pin de la **fila negra** del HUB.
3. **Conexión de Energía:** Conecte el pin **VCC** del módulo a un pin de la **fila roja** del HUB.
4. **Conexión de Señal:** Conecte el pin **IN** al pin amarillo P8 del HUB.

![rele_conexiones](/docs/electronica/img/rele_conexiones.png)

5. **Conexión de la carga:** En los terminales de salida, conecte el dispositivo que desea controlar. Utilice siempre el terminal Común (COM) en conjunto con uno de los laterales (NC o NO), según si necesita que el circuito esté cerrado o abierto por defecto.
6. **Encendido y Prueba:** Presione el interruptor del HUB para encender la placa. La Micro:bit debe estar insertada correctamente en la ranura superior.

*Para este ejemplo, utilizamos LEDs simples para verificar su funcionamiento, pero la verdadera esencia del relé se basa en controlar cargas de mayor potencia en sus terminales de salida, como circuitos de 120 voltios.*

![rele_esquema](/docs/electronica/img/rele_esquema.png)

![rele_funcionamiento](/docs/electronica/img/rele_funcionamiento.png)

