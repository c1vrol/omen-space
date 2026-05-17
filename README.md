# omen-space
Omen Legal Documentation and Privacy Policy

# Documentos Legales de Omen

## PARTE I: POLÍTICA DE PRIVACIDAD

Esta política detalla el tratamiento de los datos técnicos y operativos dentro de la App, garantizando el cumplimiento de las normativas de protección de datos vigentes (GDPR, CCPA) y las directrices de la Google Play Console.

### 1. Uso de la API de Servicios de Accesibilidad (AccessibilityService API)
Omen requiere la activación voluntaria del Servicio de Accesibilidad de Android. Su integración cumple estrictamente con los siguientes límites técnicos:

* **Ámbito de Intercepción:** La App accede exclusivamente al evento de cambio de ventana (`TYPE_WINDOW_STATE_CHANGED`) provisto por el sistema operativo.
* **Propósito Exclusivo:** Identificar el nombre del paquete (package name, ej. `com.instagram.android`) de la aplicación activa en primer plano. Este dato se contrasta de forma local e instantánea con la lista de bloqueo definida por el Usuario para activar el escudo de concentración Pomodoro.
* **Privacidad Absoluta:** No se realiza lectura, captura, registro, almacenamiento ni transmisión remota de campos de texto, credenciales, contraseñas, pulsaciones de teclas (*keylogging*) ni datos de interacción dentro de las aplicaciones analizadas. El procesamiento es volátil y local en la memoria RAM del dispositivo.

### 2. Integración con YouTube Data API v3 y Servicios de Google
Para la gestión de listas de reproducción musicales de enfoque, la App se conecta a los servicios de Google mediante el protocolo OAuth 2.0.

* **Manejo de Credenciales:** Los tokens de acceso (*Access Tokens*) y de actualización (*Refresh Tokens*) se almacenan de forma local y cifrada en el dispositivo mediante el sistema Jetpack DataStore con soporte de criptografía de hardware. Ninguna credencial es enviada a servidores externos propiedad del desarrollador.
* **Cumplimiento de Políticas de Datos:** El uso de la información recibida a través de las APIs de Google se ajusta explícitamente a la *Google API Services User Data Policy*, incluyendo los requisitos de Uso Limitado (*Limited Use Requirements*). No se comparten ni se transfieren datos de la cuenta de YouTube del Usuario a plataformas de terceros o agencias de publicidad.
* **Revocación:** El Usuario conserva el derecho de desvincular la App y revocar los permisos de acceso en cualquier momento a través del panel de control de seguridad de su cuenta de Google.

### 3. Almacenamiento Local y Sincronización con Google Play Games
El progreso lúdico (puntuación de enfoque `focus_score` y estados de desbloqueo de los planetas del Event Horizon) se gestiona de la siguiente manera:

* **Arquitectura sin Servidor Propio:** No mantenemos bases de datos ni servidores externos para el almacenamiento de perfiles.
* **API de Saved Games:** La persistencia y sincronización entre dispositivos se delega en la API de Saved Games (Snapshots) de Google Play Games. Los datos se escriben en un archivo binario/JSON privado dentro del espacio de almacenamiento en la nube del propio Usuario en Google Drive.

### 4. Retención y Eliminación de Datos
El control de la información es exclusivo del Usuario:

* **Purgado Local:** El Usuario puede eliminar de forma definitiva todas las configuraciones, caché y tokens OAuth locales desinstalando la App o mediante la ruta del sistema: *Ajustes > Aplicaciones > Omen > Almacenamiento > Borrar datos*.
* **Purgado en la Nube:** Para eliminar el archivo de guardado de Play Games, el Usuario debe gestionar la eliminación de datos de guardado directamente desde la aplicación oficial de configuración de Google Play Juegos.

### 5. Privacidad Infantil
La App no recopila ni solicita de manera consciente información de menores de 13 años (o la edad mínima legal en la jurisdicción correspondiente). Si se detecta que un menor ha eludido esta restricción, los datos locales asociados serán eliminados de inmediato.

---

## PARTE II: TÉRMINOS DE SERVICIO

### 1. Requisitos Técnicos y Permisos
El correcto funcionamiento de Omen depende de la concesión explícita de permisos a nivel de sistema operativo:

* **Servicio de Accesibilidad:** Para la ejecución del bloqueo.
* **Permiso de Notificaciones:** (`POST_NOTIFICATIONS` en Android 13+ / API 33+) para la visualización persistente del temporizador en la barra de estado a través de componentes `CallStyle`.

El Usuario reconoce que la revocación de cualquiera de estos permisos por parte del sistema o de forma manual degradará o anulará la funcionalidad de la App.

### 2. Propiedad Intelectual
Todos los derechos sobre el código fuente, la arquitectura de software (incluyendo los módulos de la interfaz Monochrome y el sistema de Canvas dinámico), los logotipos vectoriales (`ic_omen_focus.xml`), marcas, diseños y assets gráficos de la App son propiedad exclusiva del desarrollador original. Se prohíbe explícitamente la ingeniería inversa, descompilación, extracción de código o distribución de copias modificadas de la App sin autorización expresa por escrito.

### 3. Cláusula de Indemnización
El Usuario se compromete a defender, indemnizar y eximir de toda responsabilidad al desarrollador de Omen ante cualquier reclamación, demanda, daño, pérdida, responsabilidad o gasto (incluyendo honorarios legales) que surja del uso indebido de la App, la violación de estos términos, o la infracción de derechos de terceros (incluyendo los Términos de Servicio de YouTube).

### 4. Exclusión de Responsabilidad Estricta (Disclaimer)
**LA APLICACIÓN OMEN SE PROPORCIONA "TAL CUAL" (AS IS) Y "SEGÚN DISPONIBILIDAD". EL DESARROLLADOR NO OFRECE GARANTÍAS EXPLÍCITAS O IMPLÍCITAS SOBRE LA INFALIBILIDAD DEL SISTEMA DE BLOQUEO O LA PRECISIÓN DE LOS TEMPORIZADORES.**

**BAJO NINGUNA CIRCUNSTANCIA EL DESARROLLADOR SERÁ RESPONSABLE DE DAÑOS DIRECTOS, INDIRECTOS, INCIDENTALES, CONSECUENCIALES O ESPECIALES (INCLUYENDO, PERO NO LIMITADO A, PÉRDIDA DE BENEFICIOS, INTERRUPCIÓN DE LA ACTIVIDAD LABORAL, PÉRDIDA DE INFORMACIÓN O FALLOS EN DISPOSITIVOS) DERIVADOS DE:**

* **FALLOS EN LA REPRODUCCIÓN DE ALERTAS ACÚSTICAS O CRONÓMETROS.**
* **BLOQUEO ACCIDENTAL DE APLICACIONES CRÍTICAS, DE COMUNICACIÓN O DE EMERGENCIA.**
* **RESTRICCIÓN O SILENCIAMIENTO DE NOTIFICACIONES PRIORITARIAS DEL SISTEMA OPERATIVO.**
* **TERMINACIÓN AUTOMÁTICA DEL PROCESO EN SEGUNDO PLANO POR PARTE DE LOS GESTORES DE BATERÍA DE HARDWARE DE TERCEROS (EJ. SAMSUNG ONE UI, XIAOMI HYPEROS).**

La App es una herramienta de asistencia personal orientada a la productividad y no debe ser utilizada en entornos de misión crítica ni en situaciones donde el fallo de un temporizador pueda poner en riesgo la seguridad, la salud o la integridad financiera del Usuario.

### 5. Jurisdicción y Ley Aplicable
Estos Términos se rigen por la legislación vigente del país de residencia del desarrollador principal. Cualquier controversia, disputa o reclamación legal resultante del uso de la App se someterá de forma exclusiva a los tribunales competentes de dicha jurisdicción.
