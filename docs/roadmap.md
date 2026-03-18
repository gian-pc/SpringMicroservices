# Roadmap

## Fase 0 - Preparación del entorno
1. Crear una carpeta local llamada `Microservices`.
2. Revisar la guía oficial de Maven:
    - https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html
3. Generar un proyecto Maven base llamado `SpringMicroservices` usando `maven-archetype-quickstart`:

```bash
mvn archetype:generate -DgroupId=com.mycompany.app -DartifactId=SpringMicroservices -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.5 -DinteractiveMode=false
```

## Fase 1 - Inicialización del repositorio
4. Crear el repositorio remoto en GitHub con el nombre `SpringMicroservices`.
5. Crear el archivo `.gitignore`.
6. Crear el `README.md`.
7. Realizar el primer commit y hacer push del estado inicial del proyecto.