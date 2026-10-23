---
title: Troubleshooting
description: 'Troubleshoot common Performance Co-Pilot setup, data and access errors.'
keywords:
  - 'Performance Co-Pilot'
  - app
  - troubleshooting
sidebar_position: 8
---

This page explains how to fix common issues when you set up or use Performance Co-Pilot. For setup instructions, refer to the [Introduction](./index.md).

## Setup errors

These errors happen while adding or testing a PCP data source.

### "HTTP Error 502: Bad Gateway, please check the datasource and pmproxy settings"

**Symptoms:** Adding a PCP Valkey, PCP Vector or PCP bpftrace data source fails with this error.

**Possible causes and solutions:**

| Cause | Solution |
| ----- | -------- |
| `pmproxy` isn't running | Run `systemctl status pmproxy` on the monitored host and start it if it's stopped. |
| `pmproxy` was built without time-series (libuv) support | Check `/var/log/pcp/pmproxy/pmproxy.log` for confirmation that time-series support is enabled. |

## Missing data

Dashboards and the [Metric Search page](./performance-co-pilot.md) load but show no data when a data source isn't fully set up. Refer to [Connect your data](./index.md#connect-your-data) to configure a data source, and to [Before you begin](./index.md#before-you-begin) for what each one needs, such as `pmlogger` archiving metrics for the PCP Valkey data source or a `pmsearch` index for metric search.

## Get more detail about an error

For errors in the app, open the developer tools in your browser and check the console.

## Get additional help

If this page doesn't solve your problem:

- Search the [Grafana community forums](https://community.grafana.com/).
- If your Grafana Cloud or Grafana Enterprise plan includes support, contact Grafana Support.
- Search or open an issue on the [GitHub issue tracker](https://github.com/performancecopilot/grafana-pcp/issues).
- Refer to the [Performance Co-Pilot documentation](https://pcp.io/docs/) for `pmcd`, `pmproxy` and `pmlogger` setup.
When you report an issue, include:

- The Grafana and plugin versions.
- The error message, with sensitive information removed.
- The steps to reproduce the issue.
- The app page where it happens and the relevant app settings, with credentials removed.
