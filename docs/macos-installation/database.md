# Database

As you may know, Guidewire Software applications use the H2 database. Here is a best practice, which may eliminate corrupt local database instances due to mismanagement.

## Multiple Workspaces/Products

The default database location is ```/tmp/guidewire``` but this can cause issues when using multiple product instances. In other words, ```Suite-SB/PolicyCenter``` and ```PolicyCenter``` will reference the same database unless the database configuration is modified. For each local workspace or product, modify the ```database-config.xml``` JDBC URL for your local environment etnry. 

For example, given PolicyCenter is stored here:

```/Users/username/Guidewire/Suite/PolicyCenter/```

Change the ```jdbc-url``` node in database-config.xml:

### Option 1

Change the entire path to an explicit and unique path:

```jdbc-url="jdbc:h2:file:/Users/username/Guidewire/Suite/PolicyCenter/modules/db/pc;CACHE_SIZE=32000"```

### Option 2

Change the database name to a unique name:

```jdbc-url="jdbc:h2:file:/tmp/guidewire/pc1002;CACHE_SIZE=32000"```


## Microsoft SQL

While H2 is perfectly acceptable with local development environments, there are cases where configuration requires a Microsoft SQL instance. (Shame on you for coding things this way. :smirk:) 

For those on macOS needing local access to SQL Server, consider using [Microsoft SQL Server on Linux for Docker](https://hub.docker.com/_/microsoft-mssql-server). 

A future guide will address setup and configuration.