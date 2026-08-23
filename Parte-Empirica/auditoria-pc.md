# Parte Empírica — Auditoría manual de seguridad del PC

## 1. Políticas de contraseña

### Comando utilizado

```cmd
net accounts
Análisis

Se revisaron las políticas actuales de las cuentas y contraseñas del equipo mediante el comando net accounts.

Se verificaron aspectos como:

Longitud mínima de la contraseña.
Duración máxima de la contraseña.
Duración mínima de la contraseña.
Configuración relacionada con el bloqueo de cuentas.

Resultado observado: Se registraron los valores mostrados por la consola como evidencia de la configuración actual del equipo.

Recomendación: Utilizar contraseñas seguras y únicas, evitando compartirlas con otras personas.

2. Firewall
Comando utilizado
netsh advfirewall show allprofiles
Análisis

Se revisó el estado del Firewall de Windows en los diferentes perfiles de red disponibles.

Se verificó si el firewall se encontraba activado para los perfiles correspondientes.

Resultado observado: El estado mostrado en la consola fue registrado mediante una captura de pantalla.

Recomendación: Mantener activo el firewall para reducir el riesgo de conexiones no autorizadas.

3. Antivirus
Comando utilizado
Get-MpComputerStatus
Análisis

Se consultó el estado de Microsoft Defender.

Se revisaron campos relacionados con:

AntivirusEnabled.
RealTimeProtectionEnabled.
AntispywareEnabled.

Resultado observado: Los valores obtenidos fueron revisados directamente en PowerShell y registrados mediante evidencia.

Recomendación: Mantener la protección antivirus y la protección en tiempo real activadas.

4. Configuración de red
Comandos utilizados
ipconfig /all
netstat -ano
Análisis

Mediante ipconfig /all se revisó la configuración detallada de los adaptadores de red, incluyendo información relacionada con direcciones IP, DNS y DHCP.

Mediante netstat -ano se revisaron las conexiones y puertos activos junto con sus identificadores de proceso (PID).

Resultado observado: Se registró la información obtenida mediante capturas de pantalla de la consola.

Recomendación: Revisar periódicamente las conexiones activas y verificar procesos desconocidos antes de realizar cualquier acción.

5. Puntos de persistencia
Comando utilizado
Get-CimInstance Win32_StartupCommand | Select-Object Name, Command, Location
Análisis

Se revisaron elementos configurados para ejecutarse automáticamente durante el inicio del sistema.

Se verificaron el nombre del elemento, el comando asociado y su ubicación.

Tareas programadas

También se utilizó:

Get-ScheduledTask | Where-Object {$_.State -ne "Disabled"} | Select-Object TaskName, TaskPath, State

Este comando permitió revisar tareas programadas que se encuentran activas.

Resultado observado: Se revisaron los elementos obtenidos para identificar tareas o programas desconocidos.

Recomendación: No eliminar tareas o programas automáticamente. Antes de modificar un elemento desconocido se debe verificar su origen y función.
