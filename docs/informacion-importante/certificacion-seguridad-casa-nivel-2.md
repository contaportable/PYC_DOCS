# Certificación de Seguridad CASA nivel 2

## Objetivo
Dar a conocer brevemente qué es la certificación CASA nivel 2, cómo PyConta la cumple y qué beneficio obtiene el cliente en seguridad de sus datos.

## Qué es CASA nivel 2
CASA nivel 2 es una evaluación de seguridad para aplicaciones que valida controles clave como arquitectura, autenticación, sesiones, control de acceso, protección de datos y comunicaciones. En términos simples, confirma que un programa desktop que integra servicios en la nube cumple prácticas de seguridad exigentes.

## Cómo lo cumple PyConta
PyConta, reporta una validación CASA Tier 2 realizada por laboratorio independiente autorizado. En esta validación se cubrieron controles técnicos alineados con OWASP ASVS y se obtuvo resultado satisfactorio en categorías de seguridad críticas.

Áreas de cumplimiento destacadas:

- Arquitectura y modelado de amenazas.
- Autenticación y gestión de sesión.
- Control de acceso.
- Validación y sanitización de entradas.
- Criptografía y protección de datos.
- Manejo de errores y logging.
- Seguridad en comunicaciones.
- Seguridad en APIs y servicios web.
- Verificación de configuración y lógica de negocio.

Controles aplicados al uso de PyConta:

- Cifrado en tránsito (HTTPS/TLS) en las comunicaciones con servicios externos.
- Cifrado en reposo (AES-GCM-256) para la información sensible.
- Mecanismos de integridad y controles de acceso para proteger identidad y consistencia de datos.
- Gestión de autenticación y permisos (p. ej. OAuth2) con capacidad de revocación por el cliente.

## Beneficio para el cliente
El resultado para el cliente es una experiencia con mayor confianza y menor exposición de información sensible:

- Confidencialidad: el cifrado en tránsito (HTTPS/TLS) y en reposo (AES-GCM-256) protege los datos contra accesos no autorizados.
- Integridad y consistencia: los mecanismos de integridad y los controles de acceso reducen el riesgo de manipulación y mantienen la calidad de los datos.
- Control de accesos y revocabilidad: la gestión de autenticación y permisos (OAuth2) permite proteger y revocar accesos a cuentas y correos conectados.
- Certificación y cumplimiento: la validación CASA nivel 2 aporta una garantía externa sobre las prácticas y controles aplicados.

## Resumen de validación
La evidencia oficial de cumplimiento incluye el identificador de certificación, el tipo de evaluación (Tier 2 Lab Tested - Lab Verified), el laboratorio evaluador independiente y el estado del proceso de validación. Para evitar duplicaciones de contenido legal, la referencia oficial se mantiene mediante el enlace directo al documento de certificación.

## Documento de referencia
- Reporte oficial de validación CASA Tier 2: [Ver documento](https://drive.google.com/file/d/1PiDJRr_S7SFqkjIG-S9lFhqVK8aWnD_J/view?usp=sharing)

## Siguientes pasos
1. Revisar [Límites del Sistema](limites-del-sistema.md).
2. Revisar [Requisitos y Rendimiento](requisitos-hardware-rendimiento.md).
3. Continuar con [Primeros Pasos](../primeros-pasos/instalacion-acceso.md).
