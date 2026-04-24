
# Módulo Sensor de Temperatura Sumergible

Este documento describe el procedimiento para la integración y conexión del **módulo Sensor de Temperatura Sumergible** (también llamado **DS18B20**) con la placa de expansión (HUB).

![ds18b20](/docs/electronica/img/ds18b20.png)

## 1. Especificaciones del Módulo

Este es un sensor digital de temperatura que utiliza el protocolo 1-Wire para comunicarse; este protocolo necesita solo un pin de datos para comunicarse y permite conectar más de un sensor en el mismo pin. Su encapsulado viene en un tubo de acero inoxidable resistente al agua, por lo que medir temperatura sumergido en líquidos es su especialidad. Consta de **3 pines:**

| PIN | SIGNIFICADO | CONEXIÓN SUGERIDA (HUB) |
|----|---------------------|----|
| **VCC** | Alimentación 3.3V | A cualquier pin rojo (3V). |
| **GND** | Ground (Tierra) | A cualquier pin negro (G). |
| **DAT** | Salida Digital | Al pin P8. |

**Ojo:** La PCB contiene una bornera de 3 terminales, igualmente señalados con VCC, GND y DAT, donde irán atornillados los cables que van hacia el tubo de acero inoxidable. Los colores de los cables son la clave para la conexión:

* Cable color rojo = VCC.
* Cable color negro = GND.
* Cable color amarillo = DAT.

## 2. Instrucciones de Montaje

1. Asegúrese, antes de realizar alguna conexión, de **apagar el HUB.**
2. **Conecta la Tierra:** Usa un cable para unir el pin **GND** del módulo con cualquier pin de la **fila negra** del HUB.
3. **Conexión de Energía:** Conecte el pin **VCC** del módulo a un pin de la **fila roja** del HUB.
4. **Conexión de Señal:** Conecte el pin **DAT** al pin amarillo P8 del HUB.

![ds18b20_conexiones](/docs/electronica/img/ds18b20_conexiones.png)

5. **Enciende y Prueba:** Presiona el interruptor del *HUB* para encender la placa. La Micro:bit debe estar insertada correctamente en la ranura superior.

**Nota técnica:** Al ser un sensor digital y usar el protocolo 1-Wire (1 cable), los datos recibidos son ráfagas de bits (0/1), por lo que es esencial la implementación de librerías específicas para interpretar estos bits.

La temperatura varía de forma progresiva y no instantánea. Esto se debe a la inercia térmica de la cápsula de acero, la cual requiere un breve tiempo de estabilización para igualar la temperatura del fluido o ambiente que se está midiendo.

<small>En el siguiente ejemplo, medimos temperatura en celsius (°C) de un recipiente con agua fria, mostrando los datos en una OLED.</small>


![ds18b20_funcion](/docs/electronica/img/ds18b20_funcion.png)