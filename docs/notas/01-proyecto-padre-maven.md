# Notas

## Proyecto actual
El proyecto `SpringMicroservices` fue generado inicialmente como un proyecto Maven estándar usando `maven-archetype-quickstart`.

## ¿Qué es y qué problema resuelve un proyecto padre?

Se usa una **estructura modular**, donde existe un **proyecto padre** que actúa como contenedor principal. Dentro de él se agrupan varios subproyectos llamados **módulos**, y algunos de esos módulos pueden representar microservicios.

### ¿Qué problema resuelve?
Tener microservicios separados desde cero puede generar desorden: duplicación de configuraciones, dependencias repetidas y necesidad de compilar cada proyecto por separado.

Con un **proyecto padre** se logra:
- centralizar configuraciones y dependencias comunes,
- construir todo el ecosistema con un solo comando,
- mantener los módulos organizados en una sola estructura.

### Idea clave
Modular en código no significa monolítico en arquitectura. Aunque los microservicios vivan juntos dentro del proyecto padre para facilitar el desarrollo, siguen siendo independientes y cada uno puede tener:
- sus propios endpoints,
- su propia lógica,
- su propia base de datos,
- su propio despliegue.

## Configuración clave
En el `pom.xml` del padre, lo importante es indicar que será un contenedor usando:

```xml
<packaging>pom</packaging>
```
Y más adelante se agregarán módulos con una estructura como esta:
```xml
<modules>
    <module>msvc-student</module>
    <module>msvc-course</module>
</modules>
```

## Estado de esta fase
En esta etapa todavía existe la carpeta `src` y el proyecto se comporta como una aplicación Maven normal.

## Siguiente objetivo
Convertir este proyecto en un proyecto padre Maven, eliminando `src` y ajustando el `pom.xml` para que funcione como contenedor de módulos.