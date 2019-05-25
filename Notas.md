## Lista de comandos utiles en Git Bash ## 

Ctrl + L : 
    Limpia la pantalla de la consola

pwd:
    Muestra el directorio actual
    
ls :
    Muestra la lista de archivos y carpetas que se encuentran en el directorio actual
    -l > Los muestra en forma de lista
    -a > Muestra todos los archivos incluidos los ocultos
    -al > muestra en lista y tambien los ocultos

cd {ruta} :
    Te mueve a la ruta que especifiques



## Comandos de Git ##:

git init :
    Inicializa el repositorio en el directorio actual.

git status :
    Verifica el estatus de los archivos del repositorio y muestra si hay algun cambio.

git add {archivo} o git add . :
    Pone el track en los archivos del repositorio para que se empiecen a seguir los cambios en el staged del repositorio.

git commit :
    Guarda los cambios en el repositorio local, antes de usar este comando se debe de ejecutar el git add . o git add {archivo}
    -m "{mensaje}" > le pone un texto al commit 
    -am "{mensaje}" > guarda los cambios sin tener que mandar llamar el add, pero solo lo hace sobre los archivos que se encuentra trackeados en el repositorio.

git checkout :
    Muestra todas las ramas del repositorio.

git checkout {rama}:
    Crea una rama o mueve el tracking del repositorio actual a la rama seleccionada
    ## ¡importante! ## si creas una nueva rama y no has guardado los cambios en el repositorio actual, estos se perderan al moverse de rama




