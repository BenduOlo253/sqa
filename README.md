Para configurar sus entornos
Tener instalado python
Si no lo tienen descargarlo de aqui: https://www.python.org/downloads/

Verificar la instalacion
Abrir una terminal (PowerShell o CMD) y ejecutar: python --version
Tiene q aparecer algo asi: Python 3.12.4

Si no sirve usar este comando 
py --version

OJO si les sirvio usar el py en vez de python, usenlo de aqui en delante en todos los comandos
--------------------------------------------------------------------------------------------------------------------------------------
Paso 1:
Para instalar las dependencias del proyecto
Ir a la carpeta del proyecto
en mi caso es: C:\Users\riaga\Documents\proyectoCalidad\repoCalidad\proyectoSQA
Paso 2:
Crear el entorno virtual: python -m venv venv
Paso 3:
Activar el entorno virtual
Comando para que de permiso
En Windows con PowerShell: Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
despues de ejecutar ese comando activamos el entorno con este comando: venv\Scripts\activate
para saber si se activo, tiene q salir algo q diga (venv) en color verde, la terminal se veria asi
(venv) PS C:\Users\riaga\Documents\proyectoCalidad\repoCalidad\proyectoSQA>
Paso4:
Instalar dependencias
Usar este comando: pip install -r requirements.txt
si pip no les funciona usar: python -m pip install -r requirements.txt
esperamos a q se descarguen 
Paso 5:
Verificar la instalacion: python -m django --version
tiene que mostrar algo asi: 5.0.6
------------------------------------------------------------------------------------------------------------------------------------------

Para correr o levantar el server
tenemos q tener activado el entorno
lo activamos estando dentro de la carpeta de proyectoSQA: venv\Scripts\activate
OJO, si les da error usar este primero: Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass y despues el anterior

para migrar la tablas sql se usa el comando: python manage.py migrate
por ultimo para levantar o correr el server se usa este comando: python manage.py runserver
