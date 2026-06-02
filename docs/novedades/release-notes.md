# Release Notes

## Proposito
Registrar cambios funcionales y operativos por version.

## Plantilla
### Versión 1.0.0.9.3 - 2026-06-02

- **Nuevo:**
  - Implementación de un sistema de "Primera Sincronización Inteligente" para la lectura y procesamiento completo del historial de correos electrónicos descargados.
  - Integración de filtros de búsqueda avanzados en la vista de inserción manual de archivos.
  - Implementación de un flujo guiado de configuración inicial (*onboarding*) para nuevos usuarios del sistema.
  - Añadido de paneles dinámicos redimensionables en la pantalla de carga de archivos para una gestión de secciones a medida del usuario.

- **Mejorado:**
  - Optimización en el motor de búsqueda del visor de comprobantes y adición de carga por lotes (*batch loading*) para un rendimiento fluido con bases de datos pesadas.
  - Optimización de velocidad, fluidez visual y transiciones de pantalla en los formularios de registro de empresas y usuarios mediante carga progresiva (*lazy loading*).
  - Mejora en el lector de documentos PDF, optimizando los eventos de desplazamiento (*scroll*) y añadiendo soporte para atajos de teclado estándar.
  - Rediseño del algoritmo de ajuste automático para columnas de tablas, garantizando una correcta legibilidad de las fuentes en pantallas de diferentes tamaños.
  - Mejora en el algoritmo de limpieza y soporte de codificaciones para evitar errores de lectura al procesar archivos de comprobantes electrónicos (JSON).
  - Optimización en las funciones de autocompletado para operaciones de ventas a consumidores y facturas de exportación (FEX) en la tabla de Anexos de Impuestos F07.
  - Refinamiento en la lógica de sincronización mensual, aplicando filtros inteligentes para la correcta organización cronológica de los documentos.

- **Corregido:**
  - Corrección en el cálculo de las sumatorias automáticas en la columna de totales dentro de la tabla de Anexos de Impuestos F07.
  - Corrección de un error de comportamiento al utilizar el comando "Deshacer" (Ctrl + Z) dentro del registro de ventas de la tabla de Anexos de Impuestos F07.
  - Corrección y estandarización en el comportamiento y jerarquía de las ventanas de carga de archivos para evitar bloqueos visuales en la interfaz.

- **Impacto operativo:**
  - Reducción drástica de la fatiga visual y los tiempos de espera al procesar listados contables masivos gracias a las optimizaciones de renderizado y el redimensionamiento dinámico de paneles.
  - Mayor confiabilidad y velocidad en la generación de la declaración de impuestos (Anexos F07) al asegurar cálculos exactos en las sumatorias y prevenir errores de edición de datos en la cuadrícula.
  - Disminución del tiempo de configuración inicial para nuevos clientes gracias al asistente de bienvenida integrado.

- **Acciones recomendadas:**
  - Se aconseja utilizar el nuevo sistema de filtros e inserción de archivos para agilizar el procesamiento mensual de los DTEs retenidos en carpetas locales.
  - Validar las sumatorias automáticas en las plantillas de los Anexos F07 generados para verificar la correcta consistencia de los totales consolidados.

### Version X.Y.Z - AAAA-MM-DD
- Nuevo:
- Mejorado:
- Corregido:
- Impacto operativo:
- Acciones recomendadas:
