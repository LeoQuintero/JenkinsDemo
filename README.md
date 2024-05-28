# JenkinsDemo

### Requisitos:
- JDK java 8 o superior
- descarga Jenkins en esta caso se hace por archivo jenkins.war
- Tener el servicio correindo con java -jar jenkins.war
- Abrir puerto para esta caso utilizamos el de defecto http://localhost:8080/

1. Administrar el jeinkis
2. CLI
   - descargar jenkins-cli.jar en http://localhost:8080/cli/
   - abrir CMD en la ubicació descarga
   - Configurar seguridad/ autorizacion para cualquiera pueda usar.
   - en el CLI si queremos correr el job TestJob:  java -jar jenkins-cli.jar -s http://localhost:8080/ build TestJob
3. Creación usuario y asignaciones
  - Administrador Jenkins / Usuarios / nuevo usuario
  - Plugin role-based Strategy
  - Configuración seguridad / Autorizacion / role-based Strategy
  - Administracion de asignacion roles
  - Agregamos un usuario global (ejemplo: employee)
  - Agregamos un item role Role/Pattern (ej: tester/test.*, developer/dev.*) con todos los permisos.
  - Sección asignación de roles: Agregamos los usuarios creados y asingamos roles creados (ejemplo de tester y developer)
5. Plugins git e integración con SonarQube
6. Creación de Items y integración con GitHub
7. Notitificación por email
