
# Módulo Sensor de nivel de agua.

Este documento describe el procedimiento para la integración y conexión del **módulo sensor de nivel de agua** con la placa de expansión (HUB).

![oled](/docs/electronica/img/oled.png)

## 1. Especificaciones del Módulo

El dispositivo esta diseñado para detectar la presencia de líquidos, el nivel de llenado de un recipiente o la caída de gotas de lluvia. Funciona mediante un principio de conductividad eléctrica, a traves de sus pistas. Cuando el agua entra en contacto con las pistas, actúa como un puente eléctrico (resistor variable). A mayor profundidad de inmersión, mayor es el área de contacto, lo que reduce la resistencia y permite el paso de más corriente. Es un sensor analogico porque entrega datos variables dependiendo del voltaje de alimentacion y consta de **4 pines**:

|PIN |SIGNIFICADO| CONEXION SUGERIDA (HUB)|
|----|---------------------|----|
| **+** | Alimentacion 3.3v | A cualquier pin rojo (3V).|
| **-** | Ground (Tierra) | A cualquier pin negro (G).|
| **S** | Señal analogica | Al pin P1. |

**Nota Técnica:** Aunque la Micro:bit puede contar de 0 a 1023, este sensor funciona un poco diferente. Al mojarse, el valor cambia de golpe a 350 y, aunque lo sumerjas todo, nunca llega a 1023 porque el agua no conduce la electricidad tan perfectamente como un cable. Además, la placa se protege para no recibir una corriente elevada. Por eso, lo mejor es calibrar el sensor: anotar qué número da cuando está seco y qué número da cuando está lleno, y ajustar la programacion con esos valores reales.

## 2. Instrucciones de Montaje

1. Asegúrese, antes de realizar alguna conexión, de **apagar el HUB.**
2. **Conecta la Tierra:** Usa un cable para unir el pin **-** del módulo con cualquier pin de la **fila negra** del HUB.
3. **Conexión de Energía:** Conecte el pin **+** del módulo a un pin de la **fila roja** del HUB.
4. **Conexión de Señal:** Conecte el pin **OUT** al pin amarillo P8 del HUB.

![oled_esquema](/docs/electronica/img/oled_esquema.png)

 4. **Enciende y Prueba:** Presiona el interruptor del *HUB* para encender la placa . La Micro:bit debe estar insertada correctamente en la ranura superior.

**Ojo:**Las pantallas OLED ademas de poder crear lineas, cuadros, circulos o incluso imagenes y graficos, tambien podemos mostrar datos de sensores (Variables) o textos y mensajes de alerta.

<small>El ejemplo a continuacion demuestra el control de un sistema en tiempo real. La pantalla OLED visualiza la variable 'Intensidad', la cual traduce la posición física del potenciómetro en un valor porcentual (0-100%). Al mismo tiempo, la Micro:bit utiliza este dato para ajustar el brillo del LED mediante una señal de salida, permitiendo observar la relación directa entre el dato digital en pantalla y la respuesta física del componente.</small>

![oled_aplicacion](/docs/electronica/img/oled_aplicacion.png)





