# 💈 Barbería Pro

**Sistema POS profesional para barberías** — Turnos, servicios, clientes, caja, reportes y membresías.

> Desarrollado por **A2K Digital Studio**

---

## 🚀 Despliegue

- **URL en producción:** [https://tiendadigitalaipro.github.io/barberia-pro/](https://tiendadigitalaipro.github.io/barberia-pro/)
- **Hosting:** GitHub Pages
- **Arquitectura:** 100% client-side (sin backend, sin Firebase)

---

## 📦 Archivos del Proyecto

| Archivo | Descripción |
|---|---|
| `index.html` | Punto de entrada — redirige a la app principal |
| `barberia-pro.html` | App principal (~1498 líneas) |
| `bp-admin-licencias.html` | Panel de administración de licencias |
| `barber-logo.png` | Logo de la aplicación |
| `ESTRUCTURA.md` | Mapa detallado de archivos y secciones |
| `MANTENIMIENTO.md` | Guía rápida de modificaciones comunes |

---

## ✨ Funcionalidades

| Módulo | Descripción |
|---|---|
| **POS** | Punto de venta con carrito y cobro |
| **Dashboard** | Resumen general del negocio |
| **Agenda** | Gestión de turnos y citas |
| **Clientes** | Base de datos de clientes |
| **Productos** | Inventario de productos |
| **Caja** | Apertura/cierre de caja |
| **Reportes** | Estadísticas y reportes |
| **Barberos** | Gestión de barberos |
| **Cola** | Sistema de cola de espera |
| **Membresías** | Gestión de planes de membresía |
| **Config** | Configuración general |

---

## 💰 Métodos de Pago

Se soportan **10 métodos de pago** con moneda dual (**$ / Bs**):

- Efectivo $, Efectivo Bs, Pago Móvil, Transferencia, Punto de Venta, Zelle, PayPal, Tarjeta Débito, Tarjeta Crédito, Otro

---

## 🔐 Sistema de Licencias (IRON LOCK v2)

| Parámetro | Valor |
|---|---|
| **Salt** | `BPBARBER2026` |
| **Admin Password** | `BP2026ADMIN` |
| **Master Codes** | `BP-PRO-DEMO-2024`, `BP-PRO-A2K-2026`, `BP-PRO-MAST-2026` |
| **Prefijo localStorage** | `bp_` |

---

## 📊 Datos por Defecto

- **90 servicios** preconfigurados
- **46 productos** precargados

---

## 🎨 Identidad Visual

```css
--gold: #c9a96e;    /* Color principal dorado */
--bg: #0a0a0a;      /* Fondo oscuro */
```

---

## 🛠️ Stack Técnico

- HTML5 + CSS3 + JavaScript vanilla
- localStorage para persistencia de datos
- Sin dependencias externas
- Compatible con dispositivos móviles y escritorio
