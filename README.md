# <img src="https://i.servimg.com/u/f34/20/32/08/60/eg10.png" width="32" height="32"> USB Monitor v1.3

> ## 🛡️ Detección, Bloqueo y Registro de Dispositivos USB No Autorizados para Windows 10 & 11
>
> USBMonitor v1.3 es la suite profesional de seguridad y control de puertos USB para Windows. Integra funciones avanzadas de detección en tiempo real de unidades extraíbles, bloqueo automático con expulsión física forzada, gestión de lista blanca (*Whitelist*) con control de límites para edición Free/Pro, protección de acceso mediante clave maestra con cifrado SHA-256, claves de recuperación únicas y un completo panel de control con estadísticas y gráficos interactivos (*Sparklines*).
>
> Diseñado para operar 100% de forma local en segundo plano mediante la bandeja del sistema (*Tray Icon*), garantiza la privacidad total de tus datos corporativos y personales sin depender de la nube, ofreciendo almacenamiento seguro en el perfil de usuario con atributos ocultos y de sistema.

---

<div align="center">
  <h2>📸 Interfaz Principal</h2>
  <img src="https://i.servimg.com/u/f34/20/32/08/60/egafe10.png" alt="USBMonitor Interface" width="550">
</div>

---

# ✨ Funciones Principales de USBMonitor

USBMonitor v1.3 evoluciona la seguridad perimetral de los equipos de escritorio mediante un motor residente en PyQt6 altamente optimizado:

### 🔍 Detección y Monitoreo en Tiempo Real (`MonitorThread`)

* Monitoreo continuo mediante hilos asíncronos (`QThread`) que evalúan los cambios en los volúmenes lógicos y físicos conectados al sistema operativo a través de WMI y PowerShell.
* Alerta visual inmediata y expulsión física automática de cualquier dispositivo USB que no se encuentre previamente autorizado.

### 🚫 Expulsión Automática de Dispositivos No Autorizados

* Ejecución de comandos de bajo nivel en Windows (`DeviceIoControl`, `FSCTL_LOCK_VOLUME`, `FSCTL_DISMOUNT_VOLUME` y `IOCTL_STORAGE_EJECT_MEDIA`) para desmontar y bloquear de forma segura el hardware no reconocido.
* Diálogo de alerta interactivo con información detallada del dispositivo (Nombre, ID, Unidad de disco) y opciones de copiado rápido o inclusión directa a la lista blanca.

### ✅ Sistema de Lista Blanca (*Whitelist*) y Restricciones Free/Pro

* Permite registrar dispositivos de confianza mediante su identificador único de volumen (`VolumeSerialNumber`) y nombre descriptivo.
* Control inteligente de límites para la edición Free (hasta 3 dispositivos autorizados) con redirección al ecosistema Pro para habilitar registros ilimitados.

### 🔐 Seguridad y Protección de Acceso (Clave Maestra y Recuperación)

* Protección de acceso con clave maestra basada en hash **SHA-256**.
* Generación automática de una clave de recuperación única con formato de bloques aleatorios (`XXXX-XXXX-XXXX-XXXX`) durante el primer inicio o cambio de credenciales, permitiendo restablecer el acceso en caso de pérdida.
* Restricción de salida de la aplicación desde la bandeja del sistema (*Tray Icon*) solicitando la clave maestra.

### 📋 Historial Completo y Registro de Eventos (`usbmonitor_log.json`)

* Registro detallado de todas las acciones (*Conectado*, *Bloqueado*, *Autorizado*, *Desconectado*, *Agregado*, *Eliminado*) con marcas de tiempo precisas y persistencia local en formato JSON oculto en AppData.
* Acciones rápidas en tabla para copiar identificadores o autorizar dispositivos con un solo clic.

---

# 💎 Comparativa de Licencias: Free vs. Pro

<table>
<tr>
<th>Funciones y Características</th>
<th>Gratis (Free Edition)</th>
<th>USBMonitor Pro (v1.3)</th>
</tr>

<tr>
<td>Detección y bloqueo automático de USBs</td>
<td align="center">✅</td>
<td align="center">✅</td>
</tr>

<tr>
<td>Expulsión automática por comandos de bajo nivel</td>
<td align="center">✅</td>
<td align="center">✅</td>
</tr>

<tr>
<td>Procesamiento 100% local (sin telemetría ni nube)</td>
<td align="center">✅</td>
<td align="center">✅</td>
</tr>

<tr>
<td>Protección con Clave Maestra (SHA-256) y Recuperación</td>
<td align="center">✅</td>
<td align="center">✅</td>
</tr>

<tr>
<td>Minimización inteligente a la bandeja del sistema (Tray)</td>
<td align="center">✅</td>
<td align="center">✅</td>
</tr>

<tr>
<td>Panel de control moderno con gráficos Sparklines</td>
<td align="center">✅</td>
<td align="center">✅</td>
</tr>

<tr>
<td><b>Whitelist ilimitada de dispositivos autorizados</b></td>
<td align="center">❌ (Máx. 3)</td>
<td align="center">✅</td>
</tr>

<tr>
<td><b>Políticas de horario automáticas (ej. bloqueo fuera de oficina)</b></td>
<td align="center">❌</td>
<td align="center">✅</td>
</tr>

<tr>
<td><b>Exportación completa de historial de eventos a CSV / Excel</b></td>
<td align="center">❌</td>
<td align="center">✅</td>
</tr>

<tr>
<td><b>Soporte técnico prioritario y actualizaciones</b></td>
<td align="center">❌</td>
<td align="center">✅</td>
</tr>

<tr>
<td><b>Duración</b></td>
<td align="center"><b>Gratis para siempre</b></td>
<td align="center"><b>Licencia Comercial / Pro</b></td>
</tr>

<tr>
<td><b>Acción</b></td>

<td align="center">
<a href="https://github.com/escudodigitalsv/usbmonitor/releases">
<img src="https://img.shields.io/badge/VERSION_FREE-Gratis-blue?style=for-the-badge">
</a>
</td>

<td align="center">
<a href="https://escudodigitalsv.com/usbmonitor-pro">
<img src="https://img.shields.io/badge/🛒_COMPRAR_PRO-escudodigitalsv.com-blue?style=for-the-badge">
</a>
</td>

</tr>

</table>

---

# 🚀 ¿Por qué elegir USBMonitor?

| 💡 Beneficios Clave                                  | ⚙️ Especificaciones Técnicas          |
| :--------------------------------------------------- | :------------------------------------ |
| 🛡️ Bloqueo preventivo de fugas de datos por USB.     | 🖥️ Compatible con Windows 10 y 11 (x64) |
| 🔒 Seguridad reforzada con hash SHA-256 y recovery.  | ⚡ Motor residente multihilo (QThread)  |
| 📂 Almacenamiento local oculto en AppData (`Hidden`).| 🌐 Funciona 100% fuera de línea (offline) |
| 📊 Métricas visuales e historial de eventos en vivo. | 🔑 Autoelevación automática de privilegios |
| ⚡ Interfaz moderna basada en PyQt6 con tema limpio. | 📂 Registro persistente en JSON         |

---

# ⭐ Características Principales de la Versión

### 📊 Panel de Control y Estadísticas en Vivo
* Tarjetas de estado con indicadores de tendencia y gráficos de línea miniatura (`Sparklines`) renderizados dinámicamente mediante `QPainter`.
* Control de acceso integrado con minimización persistente y notificaciones flotantes en la bandeja del sistema.

### 📂 Almacenamiento Oculto y Resiliente
* Los archivos de configuración (`usbmonitor_config.json`) y registros (`usbmonitor_log.json`) se almacenan de forma segura en `AppData\Roaming\EscudoDigitalSV\USBMonitor`, aplicando de manera automática atributos de archivo oculto y de sistema (`FILE_ATTRIBUTE_HIDDEN`) mediante llamadas a la API de Windows (`kernel32.SetFileAttributesW`).

---

# 🛡️ Casos de Uso Avanzados

✅ **Seguridad Corporativa:** Impedir la conexión de memorias USB no autorizadas en equipos de oficinas para prevenir la extracción de información sensible.

✅ **Protección contra Malware:** Bloquear la introducción de códigos maliciosos o virus propagados a través de unidades extraíbles ajenas a la organización.

✅ **Auditoría de Accesos:** Mantener un registro histórico exacto de cada intento de conexión de dispositivos al sistema con sus respectivos identificadores de serie.

✅ **Control de Periféricos Personales:** Permitir únicamente el uso de teclados, ratones o discos duros corporativos registrados en la lista blanca.

---

# ⚠️ Nota de Seguridad

> [!CAUTION]
> USBMonitor interactúa directamente con los volúmenes lógicos y controladores de almacenamiento del sistema operativo Windows para realizar operaciones de bloqueo y expulsión de hardware.
>
> Debido a estas operaciones a nivel de sistema y al uso de llamadas nativas de la API de Win32 (`kernel32`), algunas herramientas antivirus pueden presentar falsos positivos preventivos durante la ejecución del binario empaquetado.

> [!NOTE]
> USBMonitor es una solución desarrollada por EscudoDigitalSV.
>
> La aplicación se ejecuta de forma predeterminada con privilegios elevados de Administrador (`ShellExecuteW` con verbo `runas`) para asegurar el control absoluto sobre los dispositivos de almacenamiento masivo conectados al equipo.

---

# 📥 Instalación y Ejecución

> [!IMPORTANT]
> Al ejecutar USBMonitor por primera vez, el sistema operativo solicitará permisos de Administrador mediante el control de cuentas de usuario (UAC) para garantizar el funcionamiento correcto de los ganchos de control de discos.

### Pasos iniciales

1. Ejecuta la aplicación.
2. Configura tu **Clave Maestra** de seguridad en el asistente de primer inicio.
3. Guarda en un lugar seguro la **Clave de Recuperación** generada de 16 caracteres.
4. Administra tus dispositivos de confianza desde la pestaña *Whitelist* y supervisa la actividad en tiempo real desde el *Dashboard*.

---

# 📦 Requisitos del Sistema

| Requisito         | Especificación |
| :---------------- | :-------------- |
| Sistema Operativo | Windows 10 / 11 (64-bit) |
| Privilegios       | Administrador (requerido para control de discos) |
| Dependencia Python| `PyQt6` (solo requerido en caso de ejecutar desde el código fuente) |
| Memoria RAM       | 2 GB o superior |
| Espacio en Disco  | 30 MB |
| Internet          | No requerido (100% offline) |

---

# 🐛 Soporte Técnico y Contacto

Si posees consultas técnicas o deseas adquirir una licencia Pro para desbloquear características avanzadas:
* **Correo de soporte:** `info@escudodigitalsv.com`
* **Sitio Web Oficial:** [https://escudodigitalsv.com](https://escudodigitalsv.com)
* **Repositorio GitHub:** [https://github.com/escudodigitalsv](https://github.com/escudodigitalsv)

---

<div align="center">

## ❤️ USBMonitor v1.3 © 2026 EscudoDigitalSV

Detección, bloqueo y registro profesional de dispositivos USB para Windows.

</div>
