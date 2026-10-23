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

Para la parte B del laboratorio se utilizaron diferentes componentes  para la medición de peso y temperatura. En la medición de peso se empleó una galga extensiométrica conectada a una pantalla LCD, la cual permitió visualizar los valores obtenidos. Por otra parte, para la medición y control de temperatura se utilizaron un termistor, un LED verde como indicador visual, un bombillo de 120 V y 100 W como fuente de calor y un ventilador de 12 V para la distribución del aire caliente.

##
Para comenzar la cubierta se realizó con ayuda de una caja de plástico transparente con el fin de tener visibilidad hacia el interior,la cual tiene las siguientes mediciones:
- 51 cm de largo
- 31 cm de alto 
- 33 cm de profundidad
  
A esta se le realizaron dos orificios circulares con sus respectivas compuertas con el fin de tener acceso al neonato sin tener pérdida de temperatura.

<img width="2000" alt="image" src="https://github.com/user-attachments/assets/3d00cfc4-c7f9-48ff-82db-6b02b8a09a02" />

En la base se reliza un orificio donde se ubica un sensor resistivo de fuerza FSR-402 el cual se implementó para tomar la medición del peso. Sobre el sensor se ubican dos borradores junto con una base de carton piedra con el fin de tener una mejor captura de la medición. 

<img width="1000" height="642" alt="image" src="https://github.com/user-attachments/assets/7d41523e-44fc-406a-866f-43ba05378002" /> <img width="1000"  alt="image" src="https://github.com/user-attachments/assets/abdced0c-5c2c-43bc-a250-4fda9c9bb138" /> <img width="1000"  alt="image" src="https://github.com/user-attachments/assets/dc3f7e95-3cf4-4319-8e62-035785a11fe5" />

Para la captura de la medición del peso se realiza mediante Arduino capturando la señal obtenida del sensor FSR-402 y mostrando el valor del peso en una pantalla LCD como se muestra a continuación:

<img width="1000" alt="image" src="https://github.com/user-attachments/assets/e93795d8-20a7-43fc-9e93-322ddd1e9460" />

Adicionalmente se agrega una sección en la parte derecha de la incubadora, donde se encuentra el elemento calefactor (bombillo 120 V y 100 W) el cual se conecta directamente a la corriente electrica mediante una extensión, este queda frente a un ventilador el cual va incrustado en la incubadora con el fin de distribuir el calor a través de toda la superficie. En esta sección se encuentra tambien un circuito el cual se compone de un termistor (sensor de temperatura) conectado con una resistencia de 1 KΩ al puerto positivo de la fuente (10 V), a la union de esa resistencia con el termistor se conecta otra resistencia de 1 kΩ a la base del transistor 2N2222 el cual va a funcionar como un interruptor activando un led verde ante la presencia de calor tomada por el termistor, el colector del transistor va a tierra (GND) y el emisor va conectado al catodo del led verde, y el ánodo del led va conectado a la fuente mediante una resistencia de 220 Ω. 

<img width="1000" alt="image" src="https://github.com/user-attachments/assets/04b90ad6-df0f-436f-abb3-f88bfe16ee7b" />  <img height="1000" alt="WhatsApp Image 2026-10-22 at 9 38 28 PM" src="https://github.com/user-attachments/assets/71bdeb08-c0e7-4405-8e8f-55da624040b4" /> <img width="1280" height="591" alt="image" src="https://github.com/user-attachments/assets/9048b38f-72ee-40ab-a3b1-a9bac0f6ecc7" />


##
Para la implementación de la medición de peso mediante la galga extensiométrica y la visualización de los datos en la pantalla LCD, se desarrolló el siguiente código en Arduino:

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

Finalmente, en la tercera parte del código se implemento un filtro exponencial que integra el 5 % de la nueva lectura con el 95 % de la lectura acumulada anterior, permitiendo suavizar la señal y reducir fluctuaciones bruscas en los valores medidos. Posteriormente, se establece una escala de 5 g mediante la operación (pesoEntero / 5) * 5, la cual aproxima el valor obtenido al múltiplo de 5 gramos más cercano, facilitando una visualización más estable. Finalmente, la instrucción delay(100) establece el ritmo de ejecución del ciclo principal, permitiendo procesar aproximadamente cinco lecturas por segundo y manteniendo un funcionamiento estable del sistema.

##
Para terminar se realiza la prueba de funcionamiento durante el laboratorio, donde se toma como ejemplo de neonato un peso de 1.8 Kg, al encender la incubadora se enciende el bombillo y el led verde que indica la presencia de temperatura, también se detecta que el ventilador transfiere el aire cálido hacia el interior de la incubadora, sin embargo este no se distribuye unifomemente por lo que se recomienda implementar un ventilador más grande para una mejor distribución del calor. Adicionalmente se toma el valor del peso, y se obtiene un valor con un 0% de error, observando en la pantalla LCD un valor de 1800 g correspondientes al peso. 

<img width="1000"  alt="image" src="https://github.com/user-attachments/assets/baed3feb-aa47-4978-9296-8a5ead5401f0" />

https://github.com/user-attachments/assets/1f669421-77f0-4bf6-af75-89301efd0e51

## Costo Estimado
Para desarrollo del prototipo funcional para la adquisición de peso y temperatura se realizó utilizando componentes de bajo costo.

| Componente | Cantidad | Función en el Proyecto | Costo Aprox. (COP) | 
| :--- | :---: | :--- | :---: |
| **Arduino Uno R3** | 1 | Procesamiento de señal y control del sistema | $36,000 |
| **Pantalla LCD 16x2** | 1 | Interfaz de usuario para visualización del peso | $29,000 |
| **Sensor de Presión FSR (2 hilos)** | 1 | Medición piezoresistiva de carga | $28,000 | 
| **Potenciómetro $10\,\text{k}\Omega$** | 1 | Ajuste de contraste para el LCD | $1,200 | 
| **Resistencia $10\,\text{k}\Omega$ ($1/4\,\text{W}$)** | 1 | Divisor de tensión para acondicionamiento del FSR | $200 | 
| **Protoboard (830 puntos)** | 2 | Base para montaje y pruebas del circuito | $24,000 | 
| **Cables Jumper (M-M / M-H)** | 1 Kit | Interconexión de señales y alimentación | $8,000 | 
| **Cable USB A-B** | 1 | Alimentación y comunicación serial | $6,000 | 
| **Base / Estructura de Plastico** | 1 | Soporte mecánico para desacople de fuerza | $43,000 | 
| **Ventilador de 12V** | 1 | Distribución del aire | $7,000 | 
| **Bombillo 12V 100W con roseta** | 1 | Parte de calefacción  | $6,000 | 
| **Termistor** | 1 | Medir la temperatura  | $700 | 
| **TOTAL** | | | **$189,100 COP** |

A continuación se realiza una comparación de costos con diferentes proveedores y páginas obteniendo la siguente comparación:

## Comparativa de Costos de Mercado vs. Desarrollo Propio

| Modelo / Opción | Proveedor / Plataforma | País | Estado | Precio Original | Precio Estimado (COP) | Factor de Costo vs. Prototipo |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Desarrollo Propio** | Prototipo Local | Colombia 🇨🇴 | Nuevo (BOM) | **$189.100 COP** | **$189.100 COP** | **1x (Base)** |
| **Draeger Isolette 8000** | Ultra Medical Equipment | Reino Unido 🇬🇧 | Usado | £1.000 GBP | ~$5.300.000 COP | ~28x |
| **Draeger Isolette 8000** | Hessen Medical Ltd. | Reino Unido 🇬🇧 | Usado / Reacondicionado | $1.571 USD | ~$6.500.000 COP | ~34.4x |
| **Draeger Isolette 8000** | Precio Promedio (Bimedis) | Europa 🇪🇺 | Usado / Reacondicionado | $1.764 USD | ~$7.300.000 COP | ~38.6x |
| **Draeger Isolette 8000** | Mediproma B.V. | Países Bajos 🇳🇱 | Usado / Reacondicionado | $1.795 USD | ~$7.400.000 COP | ~39.1x |
| **Draeger Isolette 8000** | CENTRE D'AFFAIRES MEDICAL | Francia 🇫🇷 | Usado / Reacondicionado | $1.941 USD | ~$8.000.000 COP | ~42.3x |

Los precios de referencia corresponden a equipos usados/reacondicionados de segunda mano comercializados en Europa. No incluyen gastos de importación, fletes internacionales ni nacionalización (aranceles/IVA) a Colombia, los cuales incrementarían sensiblemente su costo final.
##

El prototipo desarrollado demuestra una solución altamente económica para la adquisición y monitoreo de peso a escala académica. Sin embargo, para su implementación en un entorno clínico real, se debe considerar el incremento en el presupuesto asociado al uso de sensores de grado médico certificados fuentes de alimentación ininterrumpida (UPS), aislamiento eléctrico (norma IEC 60601-1) y la fabricación de la cúpula de acrílico grado médico con control térmico.

# Preguntas

* Pregunta 1: ¿Qué otras variables (y por qué) además de las aquí mencionadas son críticas en el monitoreo neonatal?

a) Humedad Relativa del Aire (HRA): Su control evita la pérdida excesiva de agua a través de la piel del prematuro, reduciendo el riesgo de deshidratación y alteraciones hidroelectrolíticas.

b) Saturación de Oxígeno (SpO₂) y Frecuencia Cardíaca: Permiten detectar episodios de apnea y garantizar una adecuada oxigenación, previniendo tanto la hipoxia como las complicaciones asociadas al exceso de oxígeno.

c) Concentración de Oxígeno Ambiental (FiO₂): Debe mantenerse dentro de rangos controlados para asegurar una correcta oxigenación del neonato y evitar efectos adversos.

d) Nivel de Ruido Ambiental (dB): Un ambiente con bajo nivel de ruido disminuye el estrés fisiológico y favorece el desarrollo adecuado del sistema nervioso del prematuro.


* Pregunta 2: ¿Qué haría falta para convertir el sistema desarrollado en una incubadora neonatal real?

a) Redundancia y seguridad física: Se recomienda incorporar un termostato independiente que desconecte los calentadores si la temperatura supera los 38 °C, así como una batería de respaldo para garantizar el funcionamiento ante fallos eléctricos.

b) Cumplimiento de normativas médicas: El sistema debe cumplir con la norma IEC 60601-2-19, específica para incubadoras neonatales, e incluir aislamiento eléctrico de grado BF o CF para minimizar el riesgo de corrientes de fuga. Además, la estructura puede incorporar doble pared para mejorar el aislamiento térmico.

c) Sistema de alarmas: Deben implementarse alarmas audiovisuales para fallos de temperatura, sensores o suministro eléctrico, clasificadas según los niveles de prioridad establecidos en la norma IEC 60601-1-8.


* Pregunta 3: ¿Qué semejanzas hay entre una incubadora neonatal y una servo-cuna?

A pesar de sus diferencias estructurales, la incubadora y la cuna radiante comparten características fundamentales:

a) Control servocontrolado: Ambos equipos monitorean continuamente la temperatura del neonato mediante una sonda cutánea y ajustan automáticamente el aporte de calor para mantener la temperatura programada.

b) Termorregulador: Su función principal es proporcionar un ambiente térmico neutro que reduzca el gasto metabólico y el consumo de oxígeno del recién nacido.

c) Sistemas de seguridad: Incorporan alarmas para fallos de energía, desviaciones de temperatura, errores en la sonda de medición y condiciones de sobrecalentamiento.

d) Monitoreo y soporte clínico: Permiten la integración de accesorios como balanzas, portavenoclisis, monitores multiparámetro y sistemas de radiografía, facilitando el seguimiento integral del paciente.

# Conclusiones 

En este trabajo se analizaron los parámetros y sistemas necesarios para el adecuado funcionamiento de una incubadora neonatal, con el objetivo de garantizar condiciones seguras para el cuidado de recién nacidos. A partir del estudio realizado, se determinó que variables como la temperatura, la humedad relativa, la concentración de oxígeno y los sistemas de monitoreo son esenciales para mantener un ambiente controlado que favorezca la estabilidad fisiológica del neonato. Asimismo, se evidenció la necesidad de incorporar mecanismos de seguridad, alarmas y el cumplimiento de normativas como la IEC 60601 para reducir riesgos durante la operación del equipo. La integración de estos elementos permite mejorar las condiciones de atención y contribuir a la disminución de complicaciones asociadas a la prematuridad. Como siguiente paso, se recomienda desarrollar e implementar un prototipo funcional que permita validar experimentalmente el desempeño del sistema y evaluar su capacidad de respuesta ante diferentes condiciones de operación.

## Referencias

[1] L. Restrepo Pérez, N. Durango Londoño, N. Gómez Suárez, F. González Ramírez y N. Rivera Bonilla, “Prototipo de incubadora neonatal,” Revista Ingeniería Biomédica, vol. 1, no. 1, pp. 55–59, mayo 2007.

[2] Drägerwerk AG & Co. KGaA, Isolette® 8000 plus: Neonatal Closed Care, ficha técnica, doc. 91 04 806, rev. 18.10-2, 2018.

[3] K. Tran et al., “Designing a low-cost multifunctional infant incubator,” Journal of Laboratory Automation, vol. 19, no. 3, pp. 332–337, jun. 2014, doi: 10.1177/2211068214530391.

[4] Cuervo, M. A. Rodríguez-Lázaro, R. Farré, D. Gozal, G. Solana, and J. Otero, “Low-cost and open-source neonatal incubator operated by an Arduino microcontroller,” HardwareX, vol. 15, Art. no. e00457, Sep. 2023, doi: 10.1016/j.ohx.2023.e00457.


