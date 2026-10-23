# Lab 4 - Diseño y construcción de una incubadora neonatal a escala 
- María Angel Benavides Silva - 5600852
- Evelyn Marcela Caro Rodríguez - 5600848

## Parte A 

La incubadora neonatal es un dispositivo médico que tiene como objetivo brindar un entorno controlado a los recién nacidos que necesitan cuidados especiales. Su funcionamiento combina elementos mecánicos, eléctricos y electrónicos que permiten regular las condiciones internas y facilitar la supervisión del neonato. Para esto es importante coordinar la estructura, los sensores y la alimentación eléctrica para poder mantener el microambiente de la incubadora especialmente para los recién nacidos prematuros, quienes presentan una capacidad de termorregulación limitada debido a su inmadurez fisiológica.

Los elementos fundamentales de una incubadora pueden clasificarse en estructura mecánica, sistema de calentamiento y de circulación de aire, sensores, unidad de control, sistema de humidificación, interfaz de usuario y alimentación eléctrica. Otros modelos incluyen otras funciones, como la medición de peso o la medición de la temperatura cutánea. Por tanto, las características específicas dependen del diseño y de las opciones disponibles en cada equipo

##
***Cúpula y puertas de acceso***

La cúpula constituye la cubierta que separa el ambiente externo del espacio donde se encuentra el neonato. Su función es la de limitar la exposición a corrientes de aire y reducir las alteraciones del microambiente interno, sin impedir la observación del paciente. Una opcion es el uso de acrílico transparente debido a que permite visualizar el interior y formar una barrera física frente al entorno.

Las puertas y los puertos de acceso permiten realizar intervenciones sin retirar completamente la cubierta. Estos elementos buscan facilitar la atención y disminuir la pérdida de calor durante la manipulación del neonato. En equipos comerciales, como la Isolette 8000 plus, se incorporan paneles de acceso y cortinas de aire que contribuyen a conservar las condiciones internas durante la atención.

##
***Chasis y soporte del colchón***

El chasis es la estructura que proporciona soporte mecánico a la incubadora. En el prototipo descrito por Restrepo Pérez et al., sostiene la cúpula y el portacolchón, además de alojar la fuente de alimentación y los circuitos electrónicos. Los autores emplearon acero inoxidable para obtener una estructura resistente y dispusieron una rejilla interna para separar los circuitos de la lámina metálica.

El portacolchón sostiene la superficie sobre la que permanece el neonato. También se pueden incorporar mecanismos de inclinación o elementos para la medición de peso. Como por ejemplo un sensor de carga al soporte de la cama, la medición de peso debe realizarse con esta en posición horizontal, lo que evidencia la relación entre el montaje mecánico y la confiabilidad de la lectura.

##
***Sistema de calentamiento y circulación de aire***

El sistema térmico suministra el calor necesario para alcanzar la temperatura seleccionada dentro de la incubadora. Este sistema está compuesto por un calentador cerámico y ventiladores, cuya operación permite calentar el aire y favorecer su distribución en la cámara. El ventilador contribuye a reducir las diferencias de temperatura y humedad entre distintas.

##
***Sensores***

Los sensores permiten conocer las condiciones internas y suministran la información necesaria para ejecutar acciones de regulación o activar alarmas. Con sensores de temperatura, humedad, luz y sonido y una alarma de apertura de puerta. Estas mediciones permiten monitorear variables que pueden alterar el ambiente del neonato.

En consecuencia, debe distinguirse entre la temperatura del aire de la cámara y la temperatura del neonato, esta distinción es importante para interpretar correctamente qué variable mide y regula cada sistema.

##
***Sistema de humidificación***

El sistema de humidificación permite modificar la humedad relativa dentro de la cámara. Para esto es posible implementar un nebulizador ultrasónico conectado a un ventilador para introducir aire humidificado, también un ventilador de deshumidificación que introduce aire exterior cuando es necesario reducir considerablemente la humedad interna.

La humedad y la temperatura son variables relacionadas durante la operación. La entrada de aire exterior y el funcionamiento del humidificador producen variaciones térmicas que deben ser compensadas por el controlador. Por su parte, la Isolette 8000 plus permite ajustar la humedad manualmente o utilizar un modo automático que la modifica en función de la temperatura del aire seleccionada.

##
***Sistema de medición de peso***

La medición de peso es una función complementaria que puede integrarse al soporte de la cama incorporando un sensor de carga y electrónica de adquisición basada en el módulo HX711, con visualización de la lectura en una pantalla LCD. Para evaluar su funcionamiento, se deben comparar las mediciones del sistema con las obtenidas mediante una balanza de referencia.

La incorporación de este sistema requiere considerar tanto la adquisición electrónica como la transmisión mecánica de la carga. La documentación de la Isolette 8000 plus presenta una báscula como opción del equipo, lo que indica que esta función no forma parte necesariamente de todas las configuraciones de incubadora.

##
***Interfaz de usuario y alarmas***

La interfaz de usuario permite observar las variables medidas y modificar los valores de referencia. Esto se puede realizar mediante una pantalla LCD que muestra temperatura, humedad relativa y peso, mientras que pulsadores, potenciómetros e indicadores luminosos permiten ajustar parámetros y reconocer el estado de los actuadores.

Las alarmas complementan el control automático al advertir condiciones anormales. Restrepo Pérez et al. incluyeron una alarma luminosa de puerta abierta y una señal sonora cuando la apertura se prolongaba. Cuervo et al., por su parte, incorporaron un sistema externo de alarma de temperatura independiente del controlador principal. Esta separación permite mantener una vía de advertencia adicional ante posibles fallas de la electrónica de control.

##
***Fuente de alimentación***

La fuente de alimentación suministra la energía requerida por los sensores, los circuitos de control y los actuadores. La arquitectura de alimentación puede variar entre diseños. Cuervo et al. utilizaron una fuente de 12 V para alimentar su sistema. Por ello, las características de la fuente deben corresponder a los requerimientos de los componentes seleccionados, en lugar de asumir que todas las incubadoras emplean las mismas tensiones de funcionamiento.

# Parte B 

Para la parte B del laboratorio se utilizaron diferentes componentes  para la medición de peso y temperatura. En la medición de peso se empleó una galga extensiométrica conectada a una pantalla LCD, la cual permitió visualizar los valores obtenidos. Por otra parte, para la medición y control de temperatura se utilizaron un termistor, un LED verde como indicador visual, un bombillo de 120 W como fuente de calor y un ventilador de 12 V para la distribución del aire caliente. Para la implementación de la medición de peso mediante la galga extensiométrica y la visualización de los datos en la pantalla LCD, se desarrolló el siguiente código en Arduino:

```Matlab 
#include <LiquidCrystal.h>

// RS (12), E (11), D4 (5), D5 (4), D6 (3), D7 (2)
LiquidCrystal lcd(12, 11, 5, 4, 3, 2);

const int pinSensor = A0;

// 1. Reposo (Sin peso)
int adcMin = 20;          
float pesoMin = 0.0;

// 2. Punto Intermedio 
int adcMedio = 250;       
float pesoMedio = 200.0;  

// 3. Punto Máximo 
int adcMax = 800;         
float pesoMax = 2000.0;
```

En la primera parte del código se establecieron dos puntos de calibración: un punto de referencia con un valor de 200 y un punto final de 1800. Estos valores se utilizaron para ajustar la sensibilidad y mejorar la linealidad de la respuesta de la galga extensiométrica, ya que este tipo de sensores suelen ser más sensibles. Posteriormente, se definieron las variables pesoFiltrado y pesoAnterior. La variable pesoFiltrado almacena el valor procesado de la medición, mientras que pesoAnterior conserva el último valor registrado para evitar actualizaciones innecesarias en la pantalla LCD. Finalmente, se implementó el parámetro alpha = 0,05, correspondiente a un filtro de promedio móvil exponencial, cuyo objetivo es atenuar el ruido presente en las lecturas analógicas y obtener una medición más estable y confiable.

```Matlab 
float pesoFiltrado = 0.0;
float pesoAnterior = -1.0;
float alpha = 0.05;
void setup() {
  lcd.begin(16, 2);
  lcd.clear();
  lcd.setCursor(0, 0);
  lcd.print("PESO NEONATO:");
}
long suma = 0;
for (int i = 0; i < 40; i++) {
  suma += analogRead(pinSensor);
  delay(2);
}
int adcMedido = suma / 40;
adcMedido = constrain(adcMedido, adcMin, adcMax);
```

En la segunda parte del código se configuran los pines de conexión de la pantalla LCD. Posteriormente, se realiza la adquisición de datos mediante la toma de 40 muestras consecutivas, separadas por intervalos de 2 ms. A partir de estas muestras se calcula un valor promedio, lo que contribuye a reducir el ruido presente en la señal. Adicionalmente, se implementa la función constrain(...), la cual limita los valores obtenidos a un rango previamente establecido, evitando lecturas fuera de los límites definidos.

```Matlab 
float pesoInstantaneo = 0.0;

if (adcMedido <= adcMedio) {
  pesoInstantaneo = map(adcMedido, adcMin, adcMedio, pesoMin, pesoMedio);
} else {
  pesoInstantaneo = map(adcMedido, adcMedio, adcMax, pesoMedio, pesoMax);
}
pesoFiltrado = (alpha * pesoInstantaneo) + ((1.0 - alpha) * pesoFiltrado);

int pesoEntero = round(pesoFiltrado);
pesoEntero = (pesoEntero / 5) * 5; // Pasos de 5 gramos

if (pesoEntero < 10) {
  pesoEntero = 0;
}
if (abs(pesoEntero - pesoAnterior) >= 5 || (pesoEntero == 0 && pesoAnterior != 0)) {
  lcd.setCursor(0, 1);
  lcd.print(pesoEntero);
  lcd.print(" g        ");
  pesoAnterior = pesoEntero;
}

delay(100);
```

s


## Referencias

[1] L. Restrepo Pérez, N. Durango Londoño, N. Gómez Suárez, F. González Ramírez y N. Rivera Bonilla, “Prototipo de incubadora neonatal,” Revista Ingeniería Biomédica, vol. 1, no. 1, pp. 55–59, mayo 2007.

[2] Drägerwerk AG & Co. KGaA, Isolette® 8000 plus: Neonatal Closed Care, ficha técnica, doc. 91 04 806, rev. 18.10-2, 2018.

[3] K. Tran et al., “Designing a low-cost multifunctional infant incubator,” Journal of Laboratory Automation, vol. 19, no. 3, pp. 332–337, jun. 2014, doi: 10.1177/2211068214530391.

[4] Cuervo, M. A. Rodríguez-Lázaro, R. Farré, D. Gozal, G. Solana, and J. Otero, “Low-cost and open-source neonatal incubator operated by an Arduino microcontroller,” HardwareX, vol. 15, Art. no. e00457, Sep. 2023, doi: 10.1016/j.ohx.2023.e00457.


