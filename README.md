Proyecto Backend y Frontend

Este proyecto está compuesto por dos partes principales:
1. Backend: Desarrollado con Spring Boot (Java 17).
2. Frontend: Desarrollado con Angular (v17).

A continuación, se detallan los pasos para configurar y ejecutar ambos proyectos en tu máquina local.

---

Requisitos Previos

Antes de comenzar, asegúrate de tener instalados los siguientes programas:

Backend (Spring Boot)
- Java 17:
  - Descargar Java 17 e instalarlo desde: https://adoptopenjdk.net/
  - Verifica la instalación ejecutando:
    java -version

Frontend (Angular)
- Node.js y NPM:
  - Descargar Node.js e instalarlo desde: https://nodejs.org/en/
  - Verifica la instalación ejecutando:
    node -v
    npm -v

- Angular CLI:
  - Instala Angular CLI globalmente:
    npm install -g @angular/cli

---

Backend: Spring Boot

1. Clonar el repositorio del backend:
   git clone https://github.com/usuario/backend-repo.git
   cd backend-repo

2. Configurar la base de datos:
   - Si estás utilizando una base de datos local o en la nube (como AWS RDS), configura la conexión en src/main/resources/application.properties o application.yml:
     spring.datasource.url=jdbc:mysql://localhost:3306/mi_base_de_datos
     spring.datasource.username=usuario
     spring.datasource.password=contraseña  

3. Ejecutar el backend:
   - Si tienes Maven:
     ./mvnw spring-boot:run
   - Si tienes Gradle:
     ./gradlew bootRun

4. Verificar que el backend está corriendo:
   - El backend debería estar disponible en: http://localhost:8080

---

Frontend: Angular

1. Clonar el repositorio del frontend:
   git clone https://github.com/usuario/frontend-repo.git
   cd frontend-repo

2. Instalar las dependencias:
   - Navega a la carpeta del proyecto y ejecuta:
     npm install

3. Configurar el backend (API):
   - Asegúrate de que el frontend apunte al backend correcto. Si el backend está en una URL diferente o se ejecuta en un puerto distinto, configura la URL de la API en el archivo src/environments/environment.ts:
     export const environment = {
       production: false,
       apiUrl: 'http://localhost:8080/tasks'
     };

4. Ejecutar el frontend:
   - Para iniciar el servidor de desarrollo de Angular:
     ng serve

5. Verificar que el frontend está corriendo:
   - El frontend debería estar disponible en: http://localhost:4200

---

Despliegue (Opcional)

Desplegar el Backend
Si deseas desplegar el backend, puedes hacerlo en un servicio de nube como AWS, Azure o Heroku. Asegúrate de configurar correctamente las variables de entorno de producción (por ejemplo, base de datos, credenciales, etc.).

Desplegar el Frontend
Para construir la versión de producción del frontend, ejecuta el siguiente comando:
ng build --prod

Esto generará los archivos optimizados en la carpeta dist/. Puedes desplegar estos archivos en cualquier servidor web o servicio como Netlify, Vercel o un servidor Nginx.

---

Troubleshooting

- Backend no se conecta a la base de datos:
  - Verifica que las credenciales en application.properties estén correctas y que el servicio de base de datos esté corriendo.

- Frontend no se comunica con el backend:
  - Verifica la URL del API en src/environments/environment.ts y asegúrate de que el backend esté corriendo en el puerto correcto.

---

¡Con estos pasos, deberías poder ejecutar ambos proyectos sin problemas! Si encuentras algún error, revisa los logs del backend o frontend y asegúrate de que ambos servicios están configurados correctamente.

