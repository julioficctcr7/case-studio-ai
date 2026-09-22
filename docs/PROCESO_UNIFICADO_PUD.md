# Registro del Proceso de Desarrollo según el Proceso Unificado (PUD)

**Metodología Oficial**: *The Unified Software Development Process* (Ivar Jacobson, Grady Booch, James Rumbaugh).

---

## 1. Principios Fundamentales del PUD

1. **Dirigido por Casos de Uso**: Las funcionalidades del sistema se derivan y validan a partir de los requerimientos de los actores.
2. **Centrado en la Arquitectura**: El diseño se organiza en capas y vistas ortogonales para garantizar la robustez y absorción de cambios.
3. **Iterativo e Incremental**: El ciclo de vida se descompone en ciclos y mini-proyectos iterativos que mitigan riesgos de forma temprana.

---

## 2. Fases del Ciclo de Vida

```mermaid
gantt
    title Fases e Iteraciones del Proceso Unificado (PUD)
    dateFormat  YYYY-MM-DD
    section 1. Fase de Inicio
    Alcance, Visión y Factibilidad         :done, init1, 2026-08-01, 2026-08-07
    section 2. Fase de Elaboración
    Línea Base de Arquitectura y Riesgos    :done, elab1, 2026-08-08, 2026-08-21
    section 3. Fase de Construcción
    Iteración 1: Canvas Colaborativo UML    :done, const1, 2026-08-22, 2026-09-04
    Iteración 2: Motor OMT y Spring Boot   :done, const2, 2026-09-05, 2026-09-15
    Iteración 3: App Móvil Flutter Offline  :active, const3, 2026-09-16, 2026-09-22
    section 4. Fase de Transición
    Despliegue AWS, Pruebas y Auditoría     :trans1, 2026-09-23, 2026-09-30
```

---

## 3. Flujos de Trabajo de Ingeniería

### Flujo 1: Requerimientos
- **CU-01: Modelar Clases y Relaciones**: El arquitecto interactúa con el canvas para diagramar entidades y cardinalidades.
- **CU-02: Colaboración en Tiempo Real**: Dos o más usuarios modifican el modelo simultáneamente bajo exclusión mutua.
- **CU-03: Asistencia por Voz/IA**: El usuario emite comandos hablados que transforman atómicamente el grafo.
- **CU-04: Digitalización de Foto a UML**: El usuario carga una fotografía y el sistema infiere el modelo UML correspondiente.
- **CU-05: Generar Backend Spring Boot**: El sistema transforma el diagrama a código compilable en 5 capas con PostgreSQL.
- **CU-06: Interoperar con Enterprise Architect**: Exportación e importación en formato XMI 2.1.
- **CU-07: Pruebas Móviles Offline con IA Local**: El usuario registra operaciones vía voz en su dispositivo sin conexión.

### Flujo 2: Análisis
- Traducción de Casos de Uso a Clases de Análisis (Boundary, Control, Entity).
- Definición de paquetes y subsistemas del monorepo.

### Flujo 3: Diseño
- Refinamiento del diagrama de clases hacia la implementación tecnológica.
- Diseño de interfaces REST, contratos DTO y protocolos WebSocket.
- Aplicación de las reglas de mapeo OMT/DMO para persistencia relacional.

### Flujo 4: Implementación
- Codificación en Java 21 / Spring Boot 3 para el motor CASE.
- Frontend web en Angular 21 / React TS con Canvas UML 2.5+.
- App móvil en Flutter 3.x con BLoC y SQLite local.

### Flujo 5: Pruebas
- Pruebas unitarias automatizadas (`JUnit 5`, `flutter test`).
- Pruebas de integración de concurrencia y exclusión mutua.
- Pruebas de desconexión y reconciliación offline en móvil.
