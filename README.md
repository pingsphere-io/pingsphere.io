
# PingSphere.io

Welcome to pingsphere.io! PingSphere is a product of HA Devevelopment Technologies and the first step in many modern internet services.

At it's core PingSphere.io is a uptime monitoring service designed to monitor all kinds of web services as close to real time as possible. However doing this at scale, with minimal infrastructure while achieving high availiblity makes it a hard thing to do.

We've managed it with amazing low level & kernel by passing networking code. A super resilient & redudent process for managing alert notifications,

PingSphere.io has multiple useful features and will support multiple if not all network protocals as well as commonly used API application checks.

**Why are we doing this? There are so many others out there?**

We got asked this and the answer came down to an easy list. Existing services are:

- Expensive
- No longer offer free services
- Became large enterprises
- Complicated or over simplified alerting
- Old or outdated and no longer meet modern needs
- Do not support major alert integrations

However the largest one was fundimental. In perticualr with ICMP it is hard to ping hundreds of hosts at the same time from one server without causing artifical delay.

Artifical delay occors when the networking packets are passing through the CPU, kernel, application stack before registering how long it took. e.g:

Using the `ping` command as the base line on linux (debian 9) as an example.

| Code         | RTT    |
|:------------:|:------:|
| `ping`       | 1ms    |
| `golang`     | 130ms  |
| `nodejs`     | 159ms  |
| `pingsphere` | 3ms    |

### Network Monitors

Currently we are supporting:

- ICMP

Mean while we are working on:

- TCP
- UDP
- DNS
- IPv6
- HTTP2 / gRPC
- API
- MTR

### Alerts

With each of these monitor types you're able to create alert rules, which trigger when a check of some kind has has failed and met a alert score threashold.

**Alert Score:** a integer indicating the number of failed checks.

**Alert Integration:** A medium in which you want to be notified when an alert has been triggered or resolved.

**Alert:** a defined alert which has a alert score threshold, monitors & alert integrations

### Alert Integrations

We currently integrate with some of the major alert providers which are used by teams all over the world.

## Contact Us

Email us at: support@pingsphere.io

[Raise an Issue or feature](https://github.com/pingsphere-io/pingsphere.io/issues)



<!-- got a leave a space -->
