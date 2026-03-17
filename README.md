# 🔬 Analizador de Formatos de Archivo

Herramienta web para el análisis y caracterización de documentos electrónicos, orientada a la preservación digital y la gestión documental en el contexto normativo chileno.

**[Probar la herramienta →](https://constanzaacunacerda.github.io/analizador-formatos/)**

## Descripción

El Analizador de Formatos permite examinar cualquier archivo electrónico directamente desde el navegador, sin instalación y sin enviar datos a servidores externos — todo el procesamiento ocurre localmente en el equipo del usuario.

Al cargar un archivo (PDF, Office, imágenes, audio, video, entre otros), la herramienta entrega un diagnóstico técnico completo en segundos, útil para quienes trabajan en tramitación de documentos electrónicos, revisión de expedientes, preparación de transferencias documentales o preservación digital.

## Funcionalidades

### Identificación y validación de formatos
- Identificación de formato mediante firmas binarias (magic numbers) y clasificación PRONOM, inspirada en **DROID** (The National Archives, UK)
- Validación de estructura interna (well-formedness), análoga a **JHOVE**
- Validación de conformidad PDF/A (ISO 19005), inspirada en **veraPDF**
- Clasificación de preservación según **NARA Digital Preservation Framework** (Bulletin 2014-04)

### Integridad y seguridad
- Cálculo de checksums: SHA-256, SHA-1, SHA-512, MD5, CRC32
- Comparación de checksums contra valores conocidos
- Comparación lado a lado de dos archivos (verificación de migraciones, copias, respaldos)
- Detección de indicadores de seguridad: macros, scripts, contenido activo
- Detección de OCR en PDFs escaneados

### Firma electrónica
- Detección de firmas electrónicas en documentos PDF
- Identificación de Firma Electrónica Avanzada (FEA) conforme a la Ley 19.799
- Detección de sellos de tiempo RFC 3161

### Conformidad normativa chilena
- Evaluación artículo por artículo contra el **Decreto N° 4/2021** (Reglamento de la Ley 21.180 de Transformación Digital del Estado)
- Verificación de requisitos de formato de preservación (Art. 51/53), firma electrónica (Art. 10 inc. 3°), integridad (Art. 53), metadatos (Art. 49), accesibilidad (Art. 47/52) y ausencia de elementos activos (Art. 51)

### Metadatos y estándares de preservación
- Extracción de metadatos técnicos: título, autor, fechas, software de creación, versión del formato
- Generación de eventos de caracterización **PREMIS 3.0** en formato XML
- Mapeo contra el esquema de metadatos **SGD** de 54 campos (esquema de transferencia del Archivo Nacional)
- Generación de manifiestos **BagIt** (RFC 8493) para empaquetado de objetos digitales
- Evaluación de riesgo de preservación con gráfico radar

### Herramientas adicionales
- Visor hexadecimal
- Vista de código fuente (raw)
- Análisis y sugerencias de nomenclatura de archivos
- Glosario integrado de términos de preservación digital
- Exportación de informes en formato texto y HTML
- Procesamiento por lotes (múltiples archivos)

## Estándares y referencias

La herramienta se nutre de los siguientes estándares, metodologías y marcos normativos:

| Estándar / Referencia | Uso en la herramienta |
|---|---|
| OAIS (ISO 14721) | Modelo conceptual de referencia |
| PREMIS 3.0 | Generación de metadatos de preservación |
| BagIt (RFC 8493) | Empaquetado para transferencia de objetos digitales |
| PRONOM (TNA UK) | Registro de formatos para identificación |
| NARA Digital Preservation Framework | Clasificación de riesgo de preservación |
| ISO 19005 (PDF/A) | Validación de formato de preservación |
| Ley 21.180 / Decreto N° 4/2021 | Conformidad normativa chilena |
| Ley 19.799 / DS 181/2002 | Firma electrónica y sellos de tiempo |
| ISAD(G) / ISAAR(CPF) | Esquema de metadatos descriptivos |

Funcionalidades inspiradas en: DROID, JHOVE, veraPDF, ExifTool, MediaInfo, Apache Tika y Bagger.

## Uso

1. Abrir la herramienta en el navegador: [constanzaacunacerda.github.io/analizador-formatos](https://constanzaacunacerda.github.io/analizador-formatos/)
2. Arrastrar o seleccionar un archivo
3. Navegar por las pestañas para explorar los resultados del análisis

No requiere instalación, registro ni conexión a servidores externos.

## Tecnología

Aplicación web estática construida en HTML, CSS y JavaScript puro. Todo el procesamiento se realiza en el navegador del usuario mediante la Web Crypto API y análisis binario directo. No se utilizan frameworks ni dependencias externas.

## Autoría

Desarrollada por **Constanza Acuña Cerda**, Coordinadora de Preservación Digital del Archivo Nacional de Chile.

## Licencia

Esta herramienta se comparte con fines educativos y de difusión profesional en el ámbito de la preservación digital y la gestión de documentos electrónicos.
