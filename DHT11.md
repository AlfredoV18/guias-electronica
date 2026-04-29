
# Módulo Sensor de Humedad y temperatura ambiental

Este documento describe el procedimiento para la integración y conexión del **módulo sensor de humedad y temperatura ambiental DHT11** con la placa de expansión (HUB).

![dht11](/docs/electronica/img/dht11.png)

## 1. Especificaciones del Módulo

El DHT11 es un sensor digital que integra un transductor capacitivo y un termistor NTC. Utiliza un procesador interno para convertir señales analógicas en una trama de datos digital de un solo hilo.

Su comunicación se basa en una ráfaga de 40 bits donde el valor lógico depende de la duración del pulso alto. La trama se organiza en 5 bytes (Humedad, Temperatura y Checksum de validación). Debido a la precisión requerida en microsegundos y al protocolo de "petición-respuesta", es indispensable el uso de librerías para asegurar lecturas estables y evitar errores de sincronización. Dispone de **3 pines** principales:

| PIN | SIGNIFICADO | CONEXIÓN SUGERIDA (HUB) |
| --- | --- | --- |
| **+** | Alimentación 3.3V | A cualquier pin rojo |
| **OUT** | Salida Digital | Pin de señal P8. |
| **-** | Ground (Tierra) | A cualquier pin negro. |

## 2. Datos técnicos

* **Rango de Humedad:** 20% a 90% (Precisión de ±5%).
* **Rango de Temperatura:** 0°C a 50°C (Precisión de ±2°C).
* **Tiempo de muestreo recomendado:** 2 segundos.

## 3. Instrucciones de Montaje

1. Asegúrese, antes de realizar alguna conexión, de **apagar el HUB.**
2. **Conecta la Tierra:** Usa un cable para unir el pin **-** del módulo con cualquier pin de la **fila negra** del HUB.
3. **Conexión de Energía:** Conecte el pin **+** del módulo a un pin de la **fila roja** del HUB.
4. **Conexión de Señal:** Conecte el pin **OUT** al pin amarillo P8 del HUB.

![dht11_conexionesa](/docs/electronica/img/dht11_conexiones.png)

5. **Enciende y Prueba:** Presiona el interruptor del *HUB* para encender la placa. La Micro:bit debe estar insertada correctamente en la ranura superior.

###### En el ejemplo práctico a continuación se observa la activacion de un pequeño ventilador cuando hay altas temperaturas.

![dht11_aplicacion](/docs/electronica/img/dht11_aplicacion.png)
