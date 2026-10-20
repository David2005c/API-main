## 1.Descripción de la aplicación: Qué hace el servicio y qué problema resuelve.**

En esta api puedes consultar que películas y series hay y los datos de cada una además de poder ordenarlas alfabéticamente, por año o por puntuación. Si interesa una película o serie en específico hay un buscador que te permite obtener todos los datos d euna película/serie con solo buscar el título.

## 2.URL pública: Enlace para acceder a la página web desplegada.**

Enlace de la API -> [CineAPI](https://cineapi-6mvq.onrender.com/)

## 3.Plataforma de despliegue: Indicar en qué plataforma se ha desplegado la aplicación.**

He usado _**Render**_ para desplegar la API

## 4.Descripción detallada del proceso de despliegue**

## Requisitos

-Requirements con las dependencias necesarias (fastapi y uvicorn)

-Estructura del proyecto:

![alt image](images/tree.png)

## Backend : app.py
```

```

## Enlace a static

```
<script src="/static/app.js" defer></script>
```

### Paso 1: Conectar Github a Render

Primero iniciamos sesión en Render y nos saldrá una pestaña en la que te va a pedir conectar Github (puedes usar Github o cualquira de las opciones que te ofrece Render) para obtener los archivos necesarios para desplegar la API, para ello clickamos en el icono de Github y una vez dentro se te envirá por un correo para verificar la conexión, lo introducimos y Render ya puede coger esos archivos.

### Paso 2: Configurar Render

Una vez esté conectado Github deberemos de configurar ciertos aspectos* de Render para el despliegue.
Hay que seleccionar el repositorio que se va a utilizar en _**Source**_  (usuario/API por ejemplo), en el apartado _**Build Command**_ deberemos de definir el comando para construir la API antes de lanzarla que será algo así  -**pip install -r requirements.txt**- (esto instala las dependencias necesarias), después en _**Start Comand**_ deberemos de definir el comando para arrancar la API y desplegarla, será algo así _**uvicorn app:app --host 0.0.0.0 --port $PORT**_ (susitituye app por el archivo python que tengas, si se llama apirest pues será  _**uvicorn apirest:app --host 0.0.0.0 --port $PORT**_).

_*Los aspectos mencionados son los más importantes para arrancar la API, lo demás es secundario (nombre de la api,...)_

### Paso 3: Arrancar la API

Una vez hemos configurado Render clickamos en _**'Apply Deploy'**_ y dejamos que Render lea los archivos y configure todos, si ha salido todo bien saltará un mensaje _**Build succesfull**_ y el enlace de la API que será algo así: **https://cineapi-6mvq.onrender.com/**
