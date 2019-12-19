loggarsi con utente `postgres`    
entrare in un database (`psql nome_database`)  
comando `create user nome_utente`  
cambiare owner `ALTER DATABASE nome_database OWNER TO nome_utente`  
dare i permessi all'utente con `grant all on DATABASE nome_database to nome_utente`  
e `grant all on all tables in schema public to nome_utente`  
modificare il file `sudo nano /etc/postgresql/11/main/pg_hba.conf` alla riga  
```
# "local" is for Unix domain socket connections only
local   all             all                                     peer
```
cambia peer con md5  

per loggarsi come un utente su un database: `psql -U nome_utente -d nome_database`
