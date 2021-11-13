# Reto_Multiagentes

## Integrantes

Jorge Cabiedes Acosta - A01024053
José Granger Salgado - A01023661

### Expectativas

- Lograr un modelado exitoso del reto, haciendo análisis multivariables para obtener los mejores resultados.
- Aprender más acerca de el aspecto técnico de realizar modelos como los descritos en el reto.
- Tener una presentación del modelo que sea agradable a la vista

### Compromisos

- Trabajar en el reto de forma constante cada semana.
- Utilizar los projectos de Github para mantener un control acerca de nuestros avances.
- Delegar las responsabilidades para lograr un mejor resultado.

## Descripción del reto

Nuestro trabajo para este bloque es el realizar una modelo que nos permita analizar el comportamiento del tráfico vehicular en un ambiente urbano. Para lograr esto utilizaremos herramientas como Unity y Mesa para generar agentes que representarán los actores que se presentan en le vida real, por ejemplo, los coches, los estacionamientos, los semáforos, etc. Todo esto con el fin de encontrar las mejores y más prácticas soluciones al problema de la movilidad urbana en México.

Para lograr una simulación más orgánica de este caso utilizaremos agentes que representarán las casas de las personas de donde saldrán los coches y otros agentes que representarán los destinos de los coches, de esta forma cada agente de coche tendrá un objetivo a donde ir y podremos observar y analizar los resultados de cada cambio que realizemos en la infraestructura.

## Agentes

### A1: Coche

En base al comportamiento de este agente es cómo podremos deteminar el desempeño de nuestro modelo, este deberá ser capaz de tomar ciertas decisiones de manera proactiva para determinar qué caminos tomar y otras decisiones de manera reactiva para saber de qué forma reaccionar a ciertas situaciones.

|Función del agente    | Descripción     | Relación ]
   | ------------- | -------- | ----------|
   |  Decisión Proactiva   | Tomar el camino más rápido a cierto lugar tomando en cuenta el tráfico y la distancia  | Otros agentes de coches |
   |  Decisión Reactiva    | Identificar si hay otros agentes de coches a su alrededor y evitar una colisión | Otros agentes de coches |
   | Decisión Reactiva | Identificar los agentes de calle y transitar exclusivamente por encima de ellos | Calles |
   | Decisión Reactiva | Identificar el estado de un semáforo para saber si puede avanzar o no | Agentes de semáforos |
   | Contador | El auto realiza un seguimientos de sus emisiones | - |

   
### A2: Casa

En base a la posición de este agente es de donde saldrán los coches, el agente tendrá un tipo de destino programado y cuando un destino requiera de un coche lo hará aparecer.

|Función del agente    | Descripción     | Relación ]
   | ------------- | -------- | ----------|
   | Decisión Reactiva   | Si un agente objetivo solicita un coche hace que aparezca un coche en su posición con el objetivo como destino | Agentes objetivo y agentes de coche |

### A3: Objetivo

Este agente representa cualquier tipo de tienda, entretenimiento, etc. A donde podría dirigirse un auto. Constantemente solicita la presencia de coches y registra el tiempo que se tardan en llegar a su destino.

|Función del agente    | Descripción     | Relación ]
   | ------------- | -------- | ----------|
   | Decisión Proactiva   | De forma aleatoria solicita la presencia de coches | Coches y Casas |
   | Decisión Reactiva | Registra el tiempo que se tardó un coche en llegar al objetivo | Coches |
   
### A4: Calle

Este agente simplemente define el camino sobre el cual pueden transitar los coches.

|Función del agente    | Descripción     | Relación ]
   | ------------- | -------- | ----------|
   
### A5: Semáforo (Opcional)

Este agente se encargará del tráfico en intersecciones, los coches deberán detenerse cuando el estado del semáforo represente "Rojo" y podrán avanzar cuando el estado del semáforo represente "Verde"
   |Función del agente    | Descripción     | Relación ]
   | ------------- | -------- | ----------|
   | Estado   | El estado del semáforo "Verde" o "Rojo". | A pesar de afectar a los coches, en la parte técnica no es necesario tomarlos en cuenta. |
   | Decisión Proactiva | Sincronizarse con otros semáforos que pertenezcan a un mismo grupo a criterio del usuario | Otros agentes de semáforos |
   
## Plan de trabajo
**Objetivos clave**

* [ ] Crear el agente de coche
* [ ] Crear el agente de casa
* [ ] Crear el agente de objetivo
* [ ] Crear el agente de calle
* [ ] Crear las funciones de coche
* [ ] Crear las funciones de casa
* [ ] Crear las funciones de objetivo
* [ ] Recopilar datos
* [ ] Presentar datos

**Objetivos opcionales**

* [ ] Crear el agente de semáforos
* [ ] Crear las funciones de semáforos
* [ ] Considerar variables extras como estacionamientos
   






