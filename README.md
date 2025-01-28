# Proyecto de Monitoreo en Docker

Este proyecto configura un sistema de monitoreo utilizando Zabbix, Nagios, Cacti, Prometheus y Grafana, todos ejecutándose en contenedores Docker.

## Herramientas Utilizadas

- **Zabbix**
- **Nagios**
- **Cacti**
- **Prometheus**
- **Grafana**

## Configuración

### Zabbix

1. Crear archivo `docker-compose.yml` en la carpeta `zabbix`:
   ```yaml
   version: '3.5'
   services:
     zabbix-server:
       image: zabbix/zabbix-server-pgsql:latest
       ports:
         - "10051:10051"
     zabbix-web:
       image: zabbix/zabbix-web-nginx-pgsql:latest
       ports:
         - "8080:8080"
