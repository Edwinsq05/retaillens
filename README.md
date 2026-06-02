# RetailLens — Dashboard de Inteligencia Comercial

Aplicación de **visualización de datos** (Avance 3) sobre el dataset
`retail_store_sales` (11.971 transacciones, 2022–2025). Autores: Edwin Quiñonez 


```
app.py            ← toda la app + el dataset incrustado dentro
requirements.txt  ← dependencias
```

El dataset va comprimido **dentro de `app.py`**, así no hay que subir CSV ni carpetas
y no aparece el error de "archivo no encontrado".

## Vistas

1. **Vista General** — ventas, ticket, evolución mensual, canal y método de pago.
2. **Efectividad de Descuentos** — el gancho: el descuento no genera ventas adicionales,
   con la explicación del programa y el análisis de causas (penetración, efecto por
   categoría y decisiones sugeridas).
3. **Categorías** — qué categorías impulsan los ingresos.
4. **Clientes** — clientes más valiosos y concentración de ventas.
5. **Calidad de Datos** — completitud por campo y la brecha del registro de descuento.

> Sin filtro por año: se muestran estadísticas generales. Los filtros de categoría y
> canal son opcionales.

## Correr localmente

```bash
pip install -r requirements.txt
streamlit run app.py
```

## Desplegar en Streamlit Community Cloud

1. Sube `app.py` y `requirements.txt` a la **raíz** de un repo **público** de GitHub.
2. En share.streamlit.io → **Create app** → elige el repo, rama `main`, **Main file path:** `app.py`.
3. **Deploy**.
