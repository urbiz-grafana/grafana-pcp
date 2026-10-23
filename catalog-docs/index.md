---
title: Introduction
description: 'Set up Performance Co-Pilot and find what to read next in the docs.'
keywords:
  - 'Performance Co-Pilot'
  - app
  - setup
sidebar_position: 1
---

Set up Performance Co-Pilot here, then use [Common tasks](#common-tasks) to find what to read next.

## Before you begin

Before you set up the app, ensure you have:

- **Grafana permissions:** The `Organization administrator` role. Only organization administrators can enable and configure apps.
- **Grafana version:** Grafana 12.4.3 or later.
- **Performance Co-Pilot (PCP):** `pmcd` and `pmproxy` running on each monitored host.
- **Valkey or Redis:** Required only for the PCP Valkey data source, with `pmlogger` archiving metrics and `pmproxy` configured to write them to the key server.
- **bpftrace:** Installed on the monitored host, required only for the PCP bpftrace data source.
- **Full-text metric search:** `pmproxy` with `[pmsearch] enabled = true` and a search index built by `pmsearch_daily(1)`, required only for the [Metric Search page](./performance-co-pilot.md).

## Enable the app

<!-- snippet:enable-app -->

To enable Performance Co-Pilot:

1. Click **Administration** > **Plugins and data** > **Plugins** in the left-side menu.
1. Enter `Performance Co-Pilot` in the search bar.
1. Select **Performance Co-Pilot**.
1. Click **Enable**.

<!-- /snippet:enable-app -->

After you enable the app, refer to [Configure](./configure.md) for its settings.

## Connect your data

Add a data source for each type of metric you want to analyze:

1. Click **Connections** > **Data sources** > **Add data source**.
2. Select **PCP Valkey** for historical metrics across multiple hosts, **PCP Vector** for real-time metrics from a single host, or **PCP bpftrace** for eBPF tracing scripts.
3. Set the URL to your `pmproxy` instance. The default, `http://localhost:44322`, works in most cases.
4. Click **Save & test**. A successful test confirms the data source can reach `pmproxy`.

Each data source ships with its own dashboards. Refer to [Dashboards](./dashboards.md) to import them.

## Common tasks

- [Add and configure a PCP data source](#connect-your-data)
- [Search and inspect PCP metrics](./performance-co-pilot.md)
- [Import the dashboards that ship with each data source](./dashboards.md)
- [Fix setup and data errors](./troubleshooting.md)