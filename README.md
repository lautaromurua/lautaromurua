#  Concursos GCBA 

[ https://concursosgcaba.buenosaires.gob.ar](https://concursosgcaba.buenosaires.gob.ar)

Concursos orientados a generar oportunidades para el ingreso a GCABA y el crecimiento de los empleados de planta permanente,.

## Tecnologías
   
| Backend               |Frontend                                                  
|----------------       |-------------------------- |
|node +v9               | react +v16           		|                
|express  +v4           | react-dom +v16       		|            
|knex +v0.15            | webpack +v3.12  			|
|objection +v1.5        | style-loader +v0.16		|
|morgan +v1.9           | postcss-loader +v2.1		|
|helmet +v3             | formik +v1.5                                                         
|passport +v0.4.0       |                                                            
|passport-local v1.0.0  |                                                  
|pg +v7.0               |                                        
|redis +v2.8            |
|snyk +v2.1             |

# Instalación

## Pre-requisitos

#### Requerido

* Tener instalado **Node.js v9.0** o superior.
* Tener instalado **Npm**

#### Opcional

* Instalar **Postgres** (opcional en caso de que se quiera correr la base de datos local).
* instalar **Redis** (opcional, para manejar las sesiones localmente. Se puede correr el proyecto utilizando postgres localmente y no tener instalado redis, el portal se va a conectar con redis cuando le especifiquemos en la variable de entorno donde se tiene que conectar.)

## Correr el proyecto en modo local

* Clonar el repo.
* Ir por consola a la raíz del proyecto.
* Crear el fichero **.env**
	* Crear las variables de entorno y agregar los valores respectivos.
* Correr el comando **npm install**
* Correr el comando **npm run dev**
* Abrir otra consola en la raíz del proyecto y correr el comando **npm run devfe**


# Scripts disponibles

* dev
	> **npm run dev** corre el servidor  en modo desarrollo. Toma como referencia el objeto de conexion a la base de datos postgres **development**.
	
* devlocal
	 > **npm run devlocal** corre el servidor en modo desarrollo. Toma como referencia el objeto de conexion a la base de datos postgres **local**.

* devfe
	 > **npm run devfe** llama a webpack en modo desarrollo para que empaquete los módulos escepecificados en su configuracion y quede en modo monitor escuchando. 
	 
* start  
	 > **npm run start** corre los binarios ya minificados, empaquetados y transpilados. Se utiliza para correr el portal en producción.
	 
* build
   >**npm run build** corre dos scripts: primero corre **buildbe** y luego **buildfe**   

* buildbe
	>**npm run buildbe** llama a webpack en modo producction para que minifique y empaquete los assests del portal.

* buildfe
  > **npm run buildfe** llama a babel para que transpile todo codigo y lo deje en el directorio **/bin**.


* postinstall
	 > script que utiliza **heroku** despues de instalar las dependencias.
	 
	 # Objeto de conexion a la DB.
     
     > /src/db/database.js
     
            local: {  
     	      client: 'pg',  
     	      connection: {  
     		      host : '127.0.0.1', // host de conexion  
     		      database: "mibasededatos",  // nombre de la base de datoos 
     			  user: "postgres",  // nombre de usuario en postgres
     		      password: "mipass"  // contraseña de la base de datos 
     	      },  
     	      migrations: {  
     		      directory: path.join(__dirname, './migrations')  // diretorio de las migraciones
     	     }
          }
     
     **Ejemplo del objeto de conexión a la base de datos*.
     
     	Existen 4 objetos por default creados: local, development, staging, production.

# RUTAS 

https://concursosgcaba.buenosaires.gob.ar/
  

**/auth**

<table>
	<thead>
		<tr>
			<th></th>
			<th></th>
		</tr>
	</thead>
	<tbody>
	<tr>
		<td><strong>Ruta</strong></td>
		<td><strong>Metodo</strong></td>
		<td><strong>Middleware</strong></td>
		<td><strong>Detalles</strong></td>
	</tr>
	<tr>
		<td>/auth/login</td>
		<td>GET</td>
		<td><ul><li>isLogged</li></ul></td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver</a>				
		</td>
	</tr>
	<tr>
		<td>/auth/login</td>
		<td>POST</td>
		<td>
			<ul>
				<li>isLogged</li>
				<li>validateRecaptcha</li>
			</ul>
		</td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver </a>				
		</td>
	</tr>
	<tr>
		<td>/auth/register</td>
		<td>GET</td>
		<td>
			<ul>
				<li>isLogged</li>
				<li>validateRecaptcha</li>
			</ul>
		</td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver </a>				
		</td>
	</tr>
	<tr>
		<td>/auth/register</td>
		<td>POST</td>
		<td>
			<ul>
				<li>isLogged</li>
				<li>validateRecaptcha</li>
			</ul>
		</td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver </a>				
		</td>
	</tr>
	<tr>
		<td>/auth/forgot</td>
		<td>GET</td>
		<td>
			<ul>
				<li>isLogged</li>
				<li>validateRecaptcha</li>
			</ul>
		</td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver </a>				
		</td>
	</tr>
	<tr>
		<td>/auth/forgot</td>
		<td>POST</td>
		<td>
			<ul>
				<li>isLogged</li>
				<li>validateRecaptcha</li>
			</ul>
		</td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver </a>				
		</td>
	</tr>	
	<tr>
		<td>/auth/validatemail</td>
		<td>GET</td>
		<td>
			<ul>
			</ul>
		</td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver </a>				
		</td>
	</tr>	
	<tr>
		<td>/auth/validatemail</td>
		<td>POST</td>
		<td>
			<ul>
				<li>isLogged</li>
				<li>validateRecaptcha</li>
			</ul>
		</td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver </a>				
		</td>
	</tr>	
	<tr>
		<td>/auth/validatemail/:token</td>
		<td>GET</td>
		<td>
			<ul>
				<li>validateEmailValidator</li>
			</ul>
		</td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver </a>				
		</td>
	</tr>	
	<tr>
		<td>/auth/resetpassword/:token</td>
		<td>GET</td>
		<td>
			<ul>
				<li>alreadyLogged</li>
				<li>validateGetResetPassword</li>
			</ul>
		</td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver </a>				
		</td>
	</tr>	
		<tr>
		<td>/auth/logout</td>
		<td>GET</td>
		<td>
			<ul>
				<li>loginRequired</li>
			</ul>
		</td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver </a>				
		</td>
	</tr>	
</tbody>
</table>

**/cuenta**

<table>
	<thead>
		<tr>
			<th></th>
			<th></th>
		</tr>
	</thead>
	<tbody>
	<tr>
		<td><strong>Ruta</strong></td>
		<td><strong>Método</strong></td>
		<td><strong>Middleware</strong></td>
		<td><strong>Detalles</strong></td>
	</tr>
	<tr>
		<td>/cuenta</td>
		<td>GET</td>
		<td><ul><li>loginRequired</li></ul></td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver</a>				
		</td>
	</tr>
	<tr>
		<td>/cuenta</td>
		<td>POST</td>
		<td>
			<ul>
				<li>loginRequired</li>	
		</ul>
		</td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver </a>				
		</td>
	</tr>
	<tr>
		<td>/cuenta/curriculum</td>
		<td>GET</td>
		<td>
			<ul>
				<li>loginRequired</li>
			</ul>
		</td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver </a>				
		</td>
	</tr>
	<tr>
		<td>/cuenta/change</td>
		<td>POST</td>
		<td>
			<ul>
				<li>loginRequired</li>
			</ul>
		</td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver </a>				
		</td>
	</tr>
	<tr>
		<td>/cuenta/change</td>
		<td>POST</td>
		<td>
			<ul>
				<li>loginRequired</li>
				<li>validateRecaptcha</li>
				<li>validateChangePassword</li>
			</ul>
		</td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver </a>				
		</td>
	</tr>
	<tr>
		<td>/cuenta/change/:token</td>
		<td>POST</td>
		<td>
			<ul>
				<li>loginRequired</li>
				<li>validateConfirmChangePassword</li>
			</ul>
		</td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver </a>				
		</td>
	</tr>	
</tbody>
</table>

**/concursos**

<table>
	<thead>
		<tr>
			<th></th>
			<th></th>
		</tr>
	</thead>
	<tbody>
	<tr>
		<td><strong>Ruta</strong></td>
		<td><strong>Método</strong></td>
		<td><strong>Middleware</strong></td>
		<td><strong>Detalles</strong></td>
	</tr>
	<tr>
		<td>/concursos</td>
		<td>GET</td>
		<td><ul></ul></td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver</a>				
		</td>
	</tr>
	<tr>
		<td>/concursos/publicos/abiertos</td>
		<td>GET</td>
		<td>
			<ul>	
			</ul>
		</td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver </a>				
		</td>
	</tr>
	<tr>
		<td>/concursos/cerrados/gcba</td>
		<td>GET</td>
		<td>
			<ul></ul>
		</td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver </a>				
		</td>
	</tr>
	<tr>
		<td>/concurso/:id</td>
		<td>GET</td>
		<td>
			<ul></ul>
		</td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver </a>				
		</td>
	</tr>
	<tr>
		<td>/concurso/:id/get</td>
		<td>GET</td>
		<td>
			<ul></ul>
		</td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver </a>				
		</td>
	</tr>
	<tr>
		<td>/concurso/:id/postulacion</td>
		<td>GET</td>
		<td>
			<ul>
				<li>loginRequired</li>
			</ul>
		</td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver 	</a>				
		</td>
	</tr>	
	<tr>
		<td>/concurso/:id</td>
		<td>POST</td>
		<td>
			<ul>
				<li>loginRequired</li>
			</ul>
		</td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver 	</a>				
		</td>
	</tr>	
</tbody>
</table>


**/postulacion**

<table>
	<thead>
		<tr>
			<th></th>
			<th></th>
		</tr>
	</thead>
	<tbody>
	<tr>
		<td><strong>Ruta</strong></td>
		<td><strong>Método</strong></td>
		<td><strong>Middleware</strong></td>
		<td><strong>Detalles</strong></td>
	</tr>
	<tr>
		<td>/postulacion/:id</td>
		<td>GET</td>
		<td><ul></ul></td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver</a>				
		</td>
	</tr>
</tbody>
</table>

# API  

https://concursosgcaba.buenosaires.gob.ar/api
  
**/api/postulaciones**

<table>
	<thead>
		<tr>
			<th></th>
			<th></th>
		</tr>
	</thead>
	<tbody>
	<tr>
		<td><strong>Ruta</strong></td>
		<td><strong>Método</strong></td>
		<td><strong>Middleware</strong></td>
		<td><strong>Detalles</strong></td>
	</tr>
	<tr>
		<td>/api/postulaciones/:id</td>
		<td>GET</td>
		<td><ul><li>loginRequired</li></ul></td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver</a>				
		</td>
	</tr>
	<tr>
		<td>/api/postulaciones</td>
		<td>POST</td>
		<td><ul><li>loginRequired</li></ul></td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver</a>				
		</td>
	</tr>
	<tr>
		<td>/api/postulaciones/:id/curriculum</td>
		<td>GET</td>
		<td><ul><li>loginRequired</li></ul></td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver</a>				
		</td>
	</tr>
	<tr>
		<td>/api/postulaciones/:id/modify</td>
		<td>PATCH</td>
		<td><ul></ul></td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver</a>				
		</td>
	</tr>
	<tr>
		<td>/api/postulaciones/:pid/estudios/:id</td>
		<td>DELETE</td>
		<td><ul><li>loginRequired</li></ul></td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver</a>				
		</td>
	</tr>
	<tr>
		<td>/api/postulaciones/:pid/capacitaciones/:id</td>
		<td>DELETE</td>
		<td><ul><li>loginRequired</li></ul></td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver</a>				
		</td>
	</tr>
		<tr>
		<td>/api/postulaciones/:pid/experiencias/:id</td>
		<td>DELETE</td>
		<td><ul><li>loginRequired</li></ul></td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver</a>				
		</td>
	</tr>
</tbody>
</table>

**/api/concursos**

<table>
	<thead>
		<tr>
			<th></th>
			<th></th>
		</tr>
	</thead>
	<tbody>
	<tr>
		<td><strong>Ruta</strong></td>
		<td><strong>Método</strong></td>
		<td><strong>Middleware</strong></td>
		<td><strong>Detalles</strong></td>
	</tr>
	<tr>
		<td>/api/concursos</td>
		<td>GET</td>
		<td><ul></ul></td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver</a>				
		</td>
	</tr>
	<tr>
		<td>/api/concursos/:id</td>
		<td>GET</td>
		<td><ul></ul></td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver</a>				
		</td>
	</tr>
</tbody>
</table>

**/api/curriculum**

<table>
	<thead>
		<tr>
			<th></th>
			<th></th>
		</tr>
	</thead>
	<tbody>
	<tr>
		<td><strong>Ruta</strong></td>
		<td><strong>Método</strong></td>
		<td><strong>Middleware</strong></td>
		<td><strong>Detalles</strong></td>
	</tr>
	<tr>
		<td>/api/curriculum</td>
		<td>GET</td>
		<td><ul><li>loginRequired</li></ul></td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver</a>				
		</td>
	</tr>
	<tr>
		<td>/api/curriculum	</td>
		<td>PATCH</td>
		<td><ul><li>loginRequired</li><li>validatePatchCurriculum</li></ul></td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver</a>				
		</td>
	</tr>
	<tr>
		<td>/api/curriculum/estudio	</td>
		<td>POST</td>
		<td><ul><li>validateEstudioCurriculum</li></ul></td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver</a>				
		</td>
	</tr>
	<tr>
		<td>/api/curriculum/estudio/:id</td>
		<td>PATCH</td>
		<td><ul><li>loginRequired</li><li>validateEstudioCurriculum</li></ul></td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver</a>				
		</td>
	</tr>
		<tr>
		<td>/api/curriculum/estudio/:id</td>
		<td>DELETE</td>
		<td><ul><li>loginRequired</li><li>validateEstudioCurriculum</li></ul></td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver</a>				
		</td>
	</tr>
	</tr>
	<tr>
		<td>/api/curriculum/capacitacion</td>
		<td>POST</td>
		<td><ul><li>validateEstudioCurriculum</li></ul></td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver</a>				
		</td>
	</tr>
	<tr>
		<td>/api/curriculum/capacitacion/:id</td>
		<td>PATCH</td>
		<td><ul><li>loginRequired</li><li>validateCapacitacionCurriculum</li></ul></td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver</a>				
		</td>
	</tr>
	<tr>
		<td>/api/curriculum/capacitacion/:id</td>
		<td>DELETE</td>
		<td><ul><li>loginRequired</li></ul></td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver</a>				
		</td>
	</tr>
	<tr>
		<td>/api/curriculum/experiencia</td>
		<td>POST</td>
		<td><ul><li>loginRequired</li><li>validateExperienciaCurriculum</li></ul></td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver</a>				
		</td>
	</tr>
	<tr>
		<td>/api/curriculum/experiencia/:id</td>
		<td>PATCH</td>
		<td><ul><li>loginRequired</li><li>validateExperienciaCurriculum</li></ul></td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver</a>				
		</td>
	</tr>
	<tr>
		<td>/api/curriculum/experiencia/:id</td>
		<td>DELETE</td>
		<td><ul></ul></td>
		<td>
			<a href="[https://github.com/Xappia/Concursos](https://github.com/Xappia/Concursos)">ver</a>				
		</td>
	</tr>
</tbody>
</table>

# LSITA DE VARIABLES DE ENTORNO

 <table>
 	<thead>
 		<tr>
 			<th></th>
 			<th></th>
 		</tr>
 	</thead>
 	<tbody>
 	<tr>
 		<td><strong>env</strong></td>
 		<td><strong>descripción</strong></td>
 	</tr>
 	<tr>
 		<td>DOMAIN</td>
 		<td>-</td>
 	</tr>
 	<tr>
        <td>HEROKU_POSTGRESQL_ONYX_URL</td>
        <td></td>
    </tr>
   	<tr>
       <td>MIBA_CLIENT_ID</td>
       <td></td>
   </tr>
   	<tr>
       <td>MIBA_CLIENT_SECRET</td>
       <td></td>
   </tr>
   	<tr>
       <td>MIBA_HOST</td>
       <td></td>
   </tr>
   <tr>
       <td>NODE_ENV</td>
       <td></td>
   </tr>
    <tr>
        <td>PAPERTRAIL_API_TOKEN</td>
        <td></td>
    </tr>
     <tr>
        <td>RECAPTCHA_PRIVATE</td>
        <td></td>
     </tr>
     <tr>
        <td>RECAPTCHA_PUBLIC</td>
        <td></td>
     </tr>      
     <tr>
         <td>REDIS_URL</td>
         <td></td>
     </tr> 
     <tr>
         <td>SECRET_KEY</td>
         <td></td>
     </tr>    
     <tr>
         <td>SF_CLIENT_ID</td>
         <td></td>
     </tr>        
     <tr>
         <td>SF_CLIENT_SECRET</td>
         <td></td>
     </tr>       
     <tr>
         <td>SF_DOMAIN</td>
         <td></td>
     </tr>       
     <tr>
         <td>SF_PASSWORD</td>
         <td></td>
     </tr>         
     <tr>
         <td>SF_USERNAME</td>
         <td></td>
     </tr>        
     <tr>
         <td>SMTP_PASSWORD</td>
         <td></td>
     </tr>       
     <tr>
         <td>SMTP_PORT</td>
         <td></td>
     </tr>       
     <tr>
         <td>SMTP_SERVER</td>
         <td></td>
     </tr>    
     <tr>
         <td>SMTP_USER</td>
         <td></td>
     </tr> 
     <tr>
          <td>SYNC</td>
          <td></td>
      </tr>    
      <tr>
          <td>SYNC_INTERVAL</td>
          <td></td>
      </tr>     
      <tr>
          <td>SYNC_ONLY_LAST_MODIFIED_RECORDS</td>
          <td></td>
      </tr>   
      <tr>
          <td>SYNC_URL</td>
          <td></td>
      </tr>   
      <tr>
          <td>SYNC_URL_GET_SF_TOKEN</td>
          <td></td>
      </tr>   
      <tr>
          <td>SYNC_VERSION_API</td>
          <td></td>
      </tr>   
      <tr>
          <td>TZ</td>
          <td></td>
      </tr>   
 </tbody>
 </table>

# Extras

## Funcionalidad y comportamiento del portal

StackEdit extends the standard Markdown syntax by adding extra **Markdown extensions**, providing you with some nice features.

## Conexión con postgres
La conexión casi/total del portal con postgres se realizó a partir del momento en que se estaba exediendo el límite de api calls con sf, para realizar operaciones CRUD básicas salientes desde portal.
Si bien ocurre un flujo de datos en varias direcciones desde el portal, postgres alimenta principalmente al sitio.

Para conectarnos con postgres utilizamos un query builder llamado [knex](http://knexjs.org/) asociado a otro query builder/orm llamado [objection](https://vincit.github.io/objection.js/) (objection esta basado en knex) con el cual desarrollamos nuestros modelos, asociaones, migraciones y seeders.

## Conexion con Salesforce
Principalmente el portal consumía datos desde Sf. Lo que ocurre aquí es que si queremos consumir datos de Sf desde una fuente externa, este tiene un límite de llamadas. En momentos que el portal tenia un flujo de datos arriba de lo normal, estas api calls que Sf nos proveeia se agotaban, por ende se debía pagar para obtener más.

Desde el portal se utiliza una librería [jsforce](https://jsforce.github.io/) la cual nos provee la conexión hacia Salesforce. A su vez nos entrega un objeto al estilo ORM con el cual podemos realizar consultas CRUD sql hacia nustreo entorno de Sf.


## Renderizado de vistas

El portal inicialmente comenzo con un motor de renderizado de vistas [handlebars](https://handlebarsjs.com/) .  Con el correr del tiempo y las personas que fueron desarrollando en dicho proyecto, el renderizado de las vistas fue mutando en tecnologías. 
De a poco se ha ido desacoplando handlebars y mudando toda la UI a javascript [react.js](https://reactjs.org/).
Por motivos de performace, de la tecnologpia en si y diversos motivos más practicamente todo el renderizado de las vistas se tendría que pasar a react.

En el dia de hoy, la renderizacion de dichas vistas es compartida.
* Handlebars:
	* inicio
	* navbar
	* footer
	* login
	* lista de postulaciones
	* recuperar contraseña
	* normativa
	* guia del usuario

* React: 
	* lista de concursos abiertos
	* lista de concursos cerrados
	* detalle de un concurso
	* prepostulacion
	* pospostulacion
	* curriculum

