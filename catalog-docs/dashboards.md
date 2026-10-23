---
title: Dashboards
description: 'Import and use the dashboards that ship with Performance Co-Pilot.'
keywords:
  - 'Performance Co-Pilot'
  - app
  - dashboards
sidebar_position: 6
---

Performance Co-Pilot ships with ready-made dashboards that you can import and use as they are, or as a starting point for your own. For general information about dashboards, refer to [Dashboards](https://grafana.com/docs/grafana/latest/dashboards/).

## Import a dashboard

<!-- snippet:import-app-dashboard -->

To import a dashboard that ships with Performance Co-Pilot:

1. Click **Administration** > **Plugins and data** > **Plugins** in the left-side menu.
1. Enter `Performance Co-Pilot` in the search bar.
1. Select **Performance Co-Pilot**.
1. Click the **Dashboards** tab.
1. Click **Import** next to the dashboard.

Imported dashboards don't update when you upgrade the plugin. When a plugin upgrade ships a newer version of a dashboard, click **Update** next to it. This overwrites any changes you made to it.

<!-- /snippet:import-app-dashboard -->

## Included dashboards

### PCP Valkey: Metric Preview dashboards

**PCP Valkey: Metric Preview (Graph)** and **PCP Valkey: Metric Preview (Table)** let you pick any PCP metric from a drop-down list and plot it as a time series graph or a table, using the PCP Valkey data source. Open one directly from a metric's detail page on the [Metric Search page](./performance-co-pilot.md#view-metric-details) by clicking **Preview**, which pre-fills the metric for you.

### PCP Vector Checklist dashboards

**PCP Vector Checklist** is a USE-method (Utilization Saturation and Errors) dashboard for a single host, using the PCP Vector data source. Its CPU, Storage, Memory and Network panels flag utilization above a threshold and link to a dedicated dashboard for that resource:

- PCP Vector Checklist: CPU, CPU System, CPU User
- PCP Vector Checklist: Storage
- PCP Vector Checklist: Memory, Memory Swap
- PCP Vector Checklist: Network, Network RX, Network TX

Each linked dashboard breaks down its resource further, for example per-CPU or per-disk utilization, to help you find the cause of a flagged warning.