---
description: Endpoints list
---

# Endpoint list

## API endpoint list

```text
  /delete`, deleteJson.recentErrors)
  /endpoints`, endpoints)
  /recent`, serve.recent)
  /recent-error`, serve.recentError)
  /:server/:site/days/:days`, getTime.getLastDays)
  /:server/:site/hours/:day/:between`, getTime.getHours)
  /:server/:site/uptime`, getUpTime.uptime)
  /:server/:site/today`, serve.today)
  /:server/:site/files`, serve.logFiles)
  /:server/:site/dates`, serve.dates)
  /:server/:site/:logs`, serve.server)
```

Cheat sheet

| :server | The servers name | Example |
| :--- | :--- | :--- |
| :site | The sites name | /test |
| :days | Number of days you want | /2 |
| :between | Two numbers of between or one number for one hour | /01-22 or 01 |
| :logs | Date  | /log-1-1-2020 |

