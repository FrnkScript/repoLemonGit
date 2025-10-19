# 🧭 Guía de uso de Git y GitHub

Este documento detalla los pasos realizados para crear, confirmar (commit) y subir (push)
cambios desde un repositorio local a GitHub, así como la creación y manejo de ramas.

---

## 👉 1. Creo un repositorio local:

### 🧩 Creo una carpeta con el nombre del repositorio: $ mkdir lemoncodeGit

### 🧩 Entro en el repositorio: $ cd lemoncodeGit

### 🧩 inicializo git con: $ git init

## 👉 2. Creo un repositorio en mi cuenta de GitHub:

### 🧩 Creo un repositorio en GitHub y copio mi clave ssh.

        ⚪ (el repositorio es privado y no incluye readme.md ni .gitignore).

### 🧩 En la terminal de git GitBash de VS Code conecto mi repositorio remoto:

        ⚪ ` $ git remote add origin git@github.com:FrnkScript/repoLemonGit.git `

### 🧩 Confirmo que se estableció bien la conexión con: git remote -v

        ```
        $ git remote -v
        origin  git@github.com:FrnkScript/repoLemonGit.git (fetch)
        origin  git@github.com:FrnkScript/repoLemonGit.git (push)
        ```

## 👉 3. Hacer un commit y un push:

### 🧩 Creo un archivo en mi repositorio local con: $ touch primerArchivo.txt

### 🧩 Verifico con: ⚪ $ ls ⚪ que en mi repositorio se encuentra el archivo creado.

### 🧩 Añado el archivo al staging con: `git add primerArchivo.txt`

### 🧩 Utilizo: ⚪ $ git status ⚪ para verificar que se encuentra en el área de staging:

        ```
        $ git status
        On branch master

        No commits yet

        Changes to be committed:
          (use "git rm --cached <file>..." to unstage)
                new file:   primerArchivo.txt
        ```

### 🧩 Realizo un commit:

        ⚪ ` $ git commit -m "Primer commit: de primerArchivo.txt" `

### 🧩 Verifico que el commit se haya realizado con éxito:

        ```
        $ git status
        On branch master
        nothing to commit, working tree clean
        ```

### 🧩 Subo los cambios realizados en mi repositorio local a GitHub: git push -u origin master

### 🧩 Compruebo que se ha subido al repositorio remoto desde la terminal de Git Bash:

        ⚪ ` $ git log origin/master `

## 👉 4. Creo una rama en mi repositorio local:

### 🧩 Creo una rama con: ⚪ $git switch -c development ⚪

        ```
        $ git switch -c development
        Switched to a new branch 'development'
        ```

### 🧩 Verifico que la rama ha sido creada:

        ```
        $ git branch
        * development
          master
        ```

### 🧩 Cambiarme a la rama "development":

        ⚪ Como ya he cambiado a la nueva rama utilizando $ git switch no hace falta utilizar:
        ⚪ ` $ git checkout development `

### 🧩 Realizo algunos cambios en el archivo:

        ⚪ He añadido la información de los pasos que he realizado hasta el momento en el archivo "primerArchivo.txt"

### 🧩 Hago un commit de primerArchivo.txt en la rama "development":

        ⚪ ` $ git commit -m "añado documentacion de los pasos del proyecto hasta el punto 4" `

### 🧩 Comprueba que se haya hecho bien el commit: $ git status

### 🧩 Subo los cambios a mi cuenta de GitHub: $ git push --set-upstream origin development

        ⚪ En GitHub me pide que haga un "Compare & Pull Request" en mi repositorio remoto.
        ⚪ Dejo el mismo comentario y hago clic en "Create pull Request"

## 👉 5. Hacer un merge:

### 🧩 Vuelvo a mi rama principal de mi repositorio local:

        ⚪ ` $ git switch master `

### 🧩 Actualizo mi repositorio remoto con mi local con:

        ⚪ ` $ git pull origin master `

        ⚪ Y me informa de que está todo correcto:
        ```
        From github.com:FrnkS..../repoLemonGit
        * branch            master     -> FETCH_HEAD
        Already up to date.
        ```

### 🧩 Realizo un ⏩ git merge development

        ```
        $ git merge development
        Updating 58g3522..fc55791
        Fast-forward
        primerArchivo.txt | 74 +++++++++++++++++++++++++++++++++++++++++++++++++++++++
        1 file changed, 74 insertions(+)
        ```

### 🧩 Como no hay conflictos, hago un "git push -u origin master":

        ⚪ Me muestra un mensaje de que todo ha ido bien.
          ` branch 'master' set up to track 'origin/master'. `

## 🍪🍵

📘 Autor: Fran
📅 Fecha: [19/10/2025]
💻 Proyecto: Práctica de Git y GitHub.

🏁🏁🏁🏁🏁🏁🏁🏁🏁🏁🏁🏁🏁🏁 THE END 🏁🏁🏁🏁🏁🏁🏁🏁🏁🏁🏁🏁🏁🏁🏁🏁🏁🏁🏁🏁
