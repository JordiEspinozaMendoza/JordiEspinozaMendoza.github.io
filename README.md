# 74hc595 shift register

El chip de registro de desplazamiento es un elemento electrónico capaz de adquirir un flujo de datos en serie desde uno de sus PIN (datos PIN), almacenar estos datos y exponerlos en sus 8 PIN de salida (Q0, Q1, …Q7).

<!-- img -->

![]("./src/image1.png")

Cada pin de salida puede tener un valor de 0 (apagado) o 1 (encendido). Para activar o desactivar cada uno de estos valores, ingresamos los datos utilizando los PIN de datos y reloj del chip en un diagrama de tiempo preciso. El reloj necesita recibir nueve pulsos. En cada pulso (en el flanco ascendente), si el PIN de datos es alto, se inserta un 1 en el registro de desplazamiento; en caso contrario, un 0.

![]("./src/image2.png")

Además de los PIN de salida (Q0…Q7), datos, reloj y pestillo, se exponen otros PIN 74hc595:

Vcc y GND: por supuesto 5v y tierra a salida de potencia
OE (habilitación de salida): este PIN habilita o deshabilita la salida. 74hc595 expone la salida cuando el OE es bajo (0)
MR (Master Reclear): este PIN borra la memoria cuando se establece en 0. Por lo tanto, tener 74hc595 en ejecución significa que MR está conectado a 1.
serOut (salida en serie): se usa cuando necesita controlar un segundo registro de desplazamiento adjunto.

![]("./src/image3.png")

