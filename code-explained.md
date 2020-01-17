---
description: First draft
---

# Code explained

### Write / log / read

This is the write function it needs a path, file and res\(data\) this function will write to any place aslong it has a path when the servers/site doesn't exist it will create the required servers/sites.

```text
if (fs.existsSync(pathToFile) && JSON.parse(fs.readFileSync(pathToFile, 'utf8').length > 0))
```

If the servers /site exists and isn't empty it will update the data in the file array else it will make the array and push the data in it.

```text
function write (res, path, file) {
  let updatedData = []
  let pathToFile = path + file
  // Load older and update with new data
  if (fs.existsSync(pathToFile) && JSON.parse(fs.readFileSync(pathToFile, 'utf8').length > 0)) {
    let loadedFile = JSON.parse(fs.readFileSync(pathToFile, 'utf8'))
    loadedFile.forEach(item => {
      updatedData.push(item)
    })
    updatedData.push(res)
  }
  else {
    updatedData.push(res)
  }
  // Check if DIR / File bestaat zo niet maar het aan.
  fs.ensureDir(path)
    .then(() => {
      fs.writeFile(pathToFile, JSON.stringify(updatedData), (err) => {
        if (err) throw err
      })
    })
    .catch(err => {
      console.error(err)
    })
}
```

### Get servers / sites / endpoints

**Get servers functions**

This function get all the severs in the dataset servers can contain multiple sites.

```text
async function getServers () {
  const servers = []
  fs.readdirSync(path).forEach(dir => {
    if (fs.lstatSync(`${path}/${dir}`).isDirectory()) {
      servers.push(dir)
    }
  })
  return servers
}
```

**Get site function**

This function awaits the all the servers, after the servers are loaded it will read al the servers an get all the sites from them.

```text
async function getSites () {
  const sites = []
  const servers = await getServers()

  servers.forEach(server => {
    fs.readdirSync(`${path}/${server}`).forEach(site => {
      if (fs.lstatSync(`${path}/${server}/${site}`).isDirectory()) {
        sites.push(site)
      }
    })
  })
  return sites
}
```

**Get end points**

This function gets the servers and the sites, foreach it will make a new object will with the new endpoint data. This is the way to get the api and site endpoints with these you can access the site.

{% tabs %}
{% tab title="Code" %}
```text
async function getEndpoints () {
  const getEndpoints = []
  const servers = await getServers()

  servers.forEach(server => {
    const serverObject = {
      id: ids.next(),
      name: server,
      sites: [],
      error: false,
    }

    if ((`${server}`.includes('error') || `${server}`.includes('no_server'))) {
      console.error('server', server)
    }

    else {
      fs.readdirSync(`${path}/${server}`).forEach(site => {
        if (fs.lstatSync(`${path}/${server}/${site}`).isDirectory()) {
          serverObject.sites.push({
            id: ids.next(),
            name: site,
            endpoint: `/${server}/${site}`,
            error: false,
          })
        }
      })
      getEndpoints.push(serverObject)

    }

  })
  return getEndpoints
}
```
{% endtab %}

{% tab title="Response" %}
```text
  [
    {
      "id": "ayp6ukwrbzybvj2bowli0y94w",
      "name": "delnl",
      "sites": [
        {
          "id": "amtsl5w6ovtr2m4t33ux3b9w1",
          "name": "del-invite-dev",
          "endpoint": "/delnl/del-invite-dev",
          "error": false
        },
        {
          "id": "4dajni30m088g5xlxfg5kw3z6",
          "name": "del-invite-prod",
          "endpoint": "/delnl/del-invite-prod",
          "error": false
        },
        {
          "id": "0m4hb3n0hu55o751o58va8sh3",
          "name": "del-invite-staging",
          "endpoint": "/delnl/del-invite-staging",
          "error": false
        }
      ],
      "error": false
    }
  ]
```
{% endtab %}
{% endtabs %}



