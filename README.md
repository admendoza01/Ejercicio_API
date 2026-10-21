# <div align="justify"> <span style="color: blue;">PROGRAMACIÓN DE INTELIGENCIA ARTIFICIAL: PRÁCTICA DE CREACIÓN DE API Y DESPLIEGUE <spain>

## 1. DESCRIPCIÓN DE LA APLICACIÓN
####  

<div align="justify"> La aplicación consiste en un sistema predictor de retrasos en las entregas de pedidos, diseñado para estimar el nivel de riesgo de demora a partir de diferentes variables relacionadas con el envío y las condiciones de entrega. Para realizar la predicción, el usuario debe introducir el código del pedido, la distancia hasta el destino (en kilómetros), el tipo de envío (estándar, económico o exprés) y el tiempo transcurrido desde que se realizó la solicitud. Además, el sistema considera factores externos que pueden influir en los plazos de entrega, como la realización del pedido en un día festivo, la presencia de condiciones meteorológicas adversas y la ubicación del destino en una zona remota. A partir de estos datos, la aplicación procesa la información introducida y proporciona una estimación del riesgo de retraso, clasificándolo en tres niveles: bajo, medio o alto. De este modo, la herramienta permite identificar posibles incidencias en el proceso logístico y facilita la evaluación anticipada de los factores que pueden afectar al cumplimiento de los plazos de entrega.</div>

<div align="justify"> La aplicación busca resolver diversos problemas relacionados con la gestión logística y el cumplimiento de los plazos de entrega. Entre ellos, destaca la dificultad para identificar de forma anticipada los pedidos que presentan un mayor riesgo de retraso, lo que puede generar insatisfacción en los clientes, reclamaciones y pérdidas económicas para las empresas. Asimismo, permite evaluar cómo determinados factores, como la distancia de envío, el tipo de servicio contratado, los días festivos, las condiciones meteorológicas adversas y la ubicación en zonas remotas, pueden influir en los tiempos de entrega. </div>

## 2. URL PÚBLICA
#### 

<div align="justify">Se adjunta URL para el lanzamiento de la app. URL: https://ejercicio-api-991a.onrender.com/</div>


## 3. PLATAFORMA DE DESPLIEGUE
#### 
<div align="justify">Para el despliegue de la aplicación se utiliza Render, una plataforma en la nube que permite alojar y ejecutar aplicaciones web de forma accesible y sencilla. Mediante este servicio, el predictor de retrasos de entrega puede estar disponible a través de una URL pública, lo que permite a los usuarios acceder a sus funcionalidades desde cualquier dispositivo con conexión a Internet, sin necesidad de instalar el programa localmente. El proceso de despliegue consiste en configurar el entorno de ejecución, instalar las dependencias necesarias y vincular el proyecto con el repositorio de código fuente para facilitar la publicación y actualización de la aplicación. Una vez desplegado, Render se encarga de ejecutar el servicio y gestionar su disponibilidad según la configuración establecida. De este modo, se facilita el acceso a la herramienta y se simplifica su mantenimiento y actualización.</div>

## 4. PROCESO DE DESPLIEGUE

####

<div align="justify">Para iniciar el proceso de despliegue de la aplicación en Render, es necesario disponer previamente de un repositorio creado en GitHub que contenga los archivos del proyecto. En esta explicación, nos centraremos principalmente en la configuración de Render, ya que GitHub se utiliza como repositorio del código fuente.</div>

####

<div align="justify"> Una vez creada la cuenta e iniciada la sesión en Render, debemos acceder al apartado «New +» y seleccionar la opción «Web Service». A continuación, la plataforma solicitará la dirección URL del repositorio donde se encuentra alojada la aplicación. Para ello, seleccionamos la opción «Public Git Repository», introducimos la URL correspondiente al repositorio de GitHub y pulsamos «Connect» para establecer la conexión. De este modo, Render podrá acceder al código fuente del proyecto y continuar con los siguientes pasos necesarios para configurar y desplegar la aplicación.</div>

####
<div align="justify"> Una vez conectado el repositorio de GitHub con Render, la plataforma solicitará completar una serie de campos necesarios para configurar el servicio web. En primer lugar, debemos introducir el campo **Name**, donde asignaremos un nombre identificativo al proyecto, por ejemplo, `ejercicio_API`. A continuación, en **Build Command**, indicaremos el comando `pip install -r requirements.txt`, que permite instalar las dependencias y bibliotecas de Python necesarias para el funcionamiento de la aplicación, especificadas previamente en el archivo `requirements.txt`. En el campo **Start Command**, introduciremos `uvicorn app:app --host 0.0.0.0 --port $PORT`, que permite iniciar el servidor de la aplicación mediante Uvicorn, utilizando el objeto `app` definido en el archivo `app.py` y el puerto asignado por Render. Posteriormente, seleccionaremos el tipo de instancia, pudiendo optar por un plan gratuito, si está disponible para el servicio, o por una opción de pago, en función de las necesidades del proyecto. Finalmente, tras comprobar que todos los parámetros son correctos, pulsaremos **Deploy Web Service** para iniciar el proceso de despliegue. Render se encargará de instalar las dependencias, ejecutar la aplicación y comprobar su puesta en funcionamiento, permitiendo acceder al servicio mediante una URL pública cuando el despliegue se complete correctamente.</div>

