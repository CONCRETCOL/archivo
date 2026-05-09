# 📦 SysInventa — Sistema de Control de Inventarios

Sistema web completo de control de inventarios con 4 roles de usuario, seguridad avanzada y control de entradas/producción/salidas.

---

## 🚀 Despliegue en GitHub Pages

1. Crea un repositorio en GitHub (público o privado)
2. Sube el archivo `index.html` a la raíz del repositorio
3. Ve a **Settings → Pages → Source: Deploy from branch → main / root**
4. Tu sistema estará disponible en: `https://TU_USUARIO.github.io/TU_REPO/`

---

## 👥 Usuarios del Sistema

| Usuario       | Contraseña        | Rol          | Permisos |
|---------------|-------------------|--------------|----------|
| `compras`     | `Compras2024!`    | COMPRAS      | Registrar compras y catálogo de materias primas |
| `produccion`  | `Produccion2024!` | PRODUCCIÓN   | Solo registrar órdenes de producción |
| `despachos`   | `Despachos2024!`  | DESPACHOS    | Solo registrar pedidos/despachos de productos |
| `admin`       | `Admin2024!`      | ADMIN        | Acceso completo a todo el sistema |

> ⚠️ **Cambia las contraseñas inmediatamente** al primer ingreso usando la opción "Mi Contraseña" en el menú lateral.

---

## 🔐 Características de Seguridad

| Capa | Descripción |
|------|-------------|
| **RBAC** | Control de acceso basado en roles — cada usuario solo ve su módulo |
| **Bloqueo por intentos** | 5 intentos fallidos → bloqueo de 15 minutos |
| **Timeout de sesión** | Bloqueo automático por inactividad (20 minutos) |
| **Auditoría completa** | Registro de TODAS las acciones con usuario, hora y detalle |
| **Sanitización XSS** | Todos los datos se escapan antes de renderizar |
| **Validación de datos** | Validación estricta en todos los formularios |
| **Watermark de sesión** | Marca de agua con usuario y fecha en cada pantalla |
| **Contraseñas seguras** | Mínimo 8 caracteres, mayúscula y número requeridos |
| **Detección DevTools** | Alerta en auditoría si se detectan herramientas de desarrollo |

---

## 📋 Módulos del Sistema

### 📦 COMPRAS
- Registrar compras de materias primas
- Gestionar catálogo de materias primas
- Cada compra actualiza automáticamente el stock

### 🏭 PRODUCCIÓN
- Registrar órdenes de producción
- Seleccionar producto terminado y materia prima consumida
- Actualiza automáticamente stock de productos terminados y descuenta materias primas

### 🚚 DESPACHOS
- Registrar pedidos de productos terminados vendidos
- Verificación automática de stock disponible
- Descuenta automáticamente del inventario

### 👑 ADMINISTRACIÓN
- Dashboard con estadísticas en tiempo real
- Inventario general (materias primas + productos terminados)
- Vista completa de compras, producción y despachos
- Gestión de usuarios y contraseñas
- Log de auditoría con exportación CSV

---

## 💾 Almacenamiento

El sistema usa `localStorage` del navegador para persistencia de datos. Los datos se guardan localmente en el dispositivo. **Para uso en red:** todos los usuarios deben usar el mismo navegador/dispositivo, o se requiere una solución de backend (Firebase, Supabase, etc.).

---

## 🛠️ Tecnologías

- **HTML5 + CSS3 + JavaScript Vanilla** — Sin dependencias externas
- **Fonts:** Google Fonts (Syne, DM Sans, DM Mono)
- **Almacenamiento:** localStorage
- **Compatible:** Chrome, Firefox, Edge, Safari (moderno)

---

## ⚡ Personalización

Para cambiar el nombre de la empresa, busca `SysInventa` en el `index.html` y reemplázalo.

Para agregar más usuarios, modifica el array `users` dentro de la función `initData()` en el script.

---

*Sistema desarrollado para control de inventarios con 4 roles diferenciados y seguridad multicapa.*
