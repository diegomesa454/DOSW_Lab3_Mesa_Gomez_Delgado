# 📄 Requerimientos del Sistema

## 1. Sistema
* Nombre del sistema: TechCup
* Objetivo: El sistema tiene como objetivo brindar una plataforma centralizada para la gestión del torneo de fútbol interfacultades organizado por la Escuela Colombiana de Ingeniería Julio Garavito, permitiendo la creación de torneos, el registro de equipos, el procesamiento y validación de pagos de inscripción, y la generación de reportes para los organizadores y la Decanatura.

## 2. Problema a resolver
Actualmente, la Escuela Colombiana de Ingeniería Julio Garavito no cuenta con un sistema centralizado que permita gestionar el torneo de fútbol interfacultades. Esto genera dificultades para crear torneos definiendo sus reglas básicas (fechas, tarifas, etc.), registrar equipos de forma ágil, procesar y validar los pagos de inscripción realizados por los equipos, consultar los equipos inscritos en cada torneo, generar reportes de inscripciones y de ingresos, y enviar reportes de pagos en formato JSON a la Decanatura. La ausencia de una plataforma centralizada obliga a que estos procesos se realicen de forma manual o dispersa, lo que dificulta el control, la trazabilidad y el cumplimiento de las reglas del negocio (como el límite de un torneo activo a la vez o la restricción de un torneo por equipo). TechCup busca resolver esta problemática ofreciendo una plataforma simple y segura para la creación de torneos y el registro de equipos.

## 3. Diagrama de Contexto

### 3.1 Diagrama
![Diagrama de Contexto TechCup](../uml/c4-techcup.png)

Diagrama fuente (editable): [c4-techcup.drawio](../uml/c4-techcup.drawio)

### 3.2 Actores
| Actor / Rol              | Descripción                                                                 |
|---------------------------|:----------------------------------------------------------------------------:|
| Estudiante                | Usuario del sistema que se autentica y consulta información de los torneos |
| Capitán de Equipo         | Crea equipos, realiza el pago de inscripción y registra su equipo al torneo activo |
| Organizador del Torneo    | Crea y gestiona torneos, revisa y aprueba pagos, y genera reportes |

### 3.3 Sistemas externos
| Sistema      | Descripción                                                                 |
|--------------|:----------------------------------------------------------------------------:|
| PSE          | Pasarela de pagos en línea utilizada para procesar el pago de inscripción de los equipos |
| Decanatura   | Recibe los reportes de pagos de inscripción en formato JSON generados por TechCup |

## 4. Alcance del sistema

### 4.1 Dentro del sistema
* Autenticación de usuarios (estudiantes y organizadores) mediante usuario y contraseña.
* Creación, actualización y cambio de estado de torneos (Pendiente, Activo, En Progreso, Cerrado, Cancelado) por parte de organizadores.
* Creación y actualización de equipos, y registro de equipos al torneo activo por parte de capitanes.
* Procesamiento del pago de inscripción de equipos a través de la pasarela PSE.
* Consulta y revisión, por parte de organizadores, del pago asociado a la inscripción de un equipo.
* Generación de reporte de equipos registrados por torneo.
* Generación de reporte de ingresos por concepto de inscripciones.
* Envío del reporte de pagos de inscripción en formato JSON a la Decanatura.

### 4.2 Fuera del sistema
* Gestión de torneos o disciplinas deportivas distintas al fútbol interfacultades.
* Procesamiento de pagos por medios diferentes a PSE (efectivo, transferencia directa, tarjeta física, etc.).
* Programación de partidos, arbitraje, marcadores o estadísticas deportivas del torneo.
* Generación de facturación electrónica oficial ante la DIAN u otra entidad tributaria.
* Notificaciones automáticas (correo, SMS, push) a estudiantes o capitanes sobre el estado de sus inscripciones o pagos.