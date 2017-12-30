---
layout: page
title: "Concord232 Alarm Control Panel"
description: "Instructions how to integrate Interlogix/GE Concord4 with RS-232 Automation Control Module into Home Assistant."
date: 2016-10-11 10:00
sidebar: true
comments: false
sharing: true
footer: true
logo: interlogix.png
ha_category: Alarm
ha_release: 0.31
---

The `concord232` platform provides integration with GE, Interlogix
(and other brands) alarm panels that support the RS-232 Automation
Module (60-783-02) interface (or have it built in). Supported panels
include Concord 4.

This component requires a [server](https://github.com/rwa/concord232)
process running on the device with the serial connection to the
Automation Module, and a local
[client](https://github.com/rwa/concord232) that Home Assistant
communicates with.  The server can run locally if they are the same
device.

To enable this, add the following lines to your `configuration.yaml`:

```yaml
# Example configuration.yaml entry
alarm_control_panel:
  - platform: concord232
```

Configuration variables:

- **host** (*Optional*): The host where the concord232 server process is running. Defaults to localhost.
- **port** (*Optional*): The port where the Alarm panel is listening. Defaults to 5007.

