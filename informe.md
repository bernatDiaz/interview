Al crear el virtual environment me ha salido el siguiente error

 WARNING: Failed to write executable - trying to use .deleteme logic
ERROR: Could not install packages due to an OSError: [WinError 2] El sistema no puede encontrar el archivo especificado: 
'C:\\Python310\\Scripts\\virtualenv.exe' -> 'C:\\Python310\\Scripts\\virtualenv.exe.deleteme'

WARNING: You are using pip version 21.2.4; however, version 21.3.1 is available.
You should consider upgrading via the 'C:\Python310\python.exe -m pip install --upgrade pip' command.

He probado de actualizar python pero me ha salido el siguiente mensaje

ERROR: Could not install packages due to an OSError: [WinError 5] Acceso denegado: 'c:\\python310\\lib\\site-packages\\pip-21.2.4.dist-info\\entry_points.txt'
Consider using the `--user` option or check the permissions.

He abierto un nuevo terminal ejecutandolo como administrador y entonces me ha dejado actualizar python e instalar el entorno virtual.

Al instalar pycaret me han salido muchos errores.

He instalado anaconda y pycaret se ha instalado correctamente.

Al entrenar el modelo me ha dado el siguiente error

ValueError: Setting a random_state has no effect since shuffle is False. You should leave random_state to its default (None), or set shuffle=True.

Lo he solucionado añadiendo la opcion fold_shuffle=True.

El modelo ha inferido que todas las variables son categoricas.

Algunos valores de bmi eran "34,34" los he cambiado por 34.34
Los valores de la edad por ejemplo 18 los he cambiado por 18.0

Me ha saltado el siguiente error:

AttributeError: 'Simple_Imputer' object has no attribute 'fill_value_categorical'

Para solucionarlo he añadido la siguiente opcion  imputation_type='iterative'

Me ha saltado el siguiente error:

AttributeError: 'Make_Time_Features' object has no attribute 'list_of_features'

He buscado por internet y he encontrado que pycaret necesita la version 0.23.2 de scikit. Pero al intentar instalar esa version en anaconda me da un error de compatibilidad y no se instala.

He instalado python 3.8 en un entorno virtual y pycaret se ha instalado correctamente.

A la hora de subirlo a Heroku he tenido 2 problemas:

1, Heroku no encontraba el puerto. Lo he solucionado cambiando el host de la app a 0.0.0.0

2, No encontraba la carpeta Templates ni Styles. Lo he solucionado cambiando el nombre de las carpetas de Templates a templates y de Styles a styles.

