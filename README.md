# 🔐 React Login & Role-Based Dashboard

Aplicación web interactiva de autenticación y panel de control (Dashboard) con vistas diferenciadas según el rol del usuario (**Administrador** y **Usuario Estándar**). Desarrollada como una Single Page Application (SPA) modular utilizando **React** y **Vite**.

---

## 📋 Características Principales

* **Autenticación de Usuarios (`LoginPage`):** Formulario de inicio de sesión validado contra un catálogo local de credenciales y roles (`users.js`).
* **Control de Acceso Basado en Roles (RBAC):** Redirección y renderizado condicional de vistas según el perfil del usuario autenticado:
  * **Panel de Administración (`AdminDashboard`):** Vista integral con métricas generales, tarjetas de estadísticas y tabla de gestión de datos/usuarios.
  * **Panel de Usuario (`UserDashboard`):** Vista personalizada enfocada en la información, actividad y métricas individuales del usuario.
* **Arquitectura de Diseño Reutilizable (`layout/`):** Estructura consistente compuesta por barra lateral de navegación (`Sidebar`), barra superior (`Navbar`) y contenedor principal (`DashboardLayout`).
* **Visualización de Datos (`dashboard/`):** Componentes especializados para mostrar indicadores clave de rendimiento (`StatCard`) y registros tabulares (`DataTable`).
* **Sistema de Componentes UI Propio (`common/`):** Elementos de interfaz estandarizados y reutilizables (`Button`, `Card`, `InputField`).

---

## 🛠️ Tecnologías Utilizadas

* **Librería UI:** [React](https://react.dev/) (JSX, Hooks, Props, Renderizado Condicional)
* **Entorno de Desarrollo y Empaquetador:** [Vite](https://vitejs.dev/)
* **Estilos:** CSS3 (`index.css`)
* **Linter y Calidad de Código:** ESLint (`eslint.config.js`)
* **Gestor de Paquetes:** npm

---

## 📂 Estructura del Proyecto

El proyecto implementa una arquitectura escalable separando páginas, layouts, componentes de negocio, componentes atómicos y datos:

```text
lab_react_login-dashboard/
├── public/
│   ├── favicon.svg                      # Ícono de la pestaña del navegador
│   └── icons.svg                        # Iconografía vectorial pública
├── src/
│   ├── components/
│   │   ├── common/                      # Componentes UI atómicos y reutilizables
│   │   │   ├── Button.jsx               # Botón personalizable
│   │   │   ├── Card.jsx                 # Contenedor tipo tarjeta
│   │   │   └── InputField.jsx           # Campo de entrada de texto/formulario
│   │   ├── dashboard/                   # Componentes exclusivos de visualización de datos
│   │   │   ├── DataTable.jsx            # Tabla dinámica de registros
│   │   │   └── StatCard.jsx             # Tarjeta de métricas y estadísticas (KPIs)
│   │   └── layout/                      # Estructura base de navegación
│   │       ├── DashboardLayout.jsx      # Plantilla envolvente de los paneles
│   │       ├── Navbar.jsx               # Barra superior de usuario/sesión
│   │       └── Sidebar.jsx              # Menú lateral de navegación
│   ├── data/
│   │   └── users.js                     # Datos simulados de usuarios, credenciales y roles
│   ├── pages/
│   │   ├── AdminDashboard.jsx           # Vista principal para el rol Administrador
│   │   ├── LoginPage.jsx                # Pantalla de inicio de sesión
│   │   └── UserDashboard.jsx            # Vista principal para el rol Usuario
│   ├── App.jsx                          # Componente raíz y manejo de estado de sesión
│   ├── index.css                        # Estilos globales y diseño del sistema
│   └── main.jsx                         # Punto de montaje de React en el DOM
├── .gitignore                           # Archivos ignorados por Git
├── eslint.config.js                     # Configuración de reglas de ESLint
├── index.html                           # Documento HTML principal
├── package.json                         # Dependencias y scripts del proyecto
└── vite.config.js                       # Configuración de Vite
```

---

## 🚀 Instalación y Ejecución Local

Sigue estos pasos para clonar y ejecutar el proyecto en tu entorno de desarrollo:

### Prerrequisitos

Tener instalado [Node.js](https://nodejs.org/) (versión 18 o superior recomendada) y `npm`.

### Pasos

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/Alexis4rias/lab_react_login-dashboard.git
   ```

2. **Navegar a la carpeta del proyecto:**
   ```bash
   cd lab_react_login-dashboard
   ```

3. **Instalar las dependencias:**
   ```bash
   npm install
   ```

4. **Iniciar el servidor de desarrollo:**
   ```bash
   npm run dev
   ```

5. **Abrir en el navegador:**
   Ingresa a la dirección local mostrada en tu terminal (por defecto `http://localhost:5173/`).

---

## 🔑 Uso y Credenciales de Prueba

Los usuarios de prueba y sus respectivos roles (`admin` / `user`) se encuentran definidos dentro del archivo:
```text
src/data/users.js
```
Puedes consultar o agregar nuevas cuentas directamente en ese archivo para probar la redirección entre `AdminDashboard` y `UserDashboard`.

---

## 📜 Scripts Disponibles

Comandos configurados dentro de `package.json`:

* `npm run dev` — Inicia el servidor de desarrollo local con Hot Module Replacement (HMR).
* `npm run build` — Compila y optimiza la aplicación para producción dentro del directorio `dist/`.
* `npm run lint` — Ejecuta ESLint para verificar buenas prácticas en el código.
* `npm run preview` — Levanta un servidor local para previsualizar el empaquetado de producción.

---

## 👤 Autor

* **Jesús Alexis Arias Ricárdez** — [@Alexis4rias](https://github.com/Alexis4rias)

---

## 📄 Licencia

Este proyecto fue desarrollado con fines académicos y de portafolio (Laboratorio de React + Vite).