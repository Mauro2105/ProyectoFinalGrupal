
---

# **Aplicación CRUD Full Stack con TypeScript, React, Vite y MongoDB**

Este proyecto es una aplicación CRUD (Crear, Leer, Actualizar, Eliminar) desarrollada utilizando tecnologías modernas del mercado. El sistema permite gestionar registros y está diseñado para ser escalable, robusto y eficiente.

---

## **📋 Características**

- **Frontend:** React + TypeScript con Vite.
- **Backend:** Node.js + Express con MongoDB como base de datos.
- **Interfaz moderna y responsiva.**
- **Endpoints CRUD funcionales.**
- **Despliegue listo para producción.**

---

## **🚀 Tecnologías Utilizadas**

### **Frontend**
- React ⚛️
- TypeScript 🛠️
- Vite 🚀
- Axios (para consumir la API)

### **Backend**
- Node.js 🌐
- Express 🚀
- MongoDB (con Mongoose) 📊
- Dotenv (para variables de entorno)
- CORS (para permitir comunicación entre frontend y backend)

---

## **📂 Estructura del Proyecto**

### **Backend**
```plaintext
backend/
├── src/
│   ├── config/         # Configuración de MongoDB
│   ├── controllers/    # Lógica de los endpoints CRUD
│   ├── models/         # Esquema de MongoDB
│   ├── routes/         # Rutas de la API
│   ├── server.ts       # Servidor principal
│   └── index.ts        # Punto de inicio
├── .env                # Variables de entorno
├── package.json        # Dependencias del proyecto
└── tsconfig.json       # Configuración de TypeScript
```

### **Frontend**
```plaintext
frontend/
├── src/
│   ├── components/     # Componentes de React
│   ├── services/       # Lógica para consumir la API
│   ├── App.tsx         # Componente principal
│   └── main.tsx        # Punto de entrada de React
├── vite.config.ts      # Configuración de Vite
├── package.json        # Dependencias del proyecto
└── tsconfig.json       # Configuración de TypeScript
```

---

## **🛠 Instalación y Configuración**

### **Requisitos Previos**
- Node.js y npm instalados.
- MongoDB configurado en tu máquina o en un servidor (puedes usar MongoDB Atlas).

---

### **1. Clonar el Repositorio**
```bash
git clone https://github.com/tu-usuario/tu-repositorio.git
cd tu-repositorio
```

---

### **2. Configurar el Backend**

1. Ve a la carpeta del backend:
   ```bash
   cd backend
   ```

2. Instala las dependencias:
   ```bash
   npm install
   ```

3. Crea el archivo **.env**:
   ```plaintext
   PORT=5000
   MONGODB_URI="mongodb://localhost:27017/nombre_base_datos"
   ```

4. Inicia el servidor:
   ```bash
   npx ts-node src/server.ts
   ```

5. El servidor estará disponible en `http://localhost:5000`.

---

### **3. Configurar el Frontend**

1. Ve a la carpeta del frontend:
   ```bash
   cd frontend
   ```

2. Instala las dependencias:
   ```bash
   npm install
   ```

3. Inicia el proyecto en desarrollo:
   ```bash
   npm run dev
   ```

4. El frontend estará disponible en `http://localhost:5173`.

---

## **🌐 Endpoints de la API**

| Método | Endpoint           | Descripción                 |
|--------|--------------------|-----------------------------|
| GET    | `/api/registros`   | Obtener todos los registros |
| POST   | `/api/registros`   | Crear un nuevo registro     |
| PUT    | `/api/registros/:id` | Actualizar un registro por ID |
| DELETE | `/api/registros/:id` | Eliminar un registro por ID   |

---

## **🖥 Despliegue**

1. **Backend:** Puedes desplegarlo en **Render**, **Heroku** o cualquier VPS.
2. **Base de Datos:** Configura MongoDB Atlas para acceder desde la nube.
3. **Frontend:** Despliega en **Vercel**, **Netlify** o **GitHub Pages**.

---




# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type aware lint rules:

- Configure the top-level `parserOptions` property like this:

```js
export default tseslint.config({
  languageOptions: {
    // other options...
    parserOptions: {
      project: ['./tsconfig.node.json', './tsconfig.app.json'],
      tsconfigRootDir: import.meta.dirname,
    },
  },
})
```

- Replace `tseslint.configs.recommended` to `tseslint.configs.recommendedTypeChecked` or `tseslint.configs.strictTypeChecked`
- Optionally add `...tseslint.configs.stylisticTypeChecked`
- Install [eslint-plugin-react](https://github.com/jsx-eslint/eslint-plugin-react) and update the config:

```js
// eslint.config.js
import react from 'eslint-plugin-react'

export default tseslint.config({
  // Set the react version
  settings: { react: { version: '18.3' } },
  plugins: {
    // Add the react plugin
    react,
  },
  rules: {
    // other rules...
    // Enable its recommended rules
    ...react.configs.recommended.rules,
    ...react.configs['jsx-runtime'].rules,
  },
})
```
