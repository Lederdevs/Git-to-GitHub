<h2>Git.</h2>
<div class="header">
  <img src="https://github.com/LederDev/Git-to-GitHub-/assets/162763730/d70f8677-8293-44ac-ae66-868640ae4fc2">
  <h1 align="left">¿Que es Git?</h1>
  <p align="left">Git es un sistema de control de versiones distribuido, lo que significa que un clon local del proyecto es 
   un repositorio de control de versiones completo.
    Estos repositorios locales plenamente funcionales permiten trabajar sin conexión o de forma remota con facilidad.
    Conforme los desarrolladores hacen cambios al proyecto, cualquier versión anterior de este puede recuperarse en cualquier momento.
    Los desarrolladores pueden revisar el historial de proyectos para averiguar:

  - ¿Qué cambios se hicieron?
  - ¿Quién los hizo?
  - ¿Por qué se necesitaban?
  </p>

  
 <div>
    <h2>Git tiene integridad</h2>
    <p>Todo en Git es verificado mediante una suma de comprobación (checksum en inglés) antes de ser 
    almacenado, y es identificado a partir de ese momento mediante dicha suma. Esto significa que es 
    imposible cambiar los contenidos de cualquier archivo o directorio sin que Git lo sepa.
    No puedes perder información durante su transmisión o sufrir corrupción de archivos sin que Git sea 
    capaz de detectarlo</p>
  </div>
<div>
   <h2>Los Tres Estados.</h2>
   <p>Git tiene tres estados principales en los que se pueden encontrar tus archivos: confirmado 
    (committed), modificado (modified), y preparado (staged).</p>
</div>
 
- Confirmado: <span>significa que los datos están almacenados de manera segura en tu base de datos local.</span>
- Modificado: significa que has modificado el archivo pero todavía no lo has confirmado a tu base de datos.
- Preparado: significa que has marcado un archivo modificado en su versión actual para que vaya en tu próxima confirmación.
   <p>
    Esto nos lleva a las tres secciones principales de un proyecto de Git: El directorio de Git (Git 
    directory), el directorio de trabajo (working directory), y el área de preparación (staging area).
    </p>
     <img src="https://github.com/LederDev/Git-to-GitHub-/assets/162763730/c1953063-6aab-4557-affc-238910383d46">

     <div>
       <h2> Directorio de trabajo, área de almacenamiento y el directorio Git.</h2>
       <p> El directorio de trabajo es una copia de una versión del proyecto. Estos archivos se sacan de la 
      base de datos comprimida en el directorio de Git, y se colocan en disco para que los puedas usar o 
      modificar.
       </p>
       <p>El flujo de trabajo básico en Git es algo así:</p>
  </div>
  
- Modificas una serie de archivos en tu directorio de trabajo.
- Preparas los archivos, añadiéndolos a tu área de preparación.
- Confirmas los cambios, lo que toma los archivos tal y como están en el área de preparación y almacena esa copia instantánea de manera permanente en tu directorio de Git.

  <div>
      <h2>La Línea de Comandos</h2>
    <span>
       Existen muchas formas de usar Git. Por un lado tenemos las herramientas originales de línea de comandos, y por 
      otro lado tenemos una gran variedad de interfaces de usuario con distintas capacidades.
      <p>En este guía vamos a utilizar Git desde la línea de comandos. 
      La línea de comandos es el único lugar en donde puedes ejecutar todos los comandos de Git - la mayoría de 
     interfaces gráficas de usuario solo implementan una parte de las características de Git por motivos de simplicidad.
  </p>
    </span>
  </div>
  <div>
    <h2>Instalación de Git</h2>
    <p>Para poder empezar a utilizar Git, tienes que instalarlo en tu computadora. Incluso si ya está instalado, este 
    es posiblemente un buen momento para actualizarlo a su última versión. Puedes instalarlo como un paquete, a partir 
    de un archivo instalador o bajando el código fuente y compilándolo tú mismo.</p>
  </div>
### Nota:
  <p>"Está guía fue realizada utilizando la versión 2.44.0. de Git. Aun cuando la mayoría de comandos que usaremos 
   deben funcionar en versiones más antiguas de Git (...) >>"</p>
<div>
  <h2>Instalación en Linux.</h2>
  <p>Sí deseas instalar Git en Linux a través de un instalador binario, en general puedes hacerlo mediante la 
  herramienta básica de administración de paquetes que trae tu distribución. Si estás en Fedora por ejemplo, puedes 
  usar yum:</p>

     $ yum install git
     
<p>Sí estás en una distribución basada en Debian como Ubuntu, puedes usar apt-get:</p>

     $ apt-get install git
<span>Para información adicionales, puedes visistar su página web de Git, donde puedes consultar mayor información
 http://git-scm.com/download/linux </span>
</div>
<div>
  <h2>Instalación en Mac</h2>
  <p>
    Hay varias maneras de instalar Git en un Mac. Probablemente la más sencilla es instalando las herramientas 
   Xcode 
  de Línea de Comandos. En Mavericks (10.9 o superior) puedes hacer esto desde el Terminal si intentas ejecutar git 
  por primera vez
  </p>
  <p>
    Si deseas una versión más actualizada, puedes hacerlo a partir de un instalador binario. Un instalador de Git 
   para OSX es mantenido en la página web de Git. Lo puedes descargar en http://git-scm.com/download/mac.
  </p>
  <img src="https://github.com/LederDev/Git-to-GitHub-/assets/162763730/f3d5c826-c561-4299-8af8-d5ea6aa2ae75">
</div>
<div>
  <h2>Instalación en Windows</h2>
  <p>
    Exíste  varias maneras de instalar Git en Windows. La forma más oficial está disponible para ser descargada 
   en el sitio web de Git. Solo tienes que visitar http://git-scm.com/download/win y la descarga empezará 
  automáticamente. Fíjate que éste es un proyecto conocido como Git para Windows (también llamado msysGit), el cual 
   es diferente de Git. Para más información acerca de este proyecto visita http://msysgit.github.io/.
  </p>
  <p>
    Otra forma de obtener Git fácilmente es mediante la instalación de GitHub para Windows. El instalador incluye 
   la versión de línea de comandos y la interfaz de usuario de Git. Además funciona bien con Powershell y establece 
   correctamente "caching" de credenciales y configuración CRLF adecuada. Puedes descargar este instalador del 
   sitio web de GitHub para Windows en http://windows.github.com.
  </p>
</div>
<h1>Inicio - Sobre el Control de Versiones - Configurando Git por primera véz.</h1>
<div>
    <h2>Configurando Git</h2>
    <p>
      Ahora que tienes Git en tu sistema, vas a querer hacer algunas cosas para personalizar tu entorno de Git. Es 
      necesario hacer estas cosas solamente una vez en tu computadora, y se mantendrán entre actualizaciones. 
     También 
    puedes cambiarlas en cualquier momento volviendo a ejecutar los comandos correspondientes.
    </p>
  </div>
  <h2>Tú Identidad en Git</h2>
  <p>
    Lo primero que deberás hacer cuando instales Git es establecer tu nombre de usuario y dirección de correo 
    electrónico. Esto es importante porque los "commits" de Git usan esta información, y es introducida de manera 
   inmutable en los commits que envías:
   Por ejemplo, 
  <h5>configurar el nombre de usuario:</h5>
  
     git config --global user.name "John Doe"   
  <h5>Configurar el usuario email:</5>
    
     git config --global user.email johndoe@example.com
  </p>
  <p>
  Sólo necesitas hacer esto una vez si especificas la opción --global, ya que Git siempre usará esta información 
  para todo lo que hagas en ese sistema.
  </p>
</div>
<div>
  <h2>Tu Editor</h2>
  <p>
    Ahora que tu identidad está configurada, puedes elegir el editor de texto por defecto que se utilizará cuando 
   Git necesite que introduzcas un mensaje. Si no indicas nada, Git usará el editor por defecto de tu sistema(...)>>
  </p>
</div>

### Comandos básicos de Git
<div>
  <p>
  Para utilizar Git, los desarrolladores utilizan comandos específicos para copiar, crear, cambiar y combinar el código. Estos comandos pueden ejecutarse 
 directamente desde la línea de comandos o utilizando una aplicación como GitHub Desktop. Aquí tienes algunos comandos comunes para utilizar Git:
</p>
  <h2>Inicializando un repositorio en un directorio.</h2>
 <p>Para iniciar aseguir un projecto existente en Git, debes ir al directorio del 
  proyecto y el usar el siguiente comando: </p>

       git init
<span> inicializa un repositorio nuevo de Git y comienza a supervisar el directorio existente. Este agrega una subcarpeta oculta dentro del directorio existente que hospeda la estructura de datos interna que se requiere para el control de versiones.</span>

- Observa la imagen:
  <img src="https://github.com/Lederdevs/Git-to-GitHub/assets/165498615/9ad1c16a-a57b-46a1-b655-b24311196986">
</div>
<div>
  <h2>Estado de tus Archivos.</h2>
  <span>
    Muestra las rutas de acceso que tienen diferencias entre el archivo de índice y el archivo HEAD actual, las rutas que tienen diferencias entre las y 
   el archivo de índice, y las rutas en el árbol de trabajo que no son rastreados por Git (y no son ignorados por gitignore[5]). 
  </span>

    git status
- Observa la imagen:
<img src="https://github.com/Lederdevs/Git-to-GitHub/assets/165498615/ee9ab3ef-d96f-4747-a500-e05c30e9cb30">
  <span>
    muestra el estado de los cambios como sin seguimiento, modificados o almacenados provisionalmente.
  </span>
</div>
<div>
    <h2>Rastrear Archivos Nuevos.</h2>
  <span>Este comando actualiza el índice utilizando el contenido actual que se encuentra en el árbol de trabajo, para preparar el contenido preparado para 
  la siguiente confirmación.</span>

  
    git add 'nombre del archivo'  
- Observa la imagen:
 <img src="https://github.com/LederDev/Git-to-GitHub-/assets/162763730/db0b241c-a921-420a-8a96-ce042310e6aa">
 <span>
 almacena provisionalmente un cambio. Git rastrea los cambios que se hacen a la base de código de un desarrollador, pero es necesario probarlos y tomar 
 una captura de pantalla de ellos para incluirla en el historial del proeycto.
 </span>
</div>

<div>
    <h2>Preparar Archivos Modificados</h2>
   <p>
    Vamos a cambiar un archivo que esté rastreado. Si cambias el archivo rastreado llamado “CONTRIBUTING.md” y luego ejecutas el 
    comando git status, verás algo parecido a esto:
  </p>
   <img src="https://github.com/LederDev/Git-to-GitHub-/assets/162763730/eab263de-c636-427c-ab2a-04784c9f5a73">
  <span>
    El archivo “CONTRIBUTING.md” aparece en una sección llamada “Changes not staged for commit” (“Cambios no preparado para 
   confirmar” en inglés) - lo que significa que existe un archivo rastreado que ha sido modificado en el directorio de trabajo pero 
   que aún no está preparado
  </span>
</div>
<div>
   <h2>Ratrear  todos los archivos del proyecto. </h2>
  <p>Para rastrear todos los archivos que contiene el portafolio a través de Git, puedes ejecutar lo siguiente:</p>

     git add .
- Observa la imagen:
  <img src="https://github.com/Lederdevs/Git-to-GitHub/assets/165498615/3d3d9380-85d6-45d3-915d-5c5dd61d8d7d">
 <p>Este comando podemos arastrar todos los archivos que contega  el directorio a traves de  git, al realizar un git status podemos confirmar que todos 
 nuestro archivos estan siendo restrado por git.</p>
- Observa la imagen:
 <img src="https://github.com/LederDev/Git-to-GitHub-/assets/162763730/d1a8acf7-9e54-4cac-9015-46757c09a61f">
</div>
<div>
   <h2>Estado Abreviado</h2>
  <span>
    Muestra las rutas de acceso que tienen diferencias entre el archivo de índice y el archivo HEAD actual, las rutas que tienen diferencias entre las y 
   el archivo de índice, y las rutas en el árbol de trabajo que no son rastreados por Git
  </span>

    git status -s
  
- Observa la imagen:
  <img src="https://github.com/LederDev/Git-to-GitHub-/assets/162763730/61871667-1fe6-44ad-bc23-73bb8dccd4f6">
<span>
  Es cierto que la salida de git status es bastante explícita, también es verdad que es muy extensa. Git ofrece una opción para 
   obtener un estado abreviado, de manera que puedas ver tus cambios de una forma más compacta. Si ejecutas git status -s o git status 
 --short, obtendrás una salida mucho más simplificada.
</span>
</div>

<div>
  <h2>Quitar archivo de restrar por git</h2>
  <p>
    Elimine los archivos que coincidan con pathspec del índice o del árbol de trabajo y el índice. no eliminará un archivo solo de su trabajo directorio. 
   (No hay opción para eliminar un archivo solo de la pantalla de trabajo árbol y, sin embargo, mantenerlo en el índice; úsalo si quieres hacer eso).
  </p>

     git rm --cache 'nombre del archivo'
  - Observa la imagen:
    <img src="https://github.com/LederDev/Git-to-GitHub-/assets/162763730/b300a3a5-c64c-42c1-bee8-7a1fbc90cd29">
<span>
Los archivos que se eliminan deben ser idénticos a la punta del y no se pueden almacenar provisionalmente actualizaciones de su contenido en el índice, aunque ese comportamiento predeterminado se puede anular con la opción.
</span>
</div>

<div>
    <h2>Confirmar tus Cambios</h2>
  <span>
    Cree una nueva confirmación que contenga el contenido actual del índice y El mensaje de registro dado que describe los cambios. La nueva confirmación 
 es un hijo directo de HEAD, generalmente la punta de la rama actual, y el se actualiza para que apunte a ella (a menos que no haya ninguna rama asociada 
 a 
 el árbol de trabajo, en cuyo caso HEAD está "separado"

      git commit -m 'El comentario como deseas guarda los cambios 'Mi primer commit en git''.
      
- Observa la imagen:
  <img src="https://github.com/LederDev/Git-to-GitHub-/assets/162763730/89c08fb2-7caf-4866-aa37-a2f646173d63">
<span>
guarda la instantánea del historial del proyecto y completa el proceso de seguimiento de los cambios. En resumen, una confirmación funciona tal como el tomar una fotografía. Todo lo que se haya almacenado provisionalmente con git add pasará a formar parte de la instantánea con git commit.
</span>
  </span>
</div>
<div>
    <h2>Confirmaciones de registro de usuarios.</h2>
    <p>Muestra los registros de confirmación realizado por el usuario, Enumere las confirmaciones a las que se puede acceder siguiendo 
    los enlaces de la carpeta confirmaciones dadas pero excluye las confirmaciones a las que se puede acceder de las confirmaciones dado con un ^ delante de ellos. </p>

     git log
- Observa la imagen:
  <img src="https://github.com/LederDev/Git-to-GitHub-/assets/162763730/12d70d0a-383d-43e3-926d-2e2380cbf502">
<span>
El comando git log muestra todas las commits en el historial del repositorio.
Por defecto, el comando muestra los datos de cada commit:

- Secure Hash Algorithm (SHA).
- Autor.
- Fecha.
- Mensaje del commit.

<span>
  Esto permite volver al historial del proyecto para ver quiénes son los autores, averiguar dónde se introdujeron los errores y 
    revertir los cambios problemáticos. Pero tener todo este historial no sirve de nada si no sabes cómo navegar por él. Ahí es donde 
   entra en juego el comando git log.

</span>
</span>
</div>
<div>
  <h2>Cambios en historia del registro.</h2>
  <span>
    Mostrar cambios entre el árbol de trabajo y el índice o un árbol, cambios entre el índice y un árbol, los cambios entre dos árboles, los cambios de 
   una combinación, cambia entre dos objetos blob o cambia entre dos archivos en el disco.
  </span>

     git diff 
- Observa la imagen:
<img src="https://github.com/LederDev/Git-to-GitHub-/assets/162763730/35d6cfbb-895a-4a15-b690-fefead15a540">
<span>
Enumera los cambios entre el directorio de trabajo actual y el área de preparación.
</span>
<p></p>(+) significa los cambios echos el archivo, que no hacido comiteado.</p>
<p>(-) significa los los cambios que se habian comiteado en archivo existente.</p>
</div>
<div>
  <h2>Eliminar cambios realizados en archivo</h2>
  <span>
    Actualiza los archivos del árbol de trabajo para que coincidan con la versión del índice o el árbol especificado.

        git chechout -- 'nombre del archivo'
  - Observa la imagen:
     <img src="https://github.com/LederDev/Git-to-GitHub-/assets/162763730/10e0c29e-7bde-4c75-987f-35200ed7030c">
  </span>
   <p>
    Actualiza los archivos del árbol de trabajo para que coincidan con la versión del índice o el árbol especificado. Si no se 
   proporcionó ninguna especificación de ruta, git checkout Actualice también para establecer la rama especificada como la actual rama
  </p>
</div>



<div>
  <h2>GitHub.</h2>
  <img src="https://github.com/LederDev/Git-to-GitHub-/assets/162763730/396e126a-89fa-4819-b97c-74f3f1440f02">
  <h2>Acerca de GitHub</h2>
<p>GitHub es una plataforma donde puedes almacenar, compartir y trabajar junto con otros usuarios para escribir código.
<p>Almacenar tu código en un "repositorio" en GitHub te permite:</p>
<p> 1. Presentar o compartir el trabajo.</p>
<p> 2. Seguir y administrar los cambios en el código a lo largo del tiempo.</p>
<p> 3. Dejar que otros usuarios revisen el código y realicen sugerencias para mejorarlo.</p>
<p> Colaborar en un proyecto compartido, sin preocuparse de que los cambios afectarán al trabajo de los colaboradores antes de que esté listo para integrarlos.</p>
  
El trabajo colaborativo, una de las características fundamentales de GitHub, es posible gracias al software de código abierto Git, en el que se basa GitHub.</p>
</div>
<div>
  <h2>¿Cómo funcionan Git y GitHub juntos?</h2>
  <p>
    Al cargar archivos en GitHub, los almacenas en un "repositorio de Git". Esto significa que al realizar cambios (o "compromisos") 
    en los archivos de GitHub, Git se iniciará automáticamente para realizar un seguimiento y administrar los cambios.
    <p>Hay muchas acciones relacionadas con Git que puedes completar en GitHub directamente en el navegador, como crear un 
    repositorio de Git, crear ramas y cargar y editar archivos. Sin embargo, la mayoría de las personas trabajan en sus archivos 
   localmente (en su propio ordenador), luego sincronizan continuamente estos cambios locales y todos los datos de Git relacionados, 
   con el repositorio central "remoto" en GitHub. Hay muchas herramientas que puedes usar para hacerlo, como GitHub Desktop.
    </p>
  </p>
</div>
<div>
  <h2>¿Dónde empiezo?</h2>
  <p>Para empezar a trabajar con GitHub, deberás crear una cuenta personal gratuita en GitHub.com y comprobar la dirección de correo 
  electrónico.Cada persona que utilice GitHub.com deberá iniciar sesión en una cuenta personal.</p>
  <h2>Registrarse para una cuenta personal nueva</h2>
  <p>1.Vaya a https://github.com/. </p>
  <p>2.Haga clic en Registrarse. </p>
  <p>3. Sigue las indicaciones para crear tu cuenta personal.</p>
  <p>
    Durante el registro, se te pedirá que verifiques tu dirección de correo electrónico. Sin una dirección de correo electrónico 
   verificada, no podrás completar algunas tareas básicas de GitHub, como crear un repositorio.
  </p>
</div>

<div>
  <h2>Cómo subir nuestro código, al respositorio de GitHub</h2>
 <h5>Primer paso:</h5>
</div>
<div>
  
   2. Escriba un nombre corto y fácil. Por ejemplo: "Encriptador de Texto".
  1. <span>En la esquina superior derecha de cualquier página, selecciona  y luego haz clic en Nuevo repositorio.</span>
  3. Opcionalmente, puede agregar una descripción del repositorio. Por ejemplo, "Mi primer repositorio en GitHub".
 4. Elige la visibilidad del repositorio. Para obtener más información, vea «Acerca de los repositorios».
 5. Seleccione Initialize this repository with a README (Inicializar este repositorio con un archivo Léame).
6. Haga clic en Create repository (Crear repositorio).
   
</div>

<div>
  <h1>Públicar mi primer proyecto en GitHub,</h1>
   <h5>Segundo paso:</h5>
   <p>
     La funcionalidad de las ramas de Git te permite crear nuevas ramas de un proyecto para probar ideas, aislar nuevas características, o experimentar 
     sin impactar al proyecto principal.
   </p>

     git git branch -M main 
- Observa la imagen:
  <img src="https://github.com/LederDev/Git-to-GitHub-/assets/162763730/f318799a-0a00-4bc9-9946-18e1eadacc30">
<span>
Fíjate en el carácter que precede a la rama: indica la rama que has desprotegido actualmente (es decir, la rama a la que apunta). Esto significa que si te comprometes en este punto, la rama avanzará con tu nuevo trabajo. Para ver la última confirmación en cada rama, puede ejecutar :*masterHEADmastergit branch -v
</span>
<h2>Adición de un repositorio remoto</h2>
<span>
  Para agregar un nuevo control remoto, use el comando en la terminal, en el directorio en el que está almacenado su repositorio.git remote add
  El comando toma dos argumentos:git remote add Un nombre remoto, por ejemplo, origin

       $ git remote add origin https://{% data variables.command_line.codeblock %}/OWNER/REPOSITORY.git

- Observa la imagen:
<img src="https://github.com/LederDev/Git-to-GitHub-/assets/162763730/7a243e54-327f-40e1-88d6-39e157e1a2aa">
<p>
  critico
</p>

<div>
  <span>
    Actualiza las referencias remotas mediante referencias locales, mientras se envían objetos necesario para completar las referencias dadas.
    Puedes hacer que sucedan cosas interesantes en un repositorio cada vez que empujas hacia él, colocando ganchos allí.

        git push -u  origin main 
  - Observa la imagen:
    <img src="https://github.com/LederDev/Git-to-GitHub-/assets/162763730/9ad32d73-1ee5-4b2e-bdc4-760cc2cf48ad">
<p>Al finalizar el cargue en la terminal, ingresa a tú GitHub y regarca la página y verás el cargue de tu proyecto en Github.</p>
  </span>
  <h2>proyecto públicado</h2>
  - Observa la imagen:
   <img src="https://github.com/LederDev/Git-to-GitHub-/assets/162763730/c4303a02-dcc5-443d-a84f-6d569275826a"
</div>
