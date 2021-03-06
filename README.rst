Índice de vulnerabilidad y adaptación al cambio climático
*********************************************************

Aquí se ofrece una descripción general de la solución propuesta para el Hackathon for Good, organizado conjuntamente por Amazon Web Services e Intel. 

Se han definido una serie de key performance indicators (KPIs) que nos permiten relacionar los problemas medioambiantes y sociales de las ciudades a nivel mundial. Para ello, se ha hecho uso de un conjunto de datos abiertos `2020 - Full Cities Dataset <https://data.cdp.net/Governance/2020-Full-Cities-Dataset/eja6-zden>`_ ofrecidos por `CDP <https://www.cdp.net/es>`_ y una metodología de análisis definida por Saif Shabou. Estos datos se han recogido gracias a *CDP and ICLEI - Local Governments for Sustainability*.

El panel de Amazon QuickSight donde se ilustra la analítica de datos realizada está en `Panel QuickSight <https://us-east-1.quicksight.aws.amazon.com/sn/accounts/503201639695/dashboards/d535cd35-f143-4df9-b854-b626f904527f?directory_alias=jaacubero>`_. Un vídeo corto donde se muestra la solución propuesta está en `Video explicativo <https://youtu.be/vHs10-8lCnk>`_. La siguiente URL describe de forma más detallada el trabajo realizado para desarrollar la solución: `Índice de vulnerabilidad y adaptación al cambio climático <https://indice-adaptacion-climatico.readthedocs.io/en/latest/>`_.

Desafío elegido y el valor de la solución en su resolución
==========================================================

La solución se engloba dentro de la temática de **Sostenibilidad** ofreciendo una visualización de modelo de datos sobre un área de sostenibilidad o medio ambiente. Con la solución ofrecida se pretende dar una respuesta a los objetivos 11 (Ciudades y comunidades sostenibles) y 13 (Acción por el clima) de desarrollo sostenible definidos por las `Naciones Unidas <https://www.un.org/sustainabledevelopment/es/objetivos-de-desarrollo-sostenible/>`_.

.. image:: /images/ods.png
   :width: 800 px
   :align: center

Uno de los pilares de los sistemas de gestión es la mejora continua. Todos los sistemas de gestión actuales se basan el círculo de Deming, o más conocido como círculo PDCA: Plan, Do, Check, Act. Se trata de la estrategia de mejora continua, la cual busca ofrecer un método para que las organizaciones puedan mejorar aumentando la calidad de sus productos y optimicen su productividad, lo que las convertirá en más rentables y competitivas. Una cita atribuida a Peter Drucker ilustra muy bien qué necesitamos para hacer una mejora continua:

	Lo que no se define, no se puede medir. Lo que no se mide, no se puede mejorar. Lo que no se mejora, se degrada siempre.

Con mi solución ofrezco una serie de KPIs que relacionan los problemas medioambientales y sociales y permiten identificar si las ciudades están teniendo en cuenta estos factores para mejorar su sostenibilidad y favorecer la lucha contra el cambio climático. He clasificado los indicadores en dos categorías:

* **KPIs de vulnerabilidad**: Miden la vulnerabilidad de la ciudad en su conjunto a impactos negativos en el cambio climático considerando tres componentes: exposición, sensibilidad y capacidad de adaptación.

* **KPIs de preparación**: Miden el grado de avance de la ciudad en la implementación de políticas de adaptación climática y estrategias de reducción de emisiones considerando varios sectores: análisis de riesgos, emisiones de gas invernadero, energía, transporte, agua, plan de adaptación, etc.

Utilizando estas medidas, tenemos los elementos necesarios para definir las estrategias que pueden llevar a cabo las ciudades para mejorar su sostenibilidad y favorecer la lucha contra el cambio climático.

Servicios de AWS e Intel utilizados
===================================

La siguiente imagen ilustra los servicios de AWS usados (Amazon S3, AWS Glue, Amazon Athena y Amazon QuickSight). Los procesadores Intel proporcionan la base de todos estos servicios implementandos en la nube de AWS. 

.. image:: /images/AWS.png
   :width: 800 px
   :align: center

Las razones que me han llevado a utilizar estos servicios son:

* **Amazon QuickSight** es una excelente herramienta de visualización con múltiples conectores, entre los que se encuentrsa Amazon Athena. Al formar parte del ecosistema de AWS, la integración con otros servicios de AWS como S3, Athena o RDS está garantizada. 

* Amazon QuickSight usa SPICE, el cual es un motor de cálculo en memoria. Esto permite que, una vez que importemos los datos desde su origen, podamos tenerlos almacenados en memoria, lo que se traduce en un mayor rendimiento a la hora de visualizar y navegar por los diferentes cuadros de mando. 

* Importar los datos es realmente sencillo, mediante un menú contextual dependiendo de la fuente de origen y se añadirán los datos de conexión y se cargarán los datos, pasando a un editor. Gracias a este editor podemos formatear campos, cambiar el tipo de datos, crear campos calculados o incluso unir varias fuentes de datos de una forma sencilla. Esta última funcionalidad es muy potente, ya que permite cruzar fuentes de datos de orígenes diferentes directamente en el editor de QuickSight.