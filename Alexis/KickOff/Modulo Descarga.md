Módulo de Descarga

  

El **Módulo de Descarga** es una pieza clave en el sistema SLR, encargado de conectar las estrategias de búsqueda generadas por el **Módulo de Diseño** con las etapas de selección y análisis posteriores. Su función principal es recuperar **metadatos** (título, autores, abstract, DOI, etc.) y **documentos completos** (PDFs) de fuentes académicas, asegurando que los datos estén disponibles para los módulos de **Selección** y **Extracción**. ==Este módulo no genera búsquedas ni analiza contenido, sino que actúa como un sistema automatizado de recuperación eficiente y trazable.==

---

**Objetivos del Módulo de Descarga**

**Objetivo General**

Desarrollar un sistema automatizado que recupere metadatos y documentos completos de múltiples fuentes académicas de manera eficiente.

**Objetivos Específicos**

1. **Integrar fuentes académicas clave**: Conectar al menos tres motores de búsqueda académicos (por ejemplo, IEEE Xplore, Scopus, CORE) mediante APIs o scraping.
    
2. **Estructurar metadatos**: Recuperar y organizar metadatos en formatos estándar como **BibTeX** y **RIS** para facilitar su uso en herramientas bibliográficas (Zotero, EndNote).
    
3. **Automatizar descargas**: Implementar la descarga de PDFs para estudios aprobados por el **Módulo de Selección**, priorizando fuentes de acceso abierto cuando sea posible.
    
4. **Asegurar trazabilidad**: Generar logs detallados de las operaciones (motores consultados, documentos recuperados, errores) para auditoría y seguimiento.
    
5. **Manejar errores robustamente**: Diseñar un sistema que gestione limitaciones de APIs (cuotas, autenticación) y fallos de conexión con reintentos automáticos.
    

---

**Alcance del Módulo de Descarga**

**Lo que SÍ incluirá**

|   |   |
|---|---|
|**Componente**|**Descripción**|
|**Integración con APIs**|Conexión a motores académicos como IEEE Xplore, Scopus, y CORE mediante APIs oficiales.|
|**Recuperación de metadatos**|Extracción de datos clave: DOI, título, autores, abstract, año, keywords, fuente.|
|**Descarga de PDFs**|Automatización para obtener documentos completos de estudios aprobados, priorizando acceso abierto.|
|**Formatos de exportación**|Soporte para BibTeX y RIS, con posibilidad de CSV o JSON para integración con otros módulos.|
|**Manejo de errores**|Reintentos automáticos (máx. 3) y reportes de fallos (ej: documento no disponible).|
|**Logs y estadísticas**|Registro de operaciones (motores usados, documentos recuperados) y métricas de éxito.|

**Lo que NO incluirá**

|   |   |
|---|---|
|**Componente**|**Razón de exclusión**|
|**Generación de búsquedas**|Responsabilidad del<br><br>**Módulo de Diseño**<br><br>, que entrega las cadenas de búsqueda al módulo.|
|**Selección de estudios**|El<br><br>**Módulo de Selección**<br><br>decide qué estudios son relevantes; este módulo solo los recupera.|
|**Análisis de contenido**|El procesamiento de PDFs (extracción de texto, tablas) lo realiza el<br><br>**Módulo de Extracción**<br><br>.|

**Limitaciones técnicas**

- **Dependencia de APIs**: El acceso a Scopus o IEEE Xplore puede estar limitado por cuotas o suscripciones.
    
- **Volumen de datos**: La capacidad de descarga masiva dependerá del hardware y ancho de banda disponible.
    
- **Acceso abierto**: Si no hay suscripción institucional, se priorizarán fuentes como CORE o Semantic Scholar.
    

---

**Preguntas para el Kick-Off**

**1. Sobre los Motores de Búsqueda**

- ¿Cuáles son los 3-5 motores académicos prioritarios para integrar? (Ej: IEEE Xplore, Scopus, PubMed, CORE, Semantic Scholar).
    
- ¿Está permitido el uso de web scraping ético para motores sin API oficial ?
    
- ==¿Qué restricciones éticas o legales debo considerar?==
    

**2.**

- ¿Qué formato de metadatos es prioritario (BibTeX, RIS, ambos)? ¿Se necesita conversión entre formatos?
    
- ¿El módulo debe descargar PDFs masivamente o solo proveer metadatos y enlaces iniciales?
    
- ==¿Qué campos de metadatos son esenciales para el== **==Módulo de Selección==** ==y el== **==Módulo de Extracción==** ==(ej: DOI, abstract, keywords)?==
    

**3. Sobre la Integración con Otros Módulos**

- ==¿En qué formato debo recibir las cadenas de búsqueda del== **==Módulo de Diseño==** ==(ej: texto plano, JSON)?==
    
- ==¿Cómo recibiré la lista de DOIs aprobados del== **==Módulo de Selección==** ==(ej: CSV, JSON)? ¿Quién define este estándar?==
    
- ==¿Cómo debo entregar los PDFs al== **==Módulo de Extracción==** ==(ej: sistema de archivos compartido, API)? ¿Se requiere preprocesamiento?==
    

**4. Sobre el Alcance y Limitaciones**

- ¿El módulo debe validar la calidad de los metadatos (ej: DOI resoluble) o solo recuperarlos tal cual?
    
- ¿Cuál es el volumen esperado de documentos por búsqueda (ej: 100, 1000)? ¿Hay restricciones de tiempo para la recuperación?
    
- ¿Se necesita soporte para idiomas no latinos en los metadatos (ej: chino, árabe)?
    
- ¿Cómo manejaremos documentos detrás de paywalls? ==¿Solo abstracts o buscar versiones abiertas?==
    

  

---

**Consideraciones Adicionales**

- **Riesgos**:
    
    - APIs de pago pueden tener cuotas limitadas (Scopus: 20,000 solicitudes/mes).
        
    - Cambios inesperados en las APIs requerirán mantenimiento.
        
    - Documentos no disponibles en acceso abierto pueden reducir la cobertura.
        
- **Mitigación**:
    
    - Priorizar fuentes abiertas (CORE, DBLP).
        
    - Diseñar un sistema modular para facilitar ajustes en las conexiones a APIs.
        
    - Coordinar con el cliente para obtener accesos institucionales.
        
- **Validación**:
    
    - Probar el módulo con un dataset de 50 documentos de acceso abierto.
        
    - Garantizar una tasa de éxito en descargas ≥95%.