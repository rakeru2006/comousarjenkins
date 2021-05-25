# comousarjenkins

# Jenkins es un software de integracion cntunua (CI)

Gracias a el podemos  automatizar tareas cuando se sube nuevo código a github o también se puede utilizar para desplegar las aplicaciones.

En un repositorio compartido con varios programadores es muy util esta herramienta de integración continua para mantaner la integridad en el código.

Ejemplos de otros sistemas de integracion 

**    Travis CI
**   Codeship
**    Circle CI

#  Deploying Jenkins in public cloud

Descargar de la pagina https://jenkins.io/download/




    1. Installing Jenkins LTS on macOS. (mas estable)

    2. Installing Jenkins Weekly on macOS (mas actual pero puede contener bugs)




# Prerrequisitos

Requisitos mínimos de hardware:

256 MB de RAM

1 GB de espacio en disco (aunque 10 GB es un mínimo recomendado si se ejecuta Jenkins como contenedor de Docker)

Configuración de hardware recomendada para un equipo pequeño:

4 GB + de RAM

50 GB + de espacio en disco


Requisitos de Software:

Java: consulte la página de requisitos de Java

Navegador web: consulte la página de compatibilidad del navegador web

Para el sistema operativo Windows : Política de soporte de Windows

# Ejecute el archivo WAR

El archivo ARchive (WAR) de la aplicación web Jenkins se puede iniciar desde la línea de comandos de esta manera:

Descargue el último archivo WAR estable de Jenkins en un directorio apropiado en su máquina.

Abra una ventana de terminal / símbolo del sistema en el directorio de descarga.

Ejecute el comando java -jar jenkins.war.

Busque http://localhost:8080y espere hasta que aparezca la página Desbloquear Jenkins .

Continúe con el asistente de configuración posterior a la instalación a continuación.

Notas:

A diferencia de descargar y ejecutar Jenkins con Blue Ocean en Docker ( arriba ), este proceso no instala automáticamente las funciones de Blue Ocean, que deberían instalarse por separado a través de la página Administrar Jenkins > Administrar complementos en Jenkins. Lea más sobre los detalles para instalar Blue Ocean en la página Comenzando con Blue Ocean .

Puede cambiar el puerto especificando la --httpPortopción cuando ejecuta el java -jar jenkins.warcomando. Por ejemplo, para que Jenkins sea accesible a través del puerto 9090, ejecute Jenkins con el comando:
java -jar jenkins.war --httpPort=9090

Asistente de configuración posterior a la instalación
Después de descargar, instalar y ejecutar Jenkins mediante uno de los procedimientos anteriores, comienza el asistente de configuración posterior a la instalación.

Este asistente de configuración lo lleva a través de algunos pasos rápidos "únicos" para desbloquear Jenkins, personalizarlo con complementos y crear el primer usuario administrador a través del cual puede continuar accediendo a Jenkins.

Desbloqueo de Jenkins
Cuando accede por primera vez a una nueva instancia de Jenkins, se le solicita que la desbloquee con una contraseña generada automáticamente.

Busque http://localhost:8080(o el puerto que configuró para Jenkins al instalarlo) y espere hasta que aparezca la página Desbloquear Jenkins .

Desbloquear la página de Jenkins

Desde la salida del registro de la consola de Jenkins, copie la contraseña alfanumérica generada automáticamente (entre los 2 conjuntos de asteriscos).

Copiando la contraseña de administrador inicial
Nota:

El comando: sudo cat /var/lib/jenkins/secrets/initialAdminPasswordimprimirá la contraseña en la consola.

Si está ejecutando Jenkins en Docker con la jenkins/jenkinsimagen oficial , puede usarla sudo docker exec ${CONTAINER_ID or CONTAINER_NAME} cat /var/jenkins_home/secrets/initialAdminPasswordpara imprimir la contraseña en la consola sin tener que ejecutar la ejecución en el contenedor.

En la página Desbloquear Jenkins , pegue esta contraseña en el campo Contraseña de administrador y haga clic en Continuar .
Notas:

Siempre puede acceder al registro de la consola de Jenkins desde los registros de Docker ( arriba ).

El registro de la consola de Jenkins indica la ubicación (en el directorio de inicio de Jenkins) donde también se puede obtener esta contraseña. Esta contraseña debe ingresarse en el asistente de configuración en las nuevas instalaciones de Jenkins antes de poder acceder a la interfaz de usuario principal de Jenkins. Esta contraseña también sirve como la contraseña predeterminada de la cuenta del administrador (con el nombre de usuario "admin") si omite el siguiente paso de creación de usuario en el asistente de configuración.

Personalizar Jenkins con complementos
Después de desbloquear Jenkins , aparece la página Personalizar Jenkins . Aquí puede instalar cualquier cantidad de complementos útiles como parte de su configuración inicial.

Haga clic en una de las dos opciones que se muestran:

Instalar complementos sugeridos : para instalar el conjunto de complementos recomendados, que se basan en los casos de uso más comunes.

Seleccionar complementos para instalar : para elegir qué conjunto de complementos instalar inicialmente. Cuando accede por primera vez a la página de selección de complementos, los complementos sugeridos se seleccionan de forma predeterminada.

Si no está seguro de qué complementos necesita, elija Instalar complementos sugeridos . Puede instalar (o eliminar) complementos adicionales de Jenkins en un momento posterior a través de la página Administrar Jenkins > Administrar complementos en Jenkins.
El asistente de configuración muestra la progresión de la configuración de Jenkins y la instalación de su conjunto elegido de complementos de Jenkins. Este proceso puede tardar unos minutos.

Creando el primer usuario administrador
Finalmente, después de personalizar Jenkins con complementos , Jenkins le pide que cree su primer usuario administrador.

Cuando aparezca la página Crear primer usuario administrador , especifique los detalles de su usuario administrador en los campos respectivos y haga clic en Guardar y finalizar .

Cuando aparezca la página Jenkins está listo , haga clic en Comenzar a usar Jenkins .
Notas:

¡Esta página puede indicar que Jenkins está casi listo! en su lugar, y si es así, haga clic en Reiniciar .

Si la página no se actualiza automáticamente después de un minuto, use su navegador web para actualizar la página manualmente.

Si es necesario, inicie sesión en Jenkins con las credenciales del usuario que acaba de crear y estará listo para comenzar a usar Jenkins.

⇐ macOS


