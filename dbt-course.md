---
title: "dbt Course — 30 Free Lessons with Code Examples | ChatWhole"
description: "Master dbt (data build tool) with 30 free lessons. Learn dbt Core architecture, models, seeds, snapshots, Jinja templating, ref functions, testing, incremental models, materializations, Snowflake/BigQuery integration, and best practices with hands-on SQL code examples."
keywords: "dbt course, learn dbt, dbt tutorial, dbt core, dbt models, dbt testing, dbt incremental models, dbt materializations, dbt Jinja, dbt ref function, dbt Snowflake, dbt BigQuery, dbt best practices, data transformation, analytics engineering"
canonical: "https://chatwhole.com/learn/dbt/"
og_title: "dbt Course — 30 Free Lessons with Code Examples"
og_description: "Complete dbt course with 30 free lessons. Learn dbt Core, models, Jinja, testing, incremental models, and build production data transformations."
og_url: "https://chatwhole.com/learn/dbt/"
og_type: "article"
---

# dbt Course — Complete 30-Lesson Curriculum with Code Examples

dbt (data build tool) is a SQL-based transformation tool that enables data teams to build clean, tested, documented data models using SQL and Python, applying software engineering principles to analytics code. This comprehensive 30-lesson course covers everything from core architecture to advanced patterns like data vault, SCD Type 2, and semantic layer.

**Source:** [ChatWhole Learn — dbt](https://chatwhole.com/learn/dbt/)

---

## Table of Contents

### Module 1: dbt Foundations (01-10)

Master the core dbt concepts: architecture, models, Jinja templating, and testing.

| # | Topic | Link |
|---|-------|------|
| 001 | [dbt Core Architecture](https://chatwhole.com/learn/dbt/01-dbt-core-architecture/) | Manifest, DAG, compilation pipeline, project structure |
| 002 | [Models, Seeds, Snapshots](https://chatwhole.com/learn/dbt/02-models-seeds-snapshots/) | Core components for data transformation |
| 003 | [Jinja Templating](https://chatwhole.com/learn/dbt/03-jinja-templating/) | Variables, filters, macros, dynamic SQL |
| 004 | [ref() Function](https://chatwhole.com/learn/dbt/04-ref-function/) | Model reference resolution and dependencies |
| 005 | [dbt Tests](https://chatwhole.com/learn/dbt/05-dbt-tests/) | Schema tests, data tests, custom validations |
| 006 | [dbt Docs](https://chatwhole.com/learn/dbt/06-dbt-docs/) | Documentation generation and data catalog |
| 007 | [Incremental Models](https://chatwhole.com/learn/dbt/07-incremental-models/) | Merge, append, delete+insert strategies |
| 008 | [Materializations](https://chatwhole.com/learn/dbt/08-materializations/) | Table, view, incremental, ephemeral |
| 009 | [Exposures & Semantic Layer](https://chatwhole.com/learn/dbt/09-exposures-semantic-layer/) | Defining downstream dependencies |
| 010 | [dbt Projects](https://chatwhole.com/learn/dbt/10-dbt-projects/) | Project configuration and organization |

### Module 2: Intermediate dbt (11-20)

Master advanced Jinja, data quality, platform integrations, and best practices.

| # | Topic | Link |
|---|-------|------|
| 011 | [Advanced Jinja](https://chatwhole.com/learn/dbt/11-advanced-jinja/) | Complex macros, loops, conditional logic |
| 012 | [Data Quality Tests](https://chatwhole.com/learn/dbt/12-data-quality-tests/) | Custom tests, assertions, monitoring |
| 013 | [dbt Cloud](https://chatwhole.com/learn/dbt/13-dbt-cloud/) | Managed dbt, scheduling, CI/CD |
| 014 | [Mesh & Data Collaboration](https://chatwhole.com/learn/dbt/14-mesh-data-collaboration/) | Cross-project refs, data sharing |
| 015 | [Performance Tuning](https://chatwhole.com/learn/dbt/15-performance-tuning/) | Optimization, parallelism, caching |
| 016 | [dbt BigQuery](https://chatwhole.com/learn/dbt/16-dbt-bigquery/) | BigQuery-specific features and config |
| 017 | [dbt Snowflake](https://chatwhole.com/learn/dbt/17-dbt-snowflake/) | Snowflake integration and optimization |
| 018 | [dbt Redshift](https://chatwhole.com/learn/dbt/18-dbt-redshift/) | Redshift-specific patterns |
| 019 | [dbt Postgres](https://chatwhole.com/learn/dbt/19-dbt-postgres/) | PostgreSQL integration |
| 020 | [dbt Best Practices](https://chatwhole.com/learn/dbt/20-dbt-best-practices/) | Project conventions, naming, organization |

### Module 3: Advanced dbt (21-30)

Master unit testing, advanced patterns, and cutting-edge dbt features.

| # | Topic | Link |
|---|-------|------|
| 021 | [Unit Testing](https://chatwhole.com/learn/dbt/21-dbt-unit-testing/) | Testing individual models in isolation |
| 022 | [Data Vault](https://chatwhole.com/learn/dbt/22-dbt-data-vault/) | Hub, link, and satellite patterns |
| 023 | [SCD Type 2](https://chatwhole.com/learn/dbt/23-dbt-scd-type-2/) | Slowly changing dimensions in dbt |
| 024 | [Ephemeral Models](https://chatwhole.com/learn/dbt/24-dbt-ephemeral-models/) | CTE-based transformations |
| 025 | [Custom Macros](https://chatwhole.com/learn/dbt/25-dbt-custom-macros/) | Reusable Jinja code blocks |
| 026 | [on-run-start/end](https://chatwhole.com/learn/dbt/26-dbt-on-run-start-end/) | Hook-based automation |
| 027 | [Package Development](https://chatwhole.com/learn/dbt/27-dbt-package-development/) | Building and publishing dbt packages |
| 028 | [Multi-Project](https://chatwhole.com/learn/dbt/28-dbt-multi-project/) | Scaling dbt across teams |
| 029 | [Semantic Layer](https://chatwhole.com/learn/dbt/29-dbt-semantic-layer/) | Metrics and governed definitions |
| 030 | [AI Integration](https://chatwhole.com/learn/dbt/30-dbt-ai-integration/) | AI-powered dbt features |

---

## Key Concepts Summary

### dbt Project Structure

| Directory | Purpose |
|-----------|---------|
| models/ | SQL transformation files |
| seeds/ | CSV files loaded as tables |
| snapshots/ | SCD Type 2 change tracking |
| macros/ | Reusable Jinja code |
| tests/ | Custom data tests |
| analysis/ | Ad-hoc analysis queries |
| docs/ | Documentation files |

### Materialization Types

| Type | Behavior | Use Case |
|------|----------|----------|
| Table | Drops and recreates on each run | Full refresh |
| View | Creates or replaces view | Simple transforms |
| Incremental | Only processes new/changed data | Large datasets |
| Ephemeral | Injects CTEs into downstream | Reusable logic |

### Incremental Strategies

| Strategy | Pattern | Use Case |
|----------|---------|----------|
| Merge | UPSERT (update + insert) | Most common |
| Append | Insert new rows only | Append-only logs |
| Delete+Insert | Replace partitions | Date-based refresh |

### dbt Functions

| Function | Purpose | Example |
|----------|---------|---------|
| ref() | Reference other models | `{{ ref('stg_orders') }}` |
| source() | Reference source tables | `{{ source('raw', 'orders') }}` |
| var() | Access project variables | `{{ var('start_date') }}` |
| is_incremental() | Check if incremental | `{% if is_incremental() %}` |
| this() | Reference current model | `{{ this }}` |

---

## Code Examples

### dbt_project.yml Configuration

```yaml
name: 'my_analytics'
version: '1.0.0'
config-version: 2

profile: 'analytics'

model-paths: ["models"]
test-paths: ["tests"]
seed-paths: ["seeds"]
macro-paths: ["macros"]
snapshot-paths: ["snapshots"]

models:
  my_analytics:
    staging:
      +materialized: view
      +schema: staging
    intermediate:
      +materialized: ephemeral
    marts:
      +materialized: incremental
      +schema: analytics

vars:
  start_date: '2020-01-01'
```

### Staging Model with Source

```sql
-- models/staging/stg_orders.sql
{{
    config(
        materialized='view',
        schema='staging'
    )
}}

with source as (
    select * from {{ source('raw', 'orders') }}
),

renamed as (
    select
        id as order_id,
        customer_id,
        status,
        created_at as order_date,
        amount,
        _fivetran_synced as synced_at
    from source
)

select * from renamed
```

### Source Definition

```yaml
-- models/staging/_sources.yml
version: 2

sources:
  - name: raw
    database: raw_data
    schema: public
    loader: fivetran
    loaded_at_field: _fivetran_synced
    freshness:
      warn_after: {count: 6, period: hour}
      error_after: {count: 24, period: hour}
    tables:
      - name: orders
        description: "Raw orders"
        columns:
          - name: id
            data_tests:
              - unique
              - not_null
          - name: customer_id
            data_tests:
              - not_null
```

### Incremental Model

```sql
-- models/marts/fct_orders.sql
{{
    config(
        materialized='incremental',
        unique_key='order_id',
        incremental_strategy='merge',
        partition_by={
            "field": "order_date",
            "data_type": "date"
        },
        cluster_by=['customer_id']
    )
}}

with orders as (
    select * from {{ ref('stg_orders') }}
),

customers as (
    select * from {{ ref('dim_customers') }}
),

final as (
    select
        orders.order_id,
        orders.customer_id,
        customers.customer_name,
        orders.order_date,
        orders.status,
        orders.amount,
        current_timestamp() as updated_at
    from orders
    left join customers on orders.customer_id = customers.customer_id
)

select * from final

{% if is_incremental() %}
where updated_at > (select max(updated_at) from {{ this }})
{% endif %}
```

### Snapshot Definition

```sql
-- snapshots/customers_snapshot.sql
{% snapshot customers_snapshot %}

{{
    config(
        target_schema='snapshots',
        unique_key='customer_id',
        strategy='timestamp',
        updated_at='updated_at',
        invalidate_hard_deletes=True
    )
}}

select * from {{ source('raw', 'customers') }}

{% endsnapshot %}
```

### Custom Schema Test

```sql
-- tests/assert_positive_amount.sql
{% test assert_positive_amount(model) %}

select *
from {{ model }}
where amount < 0

{% endtest %}
```

### Seed Configuration

```yaml
-- seeds/country_codes.yml
version: 2

seeds:
  - name: country_codes
    description: "ISO country codes"
    config:
      column_types:
        country_code: varchar(2)
        country_name: varchar(100)
    columns:
      - name: country_code
        data_tests:
          - unique
          - not_null
```

---

## dbt Learning Path

1. **Start Here** → [dbt Core Architecture](https://chatwhole.com/learn/dbt/01-dbt-core-architecture/)
2. **Core Concepts** → [Models, Seeds, Snapshots](https://chatwhole.com/learn/dbt/02-models-seeds-snapshots/) + [ref() Function](https://chatwhole.com/learn/dbt/04-ref-function/)
3. **Templating** → [Jinja Templating](https://chatwhole.com/learn/dbt/03-jinja-templating/) + [Advanced Jinja](https://chatwhole.com/learn/dbt/11-advanced-jinja/)
4. **Testing** → [dbt Tests](https://chatwhole.com/learn/dbt/05-dbt-tests/) + [Data Quality](https://chatwhole.com/learn/dbt/12-data-quality-tests/)
5. **Performance** → [Incremental Models](https://chatwhole.com/learn/dbt/07-incremental-models/) + [Materializations](https://chatwhole.com/learn/dbt/08-materializations/)
6. **Platform** → [dbt Snowflake](https://chatwhole.com/learn/dbt/17-dbt-snowflake/) + [dbt BigQuery](https://chatwhole.com/learn/dbt/16-dbt-bigquery/)
7. **Advanced** → [Data Vault](https://chatwhole.com/learn/dbt/22-dbt-data-vault/) + [SCD Type 2](https://chatwhole.com/learn/dbt/23-dbt-scd-type-2/)
8. **Enterprise** → [Mesh](https://chatwhole.com/learn/dbt/14-mesh-data-collaboration/) + [Semantic Layer](https://chatwhole.com/learn/dbt/29-dbt-semantic-layer/)

---

## Related Courses

| Course | Lessons | Link |
|--------|---------|------|
| Data Engineering | 55 | [Learn Data Engineering](https://chatwhole.com/learn/data-engineering/) |
| Snowflake | 50 | [Learn Snowflake](https://chatwhole.com/learn/snowflake/) |
| SQL | 100+ | [Learn SQL](https://chatwhole.com/learn/sql/) |
| Python | 126 | [Learn Python](https://chatwhole.com/learn/python/) |
| Airflow | 30 | [Learn Airflow](https://chatwhole.com/learn/airflow/) |

---

## Frequently Asked Questions

### How long does it take to complete the dbt course?
The full 30-lesson dbt course can be completed in 4-6 weeks at a pace of 1 lesson per day.

### Do I need dbt experience to take this course?
No prior dbt experience is required. Basic [SQL knowledge](https://chatwhole.com/learn/data-engineering/004-sql-fundamentals/) is recommended.

### What databases does dbt support?
dbt supports Snowflake, BigQuery, Redshift, PostgreSQL, Databricks, Azure Synapse, and many more via adapters.

### Can I learn dbt for free?
Yes! All 30 dbt lessons are available for free at [chatwhole.com/learn/dbt/](https://chatwhole.com/learn/dbt/). dbt Core is also open source.

### What is the difference between dbt Core and dbt Cloud?
dbt Core is the open-source CLI tool, while dbt Cloud provides a managed platform with scheduling, CI/CD, documentation hosting, and a visual IDE.

---

*Source: ChatWhole Learn — Free dbt Tutorials with Code Examples | https://chatwhole.com/learn/dbt/*
