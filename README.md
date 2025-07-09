**🚀 CSV to MySQL Pipeline with Airflow and Docker**
This project implements a scalable data pipeline that loads one or more CSV files into a MySQL database
using Apache Airflow. It uses csvsql to generate table schemas automatically from CSV headers, supports
parallel processing, and is fully containerized with Docker.

**✨ Features**
✅ Accepts multiple CSV files

✅ Auto-generates MySQL schema with csvsql

✅ Loads data into MySQL

✅ Parallel processing using Airflow

✅ Fully containerized with Docker and Docker Compose

**🛠 Technologies Used**
Apache Airflow – Workflow orchestration

MySQL – Relational database

csvsql (from csvkit) – Schema generation

Docker – Containerized runtime environment

**⚙️ Configuration**
The only required configuration is setting the CSV delimiter in the DAG file.

In dags/load_to_database.py, set:
delimiter = ','
You can change this to ';', '\t', or any other delimiter that matches your CSV files.

**📂 Project Structure**
.
├── airflow/                      # Airflow environment setup
│   ├── Dockerfile                # Custom Airflow Docker image
│   └── airflow.cfg              # Airflow configuration
│
├── dags/                         # DAG files
│   └── load_to_database.py      # Main DAG that processes CSV files
│
├── data/                         # Folder to place your CSV files
│   └── your_files.csv
│
├── docker-compose.yml           
└── README.md

**▶️ Usage**
Add your CSV files
Place one or more .csv files inside the data/ folder.

Set your delimiter
Open dags/load_to_database.py and adjust the delimiter variable if needed.

Build and run the pipeline
In the root directory, run:

docker-compose up --build

Access Airflow UI
Navigate to: http://localhost:8082

Trigger the DAG
Run the load_to_database DAG to start processing files.


**👤 Made By**
Abdelghafour AIT ADDI
aitaddiabdelghafour@gmail.com
