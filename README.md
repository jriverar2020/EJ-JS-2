# Herramienta software para apoyar la reasignación de becas de alimentación en la Universidad de Nariño

## 1. Introducción

La Universidad de Nariño, en sus sedes de Pasto, Tumaco e Ipiales, desarrolla procesos de apoyo alimentario dirigidos a estudiantes beneficiarios. Sin embargo, en la operación diaria pueden presentarse cupos de alimentación no utilizados por ausencias, retrasos o cambios de asistencia. Ante esta situación, cada sede ha construido mecanismos informales para redistribuir dichos cupos, con prácticas distintas y sin una herramienta institucional que permita organizar, registrar y controlar el proceso de reasignación.

En este contexto, se propone el diseño y desarrollo de una herramienta software orientada a unificar, apoyar y transparentar la reasignación de becas de alimentación no utilizadas. La solución busca responder a una necesidad operativa real de la Universidad, optimizando el aprovechamiento de los alimentos preparados, reduciendo el desorden en la asignación y generando trazabilidad sobre cada reasignación realizada.

Este documento presenta la base conceptual, funcional y técnica del proyecto, con enfoque académico y de ingeniería de software, de manera que pueda servir como soporte para el diplomado y como insumo para la sustentación final.

## 2. Planteamiento del problema

Actualmente, la reasignación de cupos de alimentación en la Universidad de Nariño no se desarrolla mediante un proceso unificado ni apoyado por un sistema de información institucional. Cada sede aplica prácticas manuales basadas en disponibilidad inmediata, comunicación verbal, apoyo de representantes estudiantiles o difusión por grupos informales de mensajería. Aunque estos mecanismos buscan evitar el desperdicio de alimentos, presentan limitaciones importantes en términos de organización, control, equidad y seguimiento.

En la sede Pasto, el proceso ocurre de manera espontánea cuando, cerca del cierre del horario de desayuno o almuerzo, se identifican cupos disponibles. El personal informa de manera informal a estudiantes cercanos para que consuman la alimentación restante. En Tumaco, la comunicación se realiza de forma indirecta a través de representantes estudiantiles que transmiten el aviso a otros estudiantes. En Ipiales, existe una dinámica un poco más estructurada, ya que se entregan fichas hasta cierta hora, luego se prioriza a estudiantes postulados no beneficiados y, si aún quedan cupos, se informa por grupos de WhatsApp.

La ausencia de un sistema centralizado genera varios problemas. En primer lugar, dificulta garantizar que los cupos sobrantes se reasignen de manera oportuna, lo que puede ocasionar desperdicio de alimentos. En segundo lugar, propicia desorden en la convocatoria y entrega de los cupos, debido a que los criterios de reasignación no siempre están claramente definidos ni registrados. En tercer lugar, limita la transparencia y la equidad del proceso, porque no existe una base de datos consolidada que permita identificar quiénes recibieron reasignaciones, con qué frecuencia y bajo qué condiciones. Finalmente, la falta de historial impide generar reportes, evaluar el comportamiento del servicio y tomar decisiones de mejora sustentadas en información.

Por lo anterior, surge la necesidad de diseñar una herramienta software que permita estandarizar el proceso de reasignación de becas de alimentación en las tres sedes, facilitando el registro, la priorización, la notificación y el control de los cupos no utilizados, bajo criterios claros y trazables.

## 3. Justificación

El desarrollo de una herramienta software para apoyar la reasignación de becas de alimentación se justifica desde perspectivas operativas, sociales, institucionales y académicas.

Desde el punto de vista operativo, el sistema permitiría administrar de forma más organizada los cupos no utilizados, reduciendo tiempos de reacción y evitando que alimentos preparados queden sin ser consumidos. Esto contribuye al uso más eficiente de los recursos institucionales.

Desde la perspectiva social, la solución favorecería una distribución más equitativa y transparente de los cupos sobrantes, al establecer reglas de priorización y registrar cada reasignación. De esta manera, se fortalece la confianza de la comunidad estudiantil en el proceso y se disminuye la dependencia de mecanismos informales o subjetivos.

En el ámbito institucional, la herramienta aportaría trazabilidad y control. La Universidad podría consultar historiales, identificar patrones de uso, conocer qué sede presenta mayor nivel de reasignaciones y tomar decisiones basadas en datos. Incluso si el sistema no se despliega en producción, el desarrollo de un prototipo funcional demuestra la viabilidad de modernizar un proceso administrativo con impacto directo en bienestar universitario.

Desde el enfoque académico, el proyecto es pertinente porque integra análisis de requerimientos, modelado de procesos, diseño de arquitectura, definición de algoritmos de negocio y construcción de una solución de software realista. Además, permite aplicar conocimientos de ingeniería de software en un problema concreto del contexto universitario, generando un producto sólido para sustentación.

## 4. Objetivo general

Diseñar y desarrollar una herramienta software que apoye la gestión eficiente, organizada y transparente de la reasignación de cupos de alimentación no utilizados en las sedes de Pasto, Tumaco e Ipiales de la Universidad de Nariño.

## 5. Objetivos específicos

1. Analizar el proceso actual de reasignación de cupos de alimentación en las sedes de Pasto, Tumaco e Ipiales, identificando similitudes, diferencias y problemáticas.
2. Definir los requerimientos funcionales y no funcionales del sistema, de acuerdo con las necesidades del proceso y del contexto institucional.
3. Diseñar un modelo de solución unificado que permita registrar cupos disponibles, gestionar estudiantes elegibles, aplicar criterios de priorización y mantener trazabilidad de las reasignaciones.
4. Implementar un prototipo funcional que integre módulos de administración, reasignación, notificación y consulta de historial.
5. Validar la coherencia de la propuesta mediante flujos operativos, reglas de negocio y una arquitectura tecnológica adecuada para un proyecto académico de corto plazo.

## 6. Alcance del sistema

El sistema propuesto tendrá como alcance principal apoyar la reasignación de cupos de alimentación no utilizados en las tres sedes objeto del proyecto: Pasto, Tumaco e Ipiales. La solución permitirá centralizar el proceso en una sola plataforma, aunque contemplando particularidades operativas de cada sede.

Dentro del alcance se incluyen:

- Registro de sedes, jornadas y tipos de servicio alimentario.
- Administración de estudiantes y estados de elegibilidad para reasignación.
- Registro de cupos no utilizados por día, sede y franja horaria.
- Gestión de postulaciones o listas de espera para estudiantes interesados en recibir cupos reasignados.
- Ejecución de un proceso de priorización para asignar los cupos disponibles.
- Registro del historial de reasignaciones realizadas.
- Consulta de reportes básicos por sede, fecha y tipo de servicio.
- Gestión de usuarios con roles administrativos y operativos.

Fuera del alcance del proyecto se consideran:

- Integración con sistemas institucionales oficiales de matrícula o bienestar universitario.
- Despliegue en ambiente de producción.
- Integración con servicios reales de mensajería como WhatsApp, correo institucional o SMS.
- Automatización avanzada de validación biométrica, códigos QR o control de acceso físico en comedores.
- Módulos financieros o presupuestales relacionados con contratación de alimentos.

## 7. Análisis del contexto actual

### 7.1 Panorama general

En las tres sedes existe una intención común: aprovechar los cupos de alimentación que no fueron utilizados por los beneficiarios inicialmente asignados. No obstante, el proceso depende de prácticas manuales y de la experiencia del personal, sin una política operativa soportada en una herramienta tecnológica unificada.

### 7.2 Funcionamiento actual por sede

#### Pasto

En la sede Pasto, la dinámica es directa e inmediata. Cuando se acerca el final del horario de servicio y el personal identifica que sobran raciones, se comunica verbalmente a estudiantes que se encuentran cerca del punto de atención. La reasignación ocurre con base en la proximidad física y la oportunidad del momento. Este mecanismo tiene la ventaja de ser rápido, pero depende completamente de la presencia del estudiante en el lugar y no deja evidencia del proceso realizado.

#### Tumaco

En Tumaco, el procedimiento incorpora un intermediario. El personal de cocina o apoyo notifica a representantes estudiantiles sobre la disponibilidad de cupos, y estos representantes transmiten la información a otros estudiantes. Aunque este modelo amplía el alcance del aviso, sigue siendo manual y depende de la capacidad de comunicación de terceros. Esto puede generar demoras, sesgos informativos o cobertura desigual entre estudiantes.

#### Ipiales

En Ipiales se observa un proceso relativamente más organizado. Primero se entregan fichas hasta una hora determinada. Después, los cupos sobrantes se ofrecen prioritariamente a estudiantes que se postularon a la beca pero no fueron beneficiados. Si persisten cupos disponibles, la información se comparte en grupos de WhatsApp para que otros estudiantes interesados puedan reclamar la alimentación. Aun cuando existe una lógica de prioridad, el procedimiento sigue siendo predominantemente manual y con escasa trazabilidad formal.

### 7.3 Comparación entre sedes

| Criterio | Pasto | Tumaco | Ipiales |
|---|---|---|---|
| Forma de aviso | Verbal y directa | A través de representantes | Fichas y grupos de WhatsApp |
| Nivel de formalidad | Bajo | Bajo | Medio |
| Criterio de priorización | Presencia cercana | Difusión por contacto | Prioridad a postulados no beneficiados |
| Registro histórico | No existe | No existe | Muy limitado o informal |
| Dependencia de terceros | Baja | Alta | Media |
| Riesgo de inequidad | Alto | Alto | Medio |

### 7.4 Problemas identificados

Del análisis comparativo se derivan los siguientes problemas:

- No existe un procedimiento institucional uniforme para las tres sedes.
- La información sobre cupos sobrantes se comunica de forma informal.
- No hay criterios homogéneos de priorización y asignación.
- El proceso depende demasiado de la disponibilidad física o del acceso a canales informales de comunicación.
- No se registra un historial confiable de reasignaciones.
- Se dificulta medir la eficiencia del proceso y el nivel de aprovechamiento de los alimentos.

### 7.5 Necesidad de unificación

La comparación evidencia que las sedes no requieren sistemas distintos, sino una sola solución adaptable a diferencias operativas menores. La unificación del proceso permitiría estandarizar reglas, mejorar la equidad, disminuir el desperdicio y fortalecer el control administrativo, manteniendo la flexibilidad suficiente para que cada sede opere con sus horarios y responsables.

## 8. Propuesta de solución

Se propone el desarrollo de una aplicación web centralizada para gestionar la reasignación de cupos de alimentación no utilizados. Esta herramienta permitiría registrar, en tiempo real o en momentos definidos del servicio, los cupos disponibles en cada sede y ejecutar un proceso de reasignación basado en reglas de prioridad previamente configuradas.

La solución funcionaría bajo un enfoque de lista de espera o banco de estudiantes elegibles. Los estudiantes interesados en recibir cupos reasignados podrían estar previamente registrados en el sistema, y el personal autorizado de cada sede podría publicar los cupos sobrantes indicando sede, jornada, fecha y cantidad. A partir de esta información, el sistema aplicaría un algoritmo simple de priorización para proponer a qué estudiantes asignar los cupos, generando un registro histórico de todas las decisiones.

La propuesta no pretende reemplazar toda la operación del servicio alimentario, sino apoyar específicamente el subproceso de reasignación, que es donde actualmente se presenta mayor informalidad. De esta manera, el software se concentra en resolver un problema puntual, con alta viabilidad para un desarrollo académico y una demostración funcional clara en sustentación.

## 9. Descripción del sistema

El sistema es una herramienta web multiusuario orientada a personal administrativo, operadores de sede y, de forma opcional, estudiantes registrados para reasignación. Su función principal es administrar el ciclo de vida de un cupo no utilizado, desde que se detecta como disponible hasta que queda reasignado y registrado en el historial.

De forma general, el software permitirá:

- Registrar estudiantes, sedes, horarios y tipos de servicio.
- Identificar estudiantes postulados, beneficiarios y no beneficiarios.
- Crear eventos de cupos sobrantes por sede y jornada.
- Consultar listas de estudiantes elegibles para reasignación.
- Ejecutar la asignación de cupos según reglas de prioridad.
- Confirmar la entrega efectiva del cupo al estudiante.
- Conservar evidencia histórica de cada reasignación.
- Generar consultas y reportes básicos para seguimiento.

## 10. Módulos del sistema

### 10.1 Módulo de autenticación y usuarios

Permite el acceso seguro al sistema según perfiles de uso. Incluye inicio de sesión, cierre de sesión y administración básica de roles.

Roles sugeridos:

- Administrador general.
- Operador de sede.
- Consultor o coordinador de bienestar.

### 10.2 Módulo de parametrización

Gestiona la información base del sistema:

- Sedes.
- Jornadas de atención.
- Tipos de servicio alimentario.
- Estados de estudiantes.
- Reglas básicas de priorización.

### 10.3 Módulo de estudiantes

Administra la información de los estudiantes que pueden participar en el proceso de reasignación. Permite registrar datos básicos, sede, programa, estado de postulación y condición de elegibilidad.

### 10.4 Módulo de cupos disponibles

Permite al operador registrar cuántos cupos quedaron libres en una fecha, sede y jornada determinada. Este módulo es el punto de inicio del proceso de reasignación.

### 10.5 Módulo de postulaciones o lista de espera

Permite consultar y mantener la lista de estudiantes que pueden ser considerados para recibir cupos reasignados, con sus respectivos niveles de prioridad.

### 10.6 Módulo de reasignación

Es el núcleo del sistema. Aquí se ejecuta el algoritmo de asignación, se generan propuestas de beneficiarios temporales y se confirma la reasignación final.

### 10.7 Módulo de historial y trazabilidad

Registra cada evento asociado al proceso:

- Cupos reportados.
- Estudiantes priorizados.
- Cupos asignados.
- Confirmaciones o rechazos.
- Usuario responsable de la operación.
- Fecha y hora de cada acción.

### 10.8 Módulo de reportes

Permite consultar información consolidada, por ejemplo:

- Número de cupos sobrantes por sede.
- Cupos reasignados por periodo.
- Estudiantes beneficiados por reasignación.
- Porcentaje de aprovechamiento de cupos.

## 11. Requisitos funcionales

1. El sistema debe permitir registrar y administrar las sedes Pasto, Tumaco e Ipiales.
2. El sistema debe permitir registrar tipos de servicio alimentario, como desayuno y almuerzo.
3. El sistema debe permitir crear y administrar usuarios con diferentes roles.
4. El sistema debe permitir registrar estudiantes con información básica y estado frente a la beca.
5. El sistema debe permitir clasificar estudiantes como beneficiarios, postulados no beneficiados o elegibles para reasignación.
6. El sistema debe permitir registrar cupos no utilizados indicando sede, fecha, jornada y cantidad disponible.
7. El sistema debe permitir consultar la lista de estudiantes elegibles por sede.
8. El sistema debe aplicar reglas de prioridad para sugerir la reasignación de cupos.
9. El sistema debe permitir confirmar, rechazar o cancelar una reasignación propuesta.
10. El sistema debe registrar en historial todas las reasignaciones realizadas.
11. El sistema debe permitir consultar reasignaciones por estudiante, sede, fecha y jornada.
12. El sistema debe permitir generar reportes básicos de cupos sobrantes y cupos reasignados.
13. El sistema debe impedir reasignar un mismo cupo más de una vez.
14. El sistema debe registrar el usuario responsable de cada operación.
15. El sistema debe permitir filtrar estudiantes por prioridad, sede y estado.
16. El sistema debe mostrar el estado de cada cupo: disponible, asignado, confirmado o vencido.

## 12. Requisitos no funcionales

1. El sistema debe ser fácil de usar para personal con conocimientos tecnológicos básicos.
2. La interfaz debe ser responsiva para uso en computador y dispositivos móviles.
3. El tiempo de respuesta para operaciones comunes debe ser bajo en entornos de demostración académica.
4. El sistema debe garantizar autenticación de usuarios y control básico de acceso por roles.
5. La solución debe mantener integridad en los registros para evitar duplicidad de asignaciones.
6. El código debe estar organizado en una arquitectura clara y mantenible.
7. La base de datos debe permitir consultas históricas y generación de reportes simples.
8. El sistema debe ser escalable a futuro para incluir nuevas sedes o nuevas reglas de negocio.
9. La solución debe ser desplegable localmente para fines de prueba y sustentación.
10. El sistema debe registrar eventos relevantes para auditoría básica del proceso.

## 13. Modelo conceptual del sistema

Desde el punto de vista conceptual, el sistema se compone de varias entidades principales relacionadas entre sí.

### 13.1 Sede

Representa cada unidad geográfica donde opera el servicio de alimentación. En este proyecto las sedes son Pasto, Tumaco e Ipiales. Cada sede tiene sus propios usuarios operadores, horarios y eventos de cupos sobrantes.

### 13.2 Estudiante

Representa a la persona que puede participar en el proceso de reasignación. Un estudiante pertenece a una sede o puede estar asociado a una sede principal de atención. Además, tiene atributos como identificación, nombre, programa académico, estado de postulación y nivel de prioridad.

### 13.3 Usuario

Representa a la persona que accede al sistema para administrarlo u operarlo. Puede tener rol de administrador, operador o consultor.

### 13.4 Servicio alimentario

Corresponde al tipo de atención que ofrece el comedor en una franja determinada, por ejemplo desayuno o almuerzo. Esta entidad ayuda a clasificar los cupos y las reasignaciones.

### 13.5 Cupo disponible

Representa una cantidad de raciones no utilizadas detectadas en una sede, fecha y servicio alimentario específico. Es el insumo principal del proceso de reasignación.

### 13.6 Postulación o elegibilidad

Describe la condición del estudiante frente al proceso de reasignación. Permite identificar si el estudiante es postulante no beneficiado, si está habilitado para recibir cupos o si tiene una prioridad determinada.

### 13.7 Reasignación

Representa el acto de asignar un cupo disponible a un estudiante elegible. Incluye estado, fecha, usuario responsable y relación con el cupo disponible.

### 13.8 Historial

Es el conjunto de eventos registrados durante la operación. Puede almacenar acciones como creación de cupos, ejecución del algoritmo, confirmación de entrega o cancelación.

En términos relacionales, una sede tiene muchos estudiantes y muchos cupos disponibles; un cupo disponible puede originar varias propuestas de reasignación, pero solo una cantidad determinada de asignaciones confirmadas; un estudiante puede recibir varias reasignaciones a lo largo del tiempo, siempre que las reglas del sistema lo permitan.

## 14. Flujo del sistema

El flujo operativo propuesto es el siguiente:

1. El operador inicia sesión en el sistema.
2. El operador selecciona la sede, la fecha y la jornada correspondiente.
3. El operador registra la cantidad de cupos de alimentación no utilizados.
4. El sistema consulta la lista de estudiantes elegibles para esa sede y jornada.
5. El sistema ordena a los estudiantes según criterios de prioridad definidos.
6. El sistema propone la reasignación de los cupos disponibles a los estudiantes priorizados.
7. El operador revisa la propuesta y confirma la asignación.
8. El sistema cambia el estado de los cupos a asignados y registra la operación en el historial.
9. Si un estudiante no reclama el cupo o se rechaza la asignación, el operador puede liberar nuevamente el cupo.
10. El sistema vuelve a ejecutar la priorización con los estudiantes restantes.
11. Finalmente, la reasignación queda marcada como confirmada o vencida, según el resultado del proceso.

## 15. Algoritmo de reasignación

Se propone un algoritmo simple, lógico y viable para el alcance académico del proyecto.

### 15.1 Criterios sugeridos de prioridad

1. Estudiantes postulados a la beca que no fueron beneficiados.
2. Estudiantes que pertenezcan a la sede donde surgió el cupo.
3. Estudiantes con menor número de reasignaciones recibidas en un periodo determinado.
4. Estudiantes registrados como activos y habilitados.
5. Orden de inscripción en la lista de espera, en caso de empate.

### 15.2 Lógica general del algoritmo

1. Recibir como entrada la sede, la fecha, la jornada y la cantidad de cupos disponibles.
2. Consultar los estudiantes elegibles que correspondan a esa sede y que estén activos.
3. Excluir estudiantes que ya tengan asignación para la misma jornada o que se encuentren bloqueados.
4. Ordenar los estudiantes según el nivel de prioridad y el menor número de reasignaciones previas.
5. Seleccionar los primeros estudiantes de la lista hasta completar la cantidad de cupos disponibles.
6. Generar una propuesta de reasignación.
7. Cuando el operador confirme la entrega, registrar la reasignación como confirmada.
8. Si algún cupo no se concreta, retornarlo al estado disponible y repetir el proceso con la siguiente persona elegible.

### 15.3 Pseudocódigo propuesto

```text
entrada: sede, fecha, jornada, cupos_disponibles

elegibles = obtener_estudiantes_elegibles(sede, jornada)
elegibles = filtrar_activos(elegibles)
elegibles = excluir_ya_asignados(elegibles, fecha, jornada)
elegibles = ordenar_por_prioridad_y_historial(elegibles)

asignados = []

para cada estudiante en elegibles:
    si longitud(asignados) < cupos_disponibles:
        asignados.agregar(estudiante)
    si no:
        salir

registrar_propuesta(asignados, sede, fecha, jornada)
retornar asignados
```

Este algoritmo es adecuado para un primer prototipo porque es fácil de explicar, implementar y validar. Además, permite incorporar mejoras futuras como reglas por vulnerabilidad socioeconómica, puntajes o notificaciones automáticas.

## 16. Tecnologías recomendadas

Considerando que el proyecto es académico, debe desarrollarse en un tiempo limitado y necesita ser entendible para sustentación, se recomienda priorizar tecnologías que ofrezcan rapidez de desarrollo, buena documentación y una curva de aprendizaje razonable.

### 16.1 Opción recomendada

- Backend: `Python con FastAPI`
- Frontend: `React con Bootstrap`
- Base de datos: `PostgreSQL`

### 16.2 Justificación de la recomendación

#### Backend: FastAPI

FastAPI es una excelente opción para proyectos académicos porque permite construir servicios web modernos de forma rápida y ordenada. Facilita la definición de rutas, validación de datos, documentación automática de API y separación clara entre lógica de negocio y acceso a datos. Esto ayuda tanto al desarrollo como a la explicación técnica en sustentación.

#### Frontend: React con Bootstrap

React permite construir una interfaz organizada por componentes, lo que resulta útil si se desean vistas para login, gestión de estudiantes, cupos, reasignación e historial. Bootstrap acelera el diseño visual y evita invertir demasiado tiempo en estilos complejos. Esta combinación ofrece una apariencia profesional en poco tiempo.

#### Base de datos: PostgreSQL

PostgreSQL es robusto, confiable y muy adecuado para manejar relaciones entre estudiantes, sedes, reasignaciones e historial. Además, ofrece consistencia y flexibilidad para consultas posteriores. Aunque MySQL también sería válido, PostgreSQL suele ser mejor valorado en proyectos académicos por sus capacidades relacionales y compatibilidad con buenas prácticas de modelado.

### 16.3 Alternativa simplificada si el equipo tiene menos tiempo

Si se requiere una curva de aprendizaje aún más simple, podría utilizarse:

- Backend: `Flask`
- Frontend: `HTML + Bootstrap`
- Base de datos: `MySQL`

Esta alternativa puede reducir complejidad técnica, pero también ofrece menos estructura para escalar. Para una sustentación más sólida desde ingeniería de software, la combinación `FastAPI + React + PostgreSQL` resulta más completa y moderna.

## 17. Arquitectura sugerida

Se recomienda una arquitectura cliente-servidor de tres capas:

- Capa de presentación: interfaz web desarrollada en React.
- Capa de lógica de negocio: API REST desarrollada con FastAPI.
- Capa de datos: base de datos PostgreSQL.

Este enfoque permite separar responsabilidades, facilitar pruebas, mejorar el mantenimiento y mostrar una estructura profesional de desarrollo de software.

## 18. Metodología recomendada

Para este proyecto se recomienda utilizar una metodología ágil, específicamente Scrum adaptado a un contexto académico.

### 18.1 ¿Por qué Scrum?

Scrum es útil porque permite organizar el trabajo en iteraciones cortas, entregar avances progresivos y ajustar el alcance según el tiempo disponible. Dado que el proyecto no será desplegado en producción, pero sí debe construirse de forma suficientemente completa para demostración y sustentación, Scrum favorece la priorización de funcionalidades de mayor valor.

### 18.2 Aplicación de Scrum al proyecto

Se pueden plantear entre tres y cuatro sprints cortos:

1. Sprint 1: levantamiento de requerimientos, análisis del problema y diseño de base de datos.
2. Sprint 2: desarrollo del backend y lógica de reasignación.
3. Sprint 3: desarrollo del frontend y conexión con la API.
4. Sprint 4: pruebas, ajustes, documentación y preparación de sustentación.

### 18.3 Beneficios de usar Scrum en este caso

- Permite dividir el proyecto en entregables manejables.
- Facilita el seguimiento del avance.
- Ayuda a priorizar funcionalidades esenciales.
- Reduce el riesgo de retrasos al tener revisiones periódicas.
- Se adapta bien al trabajo colaborativo de un diplomado.

## 19. Beneficios esperados de la solución

La implementación del sistema permitiría:

- Unificar el proceso de reasignación en las tres sedes.
- Reducir el desperdicio de alimentos preparados.
- Mejorar la organización operativa del personal encargado.
- Aumentar la transparencia en la asignación de cupos.
- Garantizar trazabilidad e historial de las reasignaciones.
- Disponer de datos para análisis y toma de decisiones.
- Presentar una solución realista, pertinente y defendible académicamente.

## 20. Riesgos y consideraciones

Aunque el proyecto es viable, es importante considerar algunos riesgos:

- La calidad del sistema dependerá de la correcta definición de reglas de prioridad.
- Puede existir resistencia al cambio frente a procesos manuales ya normalizados.
- Si no se cuenta con datos reales de estudiantes, será necesario trabajar con información simulada para demostración.
- Las notificaciones en tiempo real podrían limitarse a simulaciones dentro del prototipo.

Estos riesgos no invalidan la propuesta; por el contrario, ayudan a delimitar el proyecto y a mostrar pensamiento crítico durante la sustentación.

## 21. Conclusiones

La reasignación de becas de alimentación en la Universidad de Nariño representa un proceso necesario pero actualmente informal, heterogéneo y poco trazable en las sedes de Pasto, Tumaco e Ipiales. Esta situación genera oportunidades de mejora significativas en términos de organización, equidad y aprovechamiento de los recursos alimentarios.

La propuesta de una herramienta software unificada responde de manera directa a esta necesidad, al ofrecer un mecanismo estructurado para registrar cupos sobrantes, priorizar estudiantes elegibles, ejecutar reasignaciones con criterios claros y conservar historial de cada operación. Desde la perspectiva de ingeniería de software, el proyecto es pertinente, viable y suficientemente robusto para ser desarrollado como prototipo académico.

En consecuencia, esta solución constituye una base sólida para el diplomado, tanto por su valor técnico como por su relevancia social e institucional, y puede ser presentada como una propuesta seria de transformación digital aplicada a procesos de bienestar universitario.

## 22. Posible estructura de sustentación

Como apoyo adicional, la sustentación del proyecto podría organizarse así:

1. Presentación del problema actual en las tres sedes.
2. Comparación de procesos y limitaciones detectadas.
3. Objetivo y alcance del sistema propuesto.
4. Descripción de módulos y flujo del sistema.
5. Explicación del algoritmo de reasignación.
6. Arquitectura y tecnologías seleccionadas.
7. Demostración del prototipo.
8. Beneficios, conclusiones y trabajo futuro.

## 23. Trabajo futuro

Si en una fase posterior se quisiera fortalecer la solución, podrían incorporarse mejoras como:

- Notificaciones automáticas por correo o mensajería.
- Integración con sistemas institucionales de estudiantes.
- Códigos QR para confirmación de entrega.
- Paneles estadísticos más avanzados.
- Reglas de priorización basadas en puntajes socioeconómicos.

Estas extensiones demuestran que el prototipo puede evolucionar hacia una solución institucional de mayor alcance.
