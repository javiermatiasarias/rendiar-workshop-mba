# Criterios de revisión

Las fuentes fueron verificadas el 19 de noviembre de 2026. Los artifacts de producto todavía no fueron ejecutados; registrar nueva evidencia al revisar cada output.

## Casos ejecutables con el workbook

| Caso | Condición intencional | Qué debería expresar el diseño | Evidencia | Resultado |
|---|---|---|---|---|
| G01 | Completo | Permite revisar; la confirmación final sigue siendo humana | `verificacion_fuentes_v01.csv` | Fuente verificada |
| G02 | Sin moneda | Señala faltante; la persona aporta el dato o queda pendiente | `verificacion_fuentes_v01.csv` | Fuente verificada |
| G03 | Monto negativo | Señala R2 y la diferencia R5; requiere corrección humana | `verificacion_fuentes_v01.csv` | Fuente verificada |
| G08 | Sin identificación fiscal | Señala el campo faltante según R1 | `verificacion_fuentes_v01.csv` | Fuente verificada |
| G18 | Sin hora | Señala el campo faltante según R1 | `verificacion_fuentes_v01.csv` | Fuente verificada |
| G23 | Monto cero | Señala R2 y la diferencia R5; requiere corrección humana | `verificacion_fuentes_v01.csv` | Fuente verificada |
| G31 | Sin razón social | Señala el campo faltante según R1 | `verificacion_fuentes_v01.csv` | Fuente verificada |
| G42 | Sin descripción | Señala el campo faltante según R1 | `verificacion_fuentes_v01.csv` | Fuente verificada |
| G59 | Sin moneda | Señala el campo faltante según R1 | `verificacion_fuentes_v01.csv` | Fuente verificada |
| G63 | Sin identificación fiscal | Señala el campo faltante según R1 | `verificacion_fuentes_v01.csv` | Fuente verificada |

## Casos con tickets

Las fuentes están disponibles y fueron comparadas. Volver a registrar evidencia al comprobar que los artifacts representen estos casos.

| Caso | Escenario previsto | Regla principal | Estado |
|---|---|---|---|
| G04 | Ticket con bebida alcohólica entre varios conceptos | R6 | Fuente verificada |
| G05 | Total del ticket diferente del monto declarado | R5 | Fuente verificada |
| G06 | Ticket faltante | R3 | Fuente verificada |
| G07 | Ticket duplicado | R3 | Fuente verificada |
| G09 | Fecha del ticket diferente de la declarada | R4 | Fuente verificada |

## Comprobar el paquete

- Los requisitos tienen casos y resultados esperados.
- El flow contempla recorrido normal, corrección y pendiente.
- El blueprint corresponde al mismo escenario y asigna responsabilidades propuestas.
- El wireframe respeta las reglas y los estados.
- Las reglas R3–R6 se comprueban contra las imágenes y se cita evidencia concreta.
- La revisión cita artifact, versión y elemento observado.
- La decisión humana y el siguiente paso se registran.
- Si falta un artifact o hay versiones contradictorias, se explica qué revisión no puede completarse.

## Hallazgo

Artifact y versión / ubicación / discrepancia / impacto / cambio propuesto / decisión / evidencia posterior.

Las revisiones de documentos no prueban una aplicación funcionando ni sustituyen pruebas con usuarios reales.
