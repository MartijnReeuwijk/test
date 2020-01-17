---
description: First draft API page
---

# API endpoints

{% api-method method="get" host="http://localhost:3333/api" path="/endpoints" %}
{% api-method-summary %}
Endpoints
{% endapi-method-summary %}

{% api-method-description %}
This method will return the available server, sites and endpoints.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="/endpoints" type="string" required=false %}
Return all available servers and site.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Returns the servers and site structure.
{% endapi-method-response-example-description %}

```
[
  {
    "id": "1k2lv2sxuqta0qr0ilubhrf53",
    "name": "Name",
    "sites": [
      {
        "id": "9zfjdwa0h4ucug8081erz8oas",
        "name": "Site_name",
        "endpoint": "/Name/Site_name",
        "error": false
      },
      {
        "id": "9zfjdwa0h4ucug8081erz8oas",
        "name": "Site_name_2",
        "endpoint": "/Name/Site_name_2",
        "error": false
      },
    ],
    "error": false
  }
  ]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="" path="/recent" %}
{% api-method-summary %}
Recent
{% endapi-method-summary %}

{% api-method-description %}
This method will return the most recently added values for each server and site.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="/recent" type="string" required=false %}
return all recently added values
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
This array will hold al the most recent added values.
{% endapi-method-response-example-description %}

```
[
  {
    "server_name": "server_name",
    "name": "site_name",
    "pid": 127296,
    "version": null,
    "created_at": 1577980343733,
    "status": "online",
    "restart_time": 0,
    "unstable_restarts": 0,
    "uptime": "02 Jan 2018 16:52:23",
    "memory_use": 45,
    "cpu_use": 0,
    "time": "23:59:00",
    "date": "02-01-2020"
  }
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="" path="/:server/:site/dates" %}
{% api-method-summary %}
Get dates
{% endapi-method-summary %}

{% api-method-description %}
Returns the dates that have data
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="dates" type="string" required=true %}
dates command
{% endapi-method-parameter %}

{% api-method-parameter name="site" type="string" required=true %}
site name
{% endapi-method-parameter %}

{% api-method-parameter name="server" type="string" required=true %}
server name
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Sites available dates
{% endapi-method-response-example-description %}

```
[
  "2020-01-01",
  "2019-12-18",
  "2019-12-19",
  "2020-01-02",
  "2019-12-20",
  "2019-12-21",
  "2019-12-22",
  "2019-12-23",
  "2019-12-24",
  "2019-12-25",
  "2019-12-26",
  "2019-12-27",
  "2019-12-28",
  "2019-12-29",
  "2020-01-03",
  "2019-12-30",
  "2019-12-31",
  "2020-01-04",
  "2020-01-05",
  "2020-01-06",
  "2020-01-07",
  "2020-01-08",
  "2020-01-09"
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="" path="/:server/:site/files" %}
{% api-method-summary %}
Get files
{% endapi-method-summary %}

{% api-method-description %}
Return all the files that are associated with the site
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="/files" type="string" required=false %}
files command
{% endapi-method-parameter %}

{% api-method-parameter name="site" type="string" required=true %}
site name
{% endapi-method-parameter %}

{% api-method-parameter name="server" type="string" required=true %}
server name
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Returns all the files associated with the site.
{% endapi-method-response-example-description %}

```
[
  "log-1-1-2020.json",
  "log-18-12-2019.json",
  "log-19-12-2019.json",
  "log-2-1-2020.json",
  "log-20-12-2019.json",
  "log-21-12-2019.json",
  "log-22-12-2019.json",
  "log-23-12-2019.json",
  "log-24-12-2019.json",
  "log-25-12-2019.json",
  "log-26-12-2019.json",
  "log-27-12-2019.json",
  "log-28-12-2019.json",
  "log-29-12-2019.json",
  "log-3-1-2020.json",
  "log-30-12-2019.json",
  "log-31-12-2019.json",
  "log-4-1-2020.json",
  "log-5-1-2020.json",
  "log-6-1-2020.json",
  "log-7-1-2020.json",
  "log-8-1-2020.json",
  "log-9-1-2020.json"
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="" path="/:server/:site/today" %}
{% api-method-summary %}
Get today
{% endapi-method-summary %}

{% api-method-description %}
Get the data of today
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="/today" type="string" required=false %}
today command
{% endapi-method-parameter %}

{% api-method-parameter name="site" type="string" required=true %}
site name
{% endapi-method-parameter %}

{% api-method-parameter name="server" type="string" required=true %}
server name
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
An array with all todays entries.
{% endapi-method-response-example-description %}

```
{
 "server_name": "server_name",
 "name": "site_name",
 "pid": 127296,
 "version": null,
 "created_at": 1577980343733,
 "status": "online",
 "restart_time": 0,
 "unstable_restarts": 0,
 "uptime": "02 Jan 2018 16:52:23",
 "memory_use": 45,
 "cpu_use": 0,
 "time": "23:59:00",
 "date": "02-01-2020"
 }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="" path="/:server/:site/days/:days" %}
{% api-method-summary %}
Get days of data
{% endapi-method-summary %}

{% api-method-description %}
Retuns days worth of data
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="Days" type="number" required=true %}
the number of days of data you want to get
{% endapi-method-parameter %}

{% api-method-parameter name="Site" type="string" required=true %}
Site name
{% endapi-method-parameter %}

{% api-method-parameter name="Server" type="string" required=true %}
server name
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
This endpoint return data worth the selected amount of days
{% endapi-method-response-example-description %}

```
[
   {
    "server_name": "server_name",
    "name": "site_name",
    "pid": 127296,
    "version": null,
    "created_at": 1577980343733,
    "status": "online",
    "restart_time": 0,
    "unstable_restarts": 0,
    "uptime": "02 Jan 2018 16:52:23",
    "memory_use": 45,
    "cpu_use": 0,
    "time": "23:59:00",
    "date": "02-01-2020"
  },
  {
    "server_name": "server_name",
    "name": "site_name",
    "pid": 127296,
    "version": null,
    "created_at": 1577980343733,
    "status": "online",
    "restart_time": 0,
    "unstable_restarts": 0,
    "uptime": "02 Jan 2018 16:52:23",
    "memory_use": 45,
    "cpu_use": 0,
    "time": "23:59:00",
    "date": "02-01-2020"
  }
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="" path="/:server/:site/uptime" %}
{% api-method-summary %}
Get site uptime
{% endapi-method-summary %}

{% api-method-description %}
get the uptime and downtime of the server
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="/uptime" type="string" required=true %}
command for uptime
{% endapi-method-parameter %}

{% api-method-parameter name="site" type="string" required=true %}
site name
{% endapi-method-parameter %}

{% api-method-parameter name="server" type="string" required=true %}
server name
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Return the uptime and downtime form a site in %
{% endapi-method-response-example-description %}

```
[
  {
    "uptime": 99.9702469503124,
    "downtime": 0.029753049687599287
  }
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="" path="" %}
{% api-method-summary %}
Recent errors
{% endapi-method-summary %}

{% api-method-description %}
This endpoint will return the most recent errors, the last errors received by the server. Currently this end point is used to trigger the error / server down screen.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="/recent-error" type="string" required=false %}
Return the recent errors
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
empty state for no errors
{% endapi-method-response-example-description %}

```
[

]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="http://localhost:3333/api" path="/no\_server\_name/pm2-slack/hours/7-1-2020/10-12" %}
{% api-method-summary %}
Get time frame
{% endapi-method-summary %}

{% api-method-description %}
This endpoint will get you a time frame of the selected date
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" %}
ID of the cake to get, for free of course.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentication token to track down who is emptying our stocks.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="recipe" type="string" %}
The API will do its best to find a cake matching the provided recipe.
{% endapi-method-parameter %}

{% api-method-parameter name="gluten" type="boolean" %}
Whether the cake should be gluten-free or not.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{    "name": "Cake's name",    "recipe": "Cake's recipe name",    "cake": "Binary cake"}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```
{    "message": "Ain't no cake like that."}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



{% api-method method="get" host="" path="/:server/:site/:logs" %}
{% api-method-summary %}
Get site logs
{% endapi-method-summary %}

{% api-method-description %}
The logs are a whole day of collected data, you can also request the errors this way
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="logs" type="string" required=true %}
log-1-1-2019 this format is requested 
{% endapi-method-parameter %}

{% api-method-parameter name="Site" type="string" required=true %}
site name
{% endapi-method-parameter %}

{% api-method-parameter name="Server" type="string" required=true %}
server name
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
 "server_name": "server_name",
 "name": "site_name",
 "pid": 127296,
 "version": null,
 "created_at": 1577980343733,
 "status": "online",
 "restart_time": 0,
 "unstable_restarts": 0,
 "uptime": "02 Jan 2018 16:52:23",
 "memory_use": 45,
 "cpu_use": 0,
 "time": "23:59:00",
 "date": "02-01-2020"
 }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="delete" host="" path="/delete" %}
{% api-method-summary %}
Delete recent errors
{% endapi-method-summary %}

{% api-method-description %}
This method will overwrite the recentErrors file, removing all the recent errors
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="/delete" type="string" required=false %}
Delete
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
Recent has been deleted
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=302 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
The file doesnt exist
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

