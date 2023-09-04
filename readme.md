# Pasos para conectar git con github en windows

## Paso 1- instalar, verificar y configurar git:
<ul>
  <li>Verificar que este instalado git en el computador</li>
  <p>Desde inicio de Windows Buscar y abrir Git Bash</p>
  <p>Si en caso no tienes instalado git </p>
  <p>Descargar e instalar git en el siguiente enlace: <a href="https://git-scm.com/download/win">https://git-scm.com/download/win</a> y allí seleccionar el que dice <strong>64-bit Git for Windows Setup.</strong> </p>

  <p>Una vez descargado, tratar de ejecutar como administrador. Y luego los pasos de instalación es solo darle siguiente a todo por defecto hasta el final.</p>

  <li><h3>Configurar git</h3></li>
  <p>Para Insertar Nuestro Nombre de usuario:</p>

  ```bash
  git config --global user.name "tu nombre usuario"
  ```

  <p>Para Insertar Nuestro correo, el mismo correo que creaste o vas usar en github:</p>

  ```bash
  git config --global user.email "tucorreo@gmail.com"
  ```

  <p>Para Verificar que el correo y usuario esten correctos </p>

  ```bash
  git config --list
  ```

</ul>

## Paso 2 - Crearse la cuenta de github y activar las llaves:
<ul>
  
  <h3>Crearse la cuenta en el siguiente link: </h3> <a href="https://github.com/">https://github.com/</a> y allí recomendable crearse con una cuenta gmail personal y que este vigente, porque la verificación y activación le llegará al correo. Te llegará un código al correo que sera enviado desde github  al seguir todos los pasos para registrarse en github </p>


  <li><h3> Conectar git y github</h3></li>
  <h4>1. agregar correo: copiar y pegar el siguiente comando: 

  
  Pero  antes modificar el correo por tu correo. Una vez modificado solo es darle puro enter
  
  </h4>

  ```bash
  ssh-keygen -t ed25519 -C "tu_correo@example.com"
  ``` 
  <h4>2. generar llaves privada:  copiar y pegar el siguiente comando: 

  
  Solo es darle puro enter.
  
  </h4>
  
  ```bash
  eval "$(ssh-agent -s)"
  ``` 
  <h4>3. Agregar llave privada: copiar y pegar el siguiente comando: 

  
  Solo es darle puro enter.
  
  </h4>
  
  ```bash
  ssh-add ~/.ssh/id_ed25519
  ``` 
  <h4>4. copiar la llave generada: copiar y pegar el siguiente comando: 

  
  Solo es darle puro enter.
  
  </h4>
  
  ```bash
  clip < ~/.ssh/id_ed25519.pub
  ``` 
  Este último comando hace que tengas copiado las llave privada del computador, por tanto solo le vas a insertar en la caja de insertar llave desde github pegando la llave con la conbinacion de teclas <code> ctrl + v </code> 

  Luego seleccionas solo crear cuenta y si esta todo okey no deberia salir ningun error. 



  


  <h2>Link alternativo para documentarse</h2>

  <h3>La documentación de github para conectar con git local</h3> <a href="https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent?platform=windows">https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent?platform=windows</a></p>




</ul>

## Paso 3- subir repositorio de git a github:
<ul>
  <h4>Crear  o abrir una carpeta que tenga código, para versionar y luego subir el repositorio </h4>
  <p>La forma mas práctica de abrir la carpeta hacia el terminal es: Arrastrar la carpeta hacia la terminal Git Bash o simplemente abriendo desde github, y en github abrir la terminal pero la opción de gitbash.</p>

  <h3>1. Versionar primero  la carpeta con git </h3>
  <h4>Para inicializar git </h4>

  ```bash
  git init
  ```
  <h4>Para agregar todos los cambios con git </h4>

  ```bash
  git add .
  ```
  <h4>Para empaquetar o poner el nombre a la versión del proyecto </h4>

  ```bash
  git commit -m "mi primera versión"
  ```
  <h3>2. Crear repositorio nuevo desde la pagina de tu github </h3>
  <h4>Desde la parte superior seleccionar la opción del  simbolo "+" <code> > </code> "new repository" <code> > </code> se abrira una caja para que insertes el nombre de tu repositorio <code> > </code> presionar en el boton "create repository"<code> > </code> una vez creado nos saldra comandos para conectar nuestro repositorio remoto con la de nuestro computador   </h4>

  <p>La primera sección de comandos lleva el nombre en ingles <code> "…or create a new repository on the command line"  </code> y solo vamos a buscar el penultimo y el último comando de esta sección: </p>

  <strong>ejemplo del penultimo comando para insertar en la terminal</strong>, aquí quiza te pida autenticar le das enter y te mandará abrir el navegador para autenticarte rapido: 
  
  ```bash
  git remote add origin git@github.com:emersonxinay/tu_primer_repo.git
  ```

  ejemplo del último comando: 
  ```bash
  git push -u origin main
  ```
  Si en caso no es main, generalmente es: 
  ```bash
  git push -u origin master
  ```

  <h3> Listo, sí cargo todo okey, solo vas a ir al github a verificar solo refrescando la pagina y veras que tu código ahora debe estar en el repositorio virtual </h3>


  el main o master indica la rama, solo si en caso no sabes en que rama estas, verificar con el siguiente comando:

  ```bash
  git branch
  ```






</ul>

<h2> Sí quieres subir otro repositorio y tu configuración git esta correcto, solo repetir el paso 3 caso contrario si estas en un nuevo computador repetir todos los pasos pero oviando los que ya tienes listo. </h2>


