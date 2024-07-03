# JbossExercise

# Pre-requisitos
1. Docker
2. Kubernetes
3. Organización de Azure DevOps

# Requerimiento

#### Objetivo

* Desplegar version contenerizada de jboss en kubernetes, agregar un war file en una capa de la imagen y crear configmap con script para creación de usuario administrativo.

#### Ejercicio #1

* Crea un proceso de CI/CD donde inicialmente tengas un war versionado en tu organización de Azure DevOps ya sea en un repositorio o en un artifacts
  * [descargar war](https://github.com/ComputerTrainer0/EAR/blob/main/testing.war) (puedes tomar uno de tu eleccion sí la versión de jboss no es compatible con este war)
  * Hacer un dockerfile con imagen de jboss/wildfly e instalar war
    * [docker hub jboss](https://hub.docker.com/r/jboss/wildfly/tags)
* Una vez se inicie el despliegue:
  * En Azure DevOps en el mismo pipeline en un segundo task debes hacer :
    * Un script en bash o powershell que:
      * Determinar palindromo de palabras un arreglo.
      * Crear un repositorio via azure az devops cli en tu propia organización
* Desplegar deployment, services, ingress con la imagen creada.

#### Ejercicio #2
* Crear un script y desde un configmap mapeado en el contenedor, deberia hacer:
  * Crear un rol y usuario en la consola administrativa.
    * ``` /opt/jboss/wildfly/bin/add-user.sh ```
* Ejecutar el script al momento de inicializar el contenedor.


# Que esperamos?

1. Adjuntar el repositorio publico:
  1. Logs de ejecución
  2. Imagen de consola administrativa de jboss
  3. Imagen de aplicación desplegada
  4. Server.log de jboss
  5. Azure pipeline yaml
  6. yaml kubernetes
  7. Captura de pantalla:
     1. Services Connections
     2. Ejecución Pipeline Azure
     3. Repositorio con commits
2. Subir a dockerHub imagen creada
