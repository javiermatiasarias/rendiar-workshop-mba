# Brief de RendiAR — v01

Caso ficticio adaptado para aprendizaje. Reglas propuestas para confirmar en clase.

## Usuario y problema

Un empleado necesita revisar y corregir los datos de un gasto antes de presentarlo. Algunos registros tienen datos faltantes o inválidos.

## Hipótesis de valor

Una revisión guiada podría reducir errores y retrabajo. No se ha medido ni validado ese beneficio en este ejercicio.

## Alcance

Revisar campos, identificar errores, corregir, volver a comprobar y confirmar los datos. El estado final del recorrido es “Gasto preparado para presentar”. Si falta información que el empleado no puede aportar, permanece pendiente.

## Datos

Usar gastos_ficticios.csv. Fechas en ISO YYYY-MM-DD; montos numéricos sin separador de miles; moneda en código. La celda de moneda de G02 está vacía intencionalmente. El monto negativo de G03 también es intencional.

## Reglas propuestas

- R1: identificador, fecha, monto, moneda y descripción completos.
- R2: monto mayor que cero.
- R3: confirmación explícita del empleado después de revisar.

No inferir moneda por contexto ni cambiar un monto negativo a positivo sin una corrección aportada por la persona. No usar “ARS” como moneda automática para G02.

## Fuera del ejercicio

Extracción automática de comprobantes, aprobación empresarial, integración contable y reembolso. No se construye una aplicación funcional.

## Pendientes

Las políticas empresariales de aprobación no están definidas. No son necesarias para el recorte; registrarlas como fuera de alcance o pendientes, sin inventarlas.

## Artifacts esperados

Concepto y requisitos de una página; process flow con excepción; service blueprint del mismo recorrido; un wireframe anotado; registro de revisión y decisiones.
