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
