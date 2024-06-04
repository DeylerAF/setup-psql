# How to set up PostgreSQL

> [!TIP]
>Instructions to set up PostgreSQL on your machine

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
