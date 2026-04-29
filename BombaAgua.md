
# Bomba de Agua Sumergible.

Este documento describe el procedimiento para la integración y conexión de las **Bombas de Agua Sumergibles** con la placa de expansión (HUB).

![bomba](/docs/electronica/img/bomba.png)

## 1. Especificaciones
Es un dispositivo electromecánico de tipo centrífugo, diseñado para el transporte de líquidos en una baja escala mediante la conversión de energía eléctrica de corriente continua en energía hidráulica, su motor está sellado herméticamente, lo que permite meterla directamente dentro de un recipiente con agua sin que ocurra un cortocircuito. Consta de **2 cables generalmente de los siguientes colores:**

|COLOR DEL CABLE |SIGNIFICADO| CONEXIÓN SUGERIDA (HUB)|
|----|---------------------|----|
| **ROJO** | Alimentación 3 a 5V | Pin M1|
| **NEGRO O MARRON** | Ground (-) | Pin M1.|

## 2. Instrucciones de Montaje

1. Asegúrese, antes de realizar alguna conexión, de **apagar el HUB.**
2. **Conecta la Tierra:** Conecte el **cable negro**  de la bomba a un pin de **M1** del HUB.
3. **Conexión de Energía:** Conecte el **cable rojo** de la bomba a un pin de **M1** del HUB.

**Nota Tecnica:** El conector M1 de la placa de expansion se compone de dos pines (positivo y negativo). Como la polaridad no se percibe a simple vista, es posible conectar la bomba de forma inversa. Esto no dañará el motor, pero invertirá su sentido de giro. Dado que las aspas centrífugas están optimizadas para empujar el agua en una sola dirección, una conexión inversa resultará en una pérdida de presión y caudal, haciendo que el flujo de agua sea un poco más débil de lo normal.

![bomba_conexion](/docs/electronica/img/bomba_conexion.png)

4. **Enciende y Prueba:** Presiona el interruptor del *HUB* para encender la placa. La Micro:bit debe estar insertada correctamente en la ranura superior.

###### La bomba de agua puede combinarse con diversos sensores, funcionando como el actuador que responde a los datos recibidos. Por ejemplo, en un sistema de riego automatizado, la bomba se activa para regar una planta solo cuando el sensor de humedad de suelo detecta que el nivel de agua es insuficiente

![bomba_funcion](/docs/electronica/img/humedadsuelo_funcionalidad.png)