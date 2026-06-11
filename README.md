# 🏠 Análisis de Arriendos en Santiago, Chile — Mayo 2025

> Proyecto end-to-end de análisis de datos del mercado de arriendos en la Región Metropolitana, usando datos reales de Yapo.cl (mayo 2025).

**Autor:** Emilio Rubina Salinas  
**LinkedIn:** [linkedin.com/in/emilio-rubina-salinas-b1436a253](https://www.linkedin.com/in/emilio-rubina-salinas-b1436a253/)

---

## 🎯 Objetivo

Identificar patrones del mercado de arriendos en Santiago para responder:
- ¿Cuánto cuesta arrendar en cada comuna?
- ¿Cuál es el precio real por m²?
- ¿Qué tipo de departamento domina el mercado?
- ¿Cómo varía el precio según el número de dormitorios?

---

## 📁 Estructura del proyecto

```
├── data/
│   ├── apartments_rm_raw_yapo_may2025.csv   # Dataset original sin modificar
│   └── apartments_santiago_clean.csv        # Dataset limpio (listo para Power BI)
├── analisis_arriendos_santiago.ipynb        # Notebook con limpieza y análisis
├── outputs/
│   ├── 01_distribucion_precios.png
│   ├── 02_precio_por_comuna.png
│   ├── 03_precio_por_m2.png
│   ├── 04_precio_vs_area.png
│   ├── 05_dormitorios_tamano.png
│   └── 06_precio_por_dormitorios.png
└── README.md
```

---

## 🔍 Metodología

1. **Fuente:** Dataset de Yapo.cl con 12.690 publicaciones de departamentos en la RM
2. **Limpieza con Python (pandas):**
   - Extracción de precio desde texto sucio (`$260.000-4%Oportunidad` → `260000`)
   - Conversión de precios en UF a CLP (1 UF ≈ $37.000, mayo 2025)
   - Extracción numérica de área (`65m2` → `65`)
   - Separación de comunas pegadas (`LasCondes` → `Las Condes`)
   - Filtrado de outliers (precios < $50.000 o > $5.000.000 CLP)
   - Clasificación por tamaño y cálculo de precio por m²
3. **Análisis exploratorio** con matplotlib

---

## 📈 Principales hallazgos

| Indicador | Valor |
|---|---|
| Precio mediano arriendo | **$300.000 CLP** |
| Precio promedio (con outliers lujo) | **$454.000 CLP** |
| Precio mediano por m² | **~$7.000 CLP/m²** |
| Tipo de depto más común | **1-2 dormitorios (80%)** |
| Comuna con más publicaciones | **Santiago centro (32%)** |
| Publicaciones con precio explícito | **Solo 35%** |

---

## 🛠️ Stack técnico

- **Python:** pandas, matplotlib, numpy, re
- **Jupyter Notebook**
- **Power BI Desktop** (dashboard complementario)

---

## 🚀 Cómo ejecutar

```bash
# Clonar repositorio
git clone https://github.com/tu-usuario/arriendos-santiago-2025.git
cd arriendos-santiago-2025

# Instalar dependencias
pip install pandas matplotlib numpy jupyter openpyxl

# Ejecutar notebook
jupyter notebook analisis_arriendos_santiago.ipynb
```

---

## 📊 Dashboard Power BI

Screenshots del dashboard interactivo:

*(agregar capturas aquí después de construir el dashboard)*

---

*Datos obtenidos de fuente pública con fines académicos y de portafolio profesional.*
