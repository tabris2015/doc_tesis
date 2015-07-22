#SECCIÓN I: INTRODUCCIÓN.

La energía eléctrica, junto con el gas y el agua potable, son los principales recursos para la correcta operación de todas las actividades que una planta industrial; el funcionamiento de todas las máquinas, procesos o servicios en dichas plantas se basa en éstos. Tales recursos son cada vez más valiosos y se vuelve en una necesidad contar con procedimientos o soluciones que permitan su aprovechamiento óptimo, evitando derroches o malos usos de estos recursos. La energía eléctrica, en particular, se caracteriza por ser la más cara de los 3 recursos mencionados anteriormente.

Los sistemas de medición de energía evolucionaron mucho desde sus comienzos. En la actualidad, los sistemas electromecánicos y analógicos de medición se han reemplazado por medidores digitales por quedar ya obsoletos. Estos medidores digitales cuentan con muchas funcionalidades incorporadas; tal avance en la tecnología de los dispositivos ha permitido dar un enfoque diferente a la medición de consumo de energía haciendo posible realizar diferentes tipos de análisis sobre los datos, cosa que era prácticamente imposible o muy difícil de hacer en décadas pasadas, el presente proyecto, intenta integrar una solución para la medición de energía eléctrica en una planta, aprovechando así los beneficios de la tecnología para facilitar el trabajo y el ahorro de energía en la misma.

En la planta embotelladora Soft Drink El Alto de la Cervecería Boliviana Nacional, se ha podido identificar deficiencias en el registro y aprovechamiento de la información del consumo de energía eléctrica por la precariedad de los mecanismos y procedimientos utilizados actualmente, la información no es completamente confiable y se registra en intervalos de tiempo demasiado largos como para poder analizar el comportamiento detallado de la planta en cuanto a consumo de energía eléctrica se refiere.

Bajo este enfoque el presente proyecto propone una herramienta para contribuir a mejorar en alguna medida aspectos acerca de la medición y adquisición de los datos del consumo de energía eléctrica en la planta. Todo esto mediante la aplicación de conceptos de ingeniería electrónica y la implementación de recursos tecnológicos disponibles los cuales permitirán mejorar la medición, monitoreo y registro del consumo de energía eléctrica en la planta, actividades de vital importancia en el área de gestión de cualquier industria.

## Antecedentes.

Hasta hace algunas décadas, el poder contar con datos actualizados y pormenorizados del consumo de energía eléctrica no era una tarea importante en la industria por diversas razones:

  - La energía eléctrica era más barata y no se presentaban dificultades frecuentes en su disponibilidad.
  - No existía una necesidad de controlar el uso racional de la energía eléctrica, el ahorro de energía era un tema secundario.
  - Contar con un sistema eficaz de medición no representaba una inversión atractiva por la dificultad y elevado costo para la implementación del mismo.

En la actualidad, los sistemas de medición en la industria se limitan a medidores analógicos o digitales del total de energía consumida por una planta y no así disgregada por áreas o sectores de producción o servicios. En algunos casos, se cuentan con medidores en diversas áreas, pero la información no se aprovecha de la mejor manera.

Además, hoy en día, en el campo de la industria del envasado de bebidas, la medición del consumo de energía eléctrica de la planta embotelladora Soft Drinks El Alto (SD EA) de la cervecería Boliviana Nacional se basa en el siguiente procedimiento:

1. Se cuenta con un operador que visita medidor por medidor en las distintas áreas de consumo de la planta.
2. Los datos obtenidos por inspección visual se anotan en una planilla.
3. Los datos de la planilla se transcriben en computadora y se introducen a un archivo que los almacena.

La planta cuenta con distintos medidores ubicados en puntos estratégicos de consumo de la planta, estas áreas de medición se listan a continuación:

**Planta de tratamiento de agua cruda.** 
Es un sector que se encarga de tratar y purificar el agua cruda proveniente de varios pozos de reserva, el agua tratada proveniente de esta planta se utiliza en la elaboración del producto.

**EMPACAR**. 
En este sector se realiza el soplado de las pre-formas PET en moldes de distintos volúmenes que constituyen los envases (botellas) para el producto.

**Elaboración.** 
El agua tratada junto con distintos ingredientes pasa por un proceso complejo para convertirse en jarabe, la base del producto.

**Envasado.** 
Una vez que se cuenta con el jarabe, se procede a envasar el producto a través de un sistema de lavado de envases, llenado de producto y etiquetado de las botellas, este sector posee de 3 líneas paralelas de producción:

  - **línea GRB**: Envasa el producto en botellas de vidrio en varios formatos y/o volúmenes.
  - **línea 2 (PET 2)**: Envasa el producto en botellas PET de 2 litros de capacidad.
  - **línea 3 (PET 3)**: Envasa el producto en botellas PET de 3 litros de capacidad.

Cada línea cuenta con todo el proceso de envasado descrito anteriormente.

**Servicios.** 
Todos los procesos, tratamiento de aguas, soplado de botellas, elaboración y envasado requiere de servicios que soporten el funcionamiento de las maquinas, el consumo de estos servicios representa un importante porcentaje en el consumo total de la planta, se listan los servicios con los que cuenta la planta.

  - **Aire.** Basado en compresores de aire, se encarga de brindar aire comprimido a una presión requerida para el funcionamiento de todos los sistemas neumáticos en la planta.
  - **Frío.** Basado en compresores de amoniaco, su tarea principal es la de enfriar el producto para su envasado.
  - **Vapor.** Dos calderos proveen vapor de agua a las distintas máquinas que lo requieren dentro la planta.

Todas las áreas que se describen constituyen casi la totalidad del consumo de energía eléctrica en la planta así como también constituyen el proceso entero de producción de la bebida, desde el tratamiento del agua cruda hasta el envasado. Debido a la importancia de la medición del consumo de energía, se precisa contar con un sistema eficiente y confiable.

## Situación Actual.
 Se puede contextualizar el escenario en la actualidad, analizando las tendencias tecnológicas, desarrollos académicos y conceptos que soportan y dan el punto inicial al desarrollo de este proyecto, en tal caso se puede mencionar los siguientes aspectos que son parte de la situación actual:

### Eficiencia energética.
A partir de la última década del siglo XX y gracias a la creciente preocupación por el calentamiento global y el deterioro de la naturaleza se dedicó bastante esfuerzo en investigar y aplicar conceptos de eficiencia energética dada la creciente necesidad de disminuir la emisión de CO2 a la atmósfera y aprovechar mejor los recursos naturales de los que se dispone. Esto inspiró muchos trabajos en los cuales se abunda en conceptos, definiciones y directrices que la humanidad tiene que seguir para consumir eficientemente la energía, [18], [17], [15] .

### Telemetría.
Hace referencia a tecnologías que son capaces de medir magnitudes físicas para luego enviar la información a un sistema de almacenaje y visualización. Si bien este tipo de tecnología refiere principalmente a transmisión inalámbrica, también se han generalizado sus conceptos para sistemas cableados. Sus aplicaciones abarcan diversos cambios como redes de distribución, plantas químicas o estaciones espaciales. Los sistemas de telemetría han servido de base para muchos desarrollos en los cuales se necesita medir variables en espacios muy distanciados, sus principales avances refieren a protocolos de transmisión inalámbrica, tratamiento y adecuación de señales y algoritmos de redes de sensores distribuidos. [20]

### Sistemas de monitoreo de potencia.
En base a los sistemas de telemetría, se desarrollaron soluciones específicas para monitoreo en la industria, los sistemas de monitoreo de potencia son alternativas que constan de 2 o más medidores que están interconectados de alguna forma. según [4], los componentes primarios de un sistema de este tipo son:

1. Medidores para registrar los datos. Estos medidores se deben seleccionar de manera apropiada para la aplicación, los más básicos poseen mediciones básicas incluyendo voltaje, corriente y potencia real, activa y reactiva. Los dispositivos además deben ser capaces de acceder a una interfaz de comunicación mediante algún protocolo industrial (ModBus, ProfiBus). después de todo, la elección de un dispositivo sobre otro debe depender de la aplicación, y, obviamente el presupuesto para la propuesta de trabajo.
2. Un sistema de software para acumular, gestionar y desplegar los datos. Normalmente se implementa este sistema en una PC y no así en dispositivos específicos. El Software permite no solamente acceder a los datos de los medidores si no también desarrollar complejos análisis sobre ellos. Este sistema normalmente la información es subida a un servidor para facilitar su administración y acceso.
3. Una interfaz de comunicación entre el software y los dispositivos de medición. Se necesita una forma de permitir que los dispositivos interactúen entre sí y con el software. La comunicación puede ser establecida por un medio físico, un cable, también puede utilizarse comunicación inalámbrica o una combinación de ambos.

Todos estos componentes deben ser compatibles para asegurar su perfecto desempeño. Pueden existir otros componentes adicionales que dependen de los requerimientos de cada industria.

### Ámbito local.
En el ámbito local, se ha podido constatar la existencia de diversos proyectos de grado que abordan varios de los temas anteriormente listados. En el campo de la telemetría (véase Sec.3.2), se presenta una propuesta de control digital basada en medidores de electricidad en edificios [5]. Luego, en [13] un trabajo muy reciente se presenta una propuesta muy similar a la planteada en este documento pero abordada desde un enfoque de comunicación inalámbrica basada en GSM. Por otro lado, en [8] se propone un subsistema de metrología de energía eléctrica aplicado a la generación y transporte de energía para grandes clientes, desde un enfoque del servicio ofrecido por las empresas generadoras y distribuidoras.

La medición de consumo de energía eléctrica se ha estudiado e implementado ampliamente en entornos domiciliarios, una propuesta a mencionar está descrita en [14] donde se aborda un mecanismo de medición automática que se comunica a través de cables híbridos de fibra óptica-coaxial para poder monitorear el consumo domiciliario, brindando una propuesta de herramienta para las empresas distribuidoras de energía eléctrica.

También se ha investigado acerca de el monitoreo de la calidad de la onda entregada al consumidor, [2] presenta un sistema modular para la medición y compensación de la onda eléctrica aplicada a un sistema de distribución de energía eléctrica.

Finalmente, y avanzando un paso más en la escala de automatización [10] presenta un sistema SCADA aplicado al uso racional de energía en un edificio perteneciente a una casa de estudios superiores, este proyecto analiza con detenimiento diversos temas concernientes a supervisión y control en tiempo real.

### Soluciones comerciales.
Es posible encontrar en el mercado soluciones comerciales ofrecidas por distintos fabricantes, los cuales brindan opciones con una variedad de características y funcionalidades en cuanto a sistemas de monitoreo de potencia se refiere, se procede a listar algunas de estas soluciones comerciales a continuación:

  - **SIEMENS** ofrece una alternativa a un sistema de monitoreo integrado con posibilidad de control automático de switches y protecciones en base a la gama de dispositivos SENTRON R . Estos dispositivos incluyen medidores, gateways y switches de potencia capaces de comunicarse mediante un protocolo ModBus. El monitoreo se realiza en una PC conectada a una red mediante un software dedicado, vendido por SIEMENS.[16]Figura 1: Sistema de monitoreo integrado SENTRON R , fuente: [16]
  - **Allen-Bradley** presenta diversos dispositivos [1] que pueden ser conjuncionados en un sistema integral a través de comunicaciones industriales, pero no ofrece la instancia de software limitándose solamente a vender medidores de energía con capacidades de comunicación.Figura 2: Dispositivos de medición PowerMonitor R de Allen-Bradley, fuente: [1] 
  - **Schneider Electric** posee interesantes alternativas [6] en cuestión de medición y monitoreo de consumo de electricidad, en especial se cuenta con la línea PowerLogic R . Esta línea de dispositivos incluye medidores con capacidades de comunicación serial y gateways para ethernet, de tal manera que el sistema de monitoreo se centraliza en un pequeño servidor web alojado en el mismo gateway.Figura 3: Medidor PowerLogic PM800 R de Schneider Electric, fuente: [6]


Todas estas opciones gozan de la garantía de empresas líderes en el campo, como son SIEMENS, Allen-Bradley y Schneider Electric, garantizando su desempeño óptimo una vez instalado el sistema, la desventaja es el elevado costo de implementación de un sistema de este tipo, este podría llegar a ser privativo para la mayoría de las industrias de mediano tamaño y menores, siendo accesible solamente para grandes industrias como la industria petrolera o la industria minera.

## Planteamiento del Problema.
Anteriormente, se pudo analizar la situación de la medición y la gestión de energía eléctrica en la planta, se mostró el procedimiento con el que, en la actualidad, se registra el consumo. Este procedimiento cuenta con las siguientes desventajas desde el punto de vista técnico y operacional:

  - El operador debe visitar cada medidor y caminar a lo largo de la planta, esto implica pérdida de tiempo y fuerza de trabajo en una tarea sencilla.
  - Al realizarse la medición por inspección visual se cae en la posibilidad de errores en la lectura y anotar datos falsos.
  - Existe otro procedimiento posterior que desperdicia tiempo el cual es la transcripción de la planilla de papel a una hoja de cálculo en una computadora; este procedimiento también es sensible a errores humanos.
  - Los datos se obtienen diariamente, lo cual no otorga una resolución suficiente en la información haciendo imposible un análisis diario de consumo por horas.
  - Dado que el sistema no es 100% confiable, la gestión del consumo se dificulta limitando su análisis.

Con los elementos listados anteriormente, se puede llegar a la conclusión de que el procedimiento actual para la medición y gestión del consumo de energía eléctrica en la planta SD EA no es eficaz y la información obtenida es insuficiente para un análisis más detallado; y es necesario contar con una alternativa.

Desde el punto de vista de los retos de investigación que esta propuesta conlleva, se precisan conocimientos generales y específicos en diversas áreas de la ingeniería:

  - **Medición de energía eléctrica.** La energía consumida debe ser cuantificada con la suficiente resolución y precisión por un instrumento especializado. Se debe tener un panorama claro sobre los mecanismos, principios y tipos de medidores existentes.
  - **Redes y protocolos de comunicación industrial.** Los componentes y dispositivos industriales con los que se debe trabajar se comunicarán mediante protocolos establecidos para comunicaciones industriales. es necesario explorar documentación sobre los mismos y estudiar su aplicabilidad en el sistema.
  - **Sistemas monitoreo de potencia.** Tal como se analiza en la sección (3.3) se deben analizar las características, componentes y diseño de este tipo de sistemas para implementar en la solución.
  - **Bases de datos.** Se requieren conocimientos acerca de diseño y gestión de bases de datos enfocando su aplicación a brindar un soporte a los datos obtenidos de la medición.
  - **Desarrollo web.** La plataforma de software es tan importante como la de hardware ya que ésta será la interfaz directa con la que que se trabaje e interactúe constantemente. Es menester conocer las metodologías de diseño y desarrollo de sistemas informáticos, las herramientas adecuadas y las formas de implementar los mismos.
  - **SCADA.** Como un conjunto de herramientas de hardware y software diseñado para controlar y supervisar procesos industriales remotamente, este tipo de soluciones presentan la información de campo en tiempo real y controla automáticamente el proceso a través de dichos dispositivos. Un sistema SCADA es una solución integral para el control de procesos y la referencia a sus conceptos, técnicas y prácticas serán parcialmente referidos en el desarrollo de este proyecto.

Los temas citados anteriormente comprenden la base teórica y fundamental para el desarrollo de un sistema capaz de satisfacer la necesidad de contar con un sistema eficaz de medición y monitoreo del consumo de energía eléctrica en la planta SD EA de la cervecería Boliviana Nacional.

## Objetivos.
Desarrollar un sistema de medición y monitoreo del consumo de energía eléctrica en la Planta Embotelladora Soft Drinks El Alto de la cervecería Boliviana Nacional, que permita acceder a datos históricos del consumo para poder facilitar la gestión eficiente del uso de electricidad en dicha planta embotelladora.

Para alcanzar el objetivo será necesario:

 - Investigar y evaluar los requerimientos específicos del sistema para poderse aplicar en las instalaciones de la planta.
 - Diseñar la arquitectura del sistema de medición(hardware) y el sistema de información (software) tomando en cuenta los requerimientos previamente determinados y las tecnologías disponibles.
 - Desarrollar un sistema de información destinado al registro de mediciones instantáneas que con el tiempo de funcionamiento se convertirán en datos históricos de medidas de energía y actualizados del consumo de la planta por áreas funcionales.
 - Desarrollar herramientas de gestión básica del consumo embebidas en el sistema de información que facilite un análisis inicial de la información desplegada.
 - Implementar un prototipo del sistema en la planta embotelladora y evaluar su desempeño.


## Justificación.
### Técnica.
La incorporación de un sistema de monitoreo de potencia brindará accesibilidad a los datos del consumo soportada por la robustez de un sistema electrónico e informático que lo convierten en una alternativa eficaz para la gestión del consumo de energía eléctrica.

Hoy en día el aprovechamiento de la tecnología converge a disminuir esfuerzos y mejorar el rendimiento en cualquier tarea realizada antes manualmente. Un sistema de monitoreo limita la exposición del personal a potenciales riesgos eléctricos proveyendo de manera automática las mediciones en estas áreas peligrosas.

La disponibilidad de las tendencias de los datos puede servir para notificar al personal adecuado de la existencia de anomalías en el funcionamiento de maquinaria y equipos, permitiendo planificar futuras acciones de mantenimiento en lugar de enfrentar una parada no programada (mantenimiento preventivo).

### Económica.
Las fabricas e industrias bolivianas en la actualidad basan su funcionamiento en, principalmente, dos fuentes de energía: el gas natural y la electricidad, siendo la última uno de los principales costos de operación de cualquier planta.

Dado que la evaluación de los datos del sistema de monitoreo puede revelar problemas existentes que afecten el funcionamiento de los procesos dentro de la planta, es posible tomar decisiones tales como inversiones en nueva maquinaria o equipos que ahorren energía en procesos eléctricos, resultando éstas acciones en una mayor productividad.

Cada ventaja discutida anteriormente influye directa o indirectamente con un impacto monetario positivo: gastos por lesiones o muerte, mantenimiento preventivo y ahorro de energía; por lo que la instalación de un sistema de este tipo se perfila de una manera atractiva a una inversión en cualquier industria.

### Académica.
El presente Proyecto de Grado pretende abordar distintos temas de la ingeniería y los aglutina en un sistema integral completamente funcional, abarcando distintos tópicos que van desde la telemetría, sistemas de monitoreo de potencia, pasando por redes de comunicación industrial hasta llegar al desarrollo de sistemas informáticos y bases de datos. Es en estos campos en los que se pretende brindar un aporte académico en cuanto a desarrollo de una aplicación de la vida real se refiere.

### Medioambiental.
Un mejor conocimiento de cómo se usa la energía en una instalación permite identificar una gran variedad de perspectivas para mejorar la eficiencia, reducir residuos y reducir el consumo, permitiendo así administrar mejor los recursos naturales disponibles y minimizar el impacto ambiental.

## Alcances y limitaciones.
### Alcances.
El proyecto considera los siguientes alcances, en relación a los objetivos planteados:
>alcances del formato de proyecto

  - Para la definición del entorno de trabajo inicial, se considera una planta embotelladora de gaseosas de pequeña escala, tomando en cuenta que el sistema plantea un sistema de monitoreo de potencia genérico.
  - El análisis de los aspectos inherentes al mecanismo de gestión y registro de consumo de potencia actual actual de las plantas embotelladoras, se ha podido evidenciar que tanto las realidades en los aspectos operacionales como técnicos son similares dependiendo al tamaño de la planta. En este entendido, el proyecto presente no pretende reemplazar los métodos actualmente implementados en las plantas embotelladoras para gestionar su consumo de potencia, sino brindar una herramienta para mejorar dicha gestión pudiendo ahorrar tanto tiempo como trabajo a los analistas y operadores.
  - La identificación y evaluación de la tecnología necesaria, que permitan recoger información de campo con respecto al consumo de potencia de las líneas, se realiza con la finalidad de identificar los requerimientos para el desarrollo del sistema propuesto en todos los niveles o componentes que fueran necesarios. Asimismo, en la medida de lo posible se pretende la reutilización e integración de tecnologías ya implementadas.
  - Para el diseño del sistema se considera como base de desarrollo la metodología RUP, la cual permitirá seguir el desarrollo del proyecto en sus diferentes etapas con mayor claridad y bajo técnicas ya formalizadas. Asimismo considera la aplicación de conceptos de sistemas supervisorios, orientados a un desarrollo de componentes de software y hardware . Consecuentemente el desarrollo del proyecto abarca hasta el nivel de diseño del sistema e implementación de un prototipo básico.
  - El desarrollo de un sistema de información, para la administración de la información recolectada, se basa en los datos recolectados por la red de medidores y presentará una interfaz amigable de visualización y análisis de dichos datos.
  - La implementación de un prototipo funcional del sistema se plantea con la finalidad de probar el funcionamiento y utilidad del sistema diseñado.

>alcances mios sin corregir

  - Análisis de los requerimientos de un sistema de monitoreo de potencia para una planta embotelladora de bebidas gaseosas.
  - Se utilizará una metodología establecida y estándar para el modelado, diseño y ejecución del sistema.
  - El tipo de energía a cuantificar incluirá potencia real, potencia activa y potencia reactiva, según corresponda.
  - Estudio y diseño de un sistema integral y completamente funcional en su fase de prototipo.
  - La recolección de datos e información del consumo en la planta.


### Limitaciones
En cuanto a las limitaciones que se observan en la realización del proyecto, se pueden apreciar las siguientes:

>limitaciones del formato de proyecto

  - Este trabajo solo se centra en la aplicación de capacidades de ingeniería para el desarrollo de un sistema de supervisión, orientado a un problema recurrente en plantas industriales, se asume por tanto que la etapa de implementación de los desarrollos mostrados en este proyecto es posterior al mismo.
  - Pese a que el acceso de datos de planta es vital para el desarrollo del proyecto, la información proporcionada por el plantel técnico de la planta será utilizada solamente como referencia y las pruebas y desarrollo se basará en la generación de datos generados artificialmente.
  - El desarrollo del Sistema de Monitoreo constituye un diseño "a medida" para una situación y no se utilizarán soluciones comerciales por su elevado costo.
  - Según las particularidades de la propuesta de proyecto no se realizará ninguna evaluación de costos, por tratarse de un caso de factibilidad técnica.
  - El desarrollo del sistema de información se basará en aplicaciones y librerías *open source* y de libre uso, limitando la utilización de software licenciado y de pago; dado que el presente proyecto se presenta como una propuesta académica implementada en un prototipo.
  - El sistema de medición remota estará basado en medidores de energía con capacidades de comunicación a través de protocolos industriales por un medio físico (cable). No se contempla la comunicación inalámbrica.  
  - Las implementación y pruebas del prototipo se realizarán exclusivamente en la planta Soft Drinks El Alto de la cervecería Boliviana Nacional.
  


