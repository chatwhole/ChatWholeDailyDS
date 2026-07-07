---
title: "Apache Airflow Course — 30 Free Lessons with Code Examples | ChatWhole"
description: "Master Apache Airflow with 30 free lessons. Learn DAG design patterns, operators, XCom, scheduling, executors, sensors, branching, TaskFlow API, error handling, testing, Kubernetes executor, CI/CD, and cloud integrations with hands-on Python code examples."
keywords: "Apache Airflow course, learn Airflow, Airflow tutorial, Airflow DAG, Airflow operators, Airflow XCom, Airflow scheduling, Airflow executors, Airflow sensors, Airflow branching, Airflow TaskFlow API, Airflow testing, Airflow Kubernetes, Airflow CI/CD, data pipeline orchestration"
canonical: "https://chatwhole.com/learn/airflow/"
og_title: "Apache Airflow Course — 30 Free Lessons with Code Examples"
og_description: "Complete Apache Airflow course with 30 free lessons. Learn DAGs, operators, XCom, scheduling, executors, and build production data pipelines."
og_url: "https://chatwhole.com/learn/airflow/"
og_type: "article"
---

# Apache Airflow Course — Complete 30-Lesson Curriculum with Code Examples

Apache Airflow is the industry-standard open-source workflow orchestration platform for programmatically authoring, scheduling, and monitoring data pipelines. This comprehensive 30-lesson course covers everything from architecture fundamentals to advanced patterns like deferrable operators and cloud integrations.

**Source:** [ChatWhole Learn — Airflow](https://chatwhole.com/learn/airflow/)

---

## Table of Contents

### Module 1: Airflow Foundations (01-10)

Master the core Airflow concepts: architecture, DAGs, operators, and scheduling.

| # | Topic | Link |
|---|-------|------|
| 001 | [Airflow Architecture](https://chatwhole.com/learn/airflow/01-airflow-architecture/) | Scheduler, web server, metadata DB, executors, workers |
| 002 | [DAG Design Patterns](https://chatwhole.com/learn/airflow/02-dag-design-patterns/) | Linear, branching, fan-out/fan-in, TaskGroup patterns |
| 003 | [Operators & Hooks](https://chatwhole.com/learn/airflow/03-operators-hooks/) | Built-in operators, custom operators, hooks |
| 004 | [XCom Communications](https://chatwhole.com/learn/airflow/04-xcom-communications/) | Task communication, XCom backends, data passing |
| 005 | [Scheduling & Triggers](https://chatwhole.com/learn/airflow/05-scheduling-triggers/) | Cron expressions, triggers, timetables |
| 006 | [Executors Comparison](https://chatwhole.com/learn/airflow/06-executors-comparison/) | Sequential, Local, Celery, Kubernetes |
| 007 | [Sensors & Operators](https://chatwhole.com/learn/airflow/07-sensors-operators/) | Sensors, poke modes, reschedule mode |
| 008 | [Branching Logic](https://chatwhole.com/learn/airflow/08-branching-logic/) | BranchPythonOperator, ShortCircuitOperator |
| 009 | [TaskFlow API](https://chatwhole.com/learn/airflow/09-airflow-taskflow-api/) | Decorator-based DAGs, @task, @dag |
| 010 | [Connection Management](https://chatwhole.com/learn/airflow/10-airflow-connection-management/) | Connections, secrets backends, providers |

### Module 2: Production Airflow (11-20)

Build production-grade pipelines with error handling, testing, and monitoring.

| # | Topic | Link |
|---|-------|------|
| 011 | [Variable Management](https://chatwhole.com/learn/airflow/11-airflow-variable-management/) | Variables, environment variables, config |
| 012 | [Error Handling](https://chatwhole.com/learn/airflow/12-airflow-error-handling/) | Retries, callbacks, dead letter queues |
| 013 | [Testing DAGs](https://chatwhole.com/learn/airflow/13-airflow-testing-dags/) | Unit tests, integration tests, DAG validation |
| 014 | [Security Best Practices](https://chatwhole.com/learn/airflow/14-airflow-security-best-practices/) | RBAC, encryption, secrets management |
| 015 | [Performance Tuning](https://chatwhole.com/learn/airflow/15-airflow-performance-tuning/) | DAG optimization, parallelism, caching |
| 016 | [Kubernetes Executor](https://chatwhole.com/learn/airflow/16-airflow-kubernetes-executor/) | Pod isolation, dynamic scaling, K8s config |
| 017 | [CI/CD Pipelines](https://chatwhole.com/learn/airflow/17-airflow-cicd-pipelines/) | Automated testing and deployment |
| 018 | [Monitoring & Alerting](https://chatwhole.com/learn/airflow/18-airflow-monitoring-observability/) | Metrics, dashboards, external alerting |
| 019 | [Multi-Tenancy](https://chatwhole.com/learn/airflow/19-airflow-multi-tenancy/) | Isolating workloads across teams |
| 020 | [Data Pipelines](https://chatwhole.com/learn/airflow/20-airflow-data-pipelines/) | End-to-end ETL/ELT pipeline patterns |

### Module 3: Advanced Airflow (21-30)

Master advanced patterns, custom operators, and cloud integrations.

| # | Topic | Link |
|---|-------|------|
| 021 | [Custom Operators](https://chatwhole.com/learn/airflow/21-airflow-custom-operator/) | Building reusable operator components |
| 022 | [Deferrable Operators](https://chatwhole.com/learn/airflow/22-airflow-deferrable-operators/) | Async execution, triggerer, efficient waiting |
| 023 | [Multiple DAGs](https://chatwhole.com/learn/airflow/23-airflow-multiple-dags/) | Cross-DAG dependencies, ExternalTaskSensor |
| 024 | [Dynamic DAGs](https://chatwhole.com/learn/airflow/24-airflow-dynamic-dags/) | Config-driven generation, parameterized DAGs |
| 025 | [Databricks Integration](https://chatwhole.com/learn/airflow/25-airflow-databricks-integration/) | DatabricksSubmitRunOperator, notebooks |
| 026 | [BigQuery Integration](https://chatwhole.com/learn/airflow/26-airflow-bigquery-integration/) | BigQuery operators, data transfers |
| 027 | [Snowflake Integration](https://chatwhole.com/learn/airflow/27-airflow-snowflake-integration/) | Snowflake operators, Snowpipe, tasks |
| 028 | [Spark Integration](https://chatwhole.com/learn/airflow/28-airflow-spark-integration/) | SparkSubmitOperator, EMR, Dataproc |
| 029 | [MWAA & Cloud](https://chatwhole.com/learn/airflow/29-airflow-mwaa-cloud/) | Managed Airflow on AWS, GCP, Azure |
| 030 | [Future Trends](https://chatwhole.com/learn/airflow/30-airflow-future-trends/) | Airflow 3.0, TaskFlow improvements |

---

## Key Concepts Summary

### Airflow Architecture Components

| Component | Description | Scaling |
|-----------|-------------|---------|
| Web Server | Flask-based UI and API | Horizontal with load balancer |
| Scheduler | Orchestrates DAG runs and tasks | Single instance recommended |
| Metadata Database | Central state store (PostgreSQL) | Read replicas for queries |
| Executor | Task execution strategy | Depends on executor type |
| Workers | Compute nodes executing tasks | Horizontal scaling |
| Triggerer | Handles async sensors and deferrable operators | Horizontal scaling |

### Executor Comparison

| Executor | Scaling | Use Case | Complexity |
|----------|---------|----------|------------|
| SequentialExecutor | Single process | Development/testing | Low |
| LocalExecutor | Single machine | Small production | Low |
| CeleryExecutor | Distributed workers | Medium-large production | Medium |
| KubernetesExecutor | Dynamic pods | Cloud-native, bursty workloads | High |

### DAG Design Patterns

| Pattern | Description | Use Case |
|---------|-------------|----------|
| Linear | A → B → C | Simple sequential ETL |
| Branching | IF/ELSE conditional paths | Decision workflows |
| Fan-Out/Fan-In | A → [B,C,D] → E | Parallel processing + aggregation |
| TaskGroup | Logical grouping | Complex pipelines |
| Dynamic DAGs | Config-driven generation | Multi-tenant environments |
| Cross-DAG | ExternalTaskSensor | Inter-DAG dependencies |

### Operator Types

| Operator | Use Case | Example |
|----------|----------|---------|
| PythonOperator | Run Python functions | Data transformations |
| BashOperator | Execute shell commands | System operations |
| PostgresOperator | Run SQL queries | Database operations |
| S3KeySensor | Wait for S3 object | File availability |
| SparkSubmitOperator | Submit Spark jobs | Big data processing |
| BranchPythonOperator | Conditional branching | Decision logic |

---

## Code Examples

### Basic DAG with Dependencies

```python
from datetime import datetime, timedelta
from airflow import DAG
from airflow.operators.python import PythonOperator
from airflow.operators.bash import BashOperator

default_args = {
    'owner': 'data-engineering',
    'retries': 3,
    'retry_delay': timedelta(minutes=5),
    'email_on_failure': True,
    'email': ['alerts@company.com'],
}

def extract_data(**context):
    """Extract data from source system."""
    import pandas as pd
    from sqlalchemy import create_engine
    
    engine = create_engine("postgresql://user:pass@source/db")
    df = pd.read_sql("SELECT * FROM orders", engine)
    
    # Push row count to XCom
    context['ti'].xcom_push(key='row_count', value=len(df))
    
    # Save to staging
    df.to_parquet(f"/tmp/extract_{context['ds']}.parquet")
    return f"Extracted {len(df)} rows"

def transform_data(**context):
    """Transform extracted data."""
    import pandas as pd
    
    df = pd.read_parquet(f"/tmp/extract_{context['ds']}.parquet")
    
    # Transformations
    df = df.drop_duplicates(subset=['order_id'])
    df = df[df['amount'] > 0]
    df['processed_at'] = datetime.utcnow()
    
    df.to_parquet(f"/tmp/transform_{context['ds']}.parquet")
    return f"Transformed to {len(df)} rows"

def load_data(**context):
    """Load transformed data to warehouse."""
    import pandas as pd
    from sqlalchemy import create_engine
    
    df = pd.read_parquet(f"/tmp/transform_{context['ds']}.parquet")
    engine = create_engine("postgresql://user:pass@warehouse/db")
    
    df.to_sql('orders_fact', engine, if_exists='append', index=False)
    return f"Loaded {len(df)} rows"

with DAG(
    dag_id='daily_order_etl',
    default_args=default_args,
    description='Daily order ETL pipeline',
    schedule_interval='@daily',
    start_date=datetime(2024, 1, 1),
    catchup=False,
    tags=['etl', 'orders'],
) as dag:
    
    extract = PythonOperator(
        task_id='extract',
        python_callable=extract_data,
    )
    
    transform = PythonOperator(
        task_id='transform',
        python_callable=transform_data,
    )
    
    load = PythonOperator(
        task_id='load',
        python_callable=load_data,
    )
    
    notify = BashOperator(
        task_id='notify',
        command='echo "Pipeline completed successfully"',
    )
    
    extract >> transform >> load >> notify
```

### TaskFlow API with @task Decorators

```python
from datetime import datetime, timedelta
from airflow.decorators import dag, task
from typing import List, Dict

@dag(
    schedule_interval='@daily',
    start_date=datetime(2024, 1, 1),
    catchup=False,
    tags=['taskflow', 'etl'],
)
def taskflow_etl():
    
    @task
    def extract() -> List[Dict]:
        """Extract data from source."""
        return [
            {'id': 1, 'amount': 100.00, 'status': 'completed'},
            {'id': 2, 'amount': 250.00, 'status': 'completed'},
            {'id': 3, 'amount': 50.00, 'status': 'pending'},
        ]
    
    @task
    def transform(raw_data: List[Dict]) -> List[Dict]:
        """Transform extracted data."""
        return [
            {**record, 'processed': True}
            for record in raw_data
            if record['status'] == 'completed'
        ]
    
    @task
    def load(transformed_data: List[Dict]) -> int:
        """Load data to target."""
        # Simulate loading
        return len(transformed_data)
    
    @task
    def notify(row_count: int):
        """Send notification."""
        print(f"Loaded {row_count} records")
    
    raw = extract()
    cleaned = transform(raw)
    count = load(cleaned)
    notify(count)

taskflow_etl_dag = taskflow_etl()
```

### Branching Logic

```python
from datetime import datetime, timedelta
from airflow import DAG
from airflow.operators.python import BranchPythonOperator, PythonOperator
from airflow.operators.empty import EmptyOperator

def check_data_quality(**context):
    """Determine processing path based on data quality."""
    import random
    
    quality_score = random.uniform(0.5, 1.0)
    context['ti'].xcom_push(key='quality_score', value=quality_score)
    
    if quality_score >= 0.8:
        return 'standard_processing'
    elif quality_score >= 0.6:
        return 'quality_review'
    else:
        return 'data_reject'

with DAG(
    dag_id='branching_example',
    default_args={'owner': 'airflow'},
    schedule_interval='@daily',
    start_date=datetime(2024, 1, 1),
    catchup=False,
) as dag:
    
    start = EmptyOperator(task_id='start')
    
    check_quality = BranchPythonOperator(
        task_id='check_quality',
        python_callable=check_data_quality,
    )
    
    standard = PythonOperator(
        task_id='standard_processing',
        python_callable=lambda: print("Standard processing"),
    )
    
    review = PythonOperator(
        task_id='quality_review',
        python_callable=lambda: print("Quality review required"),
    )
    
    reject = PythonOperator(
        task_id='data_reject',
        python_callable=lambda: print("Data rejected"),
    )
    
    end = EmptyOperator(task_id='end')
    
    start >> check_quality
    check_quality >> [standard, review, reject]
    [standard, review, reject] >> end
```

### XCom Data Passing

```python
from datetime import datetime, timedelta
from airflow import DAG
from airflow.operators.python import PythonOperator

def producer(**context):
    """Push data to XCom."""
    data = {
        'row_count': 1000,
        'file_path': 's3://bucket/data.parquet',
        'status': 'success',
    }
    context['ti'].xcom_push(key='metrics', value=data)
    return data

def consumer(**context):
    """Pull data from XCom."""
    metrics = context['ti'].xcom_pull(
        task_ids='producer',
        key='metrics',
    )
    print(f"Processing {metrics['row_count']} rows from {metrics['file_path']}")
    return metrics

with DAG(
    dag_id='xcom_example',
    default_args={'owner': 'airflow'},
    schedule_interval='@daily',
    start_date=datetime(2024, 1, 1),
    catchup=False,
) as dag:
    
    producer_task = PythonOperator(
        task_id='producer',
        python_callable=producer,
    )
    
    consumer_task = PythonOperator(
        task_id='consumer',
        python_callable=consumer,
    )
    
    producer_task >> consumer_task
```

### Custom Operator

```python
from airflow.models import BaseOperator
from airflow.utils.decorators import apply_defaults

class DataQualityCheckOperator(BaseOperator):
    """Custom operator for data quality validation."""
    
    @apply_defaults
    def __init__(
        self,
        table_name: str,
        checks: list,
        *args, **kwargs,
    ):
        super().__init__(*args, **kwargs)
        self.table_name = table_name
        self.checks = checks
    
    def execute(self, context):
        """Execute data quality checks."""
        from sqlalchemy import create_engine, text
        
        engine = create_engine("postgresql://user:pass@warehouse/db")
        
        results = {}
        with engine.connect() as conn:
            for check in self.checks:
                result = conn.execute(text(check['query']))
                results[check['name']] = result.fetchone()[0]
        
        # Log results
        for check_name, value in results.items():
            self.log.info(f"{check_name}: {value}")
        
        return results

# Usage in DAG
quality_check = DataQualityCheckOperator(
    task_id='quality_check',
    table_name='orders',
    checks=[
        {'name': 'row_count', 'query': 'SELECT COUNT(*) FROM orders'},
        {'name': 'null_check', 'query': 'SELECT COUNT(*) FROM orders WHERE id IS NULL'},
    ],
)
```

### Error Handling with Callbacks

```python
from datetime import datetime, timedelta
from airflow import DAG
from airflow.operators.python import PythonOperator

def alert_on_failure(context):
    """Send alert on task failure."""
    import requests
    
    slack_webhook = "https://hooks.slack.com/services/xxx"
    message = f"Task {context['task_instance'].task_id} failed"
    
    requests.post(slack_webhook, json={"text": message})

def notify_success(context):
    """Notify on success."""
    print(f"Task {context['task_instance'].task_id} succeeded")

def task_with_retry(**context):
    """Task that may fail transiently."""
    import random
    
    if random.random() < 0.3:
        raise ValueError("Transient error")
    return "Success"

with DAG(
    dag_id='error_handling_example',
    default_args={
        'owner': 'airflow',
        'retries': 3,
        'retry_delay': timedelta(minutes=5),
        'retry_exponential_backoff': True,
        'max_retry_delay': timedelta(minutes=30),
        'on_failure_callback': alert_on_failure,
        'on_success_callback': notify_success,
        'execution_timeout': timedelta(hours=1),
    },
    schedule_interval='@daily',
    start_date=datetime(2024, 1, 1),
    catchup=False,
) as dag:
    
    task = PythonOperator(
        task_id='task_with_retry',
        python_callable=task_with_retry,
    )
```

---

## Airflow Learning Path

1. **Start Here** → [Airflow Architecture](https://chatwhole.com/learn/airflow/01-airflow-architecture/)
2. **DAG Basics** → [DAG Design Patterns](https://chatwhole.com/learn/airflow/02-dag-design-patterns/) + [TaskFlow API](https://chatwhole.com/learn/airflow/09-airflow-taskflow-api/)
3. **Operators** → [Operators & Hooks](https://chatwhole.com/learn/airflow/03-operators-hooks/) + [Sensors](https://chatwhole.com/learn/airflow/07-sensors-operators/)
4. **Communication** → [XCom](https://chatwhole.com/learn/airflow/04-xcom-communications/) + [Connections](https://chatwhole.com/learn/airflow/10-airflow-connection-management/)
5. **Scheduling** → [Scheduling & Triggers](https://chatwhole.com/learn/airflow/05-scheduling-triggers/) + [Executors](https://chatwhole.com/learn/airflow/06-executors-comparison/)
6. **Production** → [Error Handling](https://chatwhole.com/learn/airflow/12-airflow-error-handling/) + [Testing](https://chatwhole.com/learn/airflow/13-airflow-testing-dags/)
7. **Advanced** → [Deferrable Operators](https://chatwhole.com/learn/airflow/22-airflow-deferrable-operators/) + [Dynamic DAGs](https://chatwhole.com/learn/airflow/24-airflow-dynamic-dags/)
8. **Cloud** → [MWAA](https://chatwhole.com/learn/airflow/29-airflow-mwaa-cloud/) + [Snowflake](https://chatwhole.com/learn/airflow/27-airflow-snowflake-integration/)

---

## Related Courses

| Course | Lessons | Link |
|--------|---------|------|
| Data Engineering | 55 | [Learn Data Engineering](https://chatwhole.com/learn/data-engineering/) |
| Python | 126 | [Learn Python](https://chatwhole.com/learn/python/) |
| SQL | 100+ | [Learn SQL](https://chatwhole.com/learn/sql/) |
| Snowflake | 50 | [Learn Snowflake](https://chatwhole.com/learn/snowflake/) |
| Kafka | 30 | [Learn Kafka](https://chatwhole.com/learn/kafka/) |

---

## Frequently Asked Questions

### How long does it take to complete the Airflow course?
The full 30-lesson Airflow course can be completed in 4-6 weeks at a pace of 1 lesson per day.

### What prerequisites are required?
- Basic [Python programming](https://chatwhole.com/learn/python/)
- Basic [SQL knowledge](https://chatwhole.com/learn/data-engineering/004-sql-fundamentals/)
- Understanding of [data engineering concepts](https://chatwhole.com/learn/data-engineering/001-what-is-data-engineering/)

### What version of Airflow does this course cover?
The course covers Airflow 2.x including the latest features like TaskFlow API, deferrable operators, and dynamic DAGs.

### Can I learn Airflow for free?
Yes! All 30 Airflow lessons are available for free at [chatwhole.com/learn/airflow/](https://chatwhole.com/learn/airflow/).

### What is the difference between Celery and Kubernetes executor?
Celery uses pre-provisioned worker nodes, while Kubernetes dynamically creates pods for each task. Kubernetes provides better isolation and scaling but adds complexity.

---

*Source: ChatWhole Learn — Free Apache Airflow Tutorials with Code Examples | https://chatwhole.com/learn/airflow/*
