# financial-analytics-2025
# 💼 Financial Analytics — Empresa de Servicios & Distribución 2025

**Análisis financiero integral: P&L, Cashflow, IVA, Deuda y Rentabilidad por cliente**

[![Portfolio](https://img.shields.io/badge/Portfolio-AIM%20Analytics-021859?style=flat-square)](https://gondss7.github.io/ecommerce-analytics/)
[![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org)
[![Excel](https://img.shields.io/badge/Excel-Advanced-217346?style=flat-square&logo=microsoftexcel&logoColor=white)](https://microsoft.com/excel)
[![Chart.js](https://img.shields.io/badge/Chart.js-4.4-FF6384?style=flat-square)](https://chartjs.org)

---

## 📋 Descripción del proyecto

Sistema de análisis financiero y contable end-to-end para una empresa de servicios y distribución con **$284.6M en ingresos netos anuales**, operaciones en múltiples líneas de negocio y cartera activa de 52 clientes.

El proyecto cubre el ciclo financiero completo: desde el estado de resultados detallado y la posición de IVA mensual, hasta el análisis de concentración de cartera, riesgo de cobranzas y proyección de resultados para el ejercicio siguiente.

> 💡 **Insight clave del proyecto:** Los 3 principales clientes concentran el 58% del ingreso total. El DSO (días de cobro) de 47 días supera en un 34% el benchmark del sector, generando una necesidad de capital de trabajo evitable de aproximadamente $12M.

---

## 🏗️ Estructura del análisis

El proyecto trabaja sobre un modelo de datos integrado con las siguientes fuentes:

| Módulo | Descripción | Granularidad |
|--------|-------------|--------------|
| `estado_de_resultados` | P&L completo con apertura por línea de negocio | Mensual |
| `cashflow` | Flujo operativo, de inversión y financiero | Mensual |
| `posicion_iva` | Débito fiscal, crédito fiscal y posición neta | Mensual |
| `cartera_clientes` | Ingresos, márgenes y DSO por cliente | Por cliente |
| `deuda_financiera` | Detalle de pasivos financieros y vencimientos | Por instrumento |
| `kpis_financieros` | Ratios de liquidez, solvencia y rentabilidad | Mensual |
| `proyeccion_2026` | Escenarios base, optimista y conservador | Mensual |

---

## 📊 Dashboard

index.html
### Resumen Ejecutivo
Vista consolidada con los 6 KPIs más relevantes del ejercicio, waterfall de composición del resultado anual y proyección comparativa 2025 vs 2026.

**KPIs del ejercicio 2025:**
- Ingresos netos: **$284.6M** (+18.4% vs 2024)
- Margen bruto: **62.3%** (+2.1 pp interanual)
- EBITDA: **$48.2M** (16.9% del ingreso)
- Resultado neto: **$29.8M** (10.5% de margen neto)
- DSO: **47 días** ⚠️ — supera benchmark
- Deuda financiera neta: **$31.4M**

### P&L Detallado
Estado de resultados con apertura por línea de negocio, margen bruto por segmento y análisis de la estructura de costos operativos.

**Líneas de negocio por margen bruto:**
| Línea | Margen bruto |
|-------|-------------|
| Consultoría | 78% |
| Proyectos | 71% |
| Servicios recurrentes | 64% |
| Soporte técnico | 58% |
| Distribución | 41% |

### Cashflow
Desglose mensual del flujo operativo, de inversión y financiero. Análisis de la generación y consumo de caja con alerta de meses de flujo neto negativo.

### IVA & Fiscal
Posición de IVA mensual (débito vs crédito fiscal) con proyección de pagos y análisis de la carga fiscal efectiva.

### Clientes & Cartera
Concentración de ingresos por cliente, análisis de DSO individual y ranking de rentabilidad por cuenta.

---

## 🔍 Análisis destacados

### 1. Concentración de cartera
El análisis de Pareto sobre la cartera de clientes revela que **3 clientes generan el 58% del ingreso** ($66.6M sobre $284.6M). El modelo cuantifica el impacto de escenarios de pérdida o reducción de cualquiera de estos clientes sobre el resultado del ejercicio.

### 2. Gestión del capital de trabajo
Con un DSO de 47 días frente a un DPO de 38 días, la empresa financia a sus clientes por 9 días netos. El modelo calcula el costo de oportunidad de este descalce y proyecta el ahorro potencial si el DSO se reduce al benchmark del sector (35 días): **~$12M de capital de trabajo liberado**.

### 3. Estructura de costos y apalancamiento operativo
El ratio de apalancamiento operativo de 1.62× significa que un incremento del 10% en los ingresos genera un incremento del 16.2% en el resultado operativo. El análisis de punto de equilibrio muestra el nivel de ingresos mínimo para cubrir la estructura de costos fijos.

### 4. Proyección 2026
El modelo de proyección incorpora:
- Crecimiento orgánico de cartera existente (+8% base)
- Impacto de la reducción del DSO sobre el capital de trabajo
- Escenario de pérdida del cliente más concentrado (-28.4M ingreso)
- Sensibilidad del margen neto ante variaciones en costos financieros

---

## 💡 Decisiones de negocio que habilita este sistema

| Pregunta | Respuesta que da el dashboard |
|----------|-------------------------------|
| ¿Cuánto genero realmente después de todos los costos? | P&L con apertura completa hasta resultado neto |
| ¿Qué línea de negocio es más rentable? | Margen bruto y contribución por segmento |
| ¿Cuánto IVA voy a pagar este mes? | Posición neta en tiempo real |
| ¿Cuántos días tardo en cobrar? ¿Es un problema? | DSO individual por cliente vs benchmark |
| ¿Qué pasa si pierdo mi cliente más grande? | Simulación de escenarios en proyección 2026 |
| ¿Tengo liquidez para crecer? | Ratios de solvencia y capital de trabajo disponible |

---

## 📈 Indicadores financieros clave

| Ratio | Valor | Benchmark | Estado |
|-------|-------|-----------|--------|
| Liquidez corriente | 1.84× | >1.5× | ✅ |
| Deuda / EBITDA | 0.65× | <2× | ✅ |
| DSO (días cobro) | 47 días | <35 días | ⚠️ |
| DPO (días pago) | 38 días | 30-45 días | ✅ |
| ROE | 22.4% | >15% | ✅ |
| Margen EBITDA | 16.9% | >12% | ✅ |

---

## 🛠️ Stack técnico

```
Python 3.11
  ├── pandas          # ETL, modelado financiero, proyecciones
  ├── numpy           # Cálculos de ratios y simulaciones
  └── openpyxl        # Generación del modelo en Excel

Excel Avanzado
  ├── Tablas dinámicas y Power Query
  ├── Modelos de proyección con escenarios (Scenario Manager)
  ├── BUSCARX, SI.CONJUNTO, SUMAR.SI.CONJUNTO
  └── Formato condicional para semáforos de KPIs

JavaScript / HTML
  ├── Chart.js 4.4.1  # Waterfall, barras, líneas, donut
  └── CSS Grid + DM Sans / DM Mono
```

---

## 📁 Archivos del proyecto

```
financial-analytics-2025/
├── dashboard_financiero_servicios.html   # Dashboard interactivo
└── README.md
```

---

## 👤 Autor

**Gonzalo Dalmasso Müller** — Business & Data Analyst

🌐 [Portfolio](https://gondss7.github.io/ecommerce-analytics/) &nbsp;|&nbsp;
💼 [LinkedIn](https://linkedin.com/in/gonzalo-dalmasso-486094206) &nbsp;|&nbsp;
🐙 [GitHub](https://github.com/GonDss7) &nbsp;|&nbsp;
📧 gonzalodalmasso7@hotmail.com

---

*Proyecto de portfolio — datos generados con fines demostrativos · AIM Analytics 2025*
