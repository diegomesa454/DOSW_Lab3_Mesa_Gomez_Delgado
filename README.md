# DOSW_Lab3_Mesa_Gomez_Delgado

## Preguntas Parte 1

1. **¿Qué es un Maven Archetype?**
   Un Archetype es una plantilla de proyecto en Maven que genera automáticamente
   una estructura de carpetas y archivos base, para no tener que crearla manualmente.

2. **¿Cuál es el propósito de maven-archetype-quickstart?**
   Es un arquetipo específico que crea la estructura mínima de un proyecto Java
   simple: pom.xml, una clase principal (App.java) y su clase de test.

3. **¿Qué comando se puede usar para crear un proyecto basado en un Maven Archetype?**
   El comando general es `mvn archetype:generate`, indicando los parámetros `-DgroupId`, `-DartifactId`, `-DarchetypeArtifactId` y `-DarchetypeVersion` para especificar el proyecto y el arquetipo deseado.

4. **¿Qué es un Pull Request en GitHub?**
   Un Pull Request (PR) es una solicitud para fusionar los cambios de una rama dentro de otra rama del mismo repositorio (o de un fork). Permite revisar el código, discutir cambios y aprobar la integración antes de que se incorpore a la rama destino.

## Comando usado para crear el proyecto

```
mvn archetype:generate -DgroupId=edu.eci.dosw.lab -DartifactId=DOSW-Laboratorio3 -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=false
```