# 📁 ESTRUCTURA — Barbería Pro

Mapa completo de archivos y secciones de código.

---

## 🗂️ Archivos

| Archivo | Líneas | Descripción |
|---|---|---|
| `index.html` | — | Punto de entrada. Redirige automáticamente a `barberia-pro.html` |
| `barberia-pro.html` | ~1498 | App principal (CSS + HTML + JS en un solo archivo) |
| `bp-admin-licencias.html` | ~122 | Panel de administración de licencias |
| `barber-logo.png` | — | Logo de la aplicación |

---

## 📐 barberia-pro.html — Mapa de Secciones

### CSS (Líneas 1–460)

| Líneas | Sección |
|---|---|
| 1–9 | Meta tags, título, fuentes externas |
| **10–20** | **Variables CSS** (colores, fuentes, spacing) |
| 21–225 | Estilos generales, componentes, tarjetas, tablas, modales |

### HTML (Líneas 226–507)

| Líneas | Sección | Módulo |
|---|---|---|
| **226–255** | Punto de Venta | POS |
| **257–260** | Panel principal | Dashboard |
| **262–274** | Gestión de turnos | Agenda |
| **276–285** | Base de clientes | Clientes |
| **287–299** | *(sección intermedia)* | — |
| **301–309** | Inventario | Productos |
| **311–317** | Arqueo de caja | Caja |
| **319–325** | Estadísticas | Reportes |
| **327–334** | Equipo | Barberos |
| **336–343** | Cola de espera | Cola |
| **345–352** | Planes | Membresías |
| **354–360** | Ajustes | Config |
| 361–507 | Modales, controles, estructura general | — |

### JavaScript (Líneas 508–1498)

| Líneas | Sección |
|---|---|
| **508–524** | **DB helper y utilidades generales** |
| **525–545** | **Sistema de licencias IRON LOCK** |
| **546–696** | **Datos por defecto** (servicios, productos) |
| 547–646 | Servicios por defecto (90 servicios) |
| 647–696 | Productos por defecto (46 productos) |
| **697–790** | **Inicialización y navegación** |
| 725–791 | Renderizado de secciones, navegación entre módulos |
| **792–970** | **Lógica POS** (búsqueda, selección, carrito) |
| **971–1010** | **Carrito y checkout** (procesamiento de pagos) |
| 890–901 | Métodos de pago (10 métodos) |
| **1011–1036** | Dashboard (cálculo de estadísticas) |
| **1037–1100** | **Lógica Agenda** (citas, turnos) |
| **1101–1207** | **Clientes y Productos** (CRUD) |
| 1101–1153 | Clientes |
| 1154–1207 | Productos |
| **1209–1310** | **Caja y Reportes** |
| **1310–1400** | **Barberos y Cola** |
| 1321 | ⚠️ Bug conocido: comisión de barbero (`||true`) |
| **1400–1450** | **Membresías y Config** |
| **1450–1498** | **Licencia y atajos de teclado** |

---

## 🔧 bp-admin-licencias.html — Mapa

| Líneas | Sección |
|---|---|
| 1–70 | HTML y estilos del panel admin |
| **71** | Contraseña admin por defecto (`BP2026ADMIN`) |
| 72–122 | Lógica de validación y gestión de licencias |

---

## 🗄️ Claves localStorage

| Prefijo | Clave | Descripción |
|---|---|---|
| `bp_` | `bp_barberos` | Lista de barberos |
| `bp_` | `bp_servicios` | Servicios personalizados |
| `bp_` | `bp_productos` | Productos del inventario |
| `bp_` | `bp_clientes` | Base de datos de clientes |
| `bp_` | `bp_ventas` | Historial de ventas |
| `bp_` | `bp_caja` | Estado de caja |
| `bp_` | `bp_config` | Configuración general |
| `bp_` | `bp_licencia_activa` | Estado de licencia |
| `bp_` | `bp_membresias` | Planes de membresía |

> Para resetear toda la app: `localStorage.clear()` en consola del navegador.
