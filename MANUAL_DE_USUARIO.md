# ARGOS — Manual de Usuario

## Sistema de Gestión de Riesgo y Comando de Incidente

---

## 1. Introducción

ARGOS es un **centro de comando** diseñado para la gestión de emergencias e incendios. Permite monitorear incidentes activos, recursos, personal operativo, alertas en tiempo real y métricas de riesgo, todo en un único tablero de control.

---

## 2. Acceso al Sistema

### 2.1 Inicio de Sesión

1. Abra la aplicación en su navegador.
2. En la pantalla de login, ingrese su **correo electrónico** y **contraseña**.
3. Presione **"Ingresar al Sistema"**.

### 2.2 Registro de Nuevos Usuarios

1. Haga clic en la pestaña **"Registrarse"**.
2. Complete su **nombre completo**, **correo electrónico** y **contraseña** (mínimo 6 caracteres).
3. Presione **"Crear Cuenta"**.

> **Nota:** El primer usuario registrado en el sistema se convierte automáticamente en **Administrador**.

---

## 3. Roles de Usuario

| Rol | Descripción |
|-----|-------------|
| **Administrador** | Puede crear, editar y eliminar todos los datos. Gestión de usuarios. |
| **Operador** | Puede crear y editar datos, pero no gestionar usuarios. |
| **Visualizador** | Solo puede ver la información. Sin permisos de edición. |

---

## 4. Panel Principal (Dashboard)

El dashboard se divide en 6 secciones principales:

### 4.1 Barra de Estadísticas (Stats Row)

En la parte superior se muestra un resumen rápido:
- **Operadores en campo** — Total de brigadistas activos.
- **Recursos en uso** — Vehículos, helicópteros y equipos desplegados.
- **Incidentes activos** — Cantidad de incidentes con estado "activo".
- **Personal disponible** — Brigadistas en estado "disponible".
- **Alertas sin leer** — Alertas pendientes.
- **Índice de riesgo** — Promedio del nivel de riesgo actual.

---

### 4.2 Mapa de Incendios (Panel Superior Izquierdo)

**Funciones:**
- Visualiza todos los **incidentes activos** en tiempo real sobre un mapa de Argentina.
- Cada incidente se muestra como un punto con color según severidad:
  - 🔴 **Rojo** = Crítico
  - 🟠 **Naranja** = Alto
  - 🟡 **Amarillo** = Medio
  - 🟢 **Verde** = Bajo
- **Brigadistas en línea** se muestran como puntos de color según su rol.
- Haga clic en cualquier punto para ver detalles (título, dirección, descripción, severidad).

**Ruta de Escape:**
1. Presione el botón **"RUTA"** en el panel del mapa.
2. Haga clic en el mapa para marcar el **origen**.
3. Haga clic nuevamente para marcar el **destino**.
4. Se traza automáticamente una línea con la **distancia en kilómetros**.
5. Haga clic en la **X** para borrar la ruta.

---

### 4.3 Alertas del Sistema (Panel Superior Derecho)

Muestra todas las alertas activas del sistema:
- Las alertas se marcan como **"NUEVA"** hasta que se lean.
- Haga clic en una alerta para marcarla como leída.
- Tipos de alertas:
  - 🔴 **Crítica** — Rojo (requiere atención inmediata)
  - 🟠 **Advertencia** — Naranja
  - 🔵 **Info** — Azul
  - ⚪ **Fallo** — Gris

**Administradores y Operadores:**
- Pueden crear nuevas alertas con el botón **"NUEVA"**.
- Pueden editar o borrar alertas con los botones de lápiz y basura.

---

### 4.4 Registro de Incidentes (Panel Central Izquierdo)

Lista completa de todos los incidentes con filtros:
- **Tipos:** Incendio, Accidente, Médico, Químico, Otro.
- **Estados:** Activo, Controlado, Resuelto.
- **Severidades:** Crítico, Alto, Medio, Bajo.

**Acciones:**
- Haga clic en una fila para ver detalles del incidente.
- **Administradores** pueden crear, editar y borrar incidentes.
- Los iconos 🔥, 🚗, 🏥, ☣️, ⚠️ indican el tipo de incidente.

---

### 4.5 Personal Operativo (Panel Central Derecho)

Tabla del personal con:
- Nombre, grado, unidad, estado, rol.
- **Estados:** En servicio, Disponible, En descanso, Herido.
- **Grados:** Comandante, Oficial, Suboficial, Brigadista.

**Administradores:**
- Pueden crear, editar y borrar personal.
- Pueden asignar personal a incidentes específicos.

---

### 4.6 Monitor de Recursos (Panel Inferior)

**Mapa (izquierda):**
- Muestra la ubicación de todos los recursos en el mapa de Argentina.
- Iconos según tipo: 🚒 Vehículo, 🚁 Helicóptero, 🏢 Estación, ⚙️ Equipo.
- Punto de color indicando estado: 🔴 En uso, 🟢 Disponible, 🟠 Mantenimiento, ⚪ Fuera de servicio.
- Barra de combustible visible en el popup.
- **Herramientas del móvil:** Lista visible en el popup del recurso.

**Tabla (derecha):**
- Lista detallada con nombre, unidad, estado y combustible.
- Barra de combustible con colores:
  - 🔴 Rojo (< 25%)
  - 🟠 Naranja (< 50%)
  - 🟢 Verde (> 50%)

**Administradores:**
- Pueden crear, editar y borrar recursos.
- Pueden editar las **herramientas del móvil** desde el modal.

---

### 4.7 Risk Trend + Riesgo por Zona (Panel Central)

**Risk Trend:**
- Gráfico de área que muestra la evolución del índice de riesgo a lo largo del tiempo.
- Tres métricas: **Riesgo Global**, **Ponderado** y **Neto**.

**Riesgo por Zona:**
- Gráfico de barras comparando el nivel de riesgo entre diferentes zonas.

**Administradores:**
- Pueden crear, editar y borrar métricas de riesgo.
- Campos: Zona, Nivel de riesgo (0-100%), Fecha/hora, Notas.

---

## 5. Header (Barra Superior)

### 5.1 Información del Sistema
- **Logo ARGOS** — Escudo del sistema.
- **Indicador de sistema** — Punto verde: "SISTEMA ACTIVO".

### 5.2 Clima en Tiempo Real
- **Temperatura** (ej: 24°C).
- **Viento** — Velocidad en km/h y dirección en grados.
- **Emoji** indicando condición (☀️, 🌧️, ⛈️, etc.).
- Actualiza automáticamente cada 5 minutos. Fuente: Open-Meteo.

### 5.3 Contadores
- **INCIDENTES** — Total activos.
- **ALERTAS** — Total sin leer.
- **Usuarios en línea** — Icono verde con cantidad.

### 5.4 Reloj
- Hora digital con segundos (HH:MM:SS).
- Fecha completa en español.

### 5.5 Usuario y Menú
- **Avatar** con inicial del nombre y color según rol.
- **Nombre** y **rol** del usuario.
- **Campana** — Icono de notificaciones con contador de alertas.
- **Menú desplegable:**
  - Gestión de usuarios (solo administradores).
  - Cerrar sesión.

---

## 6. Gestión de Usuarios (Solo Administradores)

1. Haga clic en su avatar en el header.
2. Seleccione **"Gestión de usuarios"**.
3. Se abre una ventana con todos los usuarios registrados.
4. **Acciones disponibles:**
   - Ver nombre, correo, departamento y rol.
   - **Hacer / Quitar administrador** — Cambia el rol entre `admin` y `viewer`.
   - **Eliminar usuario** — Botón de basura con confirmación (Sí/No).

---

## 7. Envío de Alertas a Brigadistas (Solo Administradores)

1. El sistema cuenta con una función de servidor (Edge Function) para enviar alertas masivas.
2. Permite enviar notificaciones críticas a todos los brigadistas logueados simultáneamente.
3. Las alertas aparecen instantáneamente en el panel de alertas de todos los usuarios en línea.

---

## 8. Movilización de Brigadistas

- El sistema registra automáticamente la **posición en tiempo real** de cada brigadista logueado.
- Cada usuario envía su ubicación GPS al servidor cada 60 segundos.
- Se muestra en el mapa como un punto de color:
  - 🔴 Administrador
  - 🟠 Operador
  - 🔵 Visualizador

---

## 9. Seguridad

- **Autenticación** por correo y contraseña (Supabase Auth).
- **RLS (Row Level Security)** — Solo los usuarios autenticados pueden acceder a los datos.
- **Protección por rol:**
  - Visualizadores solo pueden leer.
  - Operadores pueden crear/editar.
  - Administradores tienen control total.
- Las contraseñas se almacenan encriptadas.
- No se comparte información entre usuarios no autorizados.

---

## 10. Atajos y Consejos

| Acción | Descripción |
|--------|-------------|
| F5 | Refresca la página y recarga todos los datos en tiempo real. |
| Hacer clic en alerta | Marca la alerta como leída. |
| Botón "RUTA" | Activa el modo de dibujo de ruta de escape. |
| Hacer clic en mapa (modo RUTA) | Marca origen/destino. |
| Cerrar sesión | Disponible en el menú del avatar (esquina superior derecha). |

---

## 11. Soporte y Contacto

**ARGOS** — Centro de Mando

Sistema desarrollado por **IFRE.Soft**

© 2026 — Sistema Restringido

---

## 12. Glosario

| Término | Significado |
|---------|-------------|
| **Brigadista** | Personal de primera respuesta en campo. |
| **CRÍTICO** | Nivel máximo de severidad/riesgo. |
| **IGN** | Instituto Geográfico Nacional (tile layer del mapa de Argentina). |
| **RLS** | Row Level Security — Seguridad a nivel de fila en la base de datos. |
| **Edge Function** | Función de servidor para tareas como envío de alertas masivas. |
| **Track** | Registro de posición GPS de un brigadista a lo largo del tiempo. |

---

**Fin del Manual**
