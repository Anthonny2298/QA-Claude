<!-- Fuente: DAS Agil (ReactJS) Equipo 60 3.pdf -->
<!-- Convertido: 2026-10-11T19:46:58 -->

<Corpomotriz Los Salias>
Documento de Arquitectura de Software
Versión 1.3.2

Documento de Arquitectura de Software Versión: 1.3.2
Corpomotriz Los Salias Fecha: 17/06/2025
DAS
Historia de Revisiones
Fecha Versión Descripción Autor
05/06/2025 1.0 Se indicaron las restricciones de diseño, Alejandra Teixeira,
características de la arquitectura y
Edgar Paz,
decisiones arquitectónicas.
Javier Delmoral,
Leonardo García
11/06/2025 1.1 Se indicó la lista de archivo por componente Alejandra Teixeira,
e interfaces de usuario.
Edgar Paz,
Javier Delmoral,
Leonardo García
12/06/2025 1.2 Se indicó el modelo de dominio. Alejandra Teixeira,
Edgar Paz,
Javier Delmoral,
Leonardo García
14/06/2025 1.3 Se agregaron los enlaces relacionados a la Alejandra Teixeira,
visualización de diagrama de componentes,
Edgar Paz,
árbol de Componentes y diagrama de
clases. Javier Delmoral,
Leonardo García
15/06/2025 1.3.1 Se modificaron detalles menores en el árbol Alejandra Teixeira,
de componentes y diagrama de clases, así
Edgar Paz,
como el formato de los enlaces y las tablas.
Javier Delmoral,
Leonardo García
17/06/2025 1.3.2 Se modificó el árbol de componentes y su Alejandra Teixeira,
respectiva tabla.
Edgar Paz,
Javier Delmoral,
Leonardo García
Confidencial Página 2 de 16
©UCAB, 2022

Documento de Arquitectura de Software Versión: 1.3.2
Corpomotriz Los Salias Fecha: 17/06/2025
DAS
Tabla de Contenido
1. Parte I 4
1.1 Restricciones de Diseño. 4
1.2 Modelo de Dominio 4
1.3 Características de la Arquitectura 4
1.4 Decisiones Arquitectónicas 4
1.5 Estructura de Componentes 4
1.5.1 Diagrama de Contexto 5
1.5.2 Diagrama de Contenedores 5
1.5.3 Diagrama de Componentes 5
2. Parte II 5
2.1 Sprint 1 5
2.1.1 Vista de Datos 5
2.1.2 Diagrama de clases 5
2.1.3 Lista de Archivos por componentes 5
2.1.4 Interfaces de Usuario 5
2.2 Sprint 2… 5
Confidencial Página 3 de 16
©UCAB, 2022

Documento de Arquitectura de Software Versión: 1.3.2
Corpomotriz Los Salias Fecha: 17/06/2025
DAS
Documento de Arquitectura de Software
Este documento proporciona una descripción arquitectónica del sistema Corpomotriz Los Salias, consta de dos
partes, la realizada por el arquitecto de software y la realizada por el desarrollador. Esta última será en función de
los Sprint.
1. Parte I
[La elabora el Arquitecto con base a las ideas propuestas en una sesión colaborativa con el equipo de
desarrollo realizada al inicio del proceso, se le harán todas las modificaciones que el Arquitecto considere
en el transcurso de las diferentes Sprint.]
1.1 Restricciones de Diseño.
Ambiente de Desarrollo y Producción:
- Todos los desarrolladores de este proyecto deben configurar un entorno de desarrollo local que
incluya NodeJS (Para Angular) y Java 17+ (Para Spring Boot).
- La aplicación debe ser desplegada en un servidor que soporte backend en Java y permite correr
aplicaciones Spring Boot.
Herramientas de Desarrollo:
- Git será utilizado para el control de versiones.
- Se utilizará GitHub para el almacenamiento del código.
- NPM (Node Package Manager) se utilizará para la gestión de dependencias en el proyecto de
Angular.
- Para Spring Boot (Java), se utilizará un archivo application.properties para el manejo de
configuraciones para la comunicación con la base de datos.
- Se utilizará IntelliJ IDEA Ultimate como IDE para el principal desarrollo de Java/Spring Boot. La
gestión de dependencias del backend se realizará a través de Maven.
- Se utilizará Postman para pruebas y validación de los endpoints REST
Estándares de codificación: Se mantendrá una estricta adherencia a las guías de estilo específicas de cada
tecnología para asegurar la consistencia, legibilidad y calidad del código en todo el proyecto. Para el
código del frontend, se utilizará la sintaxis de TypeScript y se seguirán las guías de estilo de Angular,
empleando Prettier para el formateo automático. En el backend, se seguirán las convenciones de código
estándar de Java, aplicando las reglas de formateo estándar.
Interfaz de usuario: La interfaz gráfica del usuario se desarrollará utilizando Angular y la biblioteca de
estilos Bootstrap 5, para asegurar una experiencia moderna y accesible. Se mantendrá coherencia visual
mediante una paleta de colores institucional y se priorizará la usabilidad.
Patrón de arquitectura: Se utilizará el modelo MVC (Model-View-Controller) como patrón de diseño del
Confidencial Página 4 de 16
©UCAB, 2022

Documento de Arquitectura de Software Versión: 1.3.2
Corpomotriz Los Salias Fecha: 17/06/2025
DAS
software.
Comunicación entre Front-End y Back-End: El Front-End (Angular) se comunicara con el Back-End a través
de una API RESTful. El Back-End (Spring Boot) implementará esta API, y todas sus respuestas están en
formato JSON.
Autenticación: La autenticación de usuarios se gestionará directamente mediante un sistema de correo
electrónico y contraseña. Cuando un usuario intente iniciar sesión, el back-end (Spring Boot) recibirá
estas credenciales y validará contra los datos almacenados en la base de datos MySQL.
Base de Datos: Como gestor de base de datos utilizaremos MySQL.
1.2 Modelo de Dominio
Confidencial Página 5 de 16
©UCAB, 2022

Documento de Arquitectura de Software Versión: 1.3.2
Corpomotriz Los Salias Fecha: 17/06/2025
DAS
1.3 Características de la Arquitectura
Rendimiento: El sistema está diseñado para manejar múltiples usuarios de manera concurrente,
aprovechando la eficiencia del framework Angular en el frontend, que permite renderizado rápido del
DOM, y la capacidad de Spring Boot en el backend, que soporta múltiples hilos de ejecución y manejo de
peticiones simultáneas mediante su motor embebido Tomcat.
Robustez: La arquitectura desacoplada, estructurada en capas (presentación, lógica de negocio y
persistencia), permite minimizar el impacto de fallos en componentes individuales. Se emplean
mecanismos de validación, manejo de excepciones y control de errores para fortalecer la fiabilidad del
sistema.
Mantenibilidad: La mantenibilidad se garantiza mediante:
- Separación clara por capas (Controller, Service, Repository)
- Uso de DTOs para desacoplar el modelo de datos del modelo de presentación.
- Aplicación de estándares de codificación.
- Modularización del frontend y backend, permitiendo realizar mejoras, actualizaciones o
refactorizaciones sin afectar el resto del sistema.
Autenticación: El sistema implementa un mecanismo de autenticación mediante correo electrónico y
contraseña, validando las credenciales del usuario contra registros almacenados en MySQL.
Seguridad: La comunicación entre el front-end y el back-end se lleva a cabo mediante una API RESTful, lo
que garantiza la seguridad en la red con el cliente.
1.4 Decisiones Arquitectónicas
ID Fecha Descripción Justificación
1 18/05/2025 Estilo arquitectónico en Se adopta el modelo de capas para separar
capas la lógica de presentación, negocio y
persistencia, facilitando la mantenibilidad y
escalabilidad.
2 19/05/2025 Implementación del Se implementa el modelo MVC para separar
patrón arquitectónico cada mayor mantenibilidad y modularidad
MVC del software.
(Model-View-Controller)
3 20/05/2025 Framework Frontend: Angular permite crear interfaces
Angular modulares, responsivas y altamente
mantenibles, además de integración fluida
con servicios REST.
Confidencial Página 6 de 16
©UCAB, 2022

Documento de Arquitectura de Software Versión: 1.3.2
Corpomotriz Los Salias Fecha: 17/06/2025
DAS
4 21/05/2025 Framework Backend: Spring Boot permite una arquitectura
Spring Boot modular, configuración automática, soporte
REST y manejo eficiente de dependencias.
5 22/05/2025 Gestor de base de datos: Se utilizó MySQL debido a su estabilidad,
MySQL su sólido soporte para la integridad
referencial y su compatibilidad con
tecnologías como JPA/Hibernate.
5 23/05/2025 Control de versiones con Se implementa Git para seguimiento de
Git/GitHub cambios y colaboración distribuida
mediante GitHub.
6 23/05/2025 API RESTful para Se implementa una API RESTful para
comunicación desacoplar el frontend del backend,
facilitando la escalabilidad y la
interoperabilidad.
7 24/05/2025 Manejo de dependencias Se utilizan Maven y NPM para automatizar
con Maven/NPM la gestión de bibliotecas y mantener
entornos coherentes.
1.5 Estructura de Componentes
[Describe en forma de diagrama cuales son los componentes que conforman la aplicación, se utilizará el
Modelo C 4, para representar los tres niveles se emplea la notación de Diagramas de Clases, pero para este
caso estereotipadas, cada nivel de un color diferente]
1.5.1 Diagrama de Contexto
1.5.2 Diagrama de Contenedores
1.5.3 Diagrama de Componentes
ESTCOMP Corpomotriz Los Salias.png
2. Parte II
[La elabora el Desarrollador y se ira modificando por cada Sprint que se desarrolle.]
2.1 Sprint 1
[Se describe nombre de la(s) Historia(s) de Usuario desarrolladas en este Sprint.]
● Añadir Proveedores
● Consultar Proveedores
● Insertar Producto
● Consultar Producto
● Crear Perfil
● Examinar Perfil
● Registrar Pago
● Modificar Pago
Confidencial Página 7 de 16
©UCAB, 2022

Documento de Arquitectura de Software Versión: 1.3.2
Corpomotriz Los Salias Fecha: 17/06/2025
DAS
2.1.1 Vista de Datos
[Esta vista consiste en una descripción de la perspectiva del almacenamiento de datos persistentes para
este Sprint. Esta vista se conforma por el Modelo Entidad-Relación para el caso de Bases de Datos
Relacionales, en caso de no serlo puede utilizar cualquier otro gráfico].
2.1.2 Diagrama de clases
DCLSSver2 Corpomotriz Los Salias.png
2.1.3 “Arbol” de Componentes del Frontend
ARBCver4 Corpomotriz Los Salias.png
[Diagrama el árbol, cada nodo será un componente de interfaz. Para cada componente que se haya
desarrollado en este Sprint se debe especificar el(os) archivo(s) que lo componen. Se sugiere la siguiente
tabla.]
Nombre del Componente Lista de archivos
Navbar login.component.html
[Navlink (Productos)] perfil.component.html
[Navlink (Proveedores)] lista-usuario.component.html
producto-lista.component.html
[Navlink (Pago)]
agregar-producto.component.html
[Botón (Cerrar sesión)]
producto-detalle.component.html
[Botón (Perfil)]
pagos-lista.component.html
pagos-registrar.component.html
proveedores-lista.component.html
proveedores-detalle.component.html
productos-proveedor.component.html
proveedores-agregar.component.html
registro.component.html
navbar.component.html
Lista (Perfil) perfil.component.html
[Botón (Examinar perfil de usuario)]
Formulario (Registro) registro.component.html
[Botón (Confirmar)]
Formulario (Login) login.component.html
[Botón (Confirmar)]
Tabla (Usuarios Registrados) lista-usuario.component.html
Formulario (Agregar Producto) agregar-producto.component.html
[Botón (Confirmar)]
Formulario de Selección (Marca) producto-lista.component.html
Placeholder (Precio máximo) producto-lista.component.html
Tabla de Productos (Registrados) producto-lista.component.html
[Botón (Ver detalles)]
Botón (Insertar producto) producto-lista.component.html
Placeholder (Cantidad Mínima) producto-lista.component.html
Confidencial Página 8 de 16
©UCAB, 2022

Documento de Arquitectura de Software
  Versión:           1.3.2

| Corpomotriz Los Salias  |     |     |     |   Fecha:  17/06/2025  |     |
| ----------------------- | --- | --- | --- | --------------------- | --- |
DAS

Lista (Detalles del proveedor)  producto-detalle.component.html
Botón (Registrar Nuevo Pago)  producto-detalle.component.html
Lista (Detalles del producto)  producto-detalle.component.html
|     | Botón (Volver)  |     |     | producto-detalle.component.html  |     |
| --- | --------------- | --- | --- | -------------------------------- | --- |
productos-proveedor.component.html
|     | Placeholder (Monto mínimo)  |     |     | pagos-lista.component.html  |     |
| --- | --------------------------- | --- | --- | --------------------------- | --- |
Formulario de Selección (Estados de Pago)  pagos-lista.component.html
| Botón (Registrar Nuevo Pago)  |                            |     |     | pagos-lista.component.html  |     |
| ----------------------------- | -------------------------- | --- | --- | --------------------------- | --- |
|                               | Tabla (Pagos registrados)  |     |     | pagos-lista.component.html  |     |
[Botón (Modificar Pago)]
|     | Formulario (Registrar Pago)  |     |     | pagos-registrar.component.html  |     |
| --- | ---------------------------- | --- | --- | ------------------------------- | --- |
[Botón (Agregar Producto)]
[Botón (Cancelar)]
Formulario (Agregar Proveedor)  proveedores-agregar.component.html
[Botón (Confirmar)]
Botón (Ver productos ofrecidos)  proveedores-detalle.component.html
Lista (Detalles del producto)  proveedores-detalle.component.html
Botón (Agregar Proveedores)  proveedores-lista.component.html
Tabla (Proveedores Agregados)  proveedores-lista.component.html
[Botón (Ver detalles)]

2.1.4  Lista de Archivos por componentes

Front-End
| Nombre del Supra Componente  |     | Nombre del Componente  |           | Lista de archivos   |                      |
| ---------------------------- | --- | ---------------------- | --------- | ------------------- | -------------------- |
|                              |     |                        |           |                     | auth.service.ts      |
|                              |     |                        |           |                     | pago.service.ts      |
|                              |     |                        | services  |                     | producto.service.ts  |
proveedor.service.ts
usuario.service.ts
|     |     |     |        |     | pagos.ts     |
| --- | --- | --- | ------ | --- | ------------ |
|     |     |     | model  |     | producto.ts  |
proveedor.ts
usuario.ts
|     |     |     | interceptors  |     | auth.interceptor.ts  |
| --- | --- | --- | ------------- | --- | -------------------- |
|     |     |     | guard         |     | auth.guard.ts        |
role.guard.ts
|     |     |     | agregar-producto  | agregar-producto.component.html  |     |
| --- | --- | --- | ----------------- | -------------------------------- | --- |

Confidencial  Página 9 de 16
©UCAB, 2022

Documento de Arquitectura de Software
  Versión:           1.3.2

Corpomotriz Los Salias    Fecha:  17/06/2025
DAS

|     |                | agregar-producto.component.ts  |
| --- | -------------- | ------------------------------ |
|     | lista-usuario  | lista-usuario.component.html   |

lista-usuario.component.ts
|     | login  | login.component.html  |
| --- | ------ | --------------------- |

login.component.css
|     |     | login.component.ts  |
| --- | --- | ------------------- |

|     | navbar  | navbar.component.html  |
| --- | ------- | ---------------------- |
|     |         | navbar.component.css   |

navbar.component.ts
|     | pagos-lista  | pagos-lista.component.html  |
| --- | ------------ | --------------------------- |

pagos-lista.component.ts

|     | pagos-registrar  | pagos-registrar.component.html  |
| --- | ---------------- | ------------------------------- |

pagos-registrar.component.ts
components
|     | perfil  | perfil.component.html  |
| --- | ------- | ---------------------- |
perfil.component.ts
|     | producto-detalle  | producto-detalle.component.html  |
| --- | ----------------- | -------------------------------- |
producto-detalle.component.ts
|     | producto-lista  | producto-lista.component.html  |
| --- | --------------- | ------------------------------ |
producto-lista.component.ts
|     | productos-proveedor  | productos-proveedor.component.html  |
| --- | -------------------- | ----------------------------------- |
productos-proveedor.component.ts
|     | proveedores-agregar  | proveedores-agregar.component.html  |
| --- | -------------------- | ----------------------------------- |
proveedores-agregar.component.ts
|     | proveedores-detalle  | proveedores-detalle.component.html  |
| --- | -------------------- | ----------------------------------- |
proveedores-detalle.component.ts
|     | proveedores-lista  | proveedores-lista.component.html  |
| --- | ------------------ | --------------------------------- |
proveedores-lista.component.ts
|     | registro  | registro.component.html  |
| --- | --------- | ------------------------ |
registro.component.ts

Back-End
Nombre del Componente  Lista de archivos
  AuthController.java
  PagoController.java
ProductoController.java
controller
ProveedorController.java
UsuarioController.java
  crear/ProductoCrearDTO.java
  crear/ProveedorCrearDTO.java
  crear/UsuarioCrearDTO.java
  request/LoginRequestDTO.java
  request/PagoRequestDTO.java
| dto  | response/LoginResponseDTO.java  |     |
| ---- | ------------------------------- | --- |
response/PagoResponseDTO.java
PagoProductoDTO.java
ProductoDTO.java

Confidencial  Página 10 de 16
©UCAB, 2022

Documento de Arquitectura de Software Versión: 1.3.2
Corpomotriz Los Salias Fecha: 17/06/2025
DAS
ProveedorDTO.java
UsuarioDTO.java
Pago.java
PagoProducto.java
model Producto.java
Proveedor.java
Usuario.java
PagoProductoRepository.java
PagoRepository.java
repository ProductoRepository.java
ProveedorRepository.java
UsuarioRepository.java
iProductoService.java
PagoService.java
service ProductoService.java
ProveedorService.java
UsuarioService.java
2.1.5 Interfaces de Usuario
[Realice una captura de pantalla de las interfaces diseñadas en este Sprint, por cada una indique:
Nombre: Añadir Proveedor
Historia a la que pertenece: Gestionar Proveedores
Diseño de interfaz:
Confidencial Página 11 de 16
©UCAB, 2022

Documento de Arquitectura de Software Versión: 1.3.2
Corpomotriz Los Salias Fecha: 17/06/2025
DAS
Nombre: Consultar Proveedor
Historia a la que pertenece: Gestionar Proveedores
Diseño de interfaz:
Nombre: Insertar Producto
Historia a la que pertenece: Gestionar Productos
Diseño de interfaz:
Confidencial Página 12 de 16
©UCAB, 2022

Documento de Arquitectura de Software Versión: 1.3.2
Corpomotriz Los Salias Fecha: 17/06/2025
DAS
Nombre: Consultar Producto.
Historia a la que pertenece: Gestionar Producto
Diseño de interfaz:
Confidencial Página 13 de 16
©UCAB, 2022

Documento de Arquitectura de Software Versión: 1.3.2
Corpomotriz Los Salias Fecha: 17/06/2025
DAS
Nombre: Crear Perfil
Historia a la que pertenece: Gestionar Perfil
Diseño de interfaz:
Confidencial Página 14 de 16
©UCAB, 2022

Documento de Arquitectura de Software Versión: 1.3.2
Corpomotriz Los Salias Fecha: 17/06/2025
DAS
Nombre: Examinar Perfil
Historia a la que pertenece: Gestionar Perfil
Diseño de interfaz:
Nombre: Registrar Pago
Historia a la que pertenece: Gestionar Pago
Diseño de interfaz:
Confidencial Página 15 de 16
©UCAB, 2022

Documento de Arquitectura de Software Versión: 1.3.2
Corpomotriz Los Salias Fecha: 17/06/2025
DAS
Nombre: Modificar Pago
Historia a la que pertenece: Gestionar Pago
Diseño de interfaz:
2.2 Sprint 2…
Confidencial Página 16 de 16
©UCAB, 2022