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
**Install pgAdmin**

**Setup the public key for the repository (if not done previously):**
```bash
curl -fsS https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo gpg --dearmor -o /usr/share/keyrings/packages-pgadmin-org.gpg
```

**Create the repository configuration file:**
```bash
sudo sh -c 'echo "deb [signed-by=/usr/share/keyrings/packages-pgadmin-org.gpg] https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list && apt update'
```

**For both desktop and web modes**
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
