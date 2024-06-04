# How to set up PostgreSQL

> [!TIP]
>Instructions to set up PostgreSQL and pgAdmin on your machine

## Linux
**Install PostgreSQL**

```bash
sudo apt install postgresql postgresql-contrib
```

**Ensure that the PostgreSQL server is running:**

```bash
sudo systemctl start postgresql.service
```

**Access PostgreSQL:**

```bash
sudo -u postgres psql
```

**Change PostgreSQL password:**

```bash
alter user postgres with password 'changeme';
```
**Install pgAdmin for both desktop and web modes**

```bash
sudo apt install pgadmin4
```

**Install for desktop mode only:**
```bash
sudo apt install pgadmin4-desktop
```

**Install for web mode only:**
```bash
sudo apt install pgadmin4-web 
```

**Configure the webserver, if you installed pgadmin4-web:**
```bash
sudo /usr/pgadmin4/bin/setup-web.sh
```
