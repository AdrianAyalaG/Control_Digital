# Introducción a Control Digital

El control digital a menudo se percibe como diferente del control analógico, que inicialmente se investiga en el campo del control. Pero en realidad es la transferencia del sistema de control analógico completo a una unidad digital lo que da origen al control digital.

## Temas de curso
El semestre cubrirá una variedad de temas, que incluyen:
* Conversión A/D y D/A.
* Ecuaciones en diferencias.
* Transformada Z.
* Función de Transferencia.
* Estabilidad
  >🔑 Enfoque: Se enfatiza en el Test de Jury. 
* Discretización de controladores.
* Métodos algebraicos.
* Respuesta en frecuencia.
* Espacio Estados.
  >🔑 Enfoque:  Retroalimentación de estados y Observadores.

## Evaluación de la materia
En este apartado se detallan los porcentajes asignados a cada actividad a realizar a lo largo del semestre.
* Corte 1:
  > 🔑 Actividades evaluativas: Este corte tiene un peso total del 20%, y se divide en 2 componentes: Un parcial, que representa el 15%, y apuentes, que representan el 5%.
* Corte 2:
  > 🔑 Actividades evaluativas: El corte tiene un peso total del 30% y se divide en 3 componentes: Un parcial, que representa el 10%; laboratorios, que representan el 15%; y apuntes, que representan el 5%.
* Corte 3:
  > 🔑 Actividades evaluativas: El corte tiene un peso total del 50% y se divide en 3 componentes: Un parcial, que representa el 20%; Proyecto, que representan el 25%; y apuntes, que representan el 5%.

## Apuntes
El tomar notas durante las clases será fundamental para repasar y prepararse adecuadamente para los exámenes parciales a lo largo del curso. Las notas deben cumplir con los siguientes requisitos:
* Cumplimiento de la plantilla (Proporcionada por el docente)
* Presentar la información de manera completa y detallada
* Debe ser escrito por el grupo de estudiantes.
* Incluir dos ejemplos de los temas presentados (En los temas que lo permitan).


## Informes
En este apartado se evalua la construcción de los informes de laboratorios, teniendo en cuenta el orden, redacción, cohesión y coherencia del documento entregado por el grupo tras la realización de la práctica de laboatorio. Los items minimos con los que debe contar el informe son:
* Introducción.
  > 🔑 Enfoque: El informe debe contener al menos un párrafo que abarque todos los temas tratados en la práctica de laboratorio.
* Materiales y métodos.
  >🔑 Enfoque: Se agregan todos los cálculos, simulación y demás información.
* Analisis y Resultados.
  > 🔑Enfoque: Consiste en adjuntar los resultados obtenidos durante la práctica de laboratorio con su respectivo análisis. El cual debe ser coherente y acrode con los objetivos de la práctica.
* Concluciones:
  > 🔑 Enfoque: No es necesario extenderse en este apartado, pero si es fundamental que sea coherente y esté bien sustentada. Debe basarse en los resultados obtenidos en la práctica y conluir de manera clara, de esta forma evitando ambigüedades.

## Bibliografía
El docente suministra material de estudio que explica de forma clara cada uno de los temas de interés dentro del curso de Control Digitla. Este material bibliográfico está compuesto por:
* Sistemas Control Digital, de A Visioli.
* Control Digital, de Digitalia.
* Control Digital, Ogatac
  >🔑 Este apoyo bibliográfico se enfoca más a la parte matemática.

01/08/2024
# Señales Analógicas y Digitales y convertidores ADC y DAC 
En el campo de la electrónica, la adquisición y generación de señales es fundamental para comprender y analizar el comportamiento de variables que percibimos tanto de manera tangible como a través de nuestros sentidos. Estas señales se dividen en las señales naturales que no siempre son generadas por el ser humano y representan medidas de variables físicas, como la temperatura, la humedad o la presión. Por otro lado, las señales digitales son creadas por el ser humano y toman valores lógicos, como "1" o "0". Ambas categorías de señales son cruciales tanto para la electrónica como para la vida cotidiana.
Para conectar el mundo analógico con el digital, se han desarrollado convertidores ADC (Analog-to-Digital Converter) y DAC (Digital-to-Analog Converter). Estos dispositivos actúan como un puente, transformando señales físicas en datos digitales que pueden ser utilizados por sistemas electrónicos mucho más modernos.

## 1. Señales Analógicas y Digitales
### 1.1 Señales Análogicas: 
>🔑 Definición: Señal continua que puede tomar cualquier valor en el dominio del tiempo.
>🔑 Características: Es muy limitado, pero es más exacto que el digital.
### 1.2 Señales Digitales:
>🔑 Definición: Solo tiene 2 posibles valores o estados. Este tipo de señales tiene forma de onda cuadrada.

Características:
*La exactitud 📉 
* Errores de implementaciöm. 📈
* Flexibilidad (Solo necesita cambio de software).
* Velocidad (Tiempo real. más baja que la análoga). 📉 
* Costos (Más barata).

![Figura de prueba](images/plantilla/Captura2.PNG)

Figura 1. Estructura para control digital.

## 2. Conversión Análoga a Digital
### 2.1 Procedimiento
#### 2.1.1 Muestreo: Medir valores de voltaje cada cierto tiempo (Poner rango en el tiempo)
* Se mide como el número de veces que se mide en 1 seg por lo tanto la unidad está dada en Hz.
* Entre más alta la tasa de muestreo, más información se está procesando.
* El muestreo puede ser periódico (único), de tasa múltiple o aleatorio.
  
  ![Figura de prueba](images/plantilla/Captura2.PNG)

Figura 2. 

#### 2.1.2 Cuantización: Se convierte en una serie de valores que corresponden a cada una de las medidas tomadas en el muestreo 
* Los conversores vienen con una información que indica si tiene error de cuantización.
  
![Figura de prueba](images/plantilla/Captura2.PNG)

Figura 3. 

#### 2.1.3 Codificación: Se asignan valores de tipo binario a cada uno de los valores del paso anterior (cuantización).
* Es importante la cantidad de bits que usará el código, es decir, los que se le van a configurar desde el inicio. Esto con el fin de que no haya desperdicio de memoria si se usan más bits de los necesarios.
* Tienen limitaciones de voltaje.

![Figura de prueba](images/plantilla/Captura2.PNG)

Figura 4. 

## 2.2 Consideraciones Prácticas
>🔑 Importante: En algunas señales hay que tener en cuenta los tiempos de retraso entre el muestreo y la cuantización del valor.

![Figura de prueba](images/plantilla/Captura2.PNG)

Figura 5. 

## 2.3 Tiempos de muestreador y retenedor
![Figura de prueba](images/plantilla/Captura2.PNG)

Figura 6. 

* Ta: Es el tiempo de adquisición, es decir, el tiempo que pasa desde que se inicia el muestreo hasta que se retiene dentro de cierto margen de tolerancia.
* Tp: Es el tiempo de apertura, lo que quiere decir que es el tiempo que pasa desde la retención hasta que se abre el muestreador.
* Ts: El movimiento constante del interruptor crea capacitancia parásita, un fenómeno que produce un estado transitorio en la señal de salida, por lo que Ts que significa tiempo de establecimiento es el tiempo que necesita la señal para que las oscilaciones desaparezcan.

## 💡'Ejemplo 1:'
### Se tienen los siguientes datos: 
* Señal analógica: [0.3]V
* Bits de representación: 2 bits
* $$2^{2}$$ = 4 posibles símbolos
* Rango analógico: 3-0=3V
* Representación: 3/4 = 0.75V
  
|  Voltaje  |  Binario  |
|---------------|---------------|
|       0       |      00       |
|     0.75      |      01       |
|      1.5      |      10       |
|      2.25     |      11       |

Tabla 1. Valores que se están cuantizando.

* Son $$2^{r}-1$$ posibles símbolos porque se toma el 0.
💡'Ejemplo 2:'
### Para Arduino: 
* Señal analógica: [0.5]V
* Bits de representación: 10 bits
* $$2^{10}$$ = 1024 posibles símbolos
* Rango analógico: 5-0=5V
* Representación: 5/1024 = 4.88mV

## 3. Conversión Digital a Análogo
>🔑 ¿Qué es?: Dispositivo que genera una correspondencia uno a uno entre valores digitales y valores análogicos.
* La resolución depende de los bits de representación al igual que en los ADC. Para rango completo hay  $$2^{n}$$ valores analógicos que incluyen el 0
* FS (Fondo de escala): Máximo voltaje que se tendrá en el rango de conversión, se representa con el símbolo de %

| Bits entrada | Resolución (V) |Resolución(%FS)|
|------------------|--------------------|-------------------|
|        4         |         1          |      6.6          |
|        8         |       0.059        |      0.4          |
|       16         |      229x10^-6     |     0.0015        |
|       32         |      3.5x10^-9     |  0.00000000023    |

Tabla 2. Explicación del fondo de escala.

*Los bits a valor digital se multiplican por su potencia de 2. 
### 3.1 Métodos de conversión
#### 3.1.1 Resistencias Ponderadas: Está compuesto por una serie de resistencias ponderadas al peso binario de cada bit y en serie con un interruptor conectado al bit de dicho peso. $$S_{0}$$ a $$S_{N-1}$$ conectan cada resistencia a 2 posibles tensiones. 1. Son iguales, pero signo contrario: Saldrá una tensión simétrica. 2. Si una es positiva y la otra está conecta a tierra permitirá únicamente rangos positivos de señal de salida. 

![Figura de prueba](images/plantilla/Captura2.PNG)

Figura 7. 

MSB= BIT más significativo.
LSB= BIT menos significativo. 
Rf= Permite fijar la tensión del fondo de escala.

* Cuando un bit es 0 no aportan corriente a la total Is mientras que los "1" aportan diferentes corrientes dependiendo del peso.
* Se analiza entonces la siguiente ecuación para obtener el valor de Vout:

$$V_{0}=-I_{f}R_{f}= \frac{Vref*R_{f}}{R}(a_{N-1}+a_{N-2}\frac{1}{2}+...+a_{0}\frac{1}{2^{N-1}})$$
  
*Donde $$a_{}$$ son bits de entrada.
*La anterior ecuación se puede resumir en :

$$V_{0}=\frac{-n*Vref}{2^{N-1}}$$

*Donde N son el número de bits que se están trabajando y n es el valor digital.

# 📚'Ejercicios'
## 1. $$N=8$$
$$Vref=-1V$$

Entonces se tiene que con: 
* $$n=128$$

 $$V_{0}= \frac{-128*-1}{2^{8-1}}= 1V$$
  
* $$n=0$$
  
$$V_{0}= \frac{-0*-1}{2^{8-1}}= 0V$$

* Los demás valores están dentro del rango de 0V a 1V.
>🔑 Desventaja: Es difícil tener "n" resistencia que sigan una progresión geométrica y una precisión buena.

#### 3.1.2 Red en escalera R-2R (Complicado de configurar pero es más exacto)

![Figura de prueba](images/plantilla/Captura2.PNG)

Figura 8. 

*Nunca se tiene Vout=Vcc aunque se hagan muchas sumas parciales 
>🔑 Desventaja: Hay relación de resistencias que afectan la tolerancia de las mismas. Además de ello a veces hay que poner FILTROS para no observar saltos de tensión (escalones), pero limita la Freq máxima que se puede obtener.
# 📚'Ejercicios'
2. 

## 4. Modelo matemático conversores A/D y D/A
* Utilizan mismos componentes. Muestreador y retenedor.
* El muestreador se analiza idealmente con una señal de reloj e interruptor.
* El retenedor se puede modelar con un sistema que contenga una función de transferencia.
  
## 5. Consideraciones 
*Asumiendo que el conversor DAC sea:
1. Las entradas y las salidas del conversor tienen igual magnitud.
2. La conversión se realiza de forma instantanea.
3. Las salidas son constantes sobre el periodo de muestreo.
   Se obtiene entonces:
### 5.1 Zero Order Hold (ZOH)
![Figura de prueba](images/plantilla/Captura2.PNG)

Figura 9.

* Subir la retención, implica un incremento en el costo del conversor.
### 5.2 First Order Hold (FOH)
>🔑 Ventaja: Toma más valores, es decir, puede tener un análisis de más información ya que tiene un modelo lineal.
### 5.3 Second Order Hold (SOH)
>🔑 Ventaja: Modelo parabólico durante intervalo de muestreo.

## 6. Conclusiones
El objetivo fundamental de un conversor es servir como un puente entre el mundo digital y el analógico. Esta responsabilidad implica que los procesos de conversión sean precisos para evitar la pérdida de información crucial. No obstante, es esencial encontrar un equilibrio, ya que cada componente del sistema influye en el resultado final. Por ejemplo, un mayor número de bits permite representar más información, pero también aumenta la complejidad del diseño del circuito y su interpretación. Asimismo, una alta resolución eleva la complejidad tanto del diseño del circuito como de su comprensión. Con esto en cuenta ya el manejo de estos conversores será algo útil por si se desea trabajar en sistemas de manejo de señales como audio o video o simplemente en el control industrial. 
  
##  Referencias
[1]“AulasVirtualesECCI: Entrar al sitio,” Edu.co. [Online]. Available: https://aulas.ecci.edu.co/course/view.php?id=9304. [Accessed: 10-Aug-2024].
[2] FabioLeon, “¿Qué son señales analógicas y digitales en electrónica?,” DynamoElectronics, 13-Jul-2022. [Online]. Available: https://www.dynamoelectronics.com/que-son-senales-analogicas-y-digitales-en-electronica/. [Accessed: 09-Aug-2024].
[3] “DAC Con Resistencias Ponderadas,” Scribd. [Online]. Available: https://es.scribd.com/document/343360980/DAC-Con-Resistencias-Ponderadas. [Accessed: 10-Aug-2024].
[4] V. T. las E. De msavalos, “¿Cómo funciona un Conversor Digital-Analógico (DAC) R2R?,” Electrónica + Programación + GNU/Linux, 19-Jan-2021. [Online]. Available: https://electronlinux.wordpress.com/2021/01/19/como-funciona-un-conversor-digital-analogico-dac-r2r/. [Accessed: 10-Aug-2024].


22/08/2024
# ESTABILIDAD EN SISTEMAS DISCRETOS 
La estabilidad es un concepto clave en el análisis de sistemas de control de movimiento que evolucionan en intervalos discretos de tiempo, ya que un sistema discreto se considera estable si su respuesta a una entrada se mantiene acotada conforme avanza el tiempo. En este contexto, el análisis en el espacio de Laplace mantiene el mismo concepto de estabilidad, aunque la representación de la frontera de estabilidad cambia: En lugar de estar representada por el eje vertical, se representa mediante un círculo en el plano z. Para evaluar la estabilidad de estos sistemas discretos, se utilizan diferentes enfoques, como la estabilidad asintótica, la estabilidad BIBO (Bounded Input-Bounded Output) y el criterio de estabilidad de Jury.
## Estabilidad absoluta
>🔑 Definición: Se se aplica un patrón en la entrada y la respuesta (salida) tiene las mismas características, entonces es ESTABLE.

![Figura de prueba](ESTABILIDADLP.PNG)

Figura 10. Estabilidad en LaPlace. 

* Con la anterior imagen se tiene la siguiente equivalencia en el plano Z: $$z=e^{Ts}$$
  Expresando: $$s= \sigma+jw$$
* Tres situaciones:
  1. Para $$\sigma>0 \to \lim_{\sigma \to 0} e^{\sigma T} = 1$$
     $$\lim_{\sigma \to \infty } e^{\sigma T} = \infty $$
     *El sistema es INESTABLE
  2. Para $$\sigma = 0 \to e^{\sigma T} = 1$$
     *El sistema es marginalmente estable
  3. Para $$\sigma < 0 \to \lim_{\sigma \to 0} = e^{-\sigma T}=1$$ y 
     $$\lim_{\sigma \to \infty } = e^{-\sigma T}= 0$$
     *El sistema es ESTABLE
     
![Figura de prueba](ESTABILIDADLP.PNG)

Figura 11. Estabilidad en el plano Z.

* Alejarse del origen, se vuelve más lento.
* El polo dominante es aquel que está más cerca del radio 1 en el plano z.
  
## 💡'Ejemplo 1:'
1. $$G(z)=\frac{4}{z^{3}-7.8z^{2}+13.4z+3}$$
Se iguala a 0 el denominador y se obtienen los tres polos:
$$z=5, z=3, z=0.2$$
Hay un polo dentro del radio de estabiidad, los otros dos polos están por fuera. Sistema INESTABLE

## 💡'Ejemplo 2:'
$$G(z)= \frac{z-3}{z^{3}-1.5z^{2}+0.66z-0.08}$$
Los polos son: 
$$z=0.5, z=0.8, z=0.2$$
El sistema es ESTABLE porque todos los polos están dentro de circulo unitario.

## 💡'Ejemplo 3:'
$$G(z)= \frac{-0.075997z+0.0101}{z^{2}-1.5804z+0.6238}$$
Los polos son: 
$$z=0.76, z=0.81$$
El zero sería: 0.132

## 1. Estabilidad Asintótica 
Se dice que un sistema es asintóticamente estable si su respuesta frente a una variedad de condiciones iniciales decae a cero. Se presenta mediante una ecuación muy sencilla: 
$$\lim_{k \to \infty } y(k)=0$$
Con esto se puede decir que si el sistema está limitado pero no decae a 0, entonces es marginalmente estable. El resto de respuestas hará inestable al sistema.

## 2. Estabilidad BIBO(Boundary INPUT,Boundary OUTPUT)
Una respuesta acotada a una entrada acotada permanece acotada en la salida. Uno de los métodos más comunes para evaluar este tipo de estabilidad es el Test de Jury, que utiliza criterios específicos que un sistema debe cumplir para garantizar su estabilidad.
### 2.1 Test de Jury 
Sabiendo que el polinomio caracteristico de una función de transferencia en el plano z, es el siguiente: 
$$D(z)= a_{0}z^{n}+a_{1}z^{n-1}+...+a_{n-1}z+a_{n}$$
#### 2.1.1 Condiciones:
1. $$a_{0}>0$$
2. $$a_{n} < a_{0}$$
3. $$P(z)|_{z=1}>0$$
4. $$P(z)|_{z=1}\to > 0 para n par$$ 
   $$\to < 0 para n impar$$ 
5. Construir arreglo de Jury. Con tres términos al final se termina de realizar el arreglo.
>🔑 Condición: Si al menos una no se cumple, el sistema es inmediatamente INESTABLE.

#### 2.1.2 Criterio de estabilidad de Jury

![Figura de prueba](ESTABILIDADLP.PNG)

Figura 12. Tabla arreglo de Jury 

Este criterio consiste en organizar los coeficientes de las potencias de  z en orden ascendente de acuerdo con sus exponentes. En la segunda fila, se utilizan los mismos coeficientes, pero en orden inverso. Esto permite calcular la siguiente ecuación matemática para determinar los valores requeridos: 
*Una matriz 2x2 que relaciona la primera columna de la tabla con la ultima pero con los coeficientes invetidos:
$$ b_{n-1}=|\begin{matrix}
a_{0} & a_{n-1}\\
a_{n-1} & a_{1}
\end{matrix}|$$
Lo que es igual a: 
$$a_{n}a_{1}-a_{0}a_{n-1}$$
Se resuelve cada arreglo de matrices hasta llegar a b0, donde:
$$b_{0}=|\begin{matrix}
a_{n} & a_{0}\\
a_{0} & a_{n}
\end{matrix}|$$
Lo que es igual a: 
$$a_{n}a_{n}-a_{0}a_{0}$$
Se vuelve a rellenar la cuarta fila con los mismos coeficientes pero invertidos y se repite el proceso hasta obtener tres valores al final de la tabla.

##### 2.1.2.1 Condiciones después del arreglo de Jury 
Después de obtener los tres valores al final del arreglo de Jury, se evaluan las siguientes condiciones:
1. $$\left| b_{0} \right| = \left| b_{n-1} \right|$$
2. $$\left| c_{0} \right| = \left| c_{n-2} \right|$$
3. $$\left| s_{0} \right| = \left| s_{3} \right|$$
4. Y en el caso de la Img.12, el ultimo valor a evaluar será $$\left| r_{0} \right| = \left| r_{2} \right|$$
>🔑 Condición: Si al menos una no se cumple, el sistema es inmediatamente INESTABLE.

## 💡'Ejemplo 1:'
Una vez comprendidos los criterios de estabilidad de Jury, se presenta el siguiente ejemplo:
* Polinomio característico:
$$z^{4} - 1.2z^{3} + 0.07z^{2} + 0.3z - 0.08 = 0$$

* Evaluación de condiciones: 
1. $$a_{0} > 0 $$, en este caso: $$1 > 0$$
2. $$|a_{n}| < a_{0}$$, en este caso: $$0.08 < 1$$
3. $$P(z)|_{z=1}$$, en este caso: $$(1)^{4} - 1.2*(1)^{3} + 0.07*(1)^{2} + 0.3*(1) - 0.08 = 0.09 > 0$$
4. $$P(z)|_{z=-1}$$, en este caso: $$(-1)^{4} - 1.2*(-1)^{3} + 0.07*(-1)^{2} + 0.3*(-1) - 0.08 = 1.89 > 0$$

* Cumplimiento de las condiciones, se construye el arreglo de Jury:
  
$$z^{4} - 1.2z^{3} + 0.07z^{2} + 0.3z - 0.08 = 0$$


| $$z^{0}$$  | $$z^{1}$$ | $$z^{2}$$  | $$z^{3}$$ | $$z^{4}$$ |
| ------ | ------ | ------ | ------ | ------ |
| -0.08  | 0.3 | 0.07 | -1.2 | 1 |
| 1 | -1.2  | 0.07 | 0.3 | -0.08 |

Realiza el calculo de las determinantes:

* (-0.08)*(-1.2) - (1)*(0.3) = -0.204
* (-0.08)*(0.07) - (1)*(0.07) = -0.0756
* (-0.08)*(0.3) - (1)*(-1.2) = 1.176
* (-0.08)*(-0.08) - (1)*(1) = -0.994

| $$z^{0}$$  | $$z^{1}$$ | $$z^{2}$$  | $$z^{3}$$ | $$z^{4}$$ |
| ------ | ------ | ------ | ------ | ------ |
| -0.08  | 0.3 | 0.07 | -1.2 | 1 |
| 1 | -1.2  | 0.07 | 0.3 | -0.08 |
| ------ | ------ | ------ | ------ | ------ |
| -0.994 | 1.176 | -0.0756 | -0.204 |
| -0.204 | -0.0756  | 1.176 | -0.994 |


* (-0.994)*(-0.0756) - (-0.204)*(1.176) = 0.315
* (-0.994)*(1.176) - (-0.204)*(-0.0756) = -1.184
* (-0.994)*(-0.994) - (0.204)*(0.204) = 0.946

| $$z^{0}$$  | $$z^{1}$$ | $$z^{2}$$  | $$z^{3}$$ | $$z^{4}$$ |
| ------ | ------ | ------ | ------ | ------ |
| -0.08  | 0.3 | 0.07 | -1.2 | 1 |
| 1 | -1.2  | 0.07 | 0.3 | -0.08 |
| ------ | ------ | ------ | ------ | ------ |
| -0.994 | 1.176 | -0.0756 | -0.204 |
| -0.204 | -0.0756  | 1.176 | -0.994 |
| ------ | ------ | ------ | ------ | ------ |
| 0.946 | -1.184  | 0.315 |

$$|-0.994| > |-0.204|$$
$$|-0.946| > |0.315|$$

Con relación a lo obtenido se determina que este sistema es estable.

## 💡'Ejemplo 2:'

$$z^{5} + 2.6z^{4} + 0.56z^{3} -2.05z^{2} + 0.0775z + 0.35 = 0$$
1. $$1 > 0$$
2. $$0.35 < 1$$
3. $$P(z)|_{z=1}$$, en este caso: $$(1)^{5} + 2.6*(1)^{4} + 0.56*(1)^{3} - 2.05*(1)^{2} + 0.0775*(1) + 0.35 = 1.41 > 0$$
4. $$P(z)|_{z=-1}$$, en este caso: $$(-1)^{5} + 2.6*(-1)^{4} + 0.56*(-1)^{3} - 2.05*(-1)^{2} + 0.0775*(-1) + 0.35 = 0.382 > 0$$

No se esta cumpliendo con el criterio de al se $$n$$ un número impar debe ser menor a 0. Por ende, el sistema es inestable



