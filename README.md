# TechnoMD5
*Gestión de proyectos*
*Grupo lunes*
## 1. Integrantes
 - Enrique Padilla Padilla (epp1012@alu.ubu.es)
 - Carlos Saiz Hernandez (csh1001@alu.ubu.es)
 - Mario Cea Heredia (mch1015@alu.ubu.es)
 - Alejandro García García (agg1068@alu.ubu.es)

 ## 2. Tareas asignadas
 ### 2.1. Gestión de usuarios
Gestión del backend del serivicio de usuarios
 #### 2.1.1. Registro

*Dirección:*

 > /API/v1/user/singup
  Protocolo: **POST**

 Servicio de registro de credenciales

 **Función interna**:
 
 Este servicio se encarga de permitir que los usuarios se registren proporcionando sus credenciales.

**Parametros de entrada:**
 - *Email*
 - *Password*
 - *Nombre*
 - *Apellidos*
 - *Fecha de nacimiento*

**Argumentos de salida:**
 - *Token de sesión MD5:* Este token de sesión MD5 se genera automaticamente al realizar un registro correcto para empezar a trabajar en la plataforma.


 #### 2.1.2. Login

*Dirección:*
 > /API/v1/user/login
  Protocolo: **POST**

 Servicio de inicio de sesión de usuario

 **Función interna**:
 
Este servicio se encarga de permitir que los usuarios inicien sesión proporcionando sus credenciales.


**Parámetros de entrada:**

 - *Email*
 - *Password*

**Argumentos de salida:**
 - *Token de sesión MD5:* Este token de sesión MD5 se genera automáticamente al realizar un login correcto, mediante este token podrá trabajar en la plataforma. Este token gestionará el tiempo de sesión del usuario y los roles que se le han otorgado.

 #### 2.1.3. Restablecer credenciales

*Dirección:*
 > /API/v1/user/changepassword 
 Protocolo: **GET**
 

 Servicio de restablecimiento de credenciales de usuario

 **Función interna**:
 
Este servicio se encarga de permitir que los usuarios puedan restablecer sus credenciales.


**Parámetros de entrada:**
 - *Email*

**Argumentos de salida:**
 - *wasTrue*: Booleano de salida que indicara al *frontend* si la petición fue correcta y el correo de restablecimiento de credenciales fue enviado
- *tokenSesion*: Token que se enviara al correo electrónico donde el usuario recibirá una URL con este token para restablecer sus credenciales

*Ejemplo:*
> https://www.technomd5.com/api/v1/user/changepassword?token=fb00927926dd5c57c02d2b1664c8bd82b9ae2b36

#### 2.1.4. Seguridad mediante tokens

**Función interna**:

Este servicio se encarga de garantizar la seguridad mediante el uso de tokens. Esto implica la generación y validación de tokens para cada transacción segura.

**Detalles de implementación:**

 - **Generación de Tokens:**

    Creación de tokens seguros para cada sesión o transacción.
    
 - **Validación de Tokens:**
    Verificación de la autenticidad del token en cada solicitud.

 - **Renovación de Tokens:**

Establecimiento de un mecanismo para renovar periódicamente los tokens de sesión.

### 2.2. Vulnerabilidades en red
Gestión de las vulnerabilidades de red solicitadas por el usuario.

 #### 2.2.1. Uso de NMAP
 Se implementará el uso de NMAP en las redes permitidas por el usuario, donde se escaneará y analizará de forma exhaustiva dichas redes en busca de vulnerabilidades, o posibles brechas de seguridad.

 [Opciones de consulta de NMAP](https://nmap.org/man/es/)

 #### 2.2.2 Registro y documentación de las vulnerabilidades activas
 Una vez finalizada la exploración y análisis de la red realizaremos una documentación de los posibles fallos que encontramos en ella, añadiendo su relevancia de peligro, los posibles daños que el uso de esa vulnerabilidad puede generar, y posteriormente las soluciones a dichas fallas en la seguridad.

 [*Ejemplo*](./html/ejemploNMAP.html)

### 2.3. Codigo malicioso
Investigación y análisis del código de programas maliciosos con el fin de identificar y comprender amenazas cibernéticas. 

  #### 2.3.1. Lectura de códigos
La lectura de códigos para encontrar malware implica analizar el código fuente o el código ejecutable de un programa para identificar la presencia de comportamientos maliciosos.

Es importante señalar que el análisis de malware es una tarea compleja y en constante evolución, ya que los desarrolladores de malware continúan mejorando sus técnicas para evadir la detección.

 #### 2.3.2 Creación de base de datos de Malwares
Una base de datos de malware será creada para la colección organizada de información sobre amenazas cibernéticas, incluyendo detalles sobre sus características, comportamientos y técnicas de evasión. 
Es una herramienta esencial para fortalecer la postura de seguridad cibernética de una organización al proporcionar información crucial para la detección, prevención y respuesta a amenazas.

---------
### 2.4. Seguridad y mantenimiento
Implementacion de medidas de seguridad robustas para salvaguardar la integridad de los datos y la infraestructura de su empresa, respaldadas por protocolos de mantenimiento proactivos que garantizan un entorno operativo eficiente y confiable.

  #### 2.4.1. Busqueda de brechas de seguridad
Realizacion exhaustiva de evaluaciones de brechas de seguridad, empleando herramientas avanzadas y análisis meticuloso para identificar posibles vulnerabilidades en sistemas y redes.

Nuestro enfoque proactivo nos permite anticipar y abordar amenazas potenciales, fortaleciendo así la resiliencia de su empresa contra ciberataques. Además, proporcionamos informes detallados y recomendaciones para mejorar continuamente las defensas cibernéticas.

 #### 2.4.2 Exploracion de vulnerabilidades mediante Metasploit
Utilizacion de Metasploit como una poderosa herramienta de evaluación de seguridad, llevando a cabo exploraciones de vulnerabilidades en sistemas y redes. Con un enfoque ético, identificamos posibles debilidades, evaluamos su impacto y proponemos soluciones para fortalecer la seguridad cibernética. Nuestro equipo experto emplea Metasploit de manera controlada y estratégica, garantizando un análisis exhaustivo y medidas preventivas efectivas.
