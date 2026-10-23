# Performance Co-Pilot Grafana Plugin

[![Build Status](https://github.com/performancecopilot/grafana-pcp/workflows/CI/badge.svg)](https://github.com/performancecopilot/grafana-pcp/actions?query=workflow:CI)
[![Documentation Status](https://readthedocs.org/projects/grafana-pcp/badge/?version=latest)](https://grafana-pcp.readthedocs.io/en/latest/?badge=latest)


## Overview

[Performance Co-Pilot (PCP)](https://pcp.io) provides a framework and services to support system-level performance monitoring and management.
It presents a unifying abstraction for all of the performance data in a system, and many tools for interrogating, retrieving and processing that data.

This Grafana app plugin integrates PCP metrics into Grafana, bundling three datasources and premade dashboards for real-time monitoring, historical analysis, and eBPF tracing.

[![Vector Overview](https://raw.githubusercontent.com/performancecopilot/grafana-pcp/main/src/img/screenshots/vector-overview.png)](https://raw.githubusercontent.com/performancecopilot/grafana-pcp/main/src/img/screenshots/vector-overview.png)
[![Vector Containers](https://raw.githubusercontent.com/performancecopilot/grafana-pcp/main/src/img/screenshots/vector-containers.png)](https://raw.githubusercontent.com/performancecopilot/grafana-pcp/main/src/img/screenshots/vector-containers.png)
[![bpftrace Flame Graph](https://raw.githubusercontent.com/performancecopilot/grafana-pcp/main/src/img/screenshots/bpftrace-flame-graph.png)](https://raw.githubusercontent.com/performancecopilot/grafana-pcp/main/src/img/screenshots/bpftrace-flame-graph.png)
[![Vector metrics autocompletion](https://raw.githubusercontent.com/performancecopilot/grafana-pcp/main/src/img/screenshots/vector-metric-autocompletion.png)](https://raw.githubusercontent.com/performancecopilot/grafana-pcp/main/src/img/screenshots/vector-metric-autocompletion.png)

[More screenshots](https://github.com/performancecopilot/grafana-pcp/tree/main/src/img/screenshots)

## Features

* Analysis of historical PCP metrics using [pmseries](https://man7.org/linux/man-pages/man1/pmseries.1.html) query language
* Analysis of real-time PCP metrics using [pmwebapi](https://man7.org/linux/man-pages/man3/pmwebapi.3.html) live services
* Enhanced Berkeley Packet Filter (eBPF) tracing using [bpftrace](https://github.com/iovisor/bpftrace/blob/master/README.md) scripts
* Dashboards for detecting potential performance issues using the Utilization Saturation and Errors (USE) method [2]
* Full-text search in metric names, descriptions, instances [1]
* Support for [Grafana Alerting](https://grafana.com/docs/grafana/latest/alerting/) [1]
* Support for [derived metrics](https://man7.org/linux/man-pages/man3/pmregisterderived.3.html#DESCRIPTION) (arithmetic operators and statistical functions inside a query) [2]
* Automated configuration of metric units [1,2,3]
* Automatic rate and time utilization conversion
* Heatmap, table [2,3] and flame graph [3] support
* Auto completion of metric names [1,2], qualifier keys and values [1], and bpftrace probes, builtin variables and functions [3]
* Display of semantics, units and help texts of metrics [2] and bpftrace builtins [3]
* Legend templating support with `$metric`, `$metric0`, `$instance`, `$some_label`, `$some_dashboard_variable`
* Container support [1,2]
* Support for custom endpoint and hostspec per panel [2,3]
* Support for repeated panels
* Sample dashboards for all datasources

[1] PCP Valkey
[2] PCP Vector
[3] PCP bpftrace

For setup, configuration and data source requirements, refer to the Documentation tab on the [plugin's catalog page](https://grafana.com/grafana/plugins/performancecopilot-pcp-app/) or to the full [Documentation](https://grafana-pcp.readthedocs.io).

## [Contributing](https://github.com/performancecopilot/grafana-pcp/blob/main/CONTRIBUTING.md)
