# Boilerplate de Django-rest-frameword

1. Crear un entorno virtual : Después de instalar el módulo venv, puedes crear un entorno virtual. Navega hasta el directorio donde deseas crear el entorno virtual y ejecuta el siguiente comando:
```powershell
python -m venv myven
```

Este comando creará un nuevo directorio llamado myvenv (puedes cambiar el nombre si lo deseas) en tu directorio actual. Este directorio almacenará todos los paquetes Python que instales mientras el entorno virtual esté activo.

2. Activar el entorno virtual : Ahora, puedes activar tu entorno virtual usando el siguiente comando:
- En Windows:
```powershell
.\myvenv\Scripts\activate
```

- En Unix o MacOS:
```powershell
source myvenv/bin/activate
```

3. creamos `requirements.tx`  con todos los paquetes python que quieres instalary los instala con el siguiente comando:

```powershell
pip install -r requirements.txt
```

4. Una vez instalado los paquetes del proyecto, puedes crear un nuevo proyecto Django con el siguiente comando:

```powershell
django-admin.exe startproject core . 
```
Para verificar y crear servidor ejecuta el siguiente comando:
```powershell
python.exe manage.py runserver 
```

## Como Confligurar la variables de entorno en settings.py

Tenemos instalado el paquete django-environ que se encuentra en requirementes.txt.

1. en el archivo `settings.py` primero importamos la biblioteca `environ`:

```py
import environ
```

2. Necesitamos inicializar una instancia de `environ`:

```py
env = environ.Env()
environ.Env.read_env()
```

## Cors 

Para las cors instalamos la bibioteca  django-cors-headers y luego debes agregarlo a tu aplicacion en settings.py
```py
THIRD_PARTY_APP=[
  'corsheaders',
]
```

Además, necesitas agregar un middleware para CORS en el settings.py. Asegurate de que este delante del middleware `CommonMiddleware`