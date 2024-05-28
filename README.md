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
   - Configurar en autorizacion para cualquiera pueda usar.
   - en el CLI si queremos correr el job TestJob:  java -jar jenkins-cli.jar -s http://localhost:8080/ build TestJob
3. Plugins git e integración con SonarQube
4. Creación de Items y integración con GitHub
5. Notitificación por email
