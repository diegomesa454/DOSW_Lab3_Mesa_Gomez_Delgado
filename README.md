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

5. **¿Cómo crear un pull request?**

   Comando usado para crear el proyecto
```
mvn archetype:generate -DgroupId=edu.eci.dosw.lab -DartifactId=DOSW-Laboratorio3 -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=false
```

6. **¿Cómo se aprueba un pull request en GitHub?**
   Para aprobar un pull request en GitHub:
   1. Entra al repositorio y haz clic en la pestaña Pull requests.
   2. Selecciona el pull request que quieres revisar.
   3. Haz clic en la pestaña Files changed para ver los cambios propuestos.
   4. Revisa el código y opcionalmente puedes dejar comentarios en líneas específicas haciendo clic en el ícono +.
   5. En la parte superior de los cambios, haz clic en "Review changes".
   6. Escribe un comentario resumiendo tu retroalimentación sobre los cambios propuestos. 
   7. Selecciona la opción "Approve" para aprobar la fusión de los cambios propuestos. 
   8. Haz clic en "Submit review" para confirmar.

7. **Incluir la bibliografía, usando formato APA**
   ## Bibliografía

   Apache Maven Project. (s.f.). *Introduction to archetypes*. Apache Maven. https://maven.apache.org/guides/introduction/introduction-to-archetypes.html

   Apache Maven Project. (s.f.). *Introduction – Maven Archetype Plugin*. Apache Maven. https://maven.apache.org/archetype/maven-archetype-plugin/

   Apache Maven Project. (s.f.). *About – Maven Archetype*. Apache Maven. https://maven.apache.org/archetype/index.html

   GitHub Docs. (s.f.). *About pull requests*. GitHub. https://docs.github.com/en/pull-requests/get-started/about-pull-requests

   GitHub Blog. (2024, 12 de agosto). *Beginner's guide to GitHub: Creating a pull request*. The GitHub Blog. https://github.blog/developer-skills/github/beginners-guide-to-github-creating-a-pull-request/

   GitHub Docs. (s.f.). *Approving a pull request with required reviews*. GitHub. https://docs.github.com/en/pull-requests/how-tos/review-pull-requests/approving-a-pull-request-with-required-reviews