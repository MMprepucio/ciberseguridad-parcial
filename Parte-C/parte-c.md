# Parte C — Tecnologías y seguridad

## 1. ¿Qué información de las tecnologías debe estar cifrada?

La información que manejan estas tecnologías debe protegerse mediante cifrado para evitar que personas no autorizadas puedan leerla o modificarla.

En Internet de las Cosas (IoT) se deben proteger datos enviados por sensores, dispositivos, ubicaciones, identificadores de dispositivos y cualquier información personal recopilada.

En los nanosatélites se debe proteger la información de telemetría, comandos de control, datos de sensores, ubicación y comunicaciones entre el satélite y las estaciones terrestres.

En los sistemas de inteligencia artificial se deben proteger los datos utilizados para entrenar y operar los modelos, además de la información que reciben y generan.

En los drones de búsqueda y rescate se deben proteger las imágenes, videos, coordenadas GPS, rutas, información de las personas encontradas y comunicaciones con los operadores.

En la interacción humano-máquina se deben proteger las credenciales de los usuarios, datos personales, comandos y registros de las operaciones.

En general, deben cifrarse tanto los datos almacenados como los datos que se transmiten por las redes.

---

## 2. ¿Cuál es el protocolo de seguridad que debe gestionar cada tecnología?

Cada tecnología debe utilizar mecanismos de seguridad adecuados para proteger sus comunicaciones y sistemas.

### IoT

Debe utilizar comunicaciones seguras mediante protocolos como TLS cuando utilice conexiones IP, además de autenticación de dispositivos y control de acceso.

### Nanosatélites

Deben utilizar canales de comunicación autenticados y cifrados entre el satélite y las estaciones terrestres. También deben existir mecanismos para verificar que los comandos recibidos provienen de una fuente autorizada.

### Inteligencia artificial

Debe proteger las interfaces y servicios mediante conexiones seguras, autenticación, autorización y control de acceso. También se deben proteger los datos utilizados por los sistemas de IA.

### Drones

Deben utilizar comunicaciones autenticadas y cifradas entre el dron y su estación de control. También deben protegerse las transmisiones de video, coordenadas y comandos.

### Interacción humano-máquina

Debe utilizar autenticación de usuarios, autorización por roles, cifrado de las comunicaciones y registros de las actividades realizadas.

La seguridad debe aplicarse tanto al dispositivo como a la red, las aplicaciones y la información.

---

## 3. ¿Cómo sería el manejo de contraseñas, usuarios y autenticación en la interacción humano-máquina?

El sistema debe utilizar cuentas individuales para cada usuario. No se deben compartir las credenciales.

Las contraseñas deben ser largas, difíciles de adivinar y diferentes para cada cuenta. Además, deben almacenarse de manera segura utilizando mecanismos de protección adecuados.

Cuando sea posible se debe utilizar autenticación multifactor (MFA), combinando la contraseña con otro factor de autenticación.

También se deben establecer diferentes niveles de permisos. Por ejemplo:

- Un administrador puede configurar el sistema.
- Un operador puede controlar determinadas funciones.
- Un usuario de consulta puede visualizar información sin modificarla.

Los permisos deben seguir el principio de mínimo privilegio, es decir, cada usuario debe tener solamente los permisos que necesita para realizar sus funciones.

---

## 4. ¿El Blockchain serviría en las tecnologías mostradas? ¿Qué es y cómo funciona?

Sí. Blockchain podría ser útil en determinados escenarios donde sea necesario mantener un registro compartido, verificable y difícil de modificar.

Blockchain es una tecnología que permite almacenar información en una cadena de bloques. Cada bloque contiene información relacionada con las transacciones o registros y se vincula con el bloque anterior mediante mecanismos criptográficos.

De forma general, funciona de la siguiente manera:

1. Se genera una transacción o registro.
2. La información es enviada a la red.
3. Los participantes de la red verifican la información mediante el mecanismo de consenso correspondiente.
4. Las transacciones verificadas se agrupan en un bloque.
5. El bloque se incorpora a la cadena.
6. La información queda registrada y puede ser verificada posteriormente.

En un sistema de emergencia, Blockchain podría utilizarse, por ejemplo, para mantener registros verificables de eventos, operaciones, mantenimiento de equipos o intercambio de información entre diferentes organizaciones.

Sin embargo, Blockchain no reemplaza todas las medidas de ciberseguridad. Debe utilizarse solamente cuando sus características aporten un beneficio real al sistema.

---

## 5. ¿Cómo sería el manejo de copias de seguridad y respaldos de información?

Las copias de seguridad deben realizarse de manera periódica y planificada.

Se recomienda mantener diferentes copias de la información y almacenarlas en ubicaciones independientes. Una estrategia útil es conservar copias locales y copias en la nube.

Para estas tecnologías se deberían respaldar:

- Configuraciones de los dispositivos.
- Bases de datos.
- Registros de eventos.
- Información de usuarios.
- Datos de sensores.
- Información de drones.
- Imágenes y videos importantes.
- Configuraciones de los sistemas de inteligencia artificial.
- Registros de comunicaciones y operaciones cuando sea necesario.

Las copias deben estar protegidas mediante controles de acceso y cifrado. También se deben realizar pruebas periódicas de restauración para comprobar que los respaldos realmente pueden utilizarse.

En sistemas críticos se recomienda contar con procedimientos de recuperación ante fallos y desastres.

---

## 6. Propuesta de un sistema de seguridad robusto

Se propone un sistema de seguridad para la atención de terremotos de gran magnitud que integre Internet de las Cosas, nanosatélites, inteligencia artificial, drones de búsqueda y rescate e interacción humano-máquina.

### Funcionamiento propuesto

1. **Sensores IoT:** se instalan sensores en diferentes zonas para detectar movimientos, daños estructurales y otras condiciones importantes.

2. **Nanosatélites:** reciben y transmiten información cuando las redes terrestres están dañadas o no disponibles.

3. **Drones de búsqueda y rescate:** utilizan cámaras y sensores para localizar personas y obtener imágenes de las zonas afectadas.

4. **Inteligencia artificial:** analiza la información obtenida por sensores, satélites y drones para ayudar a identificar zonas de mayor riesgo y priorizar las operaciones de rescate.

5. **Centro de control:** recibe la información y presenta los datos a los equipos de emergencia.

6. **Interacción humano-máquina:** los operadores pueden consultar información, enviar instrucciones y supervisar las operaciones.

### Medidas de seguridad

El sistema debe incluir:

- Cifrado de las comunicaciones.
- Autenticación de usuarios y dispositivos.
- Autenticación multifactor para usuarios con privilegios.
- Control de acceso basado en roles.
- Protección de las bases de datos.
- Copias de seguridad periódicas.
- Registro de eventos y actividades.
- Actualización de software y firmware.
- Segmentación de redes.
- Sistemas de detección de actividades sospechosas.
- Planes de recuperación ante fallos.

### Objetivo

El objetivo principal es mantener la disponibilidad de los sistemas durante una emergencia, proteger la información y permitir que los equipos de rescate reciban información confiable para tomar decisiones rápidas y seguras.
