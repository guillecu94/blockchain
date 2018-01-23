#**BLOCKCHAIN: INFORMACIÓN GENERAL.**

El blockchain, o _cadena de bloques_ , es una base de datos distribuida, formada por cadenas de bloques diseñadas para evitar su modificación una vez que un dato ha sido publicado usando un sellado de tiempo confiable y enlazando a un bloque anterior.
Es una tecnología especialmente adecuada para almacenar de forma creciente datos ordenados en el tiempo y sin posibilidad de modificación ni revisión.

Aspectos:
⋅⋅* **almacenamiento de datos**\n
⋅⋅* **transmisión de datos**
⋅⋅* **confirmación de datos (mediante un proceso de consenso entre los nodos participantes.**

Los datos almacenados en la cadena de bloques suelen ser transacciones, por eso es frecuente llamar a los datos “Transaccionales”, pero no es necesario que lo sean.

_Aplicaciones prácticas_:

1. En el **campo de las criptomonedas**, la cadena de bloques se usa como notario público no modificable de todo el sistema de transacciones a fin de evitar el problema de que una moneda se pueda gastar dos veces.

2. En el **campo de las bases de datos de registro de nombres**, la cadena de bloques es usada para tener un sistema de notario de registro de nombres, de tal forma que un nombre solo pueda ser utilizado para identificar el objeto que lo tiene efectivamente registrado (alternativa al sistema tradicional de DNS)

3. Uso como **notario distribuido en distintos tipos de transacciones** haciéndolas más seguras, baratas y rastreables. Se usa para sistemas de pago y transacciones bancarias.

4. Es utilizado como **base de plataformas descentralizadas** que permiten soportar la creacion de acuerdos de contrato inteligente entre pares. El objetivo de estas plataformas es permitir a una red de pares administrar sus propios contratos inteligentes creados por los usuarios. Primero se escribe un contrato mediante un código y se sube a la cadena de bloques mediante una transacción. Una vez en la cadena de bloques el contrato tiene una dirección desde la cual se puede interactuar con él.

_Clasificación_:

1. Segun el acceso de los datos:
··* **cadena de bloques pública**: es aquella en la que no hay restricciones ni para leer los datos de la cadena de bloques ni para enviar transacciones para que sean incluidas en la cadena de bloques. Son ideales para uso en aplicaciones totalmente descentralizadas como por ejemplo para internet.
··* **Cadena de bloques privada**: es aquella en la que tanto los accesos a los datos de la cadena de bloque como el envío de transacciones para ser incluidas, están limitadas a una lista predefinida de entidades.
2. Segun los permisos
··* **Cadena de bloques sin permisos**: es aquella en la que no hay restricciones para que las entidades puedan procesar transacciones y crear bloques. Este tipo de cadenas de bloques necesitan “tokenes nativos" para proveer incentivos que los usuarios mantengan el sistema. Un _ejemplo de “tokenes nativos”_ son los nuevos bitcoines que se obtienen al construir un bloque y las comisiones de las transacciones.
··* **Cadena de bloques con permisos**: es aquella en la que el procesamiento de transacciones está desarrollado por una predefinida lista de sujetos con entidades conocidas. Por ello generalmente no necesitan tókenes nativos. Los tokenes nativos son necesarios para proveer incentivos para los procesadores de transacciones. Por ello es típico que usen como protocolo de consenso prueba de participación.
3. Posibles combinaciones de acceso y permisos.
··* **Cadenas de bloques públicas sin permisos**: un ejemplo es el bitcoin. Como no es posible la existencia de cadenas de bloques privadas sin permisos, a éstas se les llama simplemente _cadenas de bloques sin permisos_.
··* **Cadenas de bloques públicas con permisos**: un ejemplo de éstas son las cadenas laterales federadas. Estas cadenas no pueden tener ataques Sybil (?), por lo que en principio poseen un grado más alto de escalabilidad y flexibilidad frente a las públicas sin permisos.
··* **Cadenas de bloques privadas con permisos**: esta combinación es posible ya que hay distintas formas de acceder a los datos de la cadena:
···- leer las transacciones de la cadena de bloques
···- proponer nuevas transacciones para la inclusión en la cadena  de bloques
···- crear nuevos bloques de transacciones y añadirlo a la cadena de bloques. Esta está restringida para cierto conjunto limitado de entidades.
4. Según el modelo de cambio de estado
··* basado en el gasto de salidas de transacciones, también llamado **modelo UTXO**. En ellas cada transaccion gasta salidas de transacciones anteriores y produce nuevas salidas que seran consumidas en transacciones posteriores. Este enfoque tiene _ventajas_ como:
··1. En la propia estructura de la cadena existe una prueba de que nunca se puede gastar dos veces ya que cada transaccion prueba que la suma de sus entradas es más grande que la suma de sus salidas.
··2. Cada transaccion puede ser procesada en paralelo porque son totalmente independientes y no hay conflictos en las salidas.
···El problema de este tipo de cadenas es que solo son utilizables para aplicaciones donde cada salida es propiedad de uno y solo un individuo. 
Basado en mensajes: en este caso, la cadena de bloques representa un consenso sobre el orden de los mensajes y el estado es derivado de forma determinista a partir de estos mensajes
# ¿Qué es una cadena lateral?
Una cadena lateral, en inglés Sidechain, es una cadena de bloques que valida datos desde otra cadena de bloques a la que se llama principal. Su utilidad principal es poder aportar funcionalidades nuevas, las cuales pueden estar en periodo de prueba, apoyándose en la confianza ofrecida por la cadena de bloques principal.
