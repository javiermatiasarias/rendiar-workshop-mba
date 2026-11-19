# Brief de RendiAR — v02

Caso ficticio adaptado para aprendizaje. Todos los datos son sintéticos.

## Usuario y problema

Un empleado necesita revisar los datos declarados de sus gastos antes de presentarlos. El conjunto contiene operaciones completas y otras con datos faltantes o inválidos para que el grupo pueda diseñar cómo detectar, corregir y volver a comprobar esos casos.

## Hipótesis de valor

Una revisión guiada podría reducir errores y retrabajo antes de la presentación del gasto. Este beneficio es una hipótesis: no fue medido ni validado en el workshop.

## Fuente vigente

Usar `gastos_ficticios.xlsx`, hoja `Gastos`. Contiene 75 operaciones identificadas de G01 a G75 y una hoja `Diccionario`. Sus campos son: `id`, `fecha`, `hora`, `monto`, `moneda`, `razon_social`, `identificacion_fiscal` y `descripcion`.

La `descripcion` expresa el motivo declarado por la persona. No replica los conceptos de un ticket. Los faltantes y valores inválidos son intencionales: no completarlos por inferencia ni corregirlos automáticamente.

## Alcance de esta versión

- Inspeccionar los datos declarados en el workbook.
- Detectar campos faltantes y valores inválidos según la política vigente.
- Diseñar el recorrido de corrección, nueva comprobación, salida pendiente y confirmación humana.
- Producir artifacts de concepto y requisitos, process flow, service blueprint, wireframe y revisión.

## Tickets: fuente visual

Usar las imágenes de `01_fuentes/tickets/` y su índice. Cada ticket usa el ID de la operación y contiene varios conceptos. La comparación debe usar el total y conservar los conceptos por separado; no se debe interpretar `descripcion` como si fuera el detalle del ticket.

La fuente incluye casos intencionales de ticket faltante, duplicado, total o fecha diferentes y un concepto de bebida alcohólica. Deben detectarse mediante comparación, sin corregir ni decidir automáticamente.

## Reglas

La definición completa y su estado están en `politica_gastos_v01.md`:

- R1: campos obligatorios completos.
- R2: monto mayor que cero.
- R3: ticket existente, único y legible.
- R4: coincidencia de datos principales entre declaración y ticket.
- R5: coincidencia entre monto declarado y total del ticket.
- R6: bebidas alcohólicas no reembolsables.
- R7: confirmación explícita del empleado después de la revisión.

## Fuera del ejercicio

No se construye una aplicación funcional. También quedan fuera la aprobación empresarial real, la integración contable, el pago o reembolso, el procesamiento de datos reales y cualquier decisión automática irreversible.

## Artifacts esperados

Concepto y requisitos; process flow con excepciones; service blueprint del mismo recorrido; wireframe anotado; registro de revisión y decisiones. Cada output debe identificar fuentes, versión, supuestos y limitaciones.
