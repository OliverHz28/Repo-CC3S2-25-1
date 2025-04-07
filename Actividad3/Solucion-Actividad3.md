# Actividad 3

## **Actividad: Computación en la nube**

### A. Cuestionario

1. **Motivaciones para la nube**  
 (a) ¿Qué problemas o limitaciones existían antes del surgimiento de la computación en la nube y cómo los solucionó la centralización de servidores en data centers? 

    Antes de la computación en la nube, las empresas no tenian otra opción mas que construir, operar y mantener sus propios recursos y servicios informaticos generalmente consolidados en centro de datos fisicos. 
    
    #### Principales limitaciones :

    - **Alto costo en la infraestructura**, las empresas debian comprar, operar y mantener sus propios servidores lo que resultaba costoso.   

    - **Escalabilidad limitada**, si se requeria de más capacidad las empresas debían comprar nuevos servidores lo que tomaba tiempo y dinero.    
    
    - **Mantenimiento complejo**, se requería de personal especializado para gestionar los servidores, la seguridad y actualizaciones.

    - **Baja disponibilidad**, si un servidor fallaba, los servicios podían quedar inactivos.

    #### Solución con la nube (Data Centers Centralizados)

    - **Economía de escala**, las empresas pueden alquilar recursos en la nube en lugar de comprarlos, pagando asi solo por los recursos o servicios que consumen. 

    - **Escalabilidad flexible**, las empresas pueden aumentar o reducir los recursos según la necesidad demanda sin comprar hardware adicional.   
    
    - **Mantenimiento simplificado**, las empresas transfieren la carga operativa a los proveedores de nube quienes se encargaran de gestionar la seguridad, las actualizaciones y el mantenimiento.

    - **Alta disponibilidad y redundancia**, los data centers replican datos en varios servidores, evitando asi las interrupciones.


(b) ¿Por qué se habla de “The Power Wall” y cómo influyó la aparición de procesadores multi-core en la evolución hacia la nube?





### B. Actividades de investigación y aplicación

1. **Estudio de casos**  
   - Busca dos o tres casos de empresas (startups o grandes organizaciones) que hayan migrado parte de su infraestructura a la nube. Describe:
     1. Sus motivaciones para la migración.  
     2. Los beneficios obtenidos (por ejemplo, reducción de costos, escalabilidad, flexibilidad).  
     3. Los desafíos o dificultades enfrentadas (ej. seguridad, cumplimiento normativo).

    Netflix, empresa líder en streaming de contenidos audiovisuales comenzo en 1997 alquilando DVDs dentro de Estados Unidos a travez de su plataforma diguital y en el 2008 se tomó la decisión de saltar a la nube y fue gracias a su migración al cloud computing que Netflix pudo lanzar su plataforma de streaming a nivel mundial.

    - **Motivacion**, Netflix experimentó un crecimiento explosivo en su base de suscriptores, lo cual exigía una mejor infraestructura que sea capaz de adaptarse instantáneamente al aumento de usuarios y la demanda de transmisión.

    - **Beneficios**
        1. **Escalabilidad**, la nube les permitió escalar su infraestructura de manera flexible para manejar estos picos de demanda.
        
        2. **Fiabilidad**, la infraestructura de la nube les permitio proporcionar una mayor disponibilidad y redundancia, mejorando la fiabilidad del servicio.
        
        3. **Reducción de costos**, al migrar a la nube, Netflix logró reducir los costos relacionados con el mantenimiento de su propias infraestructuras.

    Pearson, el proveedor global de contenido educativo, evaluación y servicios digitales contaba con aplicaciones locales y centros de datos heredados que dificultaban la escalabilidad e inhibían la innovación. Por ello, Pearson migró a AWS para modernizarse utilizando Amazon ECS, Amazon EC2 y Aurora, totalmente gestionados por Amazon RDS.

    - **Motivación**, Pearson buscaba modernizar sus sistemas heredados para ganar agilidad y flexibilidad en la entrega de sus servicios educativos. Al ser una empresa con presencia mundial, necesitaba una infraestructura capaz de  adaptarse a las demandas de sus usuarios en diferentes regiones.

    - **Beneficios**
        1. **Mayor agilidad y flexibilidad**, la nube les permite adaptarse rápidamente a los cambios en el mercado educativo y lanzar nuevas soluciones de aprendizaje de manera más eficiente.
        
        2. **Mejor experiencia para el usuario**, la infraestructura en la nube proporciona una mayor fiabilidad y disponibilidad, lo que mejora la experiencia de los estudiantes y educadores.

        3. **Impulso a la innovación**, la migración a la nube facilita la integración de tecnologías avanzadas como la IA, lo que permite a Pearson desarrollar soluciones de aprendizaje más personalizadas y efectivas.

        4. **Reducción de costos**, Pearson a reducido costos operativos con la migración a la nube.

---

2. **Comparativa de modelos de servicio**  
   - Realiza un cuadro comparativo en el que muestres las **responsabilidades** del desarrollador, del proveedor y del equipo de operaciones en los distintos modelos (IaaS, PaaS, SaaS).  
   - Incluye aspectos como: instalación de S.O., despliegue de aplicaciones, escalado automático, parches de seguridad, etc.

    ### Cuadro Comparativo de Responsabildades

    | **Aspecto**              | **IaaS (Infraestructura como Servicio)** | **PaaS (Plataforma como Servicio)** | **SaaS (Software como Servicio)** |
    |--------------------------|----------------------------------------|------------------------------------|----------------------------------|
    | **Instalación del S.O.** | Desarrollador / Equipo de operaciones | Proveedor                         | Proveedor                         |
    | **Administración del S.O.** | Desarrollador / Equipo de operaciones | Proveedor                         | Proveedor                         |
    | **Despliegue de aplicaciones** | Desarrollador / Equipo de operaciones | Desarrollador                     | Proveedor                         |
    | **Gestión de middleware** | Desarrollador / Equipo de operaciones | Proveedor                         | Proveedor                         |
    | **Escalado automático** | Configurable por el usuario           | Proveedor                         | Proveedor                         |
    | **Parches de seguridad** | Desarrollador / Equipo de operaciones | Proveedor                         | Proveedor                         |
    | **Monitoreo y mantenimiento** | Desarrollador / Equipo de operaciones | Compartido (Proveedor y Desarrollador) | Proveedor                         |
    | **Acceso y gestión de datos** | Desarrollador                        | Desarrollador                     | Proveedor                         |

---

3. **Armar una estrategia multi-cloud o híbrida**  
   - Imagina que trabajas en una empresa mediana que tiene una parte de su infraestructura en un data center propio y otra parte en un proveedor de nube pública.  
   - Diseña una estrategia (de forma teórica) para migrar el 50% de tus cargas de trabajo a un segundo proveedor de nube, con el fin de no depender exclusivamente de uno.  
   - Explica dónde iría la base de datos, cómo manejarías la configuración de red y cuál sería el plan de contingencia si un proveedor falla.

    ### **1. Situación Actual**
    La empresa cuenta con una infraestructura híbrida:
    - Parte de los servicios alojados en un **data center propio**.
    - Resto de la infraestructura en un **proveedor de nube pública (Proveedor A)**.

    ### **2. Objetivo**
    Reducir la dependencia de un solo proveedor de nube migrando el 50% de las cargas de trabajo a un **segundo proveedor de nube (Proveedor B)**, asegurando redundancia, escalabilidad y continuidad operativa.

    ### **3. Estrategia de Migración**
    #### **a) Distribución de la Carga de Trabajo**
    - Mantener sistemas críticos en el **data center privado** para mayor control y seguridad.
    - Dividir aplicaciones y servicios en **Proveedor A** y **Proveedor B** de forma equilibrada para evitar dependencia exclusiva.
    - Implementar **balanceo de carga** entre los dos proveedores de nube.

    #### **b) Ubicación de la Base de Datos**
    - Base de datos principal en el **data center privado**, replicada en **Proveedor A**.
    - Segunda réplica en **Proveedor B**, con sincronización en tiempo real.
    - Uso de **bases de datos distribuidas (ej. Cloud Spanner, Amazon Aurora, etc.)** para mejorar resiliencia.

    ### **4. Configuración de Red**
    - Implementar **VPN y redes privadas virtuales (VPC)** para conectar el data center y los dos proveedores de nube.
    - Uso de **CDN y DNS globales** para optimizar el tráfico entre usuarios y servidores.
    - Configuración de **firewalls y Zero Trust Security** para controlar accesos y tráfico entre entornos.

    ### **5. Plan de Contingencia**
    - **Monitoreo proactivo** con herramientas de observabilidad multi-cloud (ej. Datadog, Prometheus).
    - Si **Proveedor A falla**, se activan cargas de trabajo en **Proveedor B** automáticamente mediante orquestación con **Kubernetes** o **Terraform**.
    - **Backups regulares** en ambos proveedores con recuperación automática en caso de incidentes.
    - **Pruebas de resiliencia periódicas** para garantizar la continuidad del negocio.

    ### **6. Beneficios de la Estrategia**
    **Reducción de riesgos** por no depender de un solo proveedor.
    **Optimización de costos** utilizando precios competitivos entre proveedores.
     **Mayor flexibilidad** para escalar cargas de trabajo según demanda.


---

4. **Debate sobre costos**  
   - Prepara un breve análisis de los pros y contras de cada tipo de nube (pública, privada, híbrida, multi-cloud) considerando:
     1. Costos iniciales (CAPEX vs. OPEX).  
     2. Flexibilidad y escalabilidad a mediano y largo plazo.  
     3. Cumplimiento con normativas (p.ej. GDPR, HIPAA).  
     4. Barreras o complejidades al cambiar de proveedor.


    ### Análisis de Costos en Modelos de Nube

    #### 1. **Nube Pública**
    **Pros:**
    - Modelo OPEX: pago por uso, sin inversión inicial en infraestructura.
    - Alta escalabilidad y flexibilidad.
    - Rápido despliegue de recursos.
    - Mantenimiento y seguridad gestionados por el proveedor.

    **Contras:**
    - Dependencia de proveedores externos.
    - Posibles costos variables elevados con un uso intensivo.
    - Riesgos en cumplimiento normativo (GDPR, HIPAA) dependiendo del proveedor y región.
    - Mayor dificultad para personalizar la infraestructura.


    #### 2. **Nube Privada**
    **Pros:**
    - Mayor control sobre la seguridad y cumplimiento normativo.
    - Personalización total de la infraestructura y software.
    - Rendimiento más predecible.

    **Contras:**
    - Alto CAPEX: requiere inversión en hardware y mantenimiento.
    - Menor flexibilidad y escalabilidad en comparación con la nube pública.
    - Mayor responsabilidad en gestión y actualización de sistemas.

    #### 3. **Nube Híbrida**
    **Pros:**
    - Equilibrio entre control, seguridad y escalabilidad.
    - Permite aprovechar la elasticidad de la nube pública sin perder control sobre datos sensibles.
    - Puede optimizar costos al utilizar cada tipo de nube según la necesidad.

    **Contras:**
    - Costos de integración y administración pueden ser elevados.
    - Mayor complejidad técnica para conectar entornos públicos y privados.
    - Posibles problemas de latencia y compatibilidad.


    #### 4. **Multi-Cloud**
    **Pros:**
    - Evita dependencia de un solo proveedor.
    - Flexibilidad para seleccionar servicios de distintas nubes según costos y rendimiento.
    - Mejora la resiliencia y disponibilidad de los servicios.

    **Contras:**
    - Complejidad en la gestión y orquestación de múltiples nubes.
    - Costos administrativos y operativos pueden aumentar.
    - Dificultades en la interoperabilidad y cumplimiento normativo entre distintos proveedores.

    ### Cuadro Comparativo de los Tipos de Nube

    | **Aspecto**                | **Nube Pública** | **Nube Privada** | **Nube Híbrida** | **Multi-Cloud** |
    |----------------------------|-----------------|-----------------|----------------|--------------|
    | **Costos iniciales (CAPEX vs. OPEX)** | OPEX: pago por uso, sin inversión inicial. | Alto CAPEX: inversión en hardware y mantenimiento. | Combinación de CAPEX y OPEX según uso. | Principalmente OPEX, pero con costos administrativos altos. |
    | **Flexibilidad y escalabilidad** | Alta escalabilidad y flexibilidad. | Menor flexibilidad y escalabilidad. | Balance entre escalabilidad y control. | Gran flexibilidad al combinar servicios de distintos proveedores. |
    | **Cumplimiento normativo (GDPR, HIPAA, etc.)** | Depende del proveedor y la región, posibles riesgos. | Mayor control sobre la seguridad y cumplimiento normativo. | Permite cumplir normativas manteniendo datos sensibles en la nube privada. | Complejo al manejar normativas de múltiples proveedores. |
    | **Cambio de proveedor** | Dependencia del proveedor, puede haber barreras. | No aplica (infraestructura propia). | Moderada dificultad en migración y compatibilidad. | Alta complejidad en gestión e interoperabilidad. |

    **Conclusión**, cada modelo de nube tiene sus ventajas y desventajas según el contexto de uso. De acuerdo a las necesidades específicas de seguridad, costos y escalabilidad de la organización se realizara la elección adecuada.

---

#### C. Ejercicio de presentación de "mini-proyecto"

Como parte del **aprendizaje práctico**, forma equipos y presenten un **"Mini-proyecto de arquitectura en la nube"**:

1. **Objetivo del sistema**: Cada equipo define brevemente la aplicación o servicio (por ejemplo, un e-commerce, un sistema de reservas, una plataforma de contenido).  
2. **Selección de modelo de servicio**: Explica si se utilizará IaaS, PaaS o SaaS, y justifica por qué.  
3. **Tipo de nube**: Decide si vas a desplegar la aplicación en una nube pública, privada, híbrida o multi-cloud. Argumenta con un análisis de ventajas y desventajas.  
4. **Esquema de escalabilidad**: Describe cómo la aplicación escalaría en caso de aumento de demanda.  
5. **Costos y riesgos**: Menciona los principales costos (directos o indirectos) y los riesgos asociados a tu elección (p.ej., dependencia del proveedor, requerimientos de seguridad).  
6. **Presentación final**: Prepara un diagrama de alto nivel (físico o lógico) donde se visualice la infraestructura básica y los componentes en la nube.


