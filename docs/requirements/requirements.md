# 📄 Requerimientos del Sistema

## 1. Lista general de requerimientos
El sistema de TechCup tiene los siguientes requerimientos (descripción a alto nivel):

### 1.1 Requerimientos funcionales
El sistema de TechCup debe tener la capacidad de:
1. Permitir a los organizadores crear un torneo especificando sus reglas básicas, como fechas y valor de la inscripción.
2. Permitir a los organizadores generar un reporte de los equipos registrados en un torneo.
3. Permitir a los capitanes crear un equipo, especificando su información básica.
4. Permitir a los capitanes registrar su equipo únicamente en el torneo que se encuentre actualmente activo.
5. *(pendiente — aporte de Persona 3)*

### 1.2 Requerimientos no funcionales
El sistema de TechCup debe tener:
1. Garantía de que solo exista un torneo en estado "Activo" en un momento dado, de acuerdo con las reglas de negocio.
2. Generación del reporte de ingresos de inscripción en formato JSON para ser enviado a la Decanatura, siguiendo una estructura de datos consistente.
3. Garantía de que la información de pago de cada equipo se procese de forma segura al integrarse con PSE.
4. Validación de que un equipo no pueda registrarse en más de un torneo activo al mismo tiempo, de acuerdo con las reglas de negocio.
5. *(pendiente — aporte de Persona 3)*

## 2. Diagramas de caso de uso

### 2.1 Requerimiento Funcional 1

| Campo | Descripción |
|------|-------------|
| **ID** | RF-01 |
| **Nombre del requerimiento** | |
| **Descripción** | *El sistema debe …* |
| **Precondiciones** | *Para que el sistema cumpla con este requerimiento, Bankify debe tener previamente …* |
| **Actor** | *(El actor debe estar definido en el diagrama de contexto)* |
| **Flujo principal** | 1. El actor …<br>2. El sistema …<br>3. El sistema … |
| **Diagrama de caso de uso** | *imagen y link*|
| **Poscondiciones** | *Se espera como resultado …* |


### 2.2 Requerimiento Funcional 2
| Campo | Descripción |
|------|-------------|
| **ID** | RF-02 |
| **Nombre del requerimiento** | Crear Torneo |
| **Descripción** | El sistema debe permitir a los organizadores crear un torneo especificando sus reglas básicas, como fechas y valor de la inscripción. |
| **Precondiciones** | Para que el sistema cumpla con este requerimiento, el organizador debe estar autenticado en TechCup. |
| **Actor** | Organizador del Torneo |
| **Flujo principal** | 1. El organizador inicia la opción de crear un nuevo torneo.<br>2. El sistema solicita los datos básicos del torneo: fecha y valor de la inscripción.<br>3. El sistema valida que el torneo no exceda la duración de un día y que su ID sea un número de cinco dígitos basado en el año y semestre.<br>4. El sistema registra el torneo en estado "Pending". |
| **Diagrama de caso de uso** | ![Diagrama Crear Torneo](../uml/uc-crear-torneo.png) — [uc-crear-torneo.drawio](../uml/uc-crear-torneo.drawio) |
| **Poscondiciones** | Se espera como resultado que el torneo quede creado en el sistema en estado "Pending", disponible para ser activado posteriormente por un organizador. |

### Flujo de navegación — Crear Torneo

El requerimiento "Crear Torneo" involucra 3 pantallas:

1. **Listado de torneos** (vista inicial) — muestra los torneos existentes y el botón "Crear Torneo".
2. **Formulario Crear Torneo** — solicita fecha del torneo y valor de inscripción.
3. **Confirmación** — mensaje de éxito tras crear el torneo.

**Flujo:**
- Listado de torneos → (clic "Crear Torneo") → Formulario Crear Torneo
- Formulario Crear Torneo → (datos válidos, clic "Crear Torneo") → Confirmación
- Formulario Crear Torneo → (clic "Cancelar") → Listado de torneos
- Confirmación → (clic "Volver") → Listado de torneos

![Flujo de navegación](../images/flujo-navegacion-crear-torneo.png) — [flujo-navegacion-crear-torneo.drawio](../images/flujo-navegacion-crear-torneo.drawio)

### 2.3 Requerimiento Funcional 3

| Campo | Descripción |
|------|-------------|
| **ID** | RF-03 |
| **Nombre del requerimiento** | |
| **Descripción** | *El sistema debe …* |
| **Precondiciones** | *Para que el sistema cumpla con este requerimiento, Bankify debe tener previamente …* |
| **Actor** | *(El actor debe estar definido en el diagrama de contexto)* |
| **Flujo principal** | 1. El actor …<br>2. El sistema …<br>3. El sistema … |
| **Diagrama de caso de uso** | *imagen y link*|
| **Poscondiciones** | *Se espera como resultado …* |

## 3. Preguntas