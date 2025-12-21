# proj.contactApp

## fix MongoDB Port in use

```bash
softeng@nixxin:.../proj.contactApp   main [✶?] via  v22.21.1
✦ ❯  sudo netstat -tulnp | grep 27017
tcp        0      0 127.0.0.1:27017         0.0.0.0:*               LISTEN      57103/mongod

softeng@nixxin:.../proj.contactApp   main [✶?] via  v22.21.1
✦ ❯  sudo kill 57103

softeng@nixxin:.../proj.contactApp   main [✶?] via  v22.21.1
✦ ❯  sudo netstat -tulnp | grep 27017

mkdir -p ./mongodb-data
# Run The database
mongod --dbpath ./mongodb-data --port 27017 --unixSocketPrefix ./mongodb-socket
```
