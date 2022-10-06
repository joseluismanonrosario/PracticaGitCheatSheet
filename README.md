Comandos de GIT Básicos – Guía Completa
¿Necesitas aprender algunos comandos de GIT básicos? Has venido al lugar correcto. Sigue leyendo para descubrir nuestra práctica hoja de trucos que puedes utilizar como referencia diaria.

¡Empecemos!

Tabla de Contenidos	
Entendiendo cómo funciona GIT
Comandos de GIT básicos
Hoja de trucos de los comandos de GIT en .pdf

Entendiendo cómo funciona GIT
GIT es el SCV (sistema de control de versiones) de código abierto más utilizado que te permite rastrear los cambios realizados en los archivos. Las empresas y los programadores suelen utilizar el GIT para colaborar en el desarrollo de software y aplicaciones.

Un proyecto GIT consta de tres secciones principales: el directorio de trabajo, el área de preparación y el directorio git.

El directorio de trabajo es donde se agregan, borran y editan los archivos. Luego, los cambios son preparados (indexados) en el área de preparación. Después de que confirmes tus cambios, la instantánea de los cambios se guardará en el directorio git.

Todo el mundo puede usar GIT ya que está disponible para Linux, Windows, Mac y Solaris. El software puede tener una fuerte curva de aprendizaje, pero hay muchos tutoriales disponibles para ayudarte.

Comandos de GIT básicos
Aquí hay algunos comandos básicos de GIT que debes conocer:

git init creará un nuevo repositorio local GIT. El siguiente comando de Git creará un repositorio en el directorio actual:
git init
Como alternativa, puedes crear un repositorio dentro de un nuevo directorio especificando el nombre del proyecto:
git init [nombre del proyecto]
git clone se usa para copiar un repositorio. Si el repositorio está en un servidor remoto, usa:
git clone nombredeusuario@host:/path/to/repository
A la inversa, ejecuta el siguiente comando básico para copiar un repositorio local:
git clone /path/to/repository
git add se usa para agregar archivos al área de preparación. Por ejemplo, el siguiente comando de Git básico indexará el archivo temp.txt:
git add <temp.txt>
git commit creará una instantánea de los cambios y la guardará en el directorio git.
git commit –m “El mensaje que acompaña al commit va aquí”
Ten en cuenta que los cambios confirmados no llegarán al repositorio remoto.

git config puede ser usado para establecer una configuración específica de usuario, como el email, nombre de usuario y tipo de formato, etc. Por ejemplo, el siguiente comando se usa para establecer un email:
git config --global user.email tuemail@ejemplo.com
La opción -global le dice a GIT que vas a usar ese correo electrónico para todos los repositorios locales. Si quieres utilizar diferentes correos electrónicos para diferentes repositorios, usa el siguiente comando:
git config --local user.email tuemail@ejemplo.com
git status muestra la lista de los archivos que se han cambiado junto con los archivos que están por ser preparados o confirmados.
git status
git push se usa para enviar confirmaciones locales a la rama maestra del repositorio remoto. Aquí está la estructura básica del código:
git push  origin <master>
Reemplaza <master> con la rama en la que quieres enviar los cambios cuando no quieras enviarlos a la rama maestra.

git checkout crea ramas y te ayuda a navegar entre ellas. Por ejemplo, el siguiente comando crea una nueva y automáticamente se cambia a ella:
command git checkout -b <branch-name>
Para cambiar de una rama a otra, sólo usa:
git checkout <branch-name>
git remote te permite ver todos los repositorios remotos. El siguiente comando listará todas las conexiones junto con sus URLs:
git remote -v
Para conectar el repositorio local a un servidor remoto, usa este comando:
git remote add origin <host-or-remoteURL>
Por otro lado, el siguiente comando borrará una conexión a un repositorio remoto especificado:
git remote <nombre-del-repositorio>
git branch se usa para listar, crear o borrar ramas. Por ejemplo, si quieres listar todas las ramas presentes en el repositorio, el comando debería verse así:
git branch
Si quieres borrar una rama, usa:
 git branch -d <branch-name>
git pull fusiona todos los cambios que se han hecho en el repositorio remoto con el directorio de trabajo local.
git pull
git merge se usa para fusionar una rama con otra rama activa:
git merge <branch-name>
git diff se usa para hacer una lista de conflictos. Para poder ver conflictos con respecto al archivo base, usa:
git diff --base <file-name>
El siguiente comando se usa para ver los conflictos que hay entre ramas antes de fusionarlas:
git diff <source-branch> <target-branch>
Para ver una lista de todos los conflictos presentes usa:
git diff
git tag marca commits específicos. Los desarrolladores lo usan para marcar puntos de lanzamiento como v1.0 y v2.0.
git tag 1.1.0 <instert-commitID-here>
git log se usa para ver el historial del repositorio listando ciertos detalles de la confirmación. Al ejecutar el comando se obtiene una salida como ésta:
commit 15f4b6c44b3c8344caasdac9e4be13246e21sadw
Author: Alex Hunter <alexh@gmail.com>
Date:   Mon Oct 1 12:56:29 2016 -0600
git reset sirve para resetear el index y el directorio de trabajo al último estado de confirmación.
git reset - -hard HEAD
git rm se puede usar para remover archivos del index y del directorio de trabajo.
git rm filename.txt
git stash guardará momentáneamente los cambios que no están listos para ser confirmados. De esta manera, pudes volver al proyecto más tarde.
git stash
git show se usa para mostrar información sobre cualquier objeto git.
git show
git fetch le permite al usuario buscar todos los objetos de un repositorio remoto que actualmente no se encuentran en el directorio de trabajo local.
git fetch origin
git ls-tree te permite ver un objeto de árbol junto con el nombre y modo de cada ítem, y el valor blob de SHA-1. Si quieres ver el HEAD, usa:
git ls-tree HEAD
git cat-file se usa para ver la información de tipo y tamaño de un objeto del repositorio. Usa la opción -p junto con el valor SHA-1 del objeto para ver la información de un objeto específico, por ejemplo:
git cat-file –p d670460b4b4aece5915caf5c68d12f560a9fe3e4
git grep le permite al usuario buscar frases y palabras específicas en los árboles de confirmación, el directorio de trabajo y en el área de preparación. Para buscar por www.hostinger.com en todos los archivos, usa:
git grep “www.hostinger.com”
gitk muestra la interfaz gráfica para un repositorio local. Simplemente ejecuta:
gitk
git instaweb te permite explorar tu repositorio local en la interfaz GitWeb. Por ejemplo:
git instaweb –http=webrick
git gc limpiará archivos innecesarios y optimizará el repositorio local.
git gc
git archive le permite al usuario crear archivos zip o tar que contengan los constituyentes de un solo árbol de repositorio. Por ejemplo:
git archive - -format=tar master
git prune elimina los objetos que no tengan ningún apuntador entrante.
git prune
git fsck realiza una comprobación de integridad del sistema de archivos git e identifica cualquier objeto corrupto
git fsck
git rebase se usa para aplicar ciertos cambios de una rama en otra. Por ejemplo:
git rebase master
Hoja de trucos de los comandos de GIT en .pdf
Si estás empezando con GIT, puede ser difícil recordar incluso los comandos básicos. Por eso, hemos preparado una hoja de trucos de GIT para ayudarte a dominar el software. Guarda el archivo en tus dispositivos o imprímelo para tenerlo siempre listo cuando tengas que recordar los comandos de GIT.

Descargar (tamaño: 1.2 MB)

Conclusión
Aprender los comandos básicos de GIT será de gran ayuda para los desarrolladores, ya que pueden controlar fácilmente el código fuente de los proyectos. Puede que te lleve algo de tiempo recordarlos todos, por eso nuestra hoja de trucos de GIT podría resultarte útil.

¡Practica estos comandos de GIT y aprovecha al máximo tus habilidades en desarrollo! ¡Buena suerte!

Glosario de términos para trabajar con git/GitHub
repository
Un repositorio es el elemento más básico de GitHub. Es más fácil imaginarlos como carpetas de proyecto. Un repositorio contiene todos los archivos de un proyecto (incluyendo la documentación), y almacena el histórico de modificaciones de cada archivo. Los repositorios pueden tener múltiples colaboradores y pueden ser tanto públicos como privados.
commit
Un commit se puede entender como la confirmación de una modificación individual en un archivo (o serie de archivos). Es como cuando guardas un archivo, excepto que con Git, cada vez que haces commit se crea un ID único (también conocido como SHA o hash) que te permite registrar qué cambios se hicieron y quién los hizo. Los commits generalmente contienen un mensaje de commit que consiste en una breve descripción de los cambios realizados.
push
Literalmente, empujar. Se refiere a enviar tus cambios confirmados (tus commits) a un repositorio remoto, como por ejemplo un repositorio alojado en GitHub. Si cambias algo localmente, querrás hacer push de esos cambios para que los demás miembros de tu equipo puedan acceder a ellos.
pull
Literalmente, tirar. Se refiere a traer los cambios del servidor remoto y combinarlos con tu copia local. Por ejemplo, si alguien ha editado el archivo remoto en el que ambos estáis trabajando, querrás hacer pull de esos cambios a tu copia local para que esté actualizada.
issue
Los issues son sugerencias de mejora, tareas o cuestiones relacionadas con el repositorio o el proyecto. Cualquiera puede crear issues (en un repositorio público), y los moderan los colaboradores del repositorio. Cada issue contiene su propio foro de dissusión, y se puede etiquetar y asignar a un usuario.
pull request
Los pull requests o, literalmente, solicitudes de tirar, son cambios propuestos para un repositorio que un usuario ha enviado, y que pueden ser aceptados o rechazados por los colaboradores del repositorio. Igual que los issues, los pull requests tienen cada uno su propio foro de discusión.
branch
Un branch o, literalmente, rama, es una versión paralela de un repositorio. Está contenido dentro del repositorio, pero no afecta al branch principal o master, permitiéndote trabajar libremente sin estropear la versión “real”. Cuando has terminado de realizar los cambios que querías hacer, puedes hacer merge de tu branch al branch principal para publicar tus cambios.
merge
Literalmente, combinar. Hacer merge toma los cambios de un branch (en el mismo repositorio o también desde un fork), y los aplica en otro. Esto a menudo ocurre como un pull request (que se puede entender como una solicitud de hacer merge), o a través de la línea de comandos. Un merge puede realizarse automáticamente a través de un pull request en la interfaz web de GitHub siempre y cuando no haya cambios que generen conflictos, o puede hacerse siempre via línea de comandos.
remote
La versión remota es una versión de algo que está alojada en un servidor, muy probablemente GitHub en este contexto. Puede estar conectado a clones locales de forma que los cambios se sincronicen.
local
La versión local es la copia que tienes del repositorio en tu ordenador, sobre la que trabajas.
clone
Un clon es la copia de un repositorio que se aloja en tu ordenador, en lugar de en un servidor en alguna parte, o el acto de realizar esa copia. En tu clone puedes editar los archivos en tu editor preferido y utilizar Git para llevar un registro de esas modificaciones sin necesidad de tener conexión a internet. Sin embargo, este clon está conectado a la versión remota de forma que los cambios se puedan sincronizar entre ambos. Puedes hacer push de tus cambios locales a la versión remota para mantenerlas sincronizadas cuando estés online.
fork
Un fork o, literalmente, tenedor, es una copia personal de un repositorio de otro usuario que se aloja en tu cuenta. Los forks te permiten modificar libremente cualquier proyecto sin alterar el original. Los forks se mantienen relacionados con el original, de manera que puedes enviar un pull request al autor del repositorio original para que lo actualice con tus cambios. También puedes mantener tu fork actualizado haciendo pull de las modificaciones del original.

