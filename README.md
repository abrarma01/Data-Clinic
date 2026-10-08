# Data-Clinic
Data Clinic— Data quality &amp; pipeline observability platform for a healthcare  cloud provider: automated DQ checks on hospital data feeds, dead-letter handling,  Airflow orchestration, and real-time Prometheus/Grafana monitoring.


Data-Clinic is a production-style data engineering platform simulating a healthcare 
cloud provider that stores and manages patient data on behalf of hospitals.

Every night, partner hospitals push patient, visit, and lab-result feeds to the 
platform. DataClinic validates every batch against a data-quality framework 
(nulls, duplicates, schema, row counts, referential integrity, value ranges), 
routes bad records to a dead-letter table instead of failing silently, orchestrates 
runs with Airflow, and exposes pipeline health as Prometheus metrics with Grafana 
dashboards and alerting.

# Goal: 

data issues are caught by engineers — not reported by doctors staring at 
broken dashboards.
