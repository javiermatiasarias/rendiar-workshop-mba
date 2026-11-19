# Tickets sintéticos

Fuente visual del caso RendiAR. Todos los comprobantes son ficticios y muestran la leyenda “Documento sintético · No válido fiscalmente”.

## Contenido

- 75 archivos PNG en total.
- 74 operaciones con al menos un ticket asociado.
- Cuatro conceptos por ticket.
- Fecha, hora, moneda, razón social, identificación fiscal y total visibles.
- `indice_tickets.csv` relaciona IDs y archivos sin describir todas las discrepancias.

## Convención

El nombre principal coincide con el ID de la operación: `G01.png`, `G02.png`, etc. El campo `descripcion` del Excel es el motivo empresarial declarado y no aparece como concepto del ticket.

## Casos intencionales

- G04 contiene una bebida alcohólica entre varios conceptos.
- G05 tiene un total diferente del monto declarado en el Excel.
- G06 no tiene ticket.
- G07 tiene un ticket principal y una copia duplicada idéntica.
- G09 tiene una fecha diferente de la declarada.

Estos casos permiten ejecutar R3–R6. No corregir ni descartar automáticamente: señalar la discrepancia y conservar la decisión humana.
