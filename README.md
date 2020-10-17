# git

## Comandos Gits


Establece una configuracion basica para el usuario.

```bash
git config --global user.name "joseph"
git config --global user.email jossjack@hotmail.com
```

Este comando se usa para crear un nuevo repertorio GIT.

```bash
git init
```

Este comando puede ser utilizado para agregar archivos al index. Se puede utilizar expresiones regulares basicas.

```bash
git add .
git add --all
git add -A
git add <archivo>
git add *.txt
git add directorio/*.<extension>
git add directorio/
```

Cargar en el HEAD los cambios realizados. Ten en cuenta que cualquier cambio comprometido no afectara al repertorio remoto.

```bash
git commit -m "Texto que identifique por que se hizo el commit"
```

Agregar y Cargar en el HEAD los cambios realizados. Ten en cuenta que cualquier cambio comprometido no afectara al repertorio remoto.

```bash
git commit -a -m "Texto que identifique por que se hizo el commit"
```

Agregar al ultimo commit, este no se muestra como un nuevo commit en los logs. Se puede especificar un nuevo mensaje.

```bash
git commit --amend -m "Texto que identifique por que se hizo el commit"
```

Este comando muestra la lista de los archivos que se han cambiado junto con los archivos que están por ser añadidos o comprometidos.

```bash
git status
```

Para añadir la dirección de un repositorio remoto a origin.

```bash
git remote add origin <url>
git remote set-url origin <url>
git remote rm <name/origin>
git remote -v
git remote show origin
git remote prune origin 
git remote add bitbucket <url repositorio>
git push -u bitbucket -all
```

Tras hacer commit de cambios nuevos, podemos subirlos al repositorio remoto.

```bash
git push origin master
git push origin --delete <branchName> 
```

Clonamos el repositorio de github o bitbucket.

```bash
git clone git://servidor/ruta/a/los/archivos 
git clone https://github.com/proyectogithub
```

Para poder fusionar todos los cambios que se han hecho de manera remota con el repositorio local.

```bash
git pull
```

Muestra los logs de los commits.

```bash
git log
git log --oneline --decorate --all --graph
```

Para visualizar una lista de todos los conflictos presentes.

```bash
git diff
git diff --staged
git diff --base <file-name>
git diff <source-branch> <target-branch>
```

Para poder fusionar todos los cambios que se han hecho de manera remota con el repositorio local.

```bash
git reset HEAD <archivo>
git reset --soft <commit_sha>
git reset --hard <commit_sha>
git reset --soft HEAD^
git reset --hard HEAD^
```

Crear un branch en el repositorio local.

```bash
git branch <nameBranch>
git branch
git branch -v 
git branch --merged
git branch --no-merged
git branch -d <nameBranch>
git branch -D <nameBranch>
```

Crear y Listar Tags.

```bash
git tag
git tag -a <verison> -m "esta es la versión x"
```

Los rebase se usan cuando trabajamos con branches esto hace que los branches se pongan al día con el master sin afectar al mismo.

```bash
git rebase
git rebase --continue 
git rebase --skip
git rebase --abort
git rebase <nameBranch>
```

Quita del HEAD un archivo y le pone el estado de no trabajado.

```bash
git checkout -- <file>
```

Crea un branch en base a uno online.

```bash
git checkout -b newlocalbranchname origin/branch-name
```

Busca los cambios nuevos y actualiza el repositorio.

```bash
git pull origin <nameBranch>
```

Cambiar de branch.

```bash
git checkout <nombre-rama>
git checkout -b <nombre-rama> 
```

Une el branch actual con el especificado.

```bash
git merge <nameBranch>
```

Este comando le permite al usuario buscar todos los objetos de un repositorio remoto que actualmente no reside en el directorio local que está trabajando.

```bash
git fetch
```

Borrar un archivo del repositorio.

```bash
git rm <file> 
git rm -f <file>
git rm .
```



Descargar remote de un fork.

```bash
git remote add upstream <url>
```

Merge con master de un fork.

```bash
git fetch upstream
git merge upstream/master
```

Ayuda a salvar cambios que no están por ser comprometidos inmediatamente, pero temporalmente.

```bash
git stash
```

Se usa para mostrar información sobre cualquier objeto git.

```bash
git show
```

Crear alias.

```bash
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.st status
```

Renombrar un archivo desde git.

```bash
git mv <file> <renamed_file>
```

En segundo plano, git crea un log de a donde han estado referenciando HEAD y el resto de ramas en los últimos meses.

```bash
git reflog
```

Enviar la salida por mail al propietario del proyecto, para constribuir con otros proyectos.

```bash
git request-pull origin/master myFork 
```
