# AppNode

AppNode es un proyecto base desarrollado en Node.js y Express que incluye un sistema de autenticación dinámico con funciones de registro y inicio de sesión. Este proyecto está diseñado para ser reutilizado en diferentes aplicaciones.

## Características principales
- **Login y Registro**: Implementación de rutas para el registro de usuarios y el inicio de sesión utilizando JWT.
- **Código Base**: Diseñado para servir como plantilla inicial para proyectos en Node.js.
- **Seguridad**: Contraseñas encriptadas con bcrypt y autenticación con tokens JWT.
- **Conexión a MongoDB**: Base de datos para almacenar la información de los usuarios.

## Tecnologías utilizadas
- **Node.js**: Entorno de ejecución de JavaScript.
- **Express**: Framework web para Node.js.
- **MongoDB**: Base de datos NoSQL.
- **Mongoose**: ODM para MongoDB.
- **Bcrypt**: Para la encriptación de contraseñas.
- **JWT (JSON Web Tokens)**: Para la gestión de autenticación.
- **Dotenv**: Manejo de variables de entorno.
- **Cors**: Para habilitar el acceso entre dominios.

## Instalación

Sigue estos pasos para configurar el proyecto en tu entorno local:

1. Clona este repositorio:
   ```bash
   git clone https://github.com/JeanCorreaBarros/AppNode.js.git
   ```

2. Ve al directorio del proyecto:
   ```bash
   cd AppNode
   ```

3. Instala las dependencias:
   ```bash
   npm install
   ```

4. Configura las variables de entorno:
   Crea un archivo `.env` en la raíz del proyecto con el siguiente contenido:
   ```env
   PORT=5000
   MONGO_URI=tu_conexion_a_mongodb
   JWT_SECRET=tu_clave_secreta
   ```

5. Inicia el servidor:
   - En modo desarrollo:
     ```bash
     npm run dev
     ```
   - En modo producción:
     ```bash
     npm start
     ```

## Uso

### Registro
**Ruta**: `/api/auth/register`
- **Método**: POST
- **Cuerpo**:
  ```json
  {
      "username": "exampleUser",
      "email": "example@example.com",
      "password": "securePassword123"
  }
  ```

### Login
**Ruta**: `/api/auth/login`
- **Método**: POST
- **Cuerpo**:
  ```json
  {
      "email": "example@example.com",
      "password": "securePassword123"
  }
  ```

## Estructura del proyecto
```
/project-base
├── /src
│   ├── /config       # Configuración del proyecto
│   ├── /controllers  # Lógica de negocio
│   ├── /models       # Modelos de datos
│   ├── /routes       # Rutas del proyecto
│   ├── /middleware   # Middleware personalizado
│   └── app.js        # Configuración de Express
├── /public           # Archivos estáticos
├── .env              # Variables de entorno
├── package.json
└── README.md
```

## Contribución
Si deseas contribuir a este proyecto:
1. Haz un fork del repositorio.
2. Crea una rama para tu función: `git checkout -b feature/nueva-funcion`.
3. Realiza tus cambios y haz commit: `git commit -m "Agregada nueva función"`.
4. Sube tus cambios: `git push origin feature/nueva-funcion`.
5. Abre un Pull Request.

## Licencia
Este proyecto está bajo la licencia MIT. Puedes ver el archivo [LICENSE](LICENSE) para más detalles.

---

### Autor
Jean Carlos Correa Barros
- [GitHub](https://github.com/JeanCorreaBarros)
- [Email](mailto:Jeancorrea1000@gmail.com)

