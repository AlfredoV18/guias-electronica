 
# Módulo Pantalla OLED 0.96 pulgadas

Este documento describe el procedimiento para la integración y conexión del **módulo Pantalla OLED 0.96** con la placa de expansión (HUB).

![oled](/docs/electronica/img/oled.png)

## 1. Especificaciones del Módulo

Esta pantalla se caracteriza por su alta eficiencia energética y un contraste superior, gracias a su tecnología de píxeles auto-emisores que elimina la necesidad de retroiluminación (backlight). Ofrece una matriz de **128x64 píxeles**, permitiendo un control individual de estos. Utiliza el protocolo de comunicación **I2C**, lo que simplifica el cableado al requerir solo dos líneas de datos. Consta de **4 pines**:

|PIN |SIGNIFICADO| CONEXIÓN SUGERIDA (HUB)|
|----|---------------------|----|
| **VCC** | Alimentación 3.3v | A cualquier pin rojo (3V).|
| **GND** | Ground (Tierra) | A cualquier pin negro (G).|
| **SCL** | Reloj | Pin 19. |
| **SDA** | Datos | Pin 20.|

**Nota Técnica:** Los módulos I2C como el OLED necesitan una dirección única para ser identificados, que generalmente es 0x3C (decimal 60); esta viene grabada en el PCB y algunas pantallas permiten cambiarla a 0x3D mediante un puente de soldadura. Aunque muchas librerías de programación "asumen" la dirección por defecto para simplificar el código sin tener que escribirla manualmente.

## 2. Instrucciones de Montaje

1. Asegúrese antes de realizar alguna conexión de **Apagar el HUB.**
2. **Conecta la Tierra:** Conecte el pin **GND** del módulo al pin **G** de la fila inferior de comunicación I2C del HUB (Funciona también en cualquier pin negro).
3. **Conexión de Energía:** Conecte el pin **VCC** del módulo al pin **3V** de la fila inferior de comunicación I2C del HUB (Funciona también en cualquier pin rojo 3V).
4. **Conexión de Señal:** Conecte el pin **SCL** del módulo al pin P19 del HUB y el pin **SDA** del módulo al pin P20 del HUB.

![oled_esquema](/docs/electronica/img/oled_esquema.png)

 4. **Enciende y Prueba:** Presiona el interruptor del *HUB* para encender la placa. La Micro:bit debe estar insertada correctamente en la ranura superior.

**Ojo:** Las pantallas OLED además de poder crear líneas, cuadros, círculos o incluso imágenes y gráficos, también podemos mostrar datos de sensores (Variables) o textos y mensajes de alerta.

###### El ejemplo a continuación demuestra el control de un sistema en tiempo real. La pantalla OLED visualiza la variable 'Intensidad', la cual traduce la posición física del potenciómetro en un valor porcentual (0-100%). Al mismo tiempo, la Micro:bit utiliza este dato para ajustar el brillo del LED mediante una señal de salida, permitiendo observar la relación directa entre el dato digital en pantalla y la respuesta física del componente.

![oled_aplicacion](/docs/electronica/img/oled_aplicacion.png)