# utiles
Cajón de sastre de comandos útiles para ubuntu / centos


# Uso del sistema
1. htop
2. ps aux | sort -nrk 3,3 | head -n 20 #listado con los 20 procesos que más cpu han usado recientemente
3. iostat -y 5
4. nload eth0

# Poner color por defecto a vim

# Crear backup BBDD en cron con bajo coste computacional y aprovechando recursos

```
nice -n 10 ionice -c2 -n 7 mysqldump -h localhost -u <usuario_bbd> -p<pass> --default-character-set=utf8 --ignore-table=logs --ignore-table=backoffice_logs --ignore-table=email_queue <nombre_bbdd> | pigz -6 > /var<path>/export_bbdd_pro_$(date +"%Y-%m-%d_%Hh").sql.gz
```

# Comprimir imágenes de un servidor de manera recursiva con jpegoptimizer. 

```
find . -type f -name "*.jpg" -o -name "*.JPG" | xargs jpegoptim -f --size=30k --strip-all
```
