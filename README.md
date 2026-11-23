# Bulbificación in vitro de *Zephyranthes advena*

Repositorio de apoyo para mi tesis del Magíster en Ciencias Agropecuarias (Facultad de Ciencias Agronómicas, Universidad de Chile). Reúne en un solo lugar el diseño experimental, los protocolos de preparación de medios y una calculadora en Python (Google Colab) que automatiza las cuentas de cada tratamiento.

**Autor:** Nicolás Meza Serrano
**Trabajo práctico:** curso de Data Science en Recursos Naturales

---

## La idea

En laboratorio, preparar los medios de cultivo de muchos tratamientos a mano es lento y propenso a errores: cada medio lleva distintas cantidades de sacarosa y reguladores del crecimiento, y hay que repetir las mismas cuentas de dilución una y otra vez.

Este repositorio propone **calcular los medios con un cuaderno reproducible** en vez de hacerlo en una calculadora o a mano. A partir de unos pocos parámetros (volumen, concentraciones de stock y diseño de tratamientos), el cuaderno entrega una tabla con todo lo que hay que pesar y pipetear para cada tratamiento.

## Contexto de la investigación

Mi tesis estudia el efecto de la **sacarosa** y de los reguladores del crecimiento **BAP** (citoquinina) y **ANA** (auxina) sobre la **bulbificación in vitro** de dos poblaciones de *Zephyranthes advena*: Parque Mahuida y Playa Las Cujas.

- **Diseño factorial 3 × 5:** 3 niveles de sacarosa (30, 60 y 90 g/L) × 5 combinaciones de BAP/ANA = 15 tratamientos (T0 a T14).
- **10 repeticiones por tratamiento:** 150 unidades experimentales por población.
- **Medio base:** MS 4,43 g/L, carbón activado 0,6 g/L, agar 8 g/L, pH 5,7, autoclave a 121 °C por 20 min.

## Qué hay en este repositorio

```
├── README.md                    <- esta página
├── notebooks/
│   └── calculadora_medios.ipynb <- cuaderno de Colab con la calculadora
├── datos/
│   └── tratamientos.csv         <- tabla de cantidades generada por el cuaderno
├── protocolos/
│   └── preparacion_medio.md     <- paso a paso de preparación en laboratorio
└── referencias/
    └── README.md                <- bibliografía y material de apoyo
```

## Cómo usar la calculadora

1. Abre `notebooks/calculadora_medios.ipynb` en [Google Colab](https://colab.research.google.com/) (también puedes abrirlo desde GitHub con el botón "Open in Colab").
2. Revisa la celda de **parámetros**: volumen final por tratamiento, concentraciones de stock y las combinaciones de BAP/ANA.
3. Ejecuta todas las celdas (*Entorno de ejecución → Ejecutar todo*).
4. Obtendrás la tabla de cantidades por tratamiento, un gráfico del diseño y el archivo `tratamientos.csv`.

> **Importante:** las concentraciones de BAP y ANA del cuaderno son valores de ejemplo. Reemplázalos por los de tu diseño experimental en la celda de parámetros antes de usar los resultados en el laboratorio.

## Cómo se calcula

- **Stocks:** BAP 0,01 M (10 mM) y ANA 0,005 M (5 mM).
- **Volumen de stock a agregar** con la fórmula de dilución C₁ × V₁ = C₂ × V₂, donde C₁ es la concentración del stock, C₂ la concentración final en el medio y V₂ el volumen final.
- **Sacarosa, MS, carbón activado y agar:** se calculan por regla de tres desde su concentración por litro.
- **Volumen final de 200 mL por tratamiento:** así los volúmenes de stock quedan sobre los 20 µL, que es lo que mi micropipeta mide con precisión. El cuaderno marca los casos que quedan bajo ese límite.

## Flujo de trabajo con ramas

El repositorio se desarrolló usando ramas:

| Rama | Contenido |
|------|-----------|
| `main` | Versión estable: README y estructura del proyecto |
| `calculadora-medios` | Cuaderno de Colab y tabla de tratamientos |
| `documentacion` | Protocolos de laboratorio y referencias |

Cada rama se integró a `main` mediante un *Pull Request*.

## Referencias

Ver [`referencias/README.md`](referencias/README.md).
