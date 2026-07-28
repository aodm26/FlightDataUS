
---

# FlightDataUS: Big Data Flight Analytics Pipeline

**FlightDataUS** is a scalable big data processing and analytics pipeline designed to ingest, process, and analyze large-scale US flight dataset records using **Apache PySpark** and **Apache Parquet**.

The repository provides end-to-end workflows for transformation, aggregate reporting, and performance benchmarking across large-scale transportation datasets.

---

## Key Features

* **Distributed Processing:** Uses PySpark for distributed data ingestion, filtering, and aggregation on multi-gigabyte flight records.
* **Columnar Storage Optimization:** Converts raw tabular data (CSV) into optimized **Apache Parquet** format for accelerated queries, reduced disk footprint, and efficient memory usage.
* **Performance Analytics:** Extracts operational KPIs, including flight delay distributions, carrier reliability metrics, route density, and seasonal volume trends.
* **Scalable Architecture:** Designed for modular execution across local development clusters (PySpark standalone) or distributed cloud environments (AWS EMR, Databricks).

---

## Tech Stack & Tooling

| Component | Technology |
| --- | --- |
| **Data Engine** | Apache PySpark / Python |
| **Storage Format** | Apache Parquet / Compressed CSV |
| **Data Manipulation** | PySpark SQL, DataFrames |
| **Environment** | Ubuntu / Linux, Jupyter Notebook / PySpark Shell |

---

## Repository Structure

```text
FlightDataUS/
├── data/              # Raw and converted Parquet data directories (gitignored)
├── notebooks/         # Exploratory PySpark data analysis notebooks
├── scripts/           # Core ETL and transformation scripts
│   ├── ingest.py      # Raw CSV to Parquet conversion pipeline
│   └── analytics.py   # Aggregation & metric generation logic
├── requirements.txt   # Python dependencies
└── README.md          # Project documentation

```

---

## Getting Started

### Prerequisites

* **Python 3.9+**
* **Java Development Kit (JDK 8 or 11)** *(required for PySpark execution)*

### Installation

1. **Clone the repository:**
```bash
git clone https://github.com/aodm26/FlightDataUS.git
cd FlightDataUS

```


2. **Set up a virtual environment:**
```bash
python3 -m venv venv
source venv/bin/activate

```


3. **Install dependencies:**
```bash
pip install -r requirements.txt

```



### Execution Workflow

1. **Ingest & Convert to Parquet:**
```bash
python scripts/ingest.py --input data/raw_flights.csv --output data/parquet/

```


2. **Run Analytics Queries:**
```bash
python scripts/analytics.py --data data/parquet/

```



---
