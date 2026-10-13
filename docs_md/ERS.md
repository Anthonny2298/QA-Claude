<!-- Fuente: ERS Equipo 60 3.pdf -->
<!-- Convertido: 2026-10-11T19:46:58 -->

Especificación de Requisitos de Software
Corpomotriz Los Salias
Versión 1.0

Especificación de Requisitos de Software    Versión:           1.0
| Corpomotriz Los Salias  |     |     |     |     |   Fecha:  12/05/2025  |     |
| ----------------------- | --- | --- | --- | --- | --------------------- | --- |
ERS

Histórico de Revisiones
| Fecha  | Versión  |     | Descripción  |     |     | Autor(es)  |
| ------ | -------- | --- | ------------ | --- | --- | ---------- |
12/05/2025  1.0  Se agregaron las especificaciones de cada una de  Alejandra Teixeira,
las historias del primer y segundo Sprint, más los
Edgar Paz,
|     |     | requisitos           | suplementarios,  | basándose  | en  el            |     |
| --- | --- | -------------------- | ---------------- | ---------- | ----------------- | --- |
|     |     | estándar ISO 25010.  |                  |            | Javier Delmoral,  |     |
Leonardo García
|     |     |     |     |     |     |     |
| --- | --- | --- | --- | --- | --- | --- |
|     |     |     |     |     |     |     |
|     |     |     |     |     |     |     |

| Confidencial  |     |     | © UCAB, 2024  |     |     | Pág. 2 de 8  |
| ------------- | --- | --- | ------------- | --- | --- | ------------ |

Especificación de Requisitos de Software Versión: 1.0
Corpomotriz Los Salias Fecha: 12/05/2025
ERS
Tabla de Contenidos
1. Sprint 4
1.1 Sprint 1 4
1.1.1 Historia de Usuario “Añadir Proveedores” (Autor: Leonardo García) (Link para el
diagrama de actividades: Click acá): 4
1.1.2 Historia de Usuario “Insertar Producto” (Autor: Edgar Paz) (Link para el diagrama
de actividades: Click acá): 5
1.1.3 Historia de Usuario “Crear Perfil” (Autor: Alejandra Teixeira) (Link para el diagrama
de actividades: Click acá): 6
1.1.4 Historia de Usuario “Registrar Pago” (Autor: Javier Delmoral) (Link para el
diagrama de actividades: Click acá): 7
2. Requisitos suplementarios 7
2.1 Eficiencia de Desempeño 7
2.1.1 Capacidad 7
2.2 Capacidad de Interacción 7
2.2.1 Aprendizabilidad 7
2.3 Fiabilidad 8
2.3.1 Disponibilidad 8
2.4 Seguridad 8
2.4.1 Confidencialidad 8
Confidencial © UCAB, 2024 Pág. 3 de 8

Especificación de Requisitos de Software    Versión:           1.0
| Corpomotriz Los Salias  |     |     |     |     |   Fecha:  12/05/2025  |     |     |
| ----------------------- | --- | --- | --- | --- | --------------------- | --- | --- |
ERS

Especificación de Requisitos de Software
Corpomotriz Los Salias

Este artefacto detalla los requisitos de software para el Sistema Corpomotriz Los Salias, según
dos grandes aspectos claves para su desarrollo: Las Historias de Usuario en cada Sprint con su
especificación según el modelo Canvas, y las Especificaciones Suplementarias. Toda esta
información establece los lineamientos y las restricciones que debe considerar el equipo de
desarrollo del proyecto para el desarrollo del sistema.

1.  Sprint

1.1  Sprint 1

1.  Añadir Proveedores
2.  Consultar Proveedores
3.  Insertar Producto
4.  Consultar Producto
5.  Crear Perfil
6.  Examinar Perfil
7.  Registrar Pago
8.  Modificar Pago

1.1.1  Historia de Usuario “Añadir Proveedores” (Autor: Leonardo García) (Link para el diagrama de actividades:
Click acá):

|     | Añadir Proveedores  | Conversación  |     |     | Criterios de Aceptación  |     |     |
| --- | ------------------- | ------------- | --- | --- | ------------------------ | --- | --- |
Como  Administrador  quiero  Épica: Gestionar proveedores  El  administrador  poseerá  la
añadir  proveedores  al  negocio  capacidad de ingresar todos los
|     |     | Escenario  | de  uso:  | El  |     |     |     |
| --- | --- | ---------- | --------- | --- | --- | --- | --- |
con la finalidad de abastecer mi  datos  correspondientes  a  los
|     |              | administrador                  | accede             | a  su  |                             |                  |     |
| --- | ------------ | ------------------------------ | ------------------ | ------ | --------------------------- | ---------------- | --- |
|     | inventario.  |                                |                    |        | proveedores en el sistema:  |                  |     |
|     |              | cuenta  y                      | registra  un       | nuevo  |                             |                  |     |
|     |              | proveedor                      | para  el  negocio  |        | ●  Datos                    | de  la  empresa  |     |
|     |              | añadiendo                      | nombre  de         | la     | (Nombre,                    | localización,    |     |
|     |              | empresa,                       | localización,      |        | especialización)            |                  |     |
|     |              | especialización,               | productos          |        | ●  Productos                | que ofrece y     |     |
|     |              | ofrecidos con sus respectivos  |                    |        | sus precios.                |                  |     |
|     |              | precios, plazos de entrega de  |                    |        | ●  Plazos                   | de  Entrega      | de  |
|     |              | mercancía y fecha de contrato  |                    |        | mercancía.                  |                  |     |
|     |              | (Datos de proveedores).        |                    |        | ●  Fecha de contrato.       |                  |     |
|     |              | Reglas de negocio:             |                    |        |                             |                  |     |
|     |              | ●                              | El  proveedor      | debe   |                             |                  |     |
|     |              |                                | coincidir  con     | el     |                             |                  |     |

| Confidencial  |     | © UCAB, 2024  |     |     |     | Pág. 4 de 8  |     |
| ------------- | --- | ------------- | --- | --- | --- | ------------ | --- |

Especificación de Requisitos de Software    Versión:           1.0
| Corpomotriz Los Salias  |     |     |     |     |     |     |     |     |   Fecha:  12/05/2025  |     |
| ----------------------- | --- | --- | --- | --- | --- | --- | --- | --- | --------------------- | --- |
ERS

|     |     |     |     |     | nombre  |     | de  | la  |     |     |
| --- | --- | --- | --- | --- | ------- | --- | --- | --- | --- | --- |

empresa del mismo.
|     |     |     |     |     | ●  Todos  |     | los  campos  |     |     |     |
| --- | --- | --- | --- | --- | --------- | --- | ------------ | --- | --- | --- |

deben ser rellenados.
|     |     |     |     |     | ●  No  | se  | permiten  |     |     |     |
| --- | --- | --- | --- | --- | ------ | --- | --------- | --- | --- | --- |
proveedores

duplicados.

|     |     |     |     | Alcance: Accesible sólo a los  |     |     |     |     |     |     |
| --- | --- | --- | --- | ------------------------------ | --- | --- | --- | --- | --- | --- |
usuarios autenticados con rol
de Administrador.
|     |     |     |     | Dependencias:  |     | Existencia  |     | de  |     |     |
| --- | --- | --- | --- | -------------- | --- | ----------- | --- | --- | --- | --- |
un  proveedor con el que se
negocia.
1.1.2  Historia de Usuario “Insertar Producto” (Autor: Edgar Paz) (Link para el diagrama de actividades: Click
acá):

|     | Insertar Producto  |     |     |     | Conversación  |     |     |     | Criterios de Aceptación  |     |
| --- | ------------------ | --- | --- | --- | ------------- | --- | --- | --- | ------------------------ | --- |

Como  Administrador,  quiero  Épica: Gestionar Producto  ●  El  inventario  se  debe

|     | insertar                            | productos    | en  | el             |     |           |       |        | actualizar                 | con  cada  |
| --- | ----------------------------------- | ------------ | --- | -------------- | --- | --------- | ----- | ------ | -------------------------- | ---------- |
|     |                                     |              |     | Escenario      |     | de        | uso:  | El     |                            |            |
|     | inventario, para dar a conocer los  |              |     |                |     |           |       |        | inserción.                 |            |
|     |                                     |              |     | administrador  |     | accede    |       | a  su  |                            |            |
|     | productos                           | disponibles  | en  | el             |     |           |       |        | ●  Se  debe poder agregar  |            |
|     |                                     |              |     | cuenta         | y   | registra  | un    | nuevo  |                            |            |

catálogo a los clientes, y que los  detalles a cada producto.
|     |                            |     |     | producto   |     | en       | el  catálogo,  |     |                         |          |
| --- | -------------------------- | --- | --- | ---------- | --- | -------- | -------------- | --- | ----------------------- | -------- |
|     | mismos puedan comprarlos.  |     |     |            |     |          |                |     | ●  Los  productos       | iguales  |
|     |                            |     |     | indicando  |     | nombre,  | precio         | y   |                         |          |
|     |                            |     |     |            |     |          |                |     | deben estar agrupados,  |          |
detalles y descripción de cada
|     |     |     |     |     |     |     |     |     | actualizando la cantidad  |     |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | ------------------------- | --- |
producto.
disponible.

Reglas de negocio:
|     |     |     |     |     |        |           |     |       |     |     |
| --- | --- | --- | --- | --- | ------ | --------- | --- | ----- | --- | --- |
|     |     |     |     |     | ●  El  | producto  |     | debe  |     |     |

|     |     |     |     |     | tener       |         | un  nombre  |         |     |     |
| --- | --- | --- | --- | --- | ----------- | ------- | ----------- | ------- | --- | --- |
|     |     |     |     |     | único       | dentro  |             | de  la  |     |     |
|     |     |     |     |     | categoría.  |         |             |         |     |     |
●  La cantidad debe ser

mayor a cero.

●  El precio del producto

|     |     |     |     |     | debe  | ser  | mayor  | a   |     |     |
| --- | --- | --- | --- | --- | ----- | ---- | ------ | --- | --- | --- |

cero.

Alcance: Accesible sólo a los

usuarios autenticados con rol

de Administrador.

|     |     |     |     | Dependencias:  |     | Existencia  |     | de  |     |     |
| --- | --- | --- | --- | -------------- | --- | ----------- | --- | --- | --- | --- |

|     |     |     |     | un  | catálogo  | de  | productos  |     |     |     |
| --- | --- | --- | --- | --- | --------- | --- | ---------- | --- | --- | --- |

(inventario).

| Confidencial  |     |     |     |     | © UCAB, 2024  |     |     |     |     | Pág. 5 de 8  |
| ------------- | --- | --- | --- | --- | ------------- | --- | --- | --- | --- | ------------ |

Especificación de Requisitos de Software    Versión:           1.0
| Corpomotriz Los Salias  |     |     |     |     |     |     |   Fecha:  12/05/2025  |     |
| ----------------------- | --- | --- | --- | --- | --- | --- | --------------------- | --- |
ERS

1.1.3  Historia de Usuario “Crear Perfil” (Autor: Alejandra Teixeira) (Link para el diagrama de actividades: Click
acá):

|     |     | Crear Perfil  |     | Conversación  |     |     | Criterios de Aceptación  |     |
| --- | --- | ------------- | --- | ------------- | --- | --- | ------------------------ | --- |

Como  visitante  deseo  crear  mi  Épica: Gestionar Perfil  ●  Todos los campos deben
|     | perfil  | en  la  página  web  | para  |     |     |     | estar rellenos.  |     |
| --- | ------- | -------------------- | ----- | --- | --- | --- | ---------------- | --- |
Escenario de uso: El visitante
|     | ingresar    | todos  los       | datos  |               |               |     |     |     |
| --- | ----------- | ---------------- | ------ | ------------- | ------------- | --- | --- | --- |
|     |             |                  |        | podrá  tener  | la  libertad  | de  |     |     |
|     | necesarios  | en  el  momento  | de     |               |               |     |     |     |
crear un perfil personalizado
●
|     | realizar una compra.  |     |     |              |            |          | Si ya hay un cliente con  |     |
| --- | --------------------- | --- | --- | ------------ | ---------- | -------- | ------------------------- | --- |
|     |                       |     |     | para  poder  | disfrutar  | de  los  |                           |     |
los mismos datos no se
beneficios que esto aporta, en
podrá registrar esa
este caso poder ingresar sus
nueva cuenta.
|     |     |     |     | datos  para  | realizar  | una  |     |     |
| --- | --- | --- | --- | ------------ | --------- | ---- | --- | --- |

compra .
|     |     |     |     |     |     |     | ●  Que los datos personales  |     |
| --- | --- | --- | --- | --- | --- | --- | ---------------------------- | --- |
coincidan con los datos
Reglas de negocio :
del dueño de la cuenta
|     |     |     |     | ●   | El  visitante          | puede      | para el método de pago     |     |
| --- | --- | --- | --- | --- | ---------------------- | ---------- | -------------------------- | --- |
|     |     |     |     |     | indagar y  escoger el  |            | a la horas de ingresar la  |     |
|     |     |     |     |     | producto               | antes  de  | información al perfil.     |     |
crear su perfil .

●  Puede registrarse en
|     |     |     |     |     | la página y no tener  |     |     |     |
| --- | --- | --- | --- | --- | --------------------- | --- | --- | --- |
|     |     |     |     |     | la  obligación        | de  |     |     |

completar la compra
|     |     |     |     |     | en  ese  | mismo  |     |     |
| --- | --- | --- | --- | --- | -------- | ------ | --- | --- |
instante.
|     |     |     |     | ●   | Puede  salir  | de  una   |     |     |
| --- | --- | --- | --- | --- | ------------- | --------- | --- | --- |
|     |     |     |     |     | compra        | pero  su  |     |     |
|     |     |     |     |     | usuario       | quedará   |     |     |
|     |     |     |     |     | registrado    | en  la    |     |     |
página .

|     |     |     |     | Alcance:  | Accesible  | solo para  |     |     |
| --- | --- | --- | --- | --------- | ---------- | ---------- | --- | --- |
usuarios autenticados con rol
de visitante .
|     |     |     |     | Dependencias:  | Se  | necesita  |     |     |
| --- | --- | --- | --- | -------------- | --- | --------- | --- | --- |
una base de datos activa para
guardar los datos del perfil.

| Confidencial  |     |     |     | © UCAB, 2024  |     |     |     | Pág. 6 de 8  |
| ------------- | --- | --- | --- | ------------- | --- | --- | --- | ------------ |

Especificación de Requisitos de Software    Versión:           1.0
| Corpomotriz Los Salias  |     |     |     |     |     |     |   Fecha:  12/05/2025  |     |     |
| ----------------------- | --- | --- | --- | --- | --- | --- | --------------------- | --- | --- |
ERS

1.1.4  Historia de Usuario “Registrar Pago” (Autor: Javier Delmoral) (Link para el diagrama de actividades: Click
acá):
|     |     | Registrar Pago  |     | Conversación  |     |     | Criterios de Aceptación  |     |     |
| --- | --- | --------------- | --- | ------------- | --- | --- | ------------------------ | --- | --- |

Como Cliente, quiero registrar un  Epica: Gestionar Pago  ●  El sistema debe permitir
|     | nuevo pago en el sistema, para  |             |          |            |                       |     | registrar el pago solo si  |      |         |
| --- | ------------------------------- | ----------- | -------- | ---------- | --------------------- | --- | -------------------------- | ---- | ------- |
|     |                                 |             |          | Escenario  | de  uso:  El cliente  |     |                            |      |         |
|     | concretar                       | la  compra  | de  mis  |            |                       |     | todos                      | los  | campos  |
accede a su cuenta y registra
|     | productos.  |     |     |                |               |     | obligatorios            |     | están  |
| --- | ----------- | --- | --- | -------------- | ------------- | --- | ----------------------- | --- | ------ |
|     |             |     |     | un  pago  por  | un  servicio  | o   |                         |     |        |
|     |             |     |     |                |               |     | completos y validados.  |     |        |
producto adquirido, indicando

|     |     |     |     | el monto, método y fecha.  |     |     |                             |     |     |
| --- | --- | --- | --- | -------------------------- | --- | --- | --------------------------- | --- | --- |
|     |     |     |     |                            |     |     | ●  El  pago debe asociarse  |     |     |
correctamente al cliente
|     |     |     |     | Reglas de negocio:  |     |     |     |     |     |
| --- | --- | --- | --- | ------------------- | --- | --- | --- | --- | --- |
que lo registra.

●  El monto debe ser
|     |     |     |     |     |     |     | ●  Se  debe  | mostrar  | una  |
| --- | --- | --- | --- | --- | --- | --- | ------------ | -------- | ---- |
mayor a cero.
confirmación de registro
|     |     |     |     | ●  Debe seleccionarse  |     |     |     |     |     |
| --- | --- | --- | --- | ---------------------- | --- | --- | --- | --- | --- |
exitoso.
|     |     |     |     | un método de pago  |     |     |     |     |     |
| --- | --- | --- | --- | ------------------ | --- | --- | --- | --- | --- |
|     |     |     |     | válido.            |     |     |     |     |     |
●  El cliente debe estar

autenticado.

Alcance: Accesible solo para
|     |     |     |     |     |     |     |     |     |     |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
usuarios autenticados con rol

de cliente.

Dependencias: Existencia de

métodos de pago y vínculo del

pago con la cuenta del cliente.

2.  Requisitos suplementarios

2.1  Eficiencia de Desempeño
2.1.1  Capacidad
El software debe funcionar de manera ágil, respondiendo rápidamente a las acciones del usuario y utilizando los
recursos del sistema de forma eficiente (Tiempo de respuesta estimado: En menos de 5 segundos).

2.2  Capacidad de Interacción
2.2.1  Aprendizabilidad
La interfaz debe ser fácil de entender y usar sin necesidad de muchas explicaciones.

| Confidencial  |     |     |     | © UCAB, 2024  |     |     |     | Pág. 7 de 8  |     |
| ------------- | --- | --- | --- | ------------- | --- | --- | --- | ------------ | --- |

Especificación de Requisitos de Software Versión: 1.0
Corpomotriz Los Salias Fecha: 12/05/2025
ERS
2.3 Fiabilidad
2.3.1 Disponibilidad
El sistema debe estar operativo la mayor parte del tiempo, asegurando que los usuarios puedan acceder a sus
funciones principales sin interrupciones.
2.4 Seguridad
2.4.1 Confidencialidad
Cada transacción realizada en el sistema debe completarse correctamente y proteger la información sensible de los
usuarios contra accesos no autorizados.
Confidencial © UCAB, 2024 Pág. 8 de 8