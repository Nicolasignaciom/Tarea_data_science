# Protocolo de preparación del medio de bulbificación

Medio base para los 15 tratamientos (T0 a T14), por 200 mL de medio.

## Composición base (por litro)

| Componente | Cantidad |
|-----------|----------|
| Sales MS (mezcla basal) | 4,43 g/L |
| Carbón activado | 0,6 g/L |
| Agar | 8 g/L |
| Sacarosa | 30, 60 o 90 g/L según tratamiento |
| BAP | según tratamiento (stock 0,01 M) |
| ANA | según tratamiento (stock 0,005 M) |
| pH | 5,7 |

Las cantidades exactas por tratamiento están en [`datos/tratamientos.csv`](../datos/tratamientos.csv), generadas por la calculadora.

## Preparación de los stocks

- **BAP 0,01 M (10 mM):** pesar 0,2253 g de BAP y llevar a 100 mL (peso molecular 225,25 g/mol).
- **ANA 0,005 M (5 mM):** pesar 0,0931 g de ANA y llevar a 100 mL (peso molecular 186,21 g/mol).
- Verificar el solvente de cada regulador según el proveedor antes de disolver.

## Procedimiento

1. Disolver en agua destilada las sales MS, la sacarosa y el carbón activado.
2. Agregar el BAP del stock según el tratamiento.
3. Ajustar el pH a 5,7.
4. Agregar el agar (8 g/L) y completar al volumen final.
5. Autoclavar a 121 °C por 20 minutos.
6. **ANA (termolábil):** se agrega después del autoclave, filtro-esterilizado, dentro de la cámara de flujo laminar.
7. Dispensar en los frascos y dejar solidificar.

## Optimización por lotes

Para reducir pasos y errores, se puede preparar un lote de 400 mL de medio con BAP (sin ANA), autoclavarlo y separarlo en 2 alícuotas de 200 mL dentro de la cámara. A cada alícuota se le agrega por separado su dosis de ANA.

## Notas

- Volumen final de 200 mL por tratamiento: con 100 mL varios volúmenes de stock quedarían bajo 20 µL, límite de precisión de la micropipeta usada.
- Registrar lote de reactivos, fecha de preparación y responsable en la bitácora del laboratorio.
