<!-- Fuente: II3 Construir con calidad.pdf -->
<!-- Convertido: 2026-10-11T19:46:06 -->

Construir con calidad
Aseguramiento de la calidad del software
Unidad temática II Tema 3
Ing. Ernesto Suárez

Introducción
Se aborda el tema 3 de la unidad temática II del programa de aseguramiento
de la calidad del software y los estándares que lo respaldan.
• Introducción de construcción con calidad.
• Principios fundamentales.
• Técnicas de programación.
• Principios SOLID.
• Patrones de diseño.
• MVC.
• Herramientas tecnológicas.
• Métricas y monitoreo.
• Conclusiones.

Construcción con Calidad
en Desarrollo de Software: Introducción
Definición
Importancia
Construir con calidad
implica desarrollar
Relación con los defectos
| software que cumple con     | Asegurar calidad durante  |     |
| --------------------------- | ------------------------- | --- |
| los requisitos funcionales  | la construcción reduce    |     |
Impacto en el ciclo de vida
| y no funcionales,       | costos posteriores de  | Muchas fallas en      |
| ----------------------- | ---------------------- | --------------------- |
| mediante prácticas que  | corrección, mejora la  | software se originan  |
garantizan la correcta  mantenibilidad y facilita  durante la construcción  La calidad en
| implementación,  | la entrega continua de  | debido a malas prácticas  |
| ---------------- | ----------------------- | ------------------------- |
construcción ayuda a
| minimizando defectos  | valor al usuario. |     |
| --------------------- | ----------------- | --- |
de codificación o falta de  acelerar las pruebas
desde la etapa de
controles, por lo que la
y despliegues,
codificación.
calidad en esta fase es
optimizando todo el
crítica.
ciclo de desarrollo y
mejorando la
satisfacción del
cliente final.

Construir con calidad:
Principios fundamentales
Inspecciones periódicas y Aplicar guías y
herramientas convenciones claras que
automáticas que promuevan código
detectan errores y legible, consistente y
vulnerabilidades antes mantenible.
de la integración.
Revisiones de Estándares de
Código y Codificación y
Análisis Buenas
Estático Prácticas
Control de
Pruebas
Versiones y
Unitarias y
Gestión de
Automatizadas
Configuración
•Organización •Validación continua de
estructurada de componentes para
cambios y versiones asegurar que cada parte
para evitar conflictos y funcione
pérdidas de correctamente.
información.

Construir con calidad:
Técnicas de programación
Refactorización Continua: Patrones de Diseño:
Principios SOLID:
Programación Defensiva:
Mejorar el diseño del Soluciones reutilizables para
Conjunto de principios para
Escribir código teniendo en
código sin cambiar su problemas comunes que
diseñar software modular,
cuenta posibles errores o
funcionalidad para promueven estructuras de
flexible y fácil de mantener.
entradas incorrectas para
mantenerlo limpio y código robustas y
evitar fallas.
eficiente. escalables.

Principios SOLID
S -Principio de
Responsabilidad Única:
Cada módulo o clase debe
tener una sola razón para
cambiar, enfocándose en una
única responsabilidad.
D -Principio de Inversión de
O -Principio
Dependencias:
Abierto/Cerrado:
Los módulos de alto nivel no
Los módulos deben estar
deben depender de módulos
abiertos para extensión pero
de bajo nivel, ambos deben
cerrados para modificación.
depender de abstracciones.
I -Principio de Segregación L -Principio de Sustitución
de Interfaces: de Liskov:
Las interfaces deben ser Las subclases deben ser
específicas y no generalistas sustituibles por sus clases
para evitar métodos base sin alterar el
innecesarios. funcionamiento.

Patrones de Comportamiento (Ejemplos)
Patrones Creacionales (Ejemplos)
Patrones Estructurales (Ejemplos)
•Observer:
•Singleton:
•Adapter:
Define una dependencia de uno a muchos,
| Patrones de diseño |     |     |     |     | Asegura que una clase tenga una única  |     |     |     |     |     |     |
| ------------------ | --- | --- | --- | --- | -------------------------------------- | --- | --- | --- | --- | --- | --- |
Permite que dos interfaces
para que cuando un sujeto cambie, sus
instancia y proporciona un punto global
incompatibles trabajen juntas
observadores sean notificados
de acceso a ella.
adaptando una interfaz a otra
automáticamente.
|     |     |     |     |     | Ejemplo típico: |     |     |     | Gestión única de  |     |     |
| --- | --- | --- | --- | --- | --------------- | --- | --- | --- | ----------------- | --- | --- |
esperada.
|     |     |     |     | Ejem | p   | l o  t | í p i co | : S i s te | m as  d e  e | v e n to | s  y   |
| --- | --- | --- | --- | ---- | --- | ------ | -------- | ---------- | ------------ | -------- | ------ |
•Beneficios: c o n e x i ó n  a   b a s e  de  d a to s  o   re g is tr o de
|     |     |     |     |     | Ejemplo típico: |     |     | Adaptar una API antigua  |     |     |     |
| --- | --- | --- | --- | --- | --------------- | --- | --- | ------------------------ | --- | --- | --- |
• Facilitan la  noti l f o ic g a s c . iones en interfaces gráficas.
para que funcione con una nueva.
| comunicación entre  |     |     |     | •Stra | t   | e g y : |            |     |     |     |     |
| ------------------- | --- | --- | --- | ----- | --- | ------- | ---------- | --- | --- | --- | --- |
|                     |     |     |     |       | • F | a c to  | ry Method: |     |     |     |     |
•Decorator:
|     |     |     |     | Perm |     | i te   d | e f in | i r   u n a |  f a m ili a   d | e  a l g o | ri tm os  |
| --- | --- | --- | --- | ---- | --- | -------- | ------ | ----------- | ---------------- | ---------- | --------- |
desarrolladores D e fi n e   u n a   i n te r f a z p a r a   cr e a r  u n
Añade responsabilidades adicionales a
• Mejoran la  inter o c b a j m et b o i , a  p b e le ro s    q p u e e rm  p i u te e   d q e u n e     c l a a m s s b u ia b r c s la e s  e e n s
un objeto de forma dinámica sin alterar
| escalabilidad y  |     |                |     | tiem | p   | o   d e |   e j e | cu c ió   | n .             |     |     |
| ---------------- | --- | -------------- | --- | ---- | --- | ------- | ------- | --------- | --------------- | --- | --- |
|                  |     | Creacionales:  |     |      | d   | e c i d | a n   q | u é  c la | s e instanciar. |     |     |
su estructura.
|     |     | Singleton, Factory,  |     | Ejem | p   | lo  t | íp ic o | : M ú l | ti p le s   e s | t r a te g i a | s   d e   |
| --- | --- | -------------------- | --- | ---- | --- | ----- | ------- | ------- | --------------- | -------------- | --------- |
flexibilidad E je m p lo  t íp i co : C r e a c i ó n   d e  d i f e r e n t es
|     |     | Builder |     |      | Ejemplo típico: |       |         | Añadir funcionalidades  |             |               |                |
| --- | --- | ------- | --- | ---- | --------------- | ----- | ------- | ----------------------- | ----------- | ------------- | -------------- |
|     |     |         |     | orde | n               | a m i | e n t o |  q u e  p               | u e d e n   | a p l ic a rs | e   s e g ú n  |
• Reducen la  t ip o s  d e   p e rs o n a je s  e n   u n   v id e o j u e g o
a componentes gráficos en tiempo de
| complejidad y  |     |             |     | la sit | u    | a c ió | n .                    |     |     |     |     |
| -------------- | --- | ----------- | --- | ------ | ---- | ------ | ---------------------- | --- | --- | --- | --- |
|                |     | Soluciones  |     |        | s in |   m    | o d ificar el cliente. |     |     |     |     |
ejecución.
probadas y
|     |     |     |     | •Com |     | m a n | d : |     |     |     |     |
| --- | --- | --- | --- | ---- | --- | ----- | --- | --- | --- | --- | --- |
duplicación de código reutilizables para  •A b st r a ct Factory:
•Facade:
|     |     | problemas  |     | Encapsula una petición como un objeto,  |     |     |     |     |     |     |     |
| --- | --- | ---------- | --- | --------------------------------------- | --- | --- | --- | --- | --- | --- | --- |
Proporciona una interfaz para crear
comunes en el
Proporciona una interfaz unificada y
diseño de
permitiendo parametrizar clientes con
|     |     | software. |     |     | familias de objetos relacionados sin  |     |     |     |     |     |     |
| --- | --- | --------- | --- | --- | ------------------------------------- | --- | --- | --- | --- | --- | --- |
sencilla a un conjunto complejo de
diferentes solicitudes, incluyendo
especificar sus clases concretas.
interfaces dentro de un subsistema.
operaciones deshacer.
|     | De  |     | Estructurales:  |     | Ejemplo típico: |     |     |     | Sistemas que deben  |     |     |
| --- | --- | --- | --------------- | --- | --------------- | --- | --- | --- | ------------------- | --- | --- |
comportamiento:  Adapter,  Ejemplo típico: Simplificar el acceso a
Observer, Strategy,  Composite,  Ejemplo típico: Implementación de barras
funcionar con distintas plataformas
|     | Command |     | Decorator |     | un sistema complejo como un motor  |     |     |     |     |     |     |
| --- | ------- | --- | --------- | --- | ---------------------------------- | --- | --- | --- | --- | --- | --- |
de herramientas con comandos
gráficas, produciendo conjuntos
gráfico.
deshacer/rehacer.
compatibles de botones, menús, etc.

La separación clara entre lógica de negocio (Modelo), presentación (Vista)
y gestión de eventos (Controlador) facilita el mantenimiento, la
MVC
escalabilidad y la colaboración en equipos de desarrollo. Además, MVC es
la base para otros patrones relacionados como MVP (Modelo-Vista-
Presentador) y MVVM (Modelo-Vista-Modelo de Vista).
| Modelo  |               | Vista |           | Controlador |              |
| ------- | ------------- | ----- | --------- | ----------- | ------------ |
| Modelo  | Vista (View): |       | Presenta  |             | Controlador  |
(Model): Gestiona los  los datos al usuario y  (Controller): Recibe las
datos y la lógica de  define la interfaz gráfica  entradas del usuario
| negocio.                 |     | o visual.  |     |                           | (eventos),  |
| ------------------------ | --- | ---------- | --- | ------------------------- | ----------- |
| Se encarga de acceder a  |     |            |     | las procesa y traduce en  |             |
Muestra el estado del
| la información,  |     |     |     | acciones que pueden  |     |
| ---------------- | --- | --- | --- | -------------------- | --- |
modelo y recibe la
| actualizarla y notificar  |     |     |     | actualizar el modelo o  |     |
| ------------------------- | --- | --- | --- | ----------------------- | --- |
interacción del usuario.
| cambios a la vista. |     |     |     |     | cambiar la vista. |
| ------------------- | --- | --- | --- | --- | ----------------- |

Calidad de la construcción:
Herramientas tecnológicas
Integración Análisis Estático
Continua (CI): y Dinámico
Herramientas que
Automatiza la evalúan el código sin
compilación, pruebas ejecutarlo (análisis
e integración estático) o durante su
frecuente del código ejecución (dinámico)
para detectar errores para identificar
temprano. vulnerabilidades y
defectos.
Software con soporte
Scripts y herramientas
para depuración,
que permiten ejecutar
refactorización,
pruebas y desplegar
análisis y pruebas que
aplicaciones de forma
facilita la codificación
rápida y repetible.
de calidad.
Entornos de Automatización
Desarrollo de Pruebas y
Integrados Despliegues
(IDE)

Calidad en construcción:
Métricas y monitoreo
Porcentaje de código Medida de la Número de defectos Visualización del estado Evaluación constante
fuente ejecutado complejidad del encontrados por de calidad para de métricas para
durante pruebas. código basada en tamaño o módulo de seguimiento y toma ajustar procesos y
caminos de ejecución, código. de decisiones. mantener calidad.
impacto en
mantenibilidad.
Dashboards y
Cobertura de Complejidad Densidad de Indicadores para
Reportes
Código Ciclomática Defectos Mejora Continua
Automáticos:

Conclusiones
• Construir con calidad requiere combinación de buenas prácticas,
herramientas y cultura organizacional.
• La automatización y el monitoreo son claves para mantener calidad
constante.
• Recomendar formación continua e integración de procesos en
equipos de desarrollo.

Referencias
Duvall, P. M., Matyas, S., & Glover, A. (2007). Continuous Integration: Improving
Software Quality and Reducing Risk. Addison-Wesley.
Fenton, N., & Pfleeger, S. L. (1997). Software Metrics: A Rigorous and Practical
Approach (2nd ed.). PWS Publishing.
Fowler, M. (2018). Refactoring: Improving the Design of Existing Code (2nd ed.).
Addison-Wesley.
Gamma, E., Helm, R., Johnson, R., & Vlissides, J. (1994). Design Patterns: Elements of
Reusable Object-Oriented Software. Addison-Wesley.
Laporte, C., & April, A. (2018). Software quality assurance. John Wiley and Sons.
Martin, R. C. (2003). Agile Software Development, Principles, Patterns, and Practices.
Prentice Hall.
McConnell, S. (2004). Code Complete (2nd ed.). Microsoft Press.
Pressman, R. S. (2014). Software Engineering: A Practitioner's Approach (8th ed.).
McGraw-Hill Education.
Sommerville, I. (2011). Software Engineering (9th ed.). Pearson.