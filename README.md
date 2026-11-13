# NBConsoleCleaner

![Java](https://img.shields.io/badge/Java-Development-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Apache NetBeans](https://img.shields.io/badge/Apache_NetBeans-IDE_31-1B6AC6?style=for-the-badge&logo=apachenetbeanside&logoColor=white)
![Maven](https://img.shields.io/badge/Apache_Maven-Build-C71A36?style=for-the-badge&logo=apachemaven&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-Repository-181717?style=for-the-badge&logo=github&logoColor=white)
![Status](https://img.shields.io/badge/Status-In_Development-yellow?style=for-the-badge)

**NBConsoleCleaner** es un proyecto de código abierto cuyo objetivo es desarrollar una extensión para Apache NetBeans IDE que permita limpiar el contenido de la ventana **Output** durante la ejecución de programas Java, sin necesidad de reiniciar la aplicación ni utilizar una terminal externa.

El proyecto surge de una limitación del panel Output de NetBeans, que no interpreta determinadas secuencias de control ANSI utilizadas habitualmente para limpiar la pantalla de una terminal.

## Objetivo

Desarrollar un módulo instalable de Apache NetBeans que permita a las aplicaciones Java solicitar la limpieza de su consola de salida durante la ejecución, conservando la integración con el entorno de desarrollo.

## Problemática

En terminales compatibles con ANSI es posible limpiar la pantalla utilizando secuencias de escape. Sin embargo, la ventana Output de NetBeans no ofrece necesariamente el mismo comportamiento.

Esta limitación dificulta el desarrollo y la ejecución de aplicaciones de consola que necesitan actualizar su contenido dinámicamente, como menús interactivos, sistemas de navegación por opciones y programas que muestran información cambiante.

El proyecto busca investigar e implementar una solución que permita realizar esta operación directamente desde NetBeans.

## Funcionalidades previstas

- Limpieza de la ventana Output durante la ejecución de programas Java.
- Comunicación entre las aplicaciones Java y el módulo de NetBeans.
- Compatibilidad con proyectos Java administrados mediante Maven y Ant.
- Evaluación del funcionamiento con archivos Java ejecutados individualmente.
- Integración con el sistema de módulos de Apache NetBeans.
- Distribución de la extensión mediante un paquete instalable `.nbm`.
- Posibilidad de instalar y reutilizar la extensión en diferentes equipos.

Estas funcionalidades representan los objetivos de desarrollo y todavía no se encuentran implementadas.

## Tecnologías

| Tecnología | Propósito |
|---|---|
| Java | Desarrollo de la extensión |
| Apache NetBeans IDE | Entorno de desarrollo y plataforma de integración |
| NetBeans Platform | Sistema de módulos y APIs del IDE |
| Apache Maven | Administración de dependencias, compilación y empaquetado |
| Git | Control de versiones |
| GitHub | Alojamiento del código fuente y distribución de versiones |

## Estructura del proyecto

```text
nbConsoleCleaner/
├── pom.xml
└── src/
    └── main/
        ├── java/
        │   └── com/
        │       └── nbconsolecleaner/
        ├── nbm/
        │   └── manifest.mf
        └── resources/
            └── com/
                └── nbconsolecleaner/
                    └── Bundle.properties
```

### Descripción de los componentes

- **pom.xml:** contiene la configuración Maven, las dependencias y los parámetros necesarios para construir el módulo.
- **src/main/java:** contiene el código fuente Java de la extensión.
- **manifest.mf:** proporciona metadatos utilizados por el sistema de módulos de NetBeans.
- **Bundle.properties:** almacena propiedades y cadenas de texto asociadas al módulo.

## Estado del desarrollo

**Estado actual: fase inicial de investigación y desarrollo.**

Hasta el momento se ha creado la estructura base del módulo mediante la plantilla *NetBeans Module* de Maven.

Las siguientes actividades previstas son:

- Investigar la arquitectura de módulos de Apache NetBeans.
- Estudiar las APIs de entrada y salida del IDE.
- Analizar las posibilidades de manipulación de la ventana Output.
- Diseñar un mecanismo de comunicación entre el programa Java y la extensión.
- Implementar y probar la funcionalidad de limpieza.
- Evaluar la compatibilidad con diferentes tipos de proyectos Java.
- Generar y validar el paquete instalable.
- Preparar la primera versión distribuible.

## Compatibilidad

El desarrollo se ha iniciado utilizando **Apache NetBeans IDE 26**, con la configuración inicial de dependencias Maven `RELEASE310`.

La compatibilidad entre las APIs utilizadas y las distintas versiones del IDE deberá verificarse durante el desarrollo.

No existe todavía una versión funcional ni un instalador disponible.

## Instalación

La extensión aún se encuentra en desarrollo.

Cuando exista una versión estable, esta sección incluirá las instrucciones para instalar el paquete `.nbm` desde el administrador de plugins de Apache NetBeans.

## Contribuciones

El proyecto está abierto a futuras contribuciones relacionadas con mejoras de compatibilidad, corrección de errores, documentación y nuevas funcionalidades.

Las instrucciones específicas para contribuir se incorporarán conforme avance el desarrollo.

## Documentación y referencias

- [Apache NetBeans](https://netbeans.apache.org/)
- [Apache NetBeans GitHub](https://github.com/apache/netbeans)
- [NetBeans API Documentation](https://bits.netbeans.org/dev/javadoc/)
- [Apache Maven](https://maven.apache.org/)

## Licencia

Pendiente de definir. La publicación del código fuente en GitHub no implica por sí sola la concesión de una licencia de uso, modificación o distribución.