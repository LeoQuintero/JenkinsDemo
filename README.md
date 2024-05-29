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
7. Creación Pipeline
    - Instalar plugin
    - Dashborar / new view / nombre y  seleccionamos Build Pipeline View
    - Seleccionar el job / No Of Displayed Builds (ejemplo 5)
8. CI - jenkinsfile pipeline - sencillo "hola mundo"
   - Verificar que este instalado plugin pipeline
   - Crear un job tipo pipeline
   - Creamos en este caso un scrip (hello mundo)
   - opcional Pipeline Syntax (build a job - ej: DevJob1)
   - Build now
   - Talbien podemos modificar el script agregando mas Stage y al correr Build now vermos mas columnas con cada paso.
9. CI - jenkinsfile piple desde GitHub
   - Repositorio GitHub creado
   - Crearmos un archivo al repo (podemos crear y copiar el mismo script anterior)
   - configuramos el job pipeline: Script from SCM, la url repo gitHub, credencial, el branch principal, la ruta del archivo.
   - ejecutamos "Build now"
10. Notitificación por email
