#SECCIÓN III: DESARROLLO DEL PROYECTO: CONCEPCIÓN, REQUERIMIENTOS Y DISEÑO.
> En esta sección se detallará la parte inicial del proyecto desde la concepción hasta el diseño del mismo, tanto en la parte de hardware como de software
> 

##ANÁLISIS DE REQUERIMIENTOS

> Se lista y especifican los requerimientos de manera formal para aplicarlos en el proyecto. Se realiza a través de models de casos de uso. También se analizan las restricciones.

Se documenta la Especificación de requerimientos de manera formal para ser aplicada en el desarrollo del Proyecto de Grado. Ésta documentación se realiza a través de *Modelos de Casos de Uso*; y entre otras consideraciones, propias de la Metodología RUP, se describe el alcance de la finalidad concebida para el sistema, así como las restricciones consideradas en su diseño.

También se incluyen la visión global de las caractarísticas del sistema y las consideraciones de las propiedades de cada requerimiento en *Matrices de Atributos Funcionales*.

###Visión general
>Breve descripción del sistema citando las anteriores secciones.

De acuerdo a lo señalado en el objetivo de este proyecto, el trabajo presenta la concepción y conceptualización de UN SISTEMA DE MONITOREO Y GESTIÓN DEL CONSUMO DE ENERGÍA ELÉCTRICA PARA LA PLANTA SOFT DRINK EL ALTO DE LA CBN, cuyos aspectos contextuales han sido señalados en el Capítulo 3 "Macro de Referencia" de este documento.

Para el sistema se consideró necesario un análisis de la situación actual y las dificultades o deficiencias que presenta el procedimiento actual para el registro del consumo (Cap. 1 "Planteamiento del problema"); apoyándose en los conceptos, tecnología y técnicas de los Sistemas de Supervisión y Sistemas de Medida a distancia.

Es necesario considerar también el aspecto económico de la propuesta y pese a que en este proyecto no se abordan detalles exhaustivos acerca sobre costos de implementación, se ha intentado desarrollar una alternativa de *bajo costo* basando el sistema informático en plataformas *open source* y de libre uso. Esto, además de reducir el costo de implementación dota al sistema de facilidad de actualización y mantenimiento notable.

####ALCANCES DEL SISTEMA
  
Se abarca el alcance del Sistema hasta el nivel de diseño, ello en atención a lo expuesto en el Cap. 1 "Alcances y Limitaciones".

El diseño contempla la supervisión de la planta de envasado de la embotelladora, enfocándonos en las áreas de mayor consumo proporcional en dicha planta. 

Los resultados alcanzados de las pruebas del diseño a través de un prototipo podrán extrapolarse sin muchos problemas a una planta de mayor envergadura así como también a cualquier otro tipo de plantas industriales no solamente embotelladores o relacionadas con la industria alimenticia.
**Esquema general**.
>Planteamiento de aplicación de los objetivos del proyecto dentro los alcances mencionados en anteriores secciones. Esta parte contendrá gráficos condensando los conceptos.

A nivel de Esquema, se consideró la concepción del sistema que esté integrado por un entorno físico, distribuido compuesto por una red de medidores industriales el cual cumple la función de sensar la corriente y el voltaje de las líneas de todas y cada una de las áreas funcionales, realiza el preprocesamiento necesario y preparar la información para ser enviada hacia la siguiente instancia.

Así también, el siguiente nivel, de vital importancia al igual que el primero, denominado *Sistema de Monitoreo*, tiene la función de traducir los datos recabados por la red de medidores en información útil para el supervisor o analista.

La comunicación entre ambos sistemas, no se abordará de manera muy exhaustiva, sin embargo, se procura brindar los requerimientos mínimos de funcionalidad y seguridad necesarios. Esta interacción, traducida en transacciones y datos de respuesta se podrá apoyar en cualquier *Red de Comunicaciones*.

>grafico del esquema de la visión general del sistema

El anterior esquema puede plantearse como una Estructura con cierta Jerarquía por niveles o capas, en la que se introducen no solamente las entidades que la conforman, si no también la funcionalidad y los servicios que cada uno de ellos ofrece al nivel superior. De la misma manera, se introduce el nivel que corresponde a la parte de la aplicación, o aquellas que contienen la interfaz hombre-máquina para interactuar con las prestaciones del sistema a partir del uso de los servicios subyacentes.

>gráfico de la jerarquía

La descripción preliminar de la Estructura Jerárquica desde un enfoque conceptual se presenta en los siguientes puntos

  - **Aplicación**. En este nivel el usuario final, a través de una *HMI* (del ingés *Human-Machine Interface*), goza de todos los servicios que ofrece el sistema.
  - **Gestión**. En este nivel estan contenidos los servicios que permiten el registro y procesamiento de los datos de consumo de potencia para su traducción en datos y gráficos a mostrarse en el nivel de *Aplicación*. Entre los servicios mencionados se tiene:
    + Interacción con los dispositivos de campo (red de medidores).
    + Registro y estructuración de los datos históricos.
    + Gestión de Operación de la aplicación.
    + Visualización de gráficos y resúmenes sistematizados.
  - **Comunicaciones**. El nivel de Comunicaciones es un servicio que integra el nivel de Gestión y Aplicación con el Medio físico y se implementa mediante un dispositivo especializado para tal tarea.
  - **Medio Físico**. Este nivel se constituye por una red de dispositivos electrónicos, a nivel de software y hardware, encargados de recolectar la información respecto al consumo de potencia en la planta a través de sensores de corriente y voltaje, que constituye la información básica a procesar en el nivel de *Gestión*.

**Funcionalidad**.
> Características funcionales del sistema en su conjunto.
 
En una etapa prelimminar para la definición de los alcances, con respecto a la medición y tratamiento de los datos sensados, se establecen las funcionalidades que deve considerar el Sistema de Monitoreo, mismas que se describen someramente en las siguientes secciones.
  - **Sensado y Adquisición de Datos**. Se concibe la utilidad para el sistema de medir el consumo de potencia de la planta en determinados puntos tratando de cubrir todas las áreas funcionales con el objetivo de realizar un análisis integral.
  - **Procesamiento de Datos**. Se consideran los siguientes tipos de procesamiento de datos:
    + **Clasificación**. Los datos provenientes de los medidores de campo se clasifican de acuerdo a las áreas funcionales para posteriormente almacenar éstos en una Base de Datos.
    + **Cálculos**. Se requiere la realización de operaciones con los registros de cada medidor a nivel de funciones de agregación y detección de eventos, abstrayendo a un nivel más alto la representación de la información para poder realizar una gestión efectiva por parte del usuario de la aplicación.
  - **Almacenamiento de Datos**. Al respecto se consideran aspectos que refieren a la configuración, alta y registro de las mediciones de campo basándose en un almacenamiento cronológico (Series de Tiempo) de dichas mediciones, los datos a almacenar principalmente se reducen a la información enviada por los medidores:
    + **Datos del medidor**. Se proveen datos acerca del dispositivo que realiza la medición, el área correspondiente y otros datos para la identificación y la gestión de los dispositivos que componen la red de medidores.
    + **Datos cronológicos**. Se cuenta con una *Estampa de Tiempo*, que posee información acerca de la fecha y hora precisos del momento de la medición, procurando su unicidad (sin datos repetidos).
    + **Datos de la medición**. La medición en sí se compone del consumo en unidades de Potencia Activa del sector correspondiente al dispositivo en principio, como se detalló en las Limitaciones del sistema.
  - **Interfaz Hombre-Máquina**. Se considera una funcionalidad que permitirá el acceso a la aplicación HMI, esta funcionalidad mínima contempla:
    + **Resúmenes**. Capacidad de brindar información resumida de disponibilidad inmediata de datos de consumo, funciones de agregación.
    + **Alarmas**. Registro y despliegue de información de eventos importantes en la planta a través de mensajes de Alarma disponibles en la aplicación.
    + **Gráficos**. Capacidad de despliegue de gráficos de la evolución e informes resumidos del consumo por áreas.
  - **Comunicaciones**. La comunicación del sistema debe integrar 2 niveles principales de aplicación:
    + **Comunicación de Dispositivos de Campo**. Los dispositivos de campo o Medidores, se comunicarán a través de un protocolo Industrial que posee los estándares requeridos para su robustez en este tipo de ambientes.
    + **Comunicación con el Sistema de Monitoreo**. El sistema de monitoreo se comunicará a través de una Red de Área Local convencional (LAN) ya sea cableada o inalámbrica.
  - **Administración del Sistema de Monitoreo**. El sistema en su conjunto podrá ser administrado en 2 niveles:
    + **Administración de HMI**. La Interfaz Hombre-Máquina poseerá su propio nivel de gestión a través del control de usuarios y el acceso a la base de datos.
    + **Administración de la Red de Medidores**. La Red de Medidores también tendrá su nivel de gestión traducido en la configuración de los dispositivos de campo y la inclusión de nuevos dispositivos para la expansión de dicha red.
  - **Seguridad**. Para la seguridad del sistema se considera:
    + **Salvaguardas y restauraciones**. Permite tanto realizar respaldos de la información tanto para restauraciones como para futuras migraciones.
    + **Gestión de usuarios**. Los usuarios del sistema poseerán sus respectivas cuentas con contraseña jerarquizadas de acuerdo al nivel de acceso a la información y a la configuración del sistema.

###Atributos de requerimientos
>Se describen los requerimientos segun su categoría y niveles de aplicación en el proyecto, sistematizando la forma en que se abordarán en grupos funcionales.

|Grupo Funcional | Tipo Funcional | Requerimiento |
|---|---|---|
|**Sensado y Adquisición de Datos**|Procesamiento| 1. Pro
|**Procesamiento de Datos**|Clasificación|
|                           |Cálculos|
|**Almacenamiento de Datos**|dat0s
|**Interfaz Hombre-Máquina**|
|**Comunicaciones**|
|**Administración del sistema de monitoreo**|
|**Seguridad**|



Se han organizado los requerimientos considerando las necesidades de los usuarios finales (responsables de mantenimiento y técnicos), así como también los requerimientos necesarios para sistemas de supervisión. Ambos aspectos, se ordenan en distintos Grupos Funcionales (tabla) según las características y afinidad entre ellos.

#### Matriz de Atributos Funcionales
Una vez elaborada la lista de requerimientos, ordenadas bajo una lógica de Grupos Funcionales se formalizan mediante la metodología RUP y el lenguaje de modelado UML, a detallar en los atributos de cada requerimiento.
  - Matriz de atributos funcionales
  
###Especificación de Requerimientos
>A partir del análisis de las matrices anteriores se generan *casos de uso*

Uno de los primeros resultados obtenidos es el que refiere a la Especificación de Requerimientos del sistema. En tal caso se siguió la metodología adoptada para el desarrollo del proyecto, para definor los componentes y los Casos de Uso a partir de la Matriz de requerimientos anteriormente definida.

### Modelo de Casos de Uso
Los Casos de Uso fueron organizados en varios paquetes, considerando los Requerimientos Funcionales y otros para la especificación.


  - Modelos de casos de uso
  - Documentación de los casos de uso
  
##ARQUITECTURA DEL SISTEMA
>Representación general en diagramas de bloques por capas del proyecto

Como resultado de las consideraciones realizadas para el análisis de requerimientos (Cap. 4), se disponía de la documentación suficiente de especificaciones. Para abordar la Arquitectura, en este capítulo se presentan los componentes de la arquitectura del sistema que fuera considerada, estos componentes se organizan sobre diferentes niveles de abstracción. Finalmente se presenta el diseño de los componentes lógicos de las diferentes aplicaciones de usuario ofrecidas por el Sistema de Monitoreo.

Así mismo, También se presenta la arquitectura a nivel de Hardware para aquellos elementos que permitirían el registro de las mediciones de consumo de potencia en la planta.


###Arquitectura general
>Se describe las capas componentes del sistema y su interacción, conformando la arquitectura general.

Se señala los elementos que dan soporte a la Arquitectura del sistema, para luego describir la estructura básica sobre la cual se construyó la funcionalidad planteada.

La siguiente ilustración, muestra la arquitectura lógica general propuesta para el Sistema de Monitoreo, el cual se estratifica en base a los tipos de servicios ofrecidos por el sistema, destacando la relación entre los elementos y las capas de los mismos.

###Componentes de la red de medidores: Hardware
>La parte de hardware del sistema, la red de medidores de potencia, estará descrita en este acápite de manera detallada considerando principalmente:
  - Esquema de la red de medidores
  - Descripción de la arquitectura de la red de medidores

###Componentes del sistema de monitoreo
>La parte de software, el sistema de monitoreo y gestión en sí se detalla considerando también:
  - Esquema del sistema de monitoreo
  - Descripción de las capas y componentes
  
#SECCIÓN IV: DESARROLLO DEL PROYECTO: PROTOTIPO Y PRUEBAS

##IMPLEMENTACIÓN DEL PROTOTIPO

###Descripción general del prototipo
  - Descripción por componentes
  - Red de medidores
  - Sistema informático
  
##PRUEBAS Y RESULTADOS DEL PROTOTIPO

###Red de medidores de energía
###Sistema de monitoreo.

#SECCIÓN V: CONCLUSIONES

##CONCLUSIONES

##RECOMENDACIONES
