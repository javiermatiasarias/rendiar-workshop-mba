# Verificación de fuentes — v01

Fecha: 19 de noviembre de 2026
Alcance: IDs, importes y excepciones de `gastos_ficticios.xlsx` y `01_fuentes/tickets/`.

## Resultado

**Aprobado para revisión docente. No se encontraron inconsistencias inesperadas.**

| Comprobación | Resultado |
|---|---|
| Filas e IDs del workbook | 75 filas; 75 IDs únicos, G01–G75. |
| Archivos de tickets | 75 PNG para 74 IDs. G06 falta y G07 tiene dos archivos, según el caso previsto. |
| ID impreso frente al nombre de archivo | 75 de 75 coinciden. |
| Total impreso legible | 75 de 75 recuperados y comparados. |
| Importe frente al Excel | 71 IDs con ticket coinciden; G03, G05 y G23 difieren intencionalmente. G06 no tiene ticket. |
| Fecha frente al Excel | Todas coinciden salvo G09, diferencia intencional. |
| Moneda, hora, comercio e identificación fiscal | Sin diferencias inesperadas cuando el dato declarado existe. |
| Duplicados binarios | Sólo G07 y G07_duplicado son idénticos, como estaba previsto. |
| Alcohol | Sólo G04 contiene “Copa de vino”. |

El detalle por operación está en [verificacion_fuentes_v01.csv](verificacion_fuentes_v01.csv).

## Excepciones confirmadas

### R1 — Campos obligatorios

- G02: falta moneda.
- G08: falta identificación fiscal.
- G18: falta hora.
- G31: falta razón social.
- G42: falta descripción.
- G59: falta moneda.
- G63: falta identificación fiscal.

### R2 — Monto mayor que cero

- G03: monto declarado −3000.
- G23: monto declarado 0.

### R3 — Ticket único y legible

- G06: ticket faltante.
- G07: ticket duplicado; ambos archivos tienen el mismo hash SHA-256.

### R4 — Coincidencia de datos

- G09: el Excel declara 18/11/2026 y el ticket muestra 17/11/2026.

### R5 — Coincidencia del total

- G03: Excel −3000; ticket 3000.
- G05: Excel 24500; ticket 26800.
- G23: Excel 0; ticket 82550.

G03 y G23 son excepciones compuestas: incumplen R2 y, al compararse con un ticket positivo, también R5. Esto es coherente y debe aparecer en el diseño como más de una alerta sobre la misma operación.

### R6 — Conceptos no reembolsables

- G04: incluye “Copa de vino” por 3250 dentro de un total de 32500.

## Método y evidencia

1. Lectura estructurada del workbook y control de unicidad de IDs.
2. Inventario de imágenes y control de cobertura por ID.
3. OCR independiente sobre los 75 PNG para recuperar ID, fecha, hora, moneda, comercio, identificación fiscal y total impresos.
4. Comparación automática con el workbook.
5. Comparación de hashes para detectar duplicados.
6. Revisión visual de muestras y de tres paneles con la colección completa.

## Límite de esta verificación

La auditoría confirma consistencia de las fuentes sintéticas. No valida todavía los artifacts de producto, el comportamiento de una aplicación ni una decisión de reembolso.
