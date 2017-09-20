# Pasos básicos.

## Para hacer una sola vez por repositorio

Hacer fork del repositorio a traducir, por ejemplo
"https://github.com/Carpentries-ES/shell-novice", como Carpentries-ES, tiene que
ser desde una cuenta de github que forma parte de esta "organización".

El flujo más usado es que cada usuario haga un fork desde su cuenta personal y
después solicita "pull request" a un repositorio central cada vez que quiere
realizar un cambio. Pero en este caso queremos simplificar el proceso para la
traducción y para el uso de transifex.Tendremos que hacer pull-request para
llevar la traducción al repositorio central de Software Carpentry.

Se clona el mismo repositorio en el sistema local, y se instala el cliente de
transifex en el sistema local siguiendo estas instrucciones
https://docs.transifex.com/client/installing-the-client, luego ejecutar:

```
$ git clone https://github.com/Carpentries-ES/shell-novice.git
$ cd shell-novice/
$ tx init
```

Pienso que la idea es crear una estructura que interfiera lo menos posible con
los archivos de la version original. Los archivos a traducir son los ´*.md´,
archivos de texto en formato markdown que se encuentran en la carpeta
´_episodes´ de cada repositorio. Propongo que las traducciones se pongan en una
carpeta aparte ´_episodes_<lang>´ en nuestro caso ´_episodes_es´ donde se
colocarán las traducciones con los mismos nombres de archivo. Recomiendo
mantener los mismos nombres de archivo para facilitar el seguimiento y para
evitar problemas con la codificación.

Creé un proyecto en transifex dentro del grupo "Carpentries ES" y dentro de este
el proyecto "shell-novice-es". No son los mejores nombres si se traduce para
otros idiomas pero recién me estoy dando cuenta ahora, se puede cambiar a
futuro.

Para lograr esto he configurado la traducción de la siguiente manera:

```
$ tx set --auto-local -r shell-novice-es.01-intro-md '_episodes_<lang>/01-intro.md' --source-lang en --type GITHUBMARKDOWN --source-file _episodes/01-intro.md --execute
$ tx set --auto-local -r shell-novice-es.02-filedir-md '_episodes_<lang>/02-filedir.md' --source-lang en --type GITHUBMARKDOWN --source-file _episodes/02-filedir.md --execute
$ tx set --auto-local -r shell-novice-es.03-create-md '_episodes_<lang>/03-create.md' --source-lang en --type GITHUBMARKDOWN --source-file _episodes/03-create.md --execute
$ tx set --auto-local -r shell-novice-es.04-pipefilter-md '_episodes_<lang>/04-pipefilter.md' --source-lang en --type GITHUBMARKDOWN --source-file _episodes/04-pipefilter.md --execute
$ tx set --auto-local -r shell-novice-es.05-loop-md '_episodes_<lang>/05-loop.md' --source-lang en --type GITHUBMARKDOWN --source-file _episodes/05-loop.md --execute
$ tx set --auto-local -r shell-novice-es.06-script-md '_episodes_<lang>/06-script.md' --source-lang en --type GITHUBMARKDOWN --source-file _episodes/06-script.md --execute
$ tx set --auto-local -r shell-novice-es.07-find-md '_episodes_<lang>/07-find.md' --source-lang en --type GITHUBMARKDOWN --source-file _episodes/07-find.md --execute
```

Básicamente lo que hacen esos comandos es establecer que los archivos del idioma
fuente "en" (por inglés) se encuentran en la carpeta "_episodes" y son de
formato Github markdown, y la versión traducida quedará en la carpeta
"_episodes_<lang>", el código que devuelve <lang> depende de la configuración
que hagamos en el proyecto de transifex, allí he seleccionado "es" que define al
español genérico (cosa que sabemos no existe, pero no vamos a hacer una
traducción para cada país, ¿verdad? :-D).

Y luego el comando

```
$ tx push -st
```

Sube los archivos de fuente (s por source) y de la traducción (t) a transifex.

## Tarea de traducción

Una vez hecho esto, lo que hay que hacer es incluir a los colaboradores en
https://www.transifex.com/carpentries-es/shell-novice-es/dashboard/ Una vez allí
se puede traducir los archivos desde la interfaz web de transifex que considero
bastante intuitiva y amigable. Para esto cada quien debe recibir una invitación
a colaborar y crear una cuenta en transifex.

La mayoría de los colaboradores solamente tienen que acceder a transifex y
empezar a traducir que es el trabajo más tedioso.

Para llevar los cambios al repositorio de github lo único que hay que hacer es
ejecutar 

```
$ tx pull -a
```

Para traer la versión actual de los archivos traducidos al repositorio local.

```
$ git add <archivo> # O git add -A si quiero añadir todos los archivos modificados
$ git commit -m <mensaje>
$ git push
```

Para añadirlos al stage del repositorio, registrar los cambios y subirlo al
repositorio.

El manejo del repositorio desde la línea de comandos es recomandable que lo
hagan pocas personas para evitar conflictos. Incluso lo deseable es
automatizarlo a futuro cuando hayamos madurado el flujo de trabajo y la
interacción del equipo. También desde la línea de comandos se pueden actualizar
los archivos originales a traducir desde el repositorio original de Software
Carpentry, esto se puede realizar con una periodicidad definida, cada mes por
ejemplo, pero esos son acuerdos a los que debemos llegar entre todos.





