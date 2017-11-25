Practica 1 Git-GitHub
=====================

- ¿Qué comando utilizaste en el paso 11? ¿Por qué?
    git reset --hard HEAD~1

    Porque al haber realizado solo un commit estamos un paso por delante y por tanto solo tenemos que retroceder uno paso opcion --hard ya que queremos descartar los cambios realizados.
    
- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
    git reflog
    git reset --hard SHA

    Siendo el SHA el que encontramos donde hicimos la modificacion de la rama styled e igual que en el paso anterior con --hard para conservar los cambios.
    
- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
    git branch styled (este no es necesario pero para estar en la rama)
    git merge master

    No existe ningun conficto ya que styled esta por encima de master y tiene todos los cambios de esta.
    
- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
    git merge --no-ff styled

    Si causa conflictos porque la rama htmlify no puede acceder a la rama styled y se han modificado lineas iguales en ambos ficheros.
    
- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
    git checkout master
    git merge --no-ff styled

    No causa confictos pues los cambios que tiene styled son incorporados al fichero que estaba en master
    
- ¿Qué comando o comandos utilizaste en el paso 25?
    git log  --graph

- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
    git merge --no-ff title

    Si. Podria ser fast forwart pero no dejamos un commit por si quisieramos recuperar el cambio, ademas no tenemos ningun tipo de conflicto ya que hemos aladido un titulo que es incorporado al archivo
    
- ¿Qué comando o comandos utilizaste en el paso 27?
    git reset HEAD~1

- ¿Qué comando o comandos utilizaste en el paso 28?
    git checkout -- git-nuestro.md

- ¿Qué comando o comandos utilizaste en el paso 29?
    git branch -D tittle

- ¿Qué comando o comandos utilizaste en el paso 30?
    git reflog
    git reset --hard SHA

    Siendo SHA el HASH que localizamos con reflog donde estaba realizado el merge tittle
    En este caso sale: 241dfaa (master) HEAD@{6}: merge tittle: Merge made by the 'recursive' strategy.
    
- ¿Qué comando o comandos usaste en el paso 32?
    git reflog
    git checkout 01328a0

    Lo que nos da entre otras cosas: 01328a0 (HEAD) Create file git-nuestro
    
- ¿Qué comando o comandos usaste en el punto 33?
    git reflog
    git checkout eeacbdd

    Lo que nos da entre otras cosas: eeacbdd HEAD@{5}: commit: Modify file git-nuestro add a tittle

