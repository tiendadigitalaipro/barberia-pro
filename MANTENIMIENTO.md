# 🔧 MANTENIMIENTO — Barbería Pro

Guía rápida para modificaciones comunes. Todas las ediciones se realizan en `barberia-pro.html` salvo indicación contraria.

---

## 🎨 Cambiar Colores

**Archivo:** `barberia-pro.html` → **Línea 10** (CSS Variables)

```css
:root {
  --gold: #c9a96e;    /* Color principal — cambiar aquí */
  --bg: #0a0a0a;      /* Fondo general */
  --text: #ffffff;    /* Color de texto */
  /* ... más variables */
}
```

> Modifica los valores hexadecimales para ajustar la paleta completa.

---

## 🏪 Cambiar Nombre del Negocio

**Opción 1 — Desde la app:** Ir a **Config** y editar el nombre del negocio.

**Opción 2 — Valor por defecto en código:**
`barberia-pro.html` → **Línea 518**

```javascript
nombre: 'Barbería Pro'  // Cambiar aquí el nombre por defecto
```

---

## ✂️ Agregar / Editar Servicios

**Archivo:** `barberia-pro.html` → **Líneas 555–646**

Cada servicio se define como un objeto:

```javascript
{ id: 1, nombre: 'Corte Clásico', precio: 10, duracion: 30, categoria: 'Cortes' }
```

**Campos:**
| Campo | Tipo | Descripción |
|---|---|---|
| `id` | Number | Identificador único |
| `nombre` | String | Nombre del servicio |
| `precio` | Number | Precio en dólares ($) |
| `duracion` | Number | Duración en minutos |
| `categoria` | String | Categoría del servicio |

---

## 💳 Agregar Métodos de Pago

**Archivo:** `barberia-pro.html` → **Líneas 890–901**

```javascript
const metodos = [
  { id: 'efectivo_usd', nombre: 'Efectivo $', moneda: 'USD' },
  { id: 'efectivo_bs',  nombre: 'Efectivo Bs', moneda: 'BS' },
  // Agregar nuevo método:
  { id: 'nuevo_metodo', nombre: 'Nuevo Método', moneda: 'USD' },
];
```

---

## 🔑 Cambiar Contraseña de Admin

**Archivo:** `bp-admin-licencias.html` → **Línea 71**

```javascript
const ADMIN_PASS = 'BP2026ADMIN';  // Cambiar aquí
```

---

## 🔐 Cambiar Salt del Sistema de Licencias

**Archivo:** `barberia-pro.html` → **Línea 525**

```javascript
const SALT = 'BPBARBER2026';  // Cambiar aquí
```

> ⚠️ **Importante:** Cambiar el salt invalidará todas las licencias activas existentes.

---

## 💱 Cambiar Tasa de Cambio

**Opción 1 — Desde la app:** Ir a **Config** y modificar la tasa.

**Opción 2 — Valor por defecto:**
`barberia-pro.html` → **Línea 518**

```javascript
tasa: 50.00  // Tasa de cambio por defecto (1 USD = 50 Bs)
```

---

## ✂️ Agregar un Nuevo Barbero

Los barberos se almacenan dinámicamente en localStorage bajo la clave `bp_barberos`. Se pueden agregar:

1. **Desde la app:** Módulo **Barberos** → Agregar barbero
2. **Directo en localStorage:**
```javascript
const barberos = JSON.parse(localStorage.getItem('bp_barberos') || '[]');
barberos.push({ id: Date.now(), nombre: 'Nuevo Barbero', comision: 50 });
localStorage.setItem('bp_barberos', JSON.stringify(barberos));
```

---

## 🔄 Resetear Demo / Datos

Ejecutar en la **consola del navegador** (F12 → Console):

```javascript
localStorage.clear();
location.reload();
```

Esto elimina todos los datos almacenados y restaura la app a su estado inicial.

---

## 🐛 Bugs Conocidos

| Bug | Ubicación | Descripción |
|---|---|---|
| Comisión de barbero siempre true | **Línea 1321** (`\|\|true`) | La condición `comision > 0 \|\| true` siempre evalúa a `true`, por lo que la comisión se calcula independientemente del valor configurado. **Fix:** eliminar `\|\|true` de esa línea. |

---

## 📋 Atajos de Teclado

Sección de atajos en **Líneas 1450–1498**. Los atajos están definidos en el event listener de `keydown`.
