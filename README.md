# OpenUnison Basic Identity Platform

This project is a starting point for anyone looking to build an identity platform with OpenUnison.  It includes:

1. ScaleJS - UI for requesting access to applications and approving access
2. OpenUnison - Core system
3. Reports - For MySQL, can be adapted
4. LDAP Authentication to Active Directory

This baseline can be updated for any other solution that OpenUnison supports.  This deployment assumes you have:

1. Way to run OpenUnison as a container
2. MySQL / MariaDB available (SQL Server, PostrgeSQL and Oracle are also supported)
3. SMTP for notifications


## Parameters

*Detailed Description of Non-Secret Properties*

| Property | Description |
| -------- | ----------- |
| OU_HOST  | The host name for OpenUnison.  This is what user's will put into their browser to login to Kubernetes |
| OU_HIBERNATE_DIALECT | Hibernate dialect for accessing the database.  Unless customizing for a different database do not change |
| OU_QUARTZ_DIALECT | Dialect used by the Quartz Scheduler.  Unless customizing for a different database do not change  |
| OU_JDBC_DRIVER | JDBC driver for accessing the database.  Unless customizing for a different database do not change |
| OU_JDBC_URL | The URL for accessing the database |
| OU_JDBC_USER | The user for accessing the database |
| OU_JDBC_VALIDATION | A query for validating database connections/ Unless customizing for a different database do not change |
| SMTP_HOST | Host for an email server to send notifications |
| SMTP_PORT | Port for an email server to send notifications |
| SMTP_USER | Username for accessing the SMTP server (may be blank) |
| SMTP_FROM | The email address that messages from OpenUnison are addressed from |
| SMTP_TLS | true or false, depending if SMTP should use start tls |
| SESSION_INACTIVITY_TIMEOUT_SECONDS | The number of seconds of inactivity before the session is terminated, also the length of the refresh token's session |
| MYVD_CONFIG_PATH | The path to the MyVD configuration file, unless being customized, use `WEB-INF/myvd.conf` |


*Detailed Description of Secret Properties*

| Property | Description |
| -------- | ----------- |
| unisonKeystorePassword | The password for OpenUnison's keystore |
| SMTP_PASSWORD | Password for accessing the SMTP server (may be blank) |
| OU_JDBC_PASSWORD | The password for accessing the database |

