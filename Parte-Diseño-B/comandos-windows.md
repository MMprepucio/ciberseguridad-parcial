# Parte de Diseño B — Comandos de Windows

## Introducción

En esta actividad se utilizaron comandos de la consola de Windows para visualizar información relacionada con la conexión a Internet, configuración de red, procesos, almacenamiento, memoria RAM y copias de seguridad.

---

## 1. Comprobar conexión a Internet

### Comando utilizado

```cmd
ping 8.8.8.8
Procedimiento

Se ejecutó el comando ping desde la consola de Windows para comprobar la comunicación entre el computador y una dirección IP externa.

Resultado

El comando permitió comprobar si existía comunicación con Internet mediante las respuestas recibidas desde la dirección 8.8.8.8.

Si aparecen respuestas como:

Respuesta desde 8.8.8.8

significa que existe comunicación con dicha dirección.
2. ¿Cómo visualiza que la RED 1 es independiente de la RED 2?
Comandos utilizados
ipconfig

y

route print
Procedimiento

Se utilizó ipconfig para observar la dirección IPv4, máscara de subred y puerta de enlace del computador.

Posteriormente se utilizó route print para observar la tabla de enrutamiento de Windows.

Análisis

La dirección IP y la máscara de subred permiten identificar a qué red pertenece el computador.

La tabla de rutas permite observar las redes conocidas por el equipo y las rutas utilizadas para comunicarse con ellas.

Para determinar que dos redes son independientes se deben comparar sus rangos de direccionamiento y sus rutas. Si pertenecen a segmentos diferentes y no existe una ruta que permita la comunicación directa entre ellas, se consideran redes separadas.
3. ¿Cómo explora los procesos y tareas desde la consola de Windows?
Comando utilizado
tasklist
Procedimiento

Se ejecutó el comando tasklist para mostrar los procesos que actualmente se encuentran ejecutándose en Windows.

Información obtenida

El comando muestra información como:

Nombre del proceso.
Identificador PID.
Sesión.
Cantidad de memoria utilizada.
Análisis

La visualización de los procesos permite identificar qué programas y servicios se están ejecutando en el computador.

Durante una auditoría básica de seguridad, esta información puede ayudar a detectar procesos desconocidos o que presenten un comportamiento que deba ser investigado.
4. ¿Cómo observa el almacenamiento de los discos y la memoria RAM usada?
Almacenamiento de discos

Se utilizó el siguiente comando:

wmic logicaldisk get name,size,freespace

Este comando permite consultar las unidades de almacenamiento y mostrar información relacionada con su capacidad y espacio disponible.

Nota

En algunas versiones actuales de Windows el comando WMIC puede no estar disponible. Si esto ocurre, se puede utilizar la información proporcionada por las herramientas de almacenamiento de Windows.

Memoria RAM

Para consultar información general del sistema se utilizó:

systeminfo

Dentro de la información mostrada se pueden consultar los valores de:

Total Physical Memory.
Available Physical Memory.
Análisis

La información del almacenamiento permite conocer la capacidad de las unidades y el espacio disponible.

La información de memoria permite conocer la cantidad de memoria RAM física instalada y la cantidad disponible en el momento de la consulta.
5. ¿Cómo hace una copia de seguridad de los dispositivos en el PC?

Para realizar una copia de seguridad local se creó primero una carpeta para almacenar la información.

Crear carpeta de información
mkdir "%USERPROFILE%\Desktop\Datos-Backup"
Crear archivo de prueba
echo Archivo para copia de seguridad > "%USERPROFILE%\Desktop\Datos-Backup\prueba.txt"
Comprobar que el archivo existe
dir "%USERPROFILE%\Desktop\Datos-Backup"

Después se creó una carpeta para almacenar la copia de seguridad:

mkdir "%USERPROFILE%\Desktop\Backup-Ciberseguridad"
Realizar la copia de seguridad

Se utilizó el comando robocopy:

robocopy "%USERPROFILE%\Desktop\Datos-Backup" "%USERPROFILE%\Desktop\Backup-Ciberseguridad" /E
Comprobar la copia

Finalmente se verificó que el archivo estuviera presente en la carpeta de respaldo:

dir "%USERPROFILE%\Desktop\Backup-Ciberseguridad"
Resultado

El archivo prueba.txt fue copiado desde la carpeta original hacia la carpeta de respaldo.
