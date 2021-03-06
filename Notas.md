## :heavy_check_mark: Lista de comandos utiles en Git Bash  :ok_hand:


#### Ctrl + L : 
    Limpia la pantalla de la consola

#### pwd:
    Muestra el directorio actual
    
#### ls :
    Muestra la lista de archivos y carpetas que se encuentran en el directorio actual
    -l > Los muestra en forma de lista
    -a > Muestra todos los archivos incluidos los ocultos
    -al > muestra en lista y tambien los ocultos

#### cd {ruta} :
    Te mueve a la ruta que especifiques

#### history :
    Muestra el historial de comandos puestos en la consola con un id.

#### !{id}: 
    Ejecuta el comando con el id especificado del historial de la consola.

#### alias {nombre_alias}="{comandos}"
    Te permite crear un alias para un comando que desées

## Comandos de Git:

###### **git init :**
    Inicializa el repositorio en el directorio actual.

###### **git status :**
    Verifica el estatus de los archivos del repositorio y muestra si hay algun cambio.

###### git log:
    Muestra el log de commits del repositorio.
    --all > Muestra todos los commits de la historia del repositorio
    --graph > Agrega una grafica que muestra tambien las ramas
    --oneline > pone toda informacion en una sola linea


###### git add {archivo} o git add . :
    Pone el track en los archivos del repositorio para que se empiecen a seguir los cambios en el staged del repositorio.

###### git commit :
    Guarda los cambios en el repositorio local, antes de usar este comando se debe de ejecutar el git add . o git add {archivo}
    -m "{mensaje}" > le pone un texto al commit 
    -am "{mensaje}" > guarda los cambios sin tener que mandar llamar el add, pero solo lo hace sobre los archivos que se encuentra trackeados en el repositorio.
    --amend sirve para sobreescribir el ultimo commando con los cambios actuales.

###### git branch :
    Muestra todas las ramas del repositorio.

###### git branch {rama}:
    Crea la rama especificada.    

###### git branch -D {rama}
    Borra la rama especificada.

###### git diff:
    Muestra todos los cambios del repositorio en el commit actual y el anterior

###### git diff {id_commit_comparar_1}  {id_commit_comparar_2} :
    Muestra las diferencias en el archivo entre los dos commits especificados.

###### git checkout {rama}:
    Mueve el tracking del repositorio actual a la rama seleccionada
    ## ¡importante! ## si creas una nueva rama y no has guardado los cambios en el repositorio actual, estos se perderan al moverse de rama

###### git merge {rama} :
    Mezcla en la rama actual, la rama especificada.

###### git stash
    Regresa los cambios de la rama a la ultima version y guarda los cambios que tenias en memoria

###### git stash pop
    Regresa los cambios de memoria al archivo

###### git stash list
    Muestra una lista de los cambios que se han stasheado.

###### git clean --dry-run
    Muestra una simulacion de los archivos que se van a eliminar del repositorio si no estan trackeados.

###### git clean -f
    Elimina los archivos no trackeados del directorio.


###### git cherry-pick {id_branch}    
    Se trae los cambios hechos en una rama vieja a la rama actual.

###### git reflog
    Muestra la verdad de las cosas, nada se le escapa al ojo de git, estas en problemas y lo sabes

###### git reset --hard {id_commit}
    Regresa todo el repositorio al estado en que se encontraba en ese commit.

###### git grep "{palabra_buscar}"
    Te regresa los archivos donde se encuentre la palabra que buscas
    > -n : obtiene la linea donde se encuentra la palabra
    > -c : cuenta las apariciones de la palabra

###### git -log -S "{palabra_buscar}"
    Busca en el historial de commits la palabra a buscar.

## GITHUB

##### git clone {url_repositorio} :
    Clona el repositorio remoto en el equipo local.

##### git remote add {nombre_que_quiera_estandar_origin} {url_repositorio} :
    Añade el repositorio remoto a donde se enviaran los commits.

##### git remote set-url {nombre_origin} {nueva_url_repositorio} :
    Modifica la url del repositorio remoto.

##### git fetch :
    descarga los cambios hechos en la rama master del servidor remoto, pero no los aplica.

##### git merge:
    aplica los cambios en la rama master del servidor remoto. 

##### git pull {origin_o_nombre_remoto} {rama} :
    hace fetch y merge de los cambios que se encuentran en el servidor remoto de la rama especificada al repositorio y rama local.
    !Usar de preferencia este y siempre hacer un pull antes de llamar a un push!

    ## Nota ## si tienes un repositorio previamente creado y lo quieres enlazar al repositorio de github, es necesario añadir un commando extra --allow-unrelated-histories
    para que te permita fusionar el repositorio remoto con el repositorio local.

##### git push {origin_o_nombre_remoto} {rama} :
    Envia las modificaciones hechas en el repositorio local al servidor remoto y la rama especificada.


# Configurar el SSH en github

## Primer paso: 

Generar tus llaves SSH. Recuerda que es muy buena idea proteger tu llave privada con una contraseña.

`ssh-keygen -t rsa -b 4096 -C "tu@email.com"`

## Segundo paso: 

Terminar de configurar nuestro sistema.

En Windows y Linux:

__Encender el "servidor" de llaves SSH de tu computadora__ :

`eval $(ssh-agent -s)`

__Añadir tu llave SSH a este "servidor"__ :

`ssh-add ruta-donde-guardaste-tu-llave-privada`


#Editor.md
para crear un increible readme como este usar [este poderoso editor](https://pandao.github.io/editor.md/en.html "este")
