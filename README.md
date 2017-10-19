# Strut2-CursoRapido
Curso Rápido de Struts2

Llamaremos al directorio del proyecto <dir_proyecto>.

1. Crear un programa en **Java**:
	1. **Instala el JDK de Java**: Ahora mismo (2017) está en http://www.oracle.com/technetwork/java/javase/downloads/index.html. Pero si no aparece busca "JDK download". Bájatelo e instálalo. Puedes comprobar que funciona ejecutando (en consola) el comando "java -version".
	2. **Escribe el programa**: Abre un editor de texto y escribe Programa.java en <dir_proyecto>.
	3. **Compila el programa**: Desde <dir_proyecto> ejecuta el comando: "javac Programa.java". Como resultado aparecerá Programa.class.
	4. **Ejecuta el programa**: Desde <dir_proyecto> ejecuta el comando: "java Programa". Debe aparecer el mensaje *"Hola Mundo"*.
	
2. Instalar el **Servidor de Aplicaciones**:
	1. **Instala Apache Tomcat**: Ahora mismo (2017) está en https://tomcat.apache.org/download-80.cgi. Pero si no aparece busca "Apache Tomcat download". Bájalo y descomprímelo en un directorio (que llamaremos <dir_tomcat>).
	2. **Arranca Apache Tomcat**: Desde el directorio <dir_tomcat>/bin ejecuta el comando "./startup.sh" (en Linux). Si usas Windows... piénsatelo. 
	3. **Comprueba Apache Tomcat**: Conéctate con tu navegador a la URL http://localhost:8080. Debe aparecer la página de inicio de Apache Tomcat.
	4. **Crea un Proyecto en Apache Tomcat**: Para ello, 
		1. En <dir_tomcat>/webapps crea un directorio con el nombre "EjemploHTML".
		2. Crea el fichero <dir_proyecto>/tomcat/webapps/EjemploHTML/index.html (tendrás que crear los directorios correspondientes). Haz una página HTML bonita :)
		4. Copia el directorio <dir_proyecto>/tomcat/webapps/EjemploHTML a <dir_tomcat>/webapps.
		5. Reinicia Apache Tomcat. Para ello, desde el directorio <dir_tomcat>/bin lanza los comandos ./shutdown.sh y ./startup.sh.
		6. Con el navegador, ve a la URL http://localhost:8080/EjemploHTML. Debes ver tu página index.html.
	
3. Crea un **Servlet**: 
	Vamos a crear un Servlet de Tomcat. La documentación técnica está en http://tomcat.apache.org.
	La documentación del Servlet de JavaEE está en http://docs.oracle.com/javaee/7/api/javax/servlet/http/HttpServlet.html.
	2. Crea el fichero <dir_proyecto>/src/EjemploServlet/ClaseServlet1.java (tendrás que crear los directorios correspondientes).
	3. Programa el Servlet...
	3. Compila <dir_proyecto>/src/EjemploServlet/ClaseServlet1.java, pero utiliza las librerías de Apache Tomcat. Para ello, desde <dir_proyecto>/src/EjemploServlet ejecuta el comando "javac -classpath <dir_tomcat>/lib/servlet-api.jar ClaseServlet1.java". Aparecerá ClaseServlet1.class.
	4. Crea el fichero <dir_proyecto>/src/EjemploServlet/web.xml.
	5. **Publica el Servlet**: Para ello, 
		1. Copia <dir_proyecto>/src/EjemploServlet/ClaseServlet1.java al directorio **<dir_tomcat>/webapps/EjemploServlet/WEB-INF/classes/**. Tendrás que crear los directorios intermedios.
		2. Crea el fichero <dir_proyecto>/src/EjemploServlet/web.xml y cópialo al directorio **<dir_tomcat>/webapps/EjemploServlet/WEB-INF/**.
		3. Reinicia Apache Tomcat. Para ello, desde el directorio <dir_tomcat>/bin lanza los comandos ./shutdown.sh y ./startup.sh.
		4. Comprueba el funcionamiento del Servlet navegando a la URL **http://localhost:8080/EjemploServlet/urlServlet1**. Debe aparecer el mensaje "¡Hola Mundo! - Soy un Servlet".
".
