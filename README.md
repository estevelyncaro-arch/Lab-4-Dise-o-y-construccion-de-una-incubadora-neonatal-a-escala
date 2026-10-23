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

## Referencias

[1] L. Restrepo Pérez, N. Durango Londoño, N. Gómez Suárez, F. González Ramírez y N. Rivera Bonilla, “Prototipo de incubadora neonatal,” Revista Ingeniería Biomédica, vol. 1, no. 1, pp. 55–59, mayo 2007.

[2] Drägerwerk AG & Co. KGaA, Isolette® 8000 plus: Neonatal Closed Care, ficha técnica, doc. 91 04 806, rev. 18.10-2, 2018.

[3] K. Tran et al., “Designing a low-cost multifunctional infant incubator,” Journal of Laboratory Automation, vol. 19, no. 3, pp. 332–337, jun. 2014, doi: 10.1177/2211068214530391.

[4] Cuervo, M. A. Rodríguez-Lázaro, R. Farré, D. Gozal, G. Solana, and J. Otero, “Low-cost and open-source neonatal incubator operated by an Arduino microcontroller,” HardwareX, vol. 15, Art. no. e00457, Sep. 2023, doi: 10.1016/j.ohx.2023.e00457.


