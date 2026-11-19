# Política de gastos — v01

Política sintética para el caso RendiAR. Sirve como fuente del ejercicio; no representa una política real de UCEMA ni de otra organización.

| Regla | Criterio | Resultado esperado | Estado de la fuente |
|---|---|---|---|
| R1 | `id`, `fecha`, `hora`, `monto`, `moneda`, `razon_social`, `identificacion_fiscal` y `descripcion` deben estar completos. | Si falta un campo, la operación queda pendiente hasta que una persona aporte el dato. | Ejecutable con el Excel. |
| R2 | El monto declarado debe ser mayor que cero. | Un valor cero o negativo requiere corrección aportada por la persona. | Ejecutable con el Excel. |
| R3 | Debe existir un único ticket legible asociado al mismo ID. | Si falta, está duplicado o no puede leerse, la operación queda pendiente. | Ejecutable con los tickets. |
| R4 | Fecha, hora, moneda, razón social e identificación fiscal declaradas deben coincidir con el ticket. | Una diferencia se señala y requiere revisión humana. | Ejecutable con Excel y tickets. |
| R5 | El monto declarado debe coincidir con el total del ticket. | Una diferencia se señala y requiere corrección o justificación humana. | Ejecutable con Excel y tickets. |
| R6 | Los conceptos de bebidas alcohólicas no son reembolsables. | En un ticket mixto, se excluye el concepto no admitido y la operación queda pendiente hasta confirmar el monto ajustado. | Ejecutable con los tickets. |
| R7 | El empleado debe confirmar explícitamente después de revisar los datos y alertas. | Sólo entonces el estado puede pasar a “Gasto preparado para presentar”. | Ejecutable como requisito de diseño. |

## Guardrails del ejercicio

- No inferir moneda, campos faltantes ni contenido de tickets.
- No convertir automáticamente un monto negativo en positivo.
- Comparar fuentes y citar el ID y el elemento observado antes de afirmar una discrepancia.
- No aprobar, presentar, pagar ni reembolsar gastos.
- Mantener una salida pendiente y una instancia de decisión humana.
