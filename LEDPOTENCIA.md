
# Módulo LED de potencia 3W

Este documento describe el procedimiento para la integración y conexión del **módulo LED de potencia 3W** con la placa de expansión (HUB).

![LEDPOTENCIA](/docs/electronica/img/LEDPOTENCIA.png)

## 1. Especificaciones del Módulo

El dispositivo consta de un chip LED de alta potencia montado sobre una placa de circuito impreso con núcleo de aluminio incluyendo un transistor de potencia (MOSFET), permitiendo que una señal de baja corriente controle una carga de alta potencia. Dispone de **3 pines** principales:


![LEDPOTENCIA_PINES](/docs/electronica/img/LEDPOTENCIA_PINES.png)  


|PIN |SIGNIFICADO| CONEXIÓN SUGERIDA (HUB)|
|----|---------------------|----|
| **+** | Alimentación (3.3V-5V) | A cualquier pin rojo |
| **G** | Ground (Tierra) | A cualquier pin negro. |
| **S** | Pin de control | Pin de señal P8. |

**Nota técnica:** Si utilizas el pin analógico P0 en lugar del pin digital fijo P8. Esto te permite cambiar el encendido básico (ON/OFF) por intensidad variable, regulando el brillo automáticamente con sensores, potenciómetros, o a través del código para evitar deslumbramientos.

## 2. Instrucciones de Montaje

1. Asegúrese, antes de realizar alguna conexión, de **apagar el HUB.**
2. **Conecta la Tierra:** Usa un cable para unir el pin **G** del módulo con cualquier pin de la **fila negra** del HUB.
3. **Conexión de Energía:** Conecte el pin **+** del sensor a un pin de la **fila roja** del HUB.
4. **Conexión de Señal:** Conecte el pin **S** al pin amarillo P8 del HUB.

![LEDPOTENCIA_Conexiones](/docs/electronica/img/LEDPOTENCIA_Conexiones.png)

5. **Enciende y Prueba:** Presiona el interruptor del *HUB* para encender la placa. La Micro:bit debe estar insertada correctamente en la ranura superior.

**Ojo:** El LED no encenderá solo conectando alimentación y tierra, es indispensable usar el pin de señal **S** para su funcionamiento, ya que funciona como un interruptor.

![LEDPOTENCIA_Funcionamiento](/docs/electronica/img/LEDPOTENCIA_Funcionamiento.png) 

###### PIN S del LED de potencia recibiendo un 1 desde el HUB.