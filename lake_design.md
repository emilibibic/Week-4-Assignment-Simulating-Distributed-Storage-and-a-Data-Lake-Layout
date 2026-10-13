# Data Lake Directory Structure

To optimize query performance and reduce unnecessary data scanning, the data lake is structured hierarchically by year and month.

## Directory Layout
```text
/data_lake/loans/
├── year=2024/
│   ├── month=11/
│   │   └── loans_2024_11.parquet
│   └── month=12/
│       └── loans_2024_12.parquet
└── year=2025/
    ├── month=01/
    │   └── loans_2025_01.parquet