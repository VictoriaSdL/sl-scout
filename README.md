# SL Scout

Cuadro de mando para el análisis y *screening* de sociedades limitadas españolas, desarrollado para la asignatura *Desarrollo de Aplicaciones para la Visualización de Datos* (ICAI, curso 2026-2027).

## Descripción

SL Scout permite buscar una sociedad limitada por nombre o NIF y ver de un vistazo su evolución financiera: ventas, margen bruto y EBITDA (cuenta de resultados) y capital circulante, flujo de caja libre y capex (balance). Además:

- **Proyecta** ventas y EBITDA a 1–2 años a partir del CAGR histórico.
- Calcula un **score de atractivo como target (0–100)** que combina un modelo de riesgo financiero (regresión logística) con la posición de la empresa frente a su sector.
- Incluye un botón **Contactar** que busca el email de administradores y accionistas en Apollo, Hunter y OpenWeb Ninja (cascada con rotación según créditos disponibles) y abre un borrador de email.

Los datos proceden de una exportación de SABI (licencia académica). Por motivos de licencia, los datos no se incluyen en este repositorio.

## Objetivos

1. Reducir el tiempo de la primera evaluación de una empresa objetivo para analistas de private equity y M&A.
2. Priorizar empresas de un sector mediante un score interpretable.
3. Facilitar el contacto con los decisores de cada empresa.
4. Desplegar la aplicación en una URL accesible (Render).

## Estructura

```
sl-scout/
├── data/        # Datos de SABI (no se suben al repositorio)
├── notebooks/   # Exploración y prototipos
├── src/         # Limpieza, variables derivadas, modelos y conectores de email
├── models/      # Modelos entrenados
├── app/         # Aplicación Dash
└── requirements.txt
```

## Plan de trabajo

| Fase | Fechas | Entregable |
|---|---|---|
| 1. Propuesta y extracción | 29 sep – 11 oct | Propuesta, repositorio, exportación de SABI |
| 2. Pipeline y análisis exploratorio | 12 – 25 oct | Datos limpios en Parquet, variables derivadas, EDA |
| 3. Modelos | 26 oct – 8 nov | Proyección CAGR y score validados |
| 4. App en Dash | 2 – 15 nov | Buscador, ficha, gráficos, score y ranking |
| 5. Contacto y despliegue | 16 – 22 nov | Cascada Apollo / Hunter / OpenWeb Ninja, caché, despliegue en Render |
| 6. Mejora y presentación | 23 – 30 nov | Ajustes de diseño, pruebas y presentación |

## Tecnologías

Python · pandas · scikit-learn · Plotly · Dash · Render · GitHub

## Autora

Victoria Sánchez de León González
