---
title: Introduction
description: 'Set up Performance Co-Pilot and find what to read next in the docs.'
keywords:
  - 'Performance Co-Pilot'
  - app
  - setup
sidebar_position: 1
---

<!-- section-brief
Fill this in: Write a short orientation for someone who already has Performance Co-Pilot installed and landed here from the Documentation tab. One or two sentences on what this section covers and how it's organized. Do not restate what the app does or its feature list - that's the README's job on the Overview tab, and this reader has already seen it there. Do not list every page in this folder either - the sidebar already does that; use prose to say what to read first and why.
-->

## Before you begin

Before you set up the app, ensure you have:

- **Grafana permissions:** The `Organization administrator` role. Only organization administrators can enable and configure apps.

<!-- section-brief
Fill this in: Keep the list above. Add a bullet in the same **Label:** form for each other thing the reader needs: the Grafana version from `dependencies.grafanaDependency` in `src/plugin.json`, each plugin in `dependencies.plugins` linked to its catalog page at `https://grafana.com/grafana/plugins/<id>/`, and anything `src/plugin.json` doesn't declare, such as an external service, a telemetry pipeline or a license. Never cover installing the plugin itself, because the Installation tab on the plugin page owns it.
-->

## Enable the app

<!-- snippet:enable-app -->

To enable Performance Co-Pilot:

1. Click **Administration** > **Plugins and data** > **Plugins** in the left-side menu.
1. Enter `Performance Co-Pilot` in the search bar.
1. Select **Performance Co-Pilot**.
1. Click **Enable**.

<!-- /snippet:enable-app -->

<!-- section-brief
Fill this in: If `src/plugin.json` sets `"autoEnabled": true`, the app is enabled when it's installed, so remove this section, including the steps and their snippet markers. Otherwise keep the steps above and remove only this brief.
-->

After you enable the app, refer to [Configure](./configure.md) for its settings.

## Connect your data

<!-- section-brief
Fill this in: The steps to get the data the app shows into Grafana, such as adding a data source, setting up an agent, setting environment variables or configuring a telemetry exporter. Take them from the README's setup sections and from what the app queries in source. Give each step the commands or settings to copy, and say how the reader can tell the data has arrived. Change the heading if necessary to name the task, such as "Add a data source". Never include steps to install the plugin itself, because the Installation tab on the plugin page owns them.

If the app works without any setup of its own, remove this section entirely.
-->

## Common tasks

<!-- section-brief
Fill this in: List the jobs someone lands here to do, phrased as tasks rather than page titles, each linked to the page that answers it. For a typical app this might look like:

- [Change the app settings](./configure.md)
- [Find your way around Performance Co-Pilot](./performance-co-pilot.md)
- [Import the dashboards that ship with the app](./dashboards.md)
- [Fix setup and data errors](./troubleshooting.md)

Adapt this to Performance Co-Pilot's actual entry points - add, remove or reword tasks so each one matches a real job a user comes here to do. This is a curated set of jobs, not a mechanical list of every file in this folder.
-->
