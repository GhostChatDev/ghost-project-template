# Data kit

Charts, data processing and dashboards. All optional; install only when `PRODUCT.md` asks. Licences were read from the public repositories on 22 November 2026; recheck before reuse.

**Pipeline: data in → shape it → query → chart → screen.**

## Inside the app

| Name and GitHub URL | Licence | Use for |
|---|---|---|
| [Apache ECharts](https://github.com/apache/echarts) | Apache-2.0 | Interactive and animated charts in web apps. Theme it from the `DESIGN.md` tokens. |
| [Observable Plot](https://github.com/observablehq/plot) | ISC | Clear, small charts with little code. |
| [DuckDB](https://github.com/duckdb/duckdb) and [DuckDB-WASM](https://github.com/duckdb/duckdb-wasm) | MIT | SQL over CSV, Parquet or JSON. The WASM build runs in the browser, so the data stays on the person's device. |

Charts still follow `design-floor.md`: a chart type that fits the data, a legend, no meaning by color alone, a table or text alternative, and loading, empty and error states. Drawing a simple chart by hand in SVG is fine when no library was asked for.

## Python data apps (only when the project is one)

| Name and GitHub URL | Licence | Use for |
|---|---|---|
| [Polars](https://github.com/pola-rs/polars) | MIT | Fast dataframes. |
| [Streamlit](https://github.com/streamlit/streamlit) | Apache-2.0 | Turning a Python script into a data app. |
| [marimo](https://github.com/marimo-team/marimo) | Apache-2.0 | Reactive notebooks that can also run as apps. |
| [Evidence](https://github.com/evidence-dev/evidence) | MIT | Reports written in SQL and markdown. |
| [JupyterLab](https://github.com/jupyterlab/jupyterlab) | BSD-3-Clause | Exploring data; not a product dependency. |

## Services you run, not parts of an app

Listed so they aren't added by accident. Each is a server or platform of its own; adding one is a product decision for `PRODUCT.md`.

| Name and GitHub URL | Licence | Note |
|---|---|---|
| [Apache Superset](https://github.com/apache/superset) | Apache-2.0 | Self-hosted BI dashboards. |
| [ClickHouse](https://github.com/ClickHouse/ClickHouse) | Apache-2.0 | Analytics database for very large data. |
| [dbt](https://github.com/dbt-labs/dbt-core) | Apache-2.0 | SQL models with lineage and tests. |
| [Grafana](https://github.com/grafana/grafana) | AGPL-3.0 | Live metrics. AGPL: offering a changed version to users over a network means sharing those changes. |
| [Metabase](https://github.com/metabase/metabase) | AGPL, plus a commercial licence for its enterprise folder | Same AGPL caution as Grafana. |
| [Airbyte](https://github.com/airbytehq/airbyte) | Elastic License 2.0 | Data pipelines from many sources. ELv2 forbids offering it to others as a hosted service. |
