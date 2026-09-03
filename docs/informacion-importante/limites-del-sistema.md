---
description: Alcance operativo y límites del sistema PyConta.
---

# **Límites del Sistema**

## **Alcance y Límites Operativos**

- **Bandejas de correo**: No accede a bandejas ocultas ni a carpetas de Spam a menos que los correos sean trasladados a una bandeja visible.
- **Protocolos de correo**: Requiere servidores compatibles con IMAP o autenticación OAuth 2.0 (Gmail / Microsoft 365). Actualmente no se cuenta con soporte para POP3.
- **Permisos de cuentas**: Puede verse limitado en cuentas corporativas con permisos restringidos por políticas de TI o en cuentas Google con control parental.
- **Documentos físicos**: Únicamente se pueden registrar documentos fiscales físicos a nivel de la tabla de Anexos F07; actualmente no se incorporan a la base de datos general de DTEs ni se incluyen en los Libros de IVA.
- **Emisión de DTEs**: PyConta no es un sistema emisor o facturador de DTEs; su función es la recepción, conciliación, validación y generación de libros de IVA.
- **Consultas a Hacienda**: La validación oficial de DTEs y recuperación de sellos depende de la disponibilidad del servicio de consulta del Ministerio de Hacienda.
- **Resiliencia de conexión**: Una mala conexión a internet o falta de permisos en el correo puede interrumpir la descarga de nuevos mensajes, pero no afecta los documentos ya almacenados ni el resto de funciones de PyConta.

---

## **Enlaces Relacionados**
- [Requisitos y Rendimiento](requisitos-hardware-rendimiento.md)
- [Buenas Prácticas Operativas](buenas-practicas-operativas.md)
- [Parámetros de Validación](../flujos/parametros-validacion.md)
