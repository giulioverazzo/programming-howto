Prima cosa verificare come si chiama il servizio del
database andando a guardare il service configuration file  

`cat /etc/service | grep 5432`

Da qui vediamo che il servizio di systemd si chiama 'postgresql'.
Quindi lanciamo:

`service postgresql status` 

per avere lo stato del db.

Possiamo anche usare netstat

`sudo netstat -tulpn | grep 5432`