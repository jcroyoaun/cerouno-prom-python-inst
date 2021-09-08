# Instrucciones para Instrumentar una aplicación de Python para Prometheus

## Pre-requisitos
* Tener Python instalado (Python 3.8.10 de preferencia)
* Tener git instalado 
* Estar en alguna distribución de Linux (Ubuntu de preferencia)

## Pasos
* Clonamos este repo
`git clone https://github.com/jcroyoaun/cerouno-prom-python-inst`
* Corremos la app 
* * Ex.
`python3 app.py`
* Abrimos un navegador en localhost:8000

![image](https://user-images.githubusercontent.com/83674541/132585717-3c952bdb-0caf-4b58-9cb9-95166f755089.png)

* Instalamos prometheus_client en nuestra computadora :
`sudo apt install python3-pip`
`pip install prometheus_client` 

* (agregar el siguiente codigo en la linea #2) - Importar start_http_server de prometheus client 
`from prometheus_client import start_http_server`

* (agregar el siguiente codigo en la linea #17) - 
`start_http_server(METRICS_PORT)`

* (agregar el siguiente codigo en la linea #5)
`METRICS_PORT = 8001`
