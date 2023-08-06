## Minimum RTO for a single AZ outage

| Time  | Description                                      |
| ----- | ------------------------------------------------ |
| 00:00 | problem occurred                                 |
| 00:05 | Time to take to raise alerts                     |
| 00:08 | Automatically switch to second availability zone |

## Minimum RTO for a single region outage

|Time|Description|
|---|---|
|00:00|Problem occurred (First minute)|
|00:05|Time take to raise alerts (5 mins)|
|00:06|Alert triggers on-all staff (1 mins)|
|00:16|On-call staff may need to get out of bed, get to a computer, log in, log onto VPN (10 mins)|
|00:26|On-call Root cause Analysis starts (10 mins)|
|00:36|Root cause Analysis done (10 mins)|
|00:46|Remediation started (10 mins)|
|00:51|Issue fixed (5 mins)|

## Minimum RPO for a single AZ outage

RDS has point in time restore available after every 1 min. At the most data loss will be of 1 minute.

## Minimum RPO for a single region outage

Read replicas are almost kept in sync with the primary database, ideally, they will be having the same RPO as the primary database. For the practical purpose we can consider at most the RPO should be ±10 mins.
