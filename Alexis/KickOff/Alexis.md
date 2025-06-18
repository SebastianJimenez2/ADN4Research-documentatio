Kickoff - Alexis



## #OBJETIVO DEL KICK-OFF

Establecer una comprensión compartida de las metas, alcance y expectativas del proyecto antes de comenzar el trabajo formal. Representa el inicio oficial del proyecto donde se alinean todos los participantes.

## #COMPONENTES ESENCIALES

### #**1. Presentaciones del Equipo**

- **Propósito**: Crear confianza y familiaridad entre los miembros.
    
- **Formato**:
    
    - Nombre, rol en el proyecto y experiencia relevante.
        

### #**2. Visión General del Proyecto**

- **Antecedentes**:
    
    - Contexto del problema (ej.: "Automatizar revisiones sistemáticas de literatura").
        
    - Justificación: ¿Por qué es relevante este proyecto? (Ej.: "Reducirá el tiempo de búsqueda en SLR en un 40%").
        
- **Objetivos Generales**:
    
    - Ejemplo: "Desarrollar un sistema modular para búsqueda, selección y análisis automático de literatura académica".
        
- **Resultados Esperados**:
    
    - Producto tangible (ej.: "Plataforma con 5 módulos integrados").
        
    - Impacto (ej.: "Mejora en la eficiencia de revisiones sistemáticas").
        

---

### #**3. Descripción de Módulos y Alcance**

- **Módulos Clave ==(suposicion en base al pdf)==**:
    
    |   |   |   |
    |---|---|---|
    |**Módulo**|**Responsable**|**Funcionalidad**|
    |Diseño|Cristian Zambrano|Define estrategias de búsqueda y criterios.|
    |Descarga|Alexis Lapo|Recupera metadatos y documentos de bases como IEEE Xplore.|
    |Extracción|Jonathan Salazar|Extrae datos de PDFs (tablas, citas).|
    |Selección|Alejandro Jiménez|Filtra estudios con IA y criterios predefinidos.|
    |Interpretación|Juan Carillo|Analiza datos y genera gráficos para el informe final.|
    

---

### #**4. Cronograma y Hitos**

- **Herramienta Recomendada**: Diagrama de Gantt o tabla con fechas clave.
    
- ![](https://tic-2025b.getoutline.com/api/attachments.redirect?id=f90377a0-8ac3-476f-9fc5-9619520faf58)
    
- **Ejemplo de Hitos**:
    
    |   |   |
    |---|---|
    |**Fecha**|**Entregable**|
    |15/05/2024|Prototipo funcional del módulo de descarga.|
    |30/06/2024|Integración completa de módulos.|
    

---

### #**5. Roles y Responsabilidades**

- **[Matriz RACI](https://tic-2025b.getoutline.com/doc/matriz-raci-cw29JLhDyE)** [(ejemplo para el módulo de descarga):](https://tic-2025b.getoutline.com/doc/matriz-raci-cw29JLhDyE)
    
- ![](https://tic-2025b.getoutline.com/api/attachments.redirect?id=d423e009-9db3-47da-bed3-085b8cfac9e1)
    
    |   |   |   |   |
    |---|---|---|---|
    |**Tarea**|**Responsable (Alexis)**|**Consultado**|**Informado**|
    |Integrar API de Scopus|Alexis|Cristian (Diseño)|Equipo completo|
    

---

### #**6. Plan de Comunicación**

- **Canales**:
    
    - Reuniones semanales (Martes, 2 PM).
        
          
        
- **Protocolos**:
    
    - Reportes de avance cada viernes.
        
    - Alertas inmediatas para riesgos críticos.
        

---

### #**7. Evaluación de Riesgos**

- **Riesgos Identificados**:
    
    - **Acceso a APIs de pago** (ej.: IEEE Xplore).
        
    - **Retrasos en integración** por dependencias entre módulos.
        
- **Mitigación**:
    
    - Priorizar fuentes de acceso abierto (CORE, DBLP).
        
    - Reuniones quincenales para revisar avances técnicos.
        

---

### #**8. Sesión de Preguntas y Respuestas (Q&A)**

- **Enfoque**:
    
    - Clarificar dudas sobre roles, cronogramas o requisitos técnicos.
        

---

### #**9. Próximos Pasos y Acciones**

- **Tareas Inmediatas**:
    
    - Alexis: Investigar límites de la API de Scopus (plazo: 3 días).
        
    - Cristian: Entregar cadenas de búsqueda definitivas (plazo: 5 días).
        
    
      
    

---

# #Preguntas Alexis para el Kickoff: SLR

## #1. Persona

_==Enfocado en quiénes usarán el sistema y cómo sus características definen requisitos.==_

### #1.1. ¿Quiénes son los principales usuarios finales del sistema SLR y qué nivel de experiencia tienen?

- **¿Por qué?** Identifica a los usuarios y sus características para alinear el sistema con sus necesidades.
    

- **Impacto:** Define la complejidad de la interfaz y funcionalidades (ej.: automatización para novatos vs. control avanzado para expertos).
    

### #1.2. ¿El sistema será usado por individuos o equipos colaborativos?

- **¿Por qué?** Determina cómo interactúan los usuarios entre sí y con el sistema.
    
- **Impacto:** Si es colaborativo, se requieren funciones como gestión de permisos y trabajo en tiempo real, afectando la arquitectura global.
    

## #2. ==Propósito==

_==Responde al por qué existe el proyecto y su valor único.==_

### #==2.1. ¿Cuál es el problema central que el proyecto busca resolver en revisiones sistemáticas?==

- **==¿Por qué?==** ==Clarifica la razón de ser del proyecto y su diferenciación frente a herramientas existentes.==
    
- **==Impacto:==** ==Define si el enfoque será en automatización, accesibilidad, análisis semántico, etc., redirigiendo prioridades técnicas==.
    

## #3. Proceso

_==Define cómo se ejecutará el proyecto y su adaptabilidad.==_

### #3.1. ¿Qué nivel de trazabilidad y replicabilidad se requiere?

- **¿Por qué?** Garantiza transparencia y calidad en el uso del sistema.
    
- **Impacto:** Si se exige alta trazabilidad, todos los módulos necesitarán funciones de auditoría, aumentando la complejidad técnica.
    

### #==3.2. ¿Cómo se integrará la retroalimentación de los usuarios ?==

- **==¿Por qué?==** ==Define el flujo de validación y mejora continua.==
    
- **==Impacto:==** ==Pruebas frecuentes con usuarios implican prototipos tempranos y ciclos iterativos, afectando cronogramas.==
    

## #4. Producto

_==Detalla qué se entregará y sus capacidades técnicas.==_

### #4.1. ¿Qué áreas de investigación priorizará el sistema (ej.: ingeniería de software, medicina)?

- **¿Por qué?** Define el alcance funcional y las fuentes de datos a integrar.
    
- **Impacto:** Determina bases de datos clave (ej.: IEEE Xplore para software, PubMed para medicina) y algoritmos de búsqueda.
    

### #==4.2. ¿El sistema analizará texto completo o solo metadatos?==

- **¿Por qué?** Especifica capacidades técnicas críticas.
    
- **Impacto:** Si incluye texto completo, se necesitan funciones avanzadas (ej.: OCR, análisis semántico), afectando módulos de descarga y extracción.
    

### #4.3. ¿Qué nivel de integración con herramientas externas (ej.: Zotero, Mendeley) se espera?

- **¿Por qué?** Define interoperabilidad y usabilidad.
    
- **Impacto:** APIs y soporte para formatos como BibTeX/RIS afectan el diseño técnico y la priorización de funcionalidades.
    

### #4.4. ¿Se priorizarán fuentes de acceso abierto o de pago?

- **¿Por qué?** Establece limitaciones y técnicas.
    
- **Impacto:** Fuentes de pago (ej.: Scopus) requieren acuerdos y mayor inversión, mientras que el acceso abierto simplifica el acceso pero reduce cobertura.