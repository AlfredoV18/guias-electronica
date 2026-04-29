
# Módulo Botón Touch

Este documento describe el procedimiento para la integración y conexión del **Módulo Botón Touch** (TTP223) con la placa de expansión (HUB).

![touch](/docs/electronica/img/touch.png)

## 1. Especificaciones
Es un interruptor con salida digital que se activa al detectar el tacto. El módulo de fábrica viene con una alta sensibilidad, tanto que no hace falta presionarlo. Realmente no detecta el contacto físico, sino los cambios en la capacitancia (A través de alteraciones en el campo electromagnético); por ello, la simple cercanía de un objeto conductor (no necesariamente un dedo) es suficiente para que el sensor se active. Consta de **3 pines:**

|PINES |SIGNIFICADO| CONEXIÓN SUGERIDA (HUB)|
|----|---------------------|----|
| **VCC** | Alimentación 3 a 5V | A cualquier pin rojo (3V)|
| **GND** | Ground (Tierra) | A cualquier pin negro|
| **I/O** | Salida digital | Pin P8.|

**Nota técnica**: El fabricante del módulo permite configurar ciertas operaciones avanzadas a través de algunas pequeñas modificaciones en la placa del dispositivo. Por ejemplo:

* Podemos integrar un pequeño condensador de hasta 25pF. Una buena práctica para que el módulo se active al contacto físico y no con la simple cercanía es implementarle uno de 10pF.
* Tiene unos pequeños puntos de soldadura identificados como **A y B**:
    * Si unimos los puntos de **A**, el interruptor funciona como normalmente cerrado; si presionamos, se abre.
    * Si unimos los puntos de **B**, el interruptor funciona como un switch que se enclava en un estado; si presionamos, se mantiene en un estado (encendido o apagado) hasta que se vuelva a presionar. Al encender, comienza con un estado bajo (o apagado).
    * Si unimos los puntos de **A** y **B** al mismo tiempo, funciona también como un switch que se enclava en un estado, pero con la peculiaridad de que al encenderlo comenzará en un estado alto (o encendido).

![touch_pcb](/docs/electronica/img/touch_pcb.png)

## 2. Instrucciones de Montaje

1. Asegúrese, antes de realizar alguna conexión, de **apagar el HUB.**
2. **Conexión de Tierra:** Conecte el pin **GND** del módulo a un pin de la **fila negra** del HUB.
3. **Conexión de Energía:** Conecte el pin **VCC** del módulo a un pin de la **fila roja** del HUB.
4. **Conexión de Señal:** Conecte el pin **I/O** al pin amarillo **P8** del HUB.

![touch_conexion](/docs/electronica/img/touch_conexion.png)

5. **Encienda y Pruebe:** Presione el interruptor del *HUB* para encender la placa. La Micro:bit debe estar insertada correctamente en la ranura superior.

###### En este ejemplo sencillo, el touch presionado enciende un LED que está conectado a un pin diferente del OUT.

![touch_funcion](/docs/electronica/img/touch_funcion.png)