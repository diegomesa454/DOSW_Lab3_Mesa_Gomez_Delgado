# DOSW_Lab3_Mesa_Gomez_Delgado

## Preguntas Parte 1

1. **¿Qué es un Maven Archetype?**
   Un Archetype es una plantilla de proyecto en Maven que genera automáticamente
   una estructura de carpetas y archivos base, para no tener que crearla manualmente.

2. **¿Cuál es el propósito de maven-archetype-quickstart?**
   Es un arquetipo específico que crea la estructura mínima de un proyecto Java
   simple: pom.xml, una clase principal (App.java) y su clase de test.

## Comando usado para crear el proyecto

```
mvn archetype:generate -DgroupId=edu.eci.dosw.lab -DartifactId=DOSW-Laboratorio3 -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=false
```