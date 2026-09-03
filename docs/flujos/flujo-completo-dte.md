---
description: Resumen del ciclo de vida de un DTE en PyConta, desde su ingreso hasta las salidas contables y fiscales.
---

# **Flujo Completo de Gestión de DTEs**

PyConta centraliza la captura, validación, exportación y generación de libros y declaraciones de impuestos a partir de tus DTEs.

---

## **Diagrama del Ciclo de Vida del DTE**

```mermaid
flowchart TD
  subgraph Captura["1. Ingreso de DTEs"]
    A["📥 Descarga desde Correo"] --> B["🔄 Sincronización"]
    A2["📂 Inserción Local"]
  end

  B --> C["📊 2. Lector JSON<br/>(Visualización y Búsqueda)"]
  A2 --> C

  C --> D["🔎 3. Consulta en Hacienda<br/>(Validación de estado y sellos)"]
  
  D --> G["📤 4. Extracción y Exportación<br/>(Excel, DTEs y Metadata)"]
  D --> E["📑 5. Libros de IVA<br/>(PDF y Excel)"]
  D --> F["📝 6. Anexos de Impuestos F07<br/>(CSV para Hacienda)"]

  style Captura fill:#fafafa,stroke:#9e9e9e,stroke-width:1px,stroke-dasharray: 5 5;
  style A fill:#e3f2fd,stroke:#1976d2,stroke-width:2px;
  style B fill:#e8f5e9,stroke:#388e3c,stroke-width:2px;
  style A2 fill:#ede7f6,stroke:#512da8,stroke-width:2px;
  style C fill:#fff3e0,stroke:#f57c00,stroke-width:2px;
  style D fill:#f3e5f5,stroke:#7b1fa2,stroke-width:2px;
  style G fill:#fffde7,stroke:#fbc02d,stroke-width:2px;
  style E fill:#e0f7fa,stroke:#0097a7,stroke-width:2px;
  style F fill:#fbe9e7,stroke:#d84315,stroke-width:2px;
```

---

## **Etapas del Flujo de Trabajo**

### 1. Ingreso de DTEs
- **[Descarga Desde Correo](descarga-desde-correo.md)** y **[Sincronización](sincronizacion.md)**: Extrae DTEs de tus buzones y los clasifica automáticamente por periodo y categoría.
- **[Inserción Local](importacion-json.md)**: Carga manual de archivos o carpetas `.json` desde tu equipo.

### 2. Exploración en Lector JSON
- **[Lector JSON](lector-json.md)**: Visualización dual (PDF y JSON), búsqueda rápida por cualquier dato de la tabla, reclasificación de periodos y resumen financiero.

### 3. Validación ante Hacienda
- **[Consulta en Hacienda](consulta-hacienda.md)**: Verifica estados oficiales (Aceptado, Rechazado, Invalidado) y recupera sellos de recepción directamente del servicio de consulta del Ministerio de Hacienda.

### 4. Extracción y Exportación
- **Excel y DTEs**: Exporta listados consolidados en `.xlsx` o empaqueta los archivos `.json` originales.
- **Exportar Metadata**: Genera resúmenes estructurados por año o mes para análisis contable o integración con IA.

### 5. Salidas Fiscales
- **[Libros de IVA](libros-iva.md)**: Emisión de libros de Consumidor, Compras y Contribuyente en PDF y Excel.
- **[Anexos de Impuestos F07](anexos-de-impuestos-f07.md)**: Edición en tabla y generación del archivo CSV para el Ministerio de Hacienda.
