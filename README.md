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
   git clone https://github.com/usuario/task-mngr
   cd task-mngr

2.Instala dependencias
   - Navega a la carpeta del proyecto y ejecuta:
        mvn clean install

3. Ejecutar el backend:
   - Si tienes Maven:
         mvn spring-boot:run
     o
       ./mvnw spring-boot:run
   - Si tienes Gradle:
       ./gradlew bootRun

4. Verificar que el backend está corriendo:
   - El backend debería estar disponible en: http://localhost:8080

---

Frontend: Angular

1. Clonar el repositorio del frontend:
   git clone https://github.com/usuario/task-web-ui
   cd task-web-ui

2. Instalar las dependencias:
   - Navega a la carpeta del proyecto y ejecuta:
     npm install

4. Ejecutar el frontend:
   - Para iniciar el servidor de desarrollo de Angular:
     ng serve

5. Verificar que el frontend está corriendo:
   - El frontend debería estar disponible en: http://localhost:4200

---

Troubleshooting

- Backend no se conecta a una base de datos:
  - Los datos se almacenan en memoria, no deberias necesitar ninguna configuracion de bases de datos

- Frontend no se comunica con el backend:
  - Verifica la URL del API en src/apps/services/task.service.ts y asegúrate de que el backend esté corriendo en el puerto correcto.

----------------------------------------------------------------------------------------------------------------------------------------------------

Proyecto Hash

1. Requisitos previos para ejecutar el código:
  - Python 3.x instalado:
      Puedes verificar si lo tienes ejecutando en la terminal o CMD: python --version
    
2. Asegurar que el módulo hashlib esté disponible

  - hashlib es una biblioteca estándar de Python, así que no necesitas instalarla.
      Para verificar que funciona, ejecuta en Python:
        - import hashlib
        - print(hashlib.sha256("test".encode()).hexdigest())

3. Cómo ejecutar el script
  - Guarda el código en un archivo llamado custom_hash.py y ejecútalo desde la terminal o CMD:
        python custom_hash.py

¡Con estos pasos, deberías poder ejecutar ambos proyectos sin problemas! Si encuentras algún error, revisa los logs del backend o frontend y asegúrate de que ambos servicios están configurados correctamente.

