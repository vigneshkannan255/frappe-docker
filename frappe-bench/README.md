## Frappe bench

### After login in to frappe docker intitae frappe-bench using below command

```
▶ bench init --skip-redis-config-generation frappe-bench
▶ cd frappe-bench/
```
### Configuration

```
▶ bench set-config -g db_host mariadb
▶ bench set-config -g redis_cache redis://redis-cache:6379
▶ bench set-config -g redis_queue redis://redis-queue:6379
▶ bench set-config -g redis_socketio redis://redis-socketio:6379
```

```
▶ sed -i '/redis/d' ./Procfile
```

### Site Creation with DB and admin Credential

```
▶ bench new-site frappe.site.domain --mariadb-root-password <db_password> --admin-password <admin_password> --no-mariadb-socket --db-name <db_name>
```
### Site Creation

`This command will ask the DB and admin password`

```
▶ bench new-site edu.sagasoft.io
```
