---
title: Configure
description: 'Change the Performance Co-Pilot settings in Grafana or provision them as code.'
keywords:
  - 'Performance Co-Pilot'
  - app
  - configuration
  - provisioning
sidebar_position: 2
---

This document explains how to configure Performance Co-Pilot after you enable it.

## Before you begin

Before you configure the app, ensure you have:

- **Grafana permissions:** The `Organization administrator` role. Only organization administrators can configure apps.
- **The app enabled:** Follow [Enable the app](./index.md#enable-the-app).

## Open the configuration page

<!-- snippet:open-app-config -->

To open the Performance Co-Pilot configuration page:

1. Click **Administration** > **Plugins and data** > **Plugins** in the left-side menu.
1. Enter `Performance Co-Pilot` in the search bar.
1. Select **Performance Co-Pilot**.

<!-- /snippet:open-app-config -->

Then click the **Config** tab.

## Configure settings

The Config tab has no settings of its own. It shows whether the app is enabled and a button to toggle it:

- **Enable:** Turns the app on. Shown when the app is disabled.
- **Disable:** Turns the app off. Shown when the app is enabled.

Clicking either button reloads the page with the new state applied. Add and configure the PCP data sources separately, as described in [Connect your data](./index.md#connect-your-data).
## Provision the app

You can provision Performance Co-Pilot as code with a Grafana provisioning file. For more information, refer to [Provision Grafana](https://grafana.com/docs/grafana/latest/administration/provisioning/#plugins).

```yaml
apiVersion: 1

apps:
  - type: performancecopilot-pcp-app
    org_id: 1
    disabled: false
```

| Key | Sets |
| --- | ----- |
| `type` | The plugin ID. Always `performancecopilot-pcp-app`. |
| `org_id` | The organization to apply the setting to. |
| `disabled` | Whether the app is disabled. Set to `false` to enable it. |

The app declares no `jsonData` or `secureJsonData`, so there is nothing else to provision.