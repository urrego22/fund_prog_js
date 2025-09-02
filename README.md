// creacion de repositorio local, sirve para inicializar el repositorio vacio de git
git init 

//Se prepara para decirle a git que quiere guardar el proximo commit
git add .

//guada una evidencia de los archivos en el repositorio local
git commit -m "cracion de archivo index.js"

//creacion y manejo de ramas, c rea una rama llamada develop a partir de la rama actual que en este caso es master
git branch develop

//cambia de la rama master a la rama develop para trabajar en ella 
git checkout develop

//cambia a la rama feacture/operadores-calcula-propina despues de ser creada esta sirve para desarrollar una funcionalidad especifica sin afectar el codigo develop ni master
git checkout feacture/operadores-calcula-propina

// eliminamos una rama la de faature/operadores-calcula-propina ya que tenia un erro de escritura sirve para evitar confusiones
git branch -d faature/operadores-calcula-propina

//cambiamos a la rama master y fusionamos los cambios de develop dentro de master esto quiere decir que el codigo de devlop pasa a ser parte de master
git checkout master
git merge develop

//vinculo mi repositorio local con el repositorio remoto en github
git remote add origin https://github.com/urrego22/fund_prog_js.git

//muestra que direcciones remotas estan configuradas
git remote -v

//subimos todas las ramas locales al repositorio remoto
git push --all https://github.com/urrego22/fund_prog_js.git

//retos enfrentados
Errores en el nombre lo que me genero confusio y fue necesario eliminar y volver a crear de manera correcto.
Confusion inicial entre la rama master y develop al principio no tenia claro el flujo en el cual trabajaban.
El primer contacto con github remoto entender como conctar en el repositorio local con un remoto.

//aprendizaje clave
Comprension del flujo de ramas git aprendi la diferencia entre ramas principales master,develop y ramas funcionales feature y como cada una se usa en el desarrollo.
Dominio en el uso del merge comprendi como fusionar ramas correctamente evitando duplicar cambios.
