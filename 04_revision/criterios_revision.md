# Criterios de revisión

Estado inicial: ninguno de estos casos fue ejecutado. Registrar evidencia después de revisar un output concreto.

## Casos ejecutables con el workbook

| Caso | Condición intencional | Qué debería expresar el diseño | Evidencia | Resultado |
|---|---|---|---|---|
| G01 | Completo | Permite revisar; la confirmación final sigue siendo humana | Por registrar | Por revisar |
| G02 | Sin moneda | Señala faltante; la persona aporta el dato o queda pendiente | Por registrar | Por revisar |
| G03 | Monto negativo | Señala monto inválido; requiere corrección aportada por la persona | Por registrar | Por revisar |
| G08 | Sin identificación fiscal | Señala el campo faltante según R1 | Por registrar | Por revisar |
| G18 | Sin hora | Señala el campo faltante según R1 | Por registrar | Por revisar |
| G23 | Monto cero | Señala monto inválido según R2 | Por registrar | Por revisar |
| G31 | Sin razón social | Señala el campo faltante según R1 | Por registrar | Por revisar |
| G42 | Sin descripción | Señala el campo faltante según R1 | Por registrar | Por revisar |
| G59 | Sin moneda | Señala el campo faltante según R1 | Por registrar | Por revisar |
| G63 | Sin identificación fiscal | Señala el campo faltante según R1 | Por registrar | Por revisar |

## Casos previstos para la etapa de tickets

Estos casos no pueden ejecutarse todavía. No registrar un resultado hasta incorporar la fuente.

| Caso | Escenario previsto | Regla principal | Estado |
|---|---|---|---|
| G04 | Ticket con bebida alcohólica entre varios conceptos | R6 | Pendiente de ticket |
| G05 | Total del ticket diferente del monto declarado | R5 | Pendiente de ticket |
| G06 | Ticket faltante | R3 | Pendiente de ticket |
| G07 | Ticket duplicado | R3 | Pendiente de ticket |
| G09 | Fecha del ticket diferente de la declarada | R4 | Pendiente de ticket |

## Comprobar el paquete

- Los requisitos tienen casos y resultados esperados.
- El flow contempla recorrido normal, corrección y pendiente.
- El blueprint corresponde al mismo escenario y asigna responsabilidades propuestas.
- El wireframe respeta las reglas y los estados.
- Las reglas dependientes de tickets se identifican como pendientes de fuente.
- La revisión cita artifact, versión y elemento observado.
- La decisión humana y el siguiente paso se registran.
- Si falta un artifact o hay versiones contradictorias, se explica qué revisión no puede completarse.

## Hallazgo

Artifact y versión / ubicación / discrepancia / impacto / cambio propuesto / decisión / evidencia posterior.

Las revisiones de documentos no prueban una aplicación funcionando ni sustituyen pruebas con usuarios reales.
