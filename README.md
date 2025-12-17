# 🧾 Invoice Manager System

<div align="center">

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

**Sistema de Gestión de Facturas Web - Profesional, Moderno y Eficiente**

[Características](#-características) •
[Tecnologías](#-tecnologías) •
[Instalación](#-instalación) •
[Uso](#-uso) •
[API](#-api-endpoints) •
[Contribuir](#-cómo-contribuir)

[![Stars](https://img.shields.io/github/stars/danielcastillomera/invoice-manager-system?style=social)](https://github.com/danielcastillomera/invoice-manager-system/stargazers)
[![Forks](https://img.shields.io/github/forks/danielcastillomera/invoice-manager-system?style=social)](https://github.com/danielcastillomera/invoice-manager-system/forks)
[![Issues](https://img.shields.io/github/issues/danielcastillomera/invoice-manager-system)](https://github.com/danielcastillomera/invoice-manager-system/issues)

</div>

---

## 📖 Descripción

**Invoice Manager System** es una aplicación web completa para la gestión profesional de facturas. Desarrollada con tecnologías modernas, ofrece una interfaz intuitiva y un backend robusto para administrar clientes, productos, servicios y facturas de manera eficiente.

### 🎯 Objetivo del Proyecto

Proporcionar una solución integral y fácil de usar para pequeñas y medianas empresas que necesitan gestionar su facturación de manera profesional, con generación de PDF, seguimiento de pagos y reportes detallados.

---

## ✨ Características

### 🔥 Funcionalidades Principales

- **📝 Gestión de Facturas**
  - Creación rápida de facturas
  - Edición y duplicación de facturas existentes
  - Eliminación segura con confirmación
  - Numeración automática y consecutiva

- **👥 Administración de Clientes**
  - Base de datos de clientes completa
  - Información de contacto y facturación
  - Historial de facturas por cliente
  - Búsqueda y filtrado avanzado

- **🛍️ Catálogo de Productos/Servicios**
  - Gestión de inventario
  - Precios y descripciones detalladas
  - Categorización flexible
  - Stock y disponibilidad

- **💰 Control Financiero**
  - Dashboard con métricas en tiempo real
  - Reportes de ventas
  - Seguimiento de pagos pendientes
  - Análisis de ingresos por período

- **📄 Generación de Documentos**
  - Exportación a PDF profesional
  - Plantillas personalizables
  - Logo y marca personalizada
  - Envío automático por email

- **🔐 Seguridad**
  - Autenticación de usuarios
  - Roles y permisos
  - Protección de datos sensibles
  - Sesiones seguras

---

## 🛠️ Tecnologías

<div align="center">

### Frontend

| Tecnología | Descripción |
|-----------|-------------|
| **TypeScript** | Tipado estático para mayor confiabilidad |
| **React.js** | Biblioteca para interfaces de usuario |
| **CSS3** | Estilos modernos y responsivos |
| **Vite** | Build tool ultra rápido |

### Backend

| Tecnología | Descripción |
|-----------|-------------|
| **Node.js** | Runtime de JavaScript |
| **Express** | Framework web minimalista |
| **TypeScript** | Para backend type-safe |
| **MongoDB/PostgreSQL** | Base de datos |

</div>

---

## 📋 Requisitos Previos

Asegúrate de tener instalado:

- **Node.js** (v16 o superior)
- **npm** o **yarn**
- **Git**
- **MongoDB** o **PostgreSQL** (según configuración)

---

## 🚀 Instalación

### 1️⃣ Clonar el Repositorio
```bash
git clone https://github.com/danielcastillomera/invoice-manager-system.git
cd invoice-manager-system
```

### 2️⃣ Instalar Dependencias del Backend
```bash
cd server
npm install
# o
yarn install
```

### 3️⃣ Configurar Variables de Entorno

Crea un archivo `.env` en la carpeta `server`:
```env
# Server Configuration
PORT=5000
NODE_ENV=development

# Database
DATABASE_URL=mongodb://localhost:27017/invoice-manager
# o para PostgreSQL
# DATABASE_URL=postgresql://user:password@localhost:5432/invoice-manager

# JWT Secret
JWT_SECRET=your_super_secret_key_here
JWT_EXPIRE=7d

# Email Configuration (opcional)
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your-email@gmail.com
SMTP_PASS=your-email-password

# Frontend URL
CLIENT_URL=http://localhost:3000
```

### 4️⃣ Instalar Dependencias del Frontend
```bash
cd ../client
npm install
# o
yarn install
```

### 5️⃣ Configurar Variables de Entorno del Frontend

Crea un archivo `.env` en la carpeta `client`:
```env
VITE_API_URL=http://localhost:5000/api
VITE_APP_NAME=Invoice Manager
```

### 6️⃣ Iniciar la Base de Datos
```bash
# Para MongoDB
mongod

# Para PostgreSQL
sudo service postgresql start
```

### 7️⃣ Ejecutar las Migraciones (si aplica)
```bash
cd server
npm run migrate
# o
npm run db:setup
```

### 8️⃣ Iniciar el Backend
```bash
cd server
npm run dev
```

El servidor estará corriendo en `http://localhost:5000`

### 9️⃣ Iniciar el Frontend

En otra terminal:
```bash
cd client
npm run dev
```

La aplicación estará disponible en `http://localhost:3000`

---

## 📂 Estructura del Proyecto
```
invoice-manager-system/
│
├── 📁 client/                    # Frontend de la aplicación
│   ├── 📁 public/               # Archivos estáticos
│   ├── 📁 src/
│   │   ├── 📁 assets/           # Imágenes, fuentes, etc.
│   │   ├── 📁 components/       # Componentes React reutilizables
│   │   │   ├── 📄 Invoice.tsx
│   │   │   ├── 📄 InvoiceForm.tsx
│   │   │   ├── 📄 ClientList.tsx
│   │   │   └── 📄 Dashboard.tsx
│   │   ├── 📁 pages/            # Páginas principales
│   │   │   ├── 📄 Home.tsx
│   │   │   ├── 📄 Invoices.tsx
│   │   │   ├── 📄 Clients.tsx
│   │   │   └── 📄 Products.tsx
│   │   ├── 📁 services/         # Servicios API
│   │   │   └── 📄 api.ts
│   │   ├── 📁 store/            # Estado global (Redux/Context)
│   │   ├── 📁 utils/            # Funciones utilitarias
│   │   ├── 📁 types/            # Tipos TypeScript
│   │   ├── 📄 App.tsx           # Componente principal
│   │   └── 📄 main.tsx          # Punto de entrada
│   ├── 📄 package.json
│   ├── 📄 tsconfig.json
│   └── 📄 vite.config.ts
│
├── 📁 server/                    # Backend de la aplicación
│   ├── 📁 src/
│   │   ├── 📁 config/           # Configuración
│   │   │   └── 📄 database.ts
│   │   ├── 📁 controllers/      # Controladores
│   │   │   ├── 📄 invoiceController.ts
│   │   │   ├── 📄 clientController.ts
│   │   │   └── 📄 productController.ts
│   │   ├── 📁 models/           # Modelos de datos
│   │   │   ├── 📄 Invoice.ts
│   │   │   ├── 📄 Client.ts
│   │   │   └── 📄 Product.ts
│   │   ├── 📁 routes/           # Rutas de la API
│   │   │   ├── 📄 invoices.ts
│   │   │   ├── 📄 clients.ts
│   │   │   └── 📄 products.ts
│   │   ├── 📁 middleware/       # Middleware personalizado
│   │   │   ├── 📄 auth.ts
│   │   │   └── 📄 errorHandler.ts
│   │   ├── 📁 services/         # Lógica de negocio
│   │   │   ├── 📄 pdfService.ts
│   │   │   └── 📄 emailService.ts
│   │   ├── 📁 utils/            # Utilidades
│   │   └── 📄 index.ts          # Punto de entrada
│   ├── 📄 package.json
│   └── 📄 tsconfig.json
│
├── 📄 .gitignore
├── 📄 README.md
└── 📄 LICENSE
```

---

## 💻 Uso

### Crear una Nueva Factura

1. Navega a **"Nueva Factura"** en el menú
2. Selecciona o crea un cliente
3. Agrega productos/servicios con cantidades
4. Revisa el resumen
5. Guarda y/o genera el PDF

### Gestionar Clientes

1. Ve a la sección **"Clientes"**
2. Haz clic en **"Agregar Cliente"**
3. Completa la información requerida
4. Guarda los cambios

### Ver Dashboard

El dashboard muestra:
- Total de facturas del mes
- Ingresos totales
- Facturas pendientes
- Gráficos de ventas
- Últimas transacciones

---

## 🔌 API Endpoints

### Facturas
```http
GET    /api/invoices           # Obtener todas las facturas
GET    /api/invoices/:id       # Obtener una factura específica
POST   /api/invoices           # Crear nueva factura
PUT    /api/invoices/:id       # Actualizar factura
DELETE /api/invoices/:id       # Eliminar factura
GET    /api/invoices/:id/pdf   # Generar PDF de factura
```

### Clientes
```http
GET    /api/clients            # Obtener todos los clientes
GET    /api/clients/:id        # Obtener un cliente específico
POST   /api/clients            # Crear nuevo cliente
PUT    /api/clients/:id        # Actualizar cliente
DELETE /api/clients/:id        # Eliminar cliente
```

### Productos
```http
GET    /api/products           # Obtener todos los productos
GET    /api/products/:id       # Obtener un producto específico
POST   /api/products           # Crear nuevo producto
PUT    /api/products/:id       # Actualizar producto
DELETE /api/products/:id       # Eliminar producto
```

### Autenticación
```http
POST   /api/auth/register      # Registrar usuario
POST   /api/auth/login         # Iniciar sesión
GET    /api/auth/me            # Obtener usuario actual
POST   /api/auth/logout        # Cerrar sesión
```

---

## 🧪 Testing
```bash
# Backend tests
cd server
npm test

# Frontend tests
cd client
npm test

# E2E tests
npm run test:e2e

# Coverage
npm run test:coverage
```

---

## 📦 Build para Producción

### Backend
```bash
cd server
npm run build
npm start
```

### Frontend
```bash
cd client
npm run build
```

Los archivos optimizados estarán en `client/dist`

---

## 🐳 Docker (Opcional)
```bash
# Construir imágenes
docker-compose build

# Iniciar servicios
docker-compose up -d

# Ver logs
docker-compose logs -f

# Detener servicios
docker-compose down
```

---

## 🤝 Cómo Contribuir

¡Las contribuciones son bienvenidas! Sigue estos pasos:

### 1️⃣ Fork el Proyecto

Haz clic en el botón "Fork" en la parte superior derecha

### 2️⃣ Clona tu Fork
```bash
git clone https://github.com/TU-USUARIO/invoice-manager-system.git
cd invoice-manager-system
```

### 3️⃣ Crea una Rama
```bash
git checkout -b feature/nueva-caracteristica
```

### 4️⃣ Realiza tus Cambios
```bash
git add .
git commit -m "✨ Agregar nueva característica"
```

### 5️⃣ Push a tu Fork
```bash
git push origin feature/nueva-caracteristica
```

### 6️⃣ Abre un Pull Request

Ve a GitHub y crea un Pull Request desde tu rama

### 📋 Guías de Contribución

- ✅ Escribe código limpio y legible
- ✅ Sigue las convenciones de TypeScript
- ✅ Agrega pruebas para nuevas funcionalidades
- ✅ Actualiza la documentación si es necesario
- ✅ Asegúrate de que todos los tests pasen
- ✅ Usa commits descriptivos (Conventional Commits)

---

## 🎨 Capturas de Pantalla

<div align="center">

### Dashboard Principal
![Dashboard](https://via.placeholder.com/800x400?text=Dashboard+Principal)

### Lista de Facturas
![Facturas](https://via.placeholder.com/800x400?text=Lista+de+Facturas)

### Crear Nueva Factura
![Nueva Factura](https://via.placeholder.com/800x400?text=Crear+Nueva+Factura)

### Vista PDF
![PDF](https://via.placeholder.com/800x400?text=Vista+PDF+de+Factura)

</div>

---

## 🗺️ Roadmap

- [x] Gestión básica de facturas
- [x] CRUD de clientes
- [x] CRUD de productos
- [x] Generación de PDF
- [ ] Dashboard con estadísticas
- [ ] Sistema de autenticación completo
- [ ] Roles y permisos avanzados
- [ ] Notificaciones por email
- [ ] Multi-moneda
- [ ] Multi-idioma (i18n)
- [ ] Modo oscuro
- [ ] App móvil (React Native)
- [ ] Integración con sistemas de pago
- [ ] Facturación recurrente
- [ ] API pública con documentación Swagger

---

## 📝 Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.
```
MIT License

Copyright (c) 2024 Daniel Castillo Mera

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 👨‍💻 Autor

<div align="center">

**Daniel Fernando Castillo Mera**

[![GitHub](https://img.shields.io/badge/GitHub-@danielcastillomera-181717?style=for-the-badge&logo=github)](https://github.com/danielcastillomera)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin)](https://linkedin.com/in/danielcastillomera)
[![Email](https://img.shields.io/badge/Email-Contact-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:daniel@example.com)

</div>

---

## 🙏 Agradecimientos

- Gracias a todos los [contribuidores](https://github.com/danielcastillomera/invoice-manager-system/graphs/contributors)
- Inspirado en las mejores prácticas de desarrollo web moderno
- Comunidad de TypeScript, React y Node.js

---

## 📊 Estado del Proyecto

<div align="center">

![GitHub last commit](https://img.shields.io/github/last-commit/danielcastillomera/invoice-manager-system)
![GitHub issues](https://img.shields.io/github/issues/danielcastillomera/invoice-manager-system)
![GitHub pull requests](https://img.shields.io/github/issues-pr/danielcastillomera/invoice-manager-system)
![Code size](https://img.shields.io/github/languages/code-size/danielcastillomera/invoice-manager-system)

**Estado**: 🟢 Activo | **Versión**: 1.0.0 | **Última actualización**: Diciembre 2024

</div>

---

## 🔗 Links Útiles

- [Documentación Completa](https://github.com/danielcastillomera/invoice-manager-system/wiki)
- [Issues y Bugs](https://github.com/danielcastillomera/invoice-manager-system/issues)
- [Discussions](https://github.com/danielcastillomera/invoice-manager-system/discussions)
- [Changelog](https://github.com/danielcastillomera/invoice-manager-system/blob/main/CHANGELOG.md)

---

<div align="center">

**⭐ Si este proyecto te fue útil, considera darle una estrella ⭐**

**Hecho con ❤️ y ☕ por [Daniel Fernando Castillo Mera](https://github.com/danielcastillomera)**

</div>
