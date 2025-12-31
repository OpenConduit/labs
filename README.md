# Open Data Engineering Academy Labs

A Dockerized JupyterLab environment with JupySQL, Postgres 15, and DuckDB pre-wired.

## 🚀 Quick Start
1. Prerequisites
   - Docker Desktop (For the Lab)
   - Python 3.10+ (For the Textbook)

2. The Lab (Write Code)
- This spins up your "Workstation." It includes a Postgres database (OLTP) and a Jupyter environment with DuckDB (OLAP).

3. Start the Engine:
```bash
docker-compose up -d
```

4. Enter the Lab:
- Open your browser to: http://localhost:8888
- Password: dataengineer

5. Start Coding:
- Open notebooks/sql_and_internals/00_Start_Here.ipynb.
- Run the cells to generate the 1-Million Row datasets needed for the advanced modules.

## 🛠️ Troubleshooting
"Port 5432 is already in use" You likely have a local Postgres instance running on your laptop. Stop it, or modify docker-compose.yml to map to a different port (e.g., "5433:5432").

"Magic %sql not found" Make sure you ran the initialization cell at the top of the notebook. It loads the jupysql extension.

"MkDocs command not found" Ensure your virtual environment is active. Your terminal prompt should start with (.venv).