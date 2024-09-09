Instrucciones para ejecutar pruebas con Karate en el Proyecto de PetStore API
Descripción
Este proyecto utiliza Karate para realizar pruebas automatizadas sobre la API de PetStore (https://petstore.swagger.io/). A continuación se detallan los pasos necesarios para configurar y ejecutar las pruebas.

Requisitos
Java Development Kit (JDK): Versión 11 o superior.
Maven: Versión 3.9.6 o superior 
IntelliJ IDEA: Versión 2021.1 o superior 
Configuración del Entorno
Instalar JDK:

Descarga e instala JDK desde Oracle o OpenJDK.
Asegúrate de configurar la variable de entorno JAVA_HOME apuntando al directorio de instalación de JDK.
Instalar Maven (si es necesario):

Descarga e instala Maven desde Apache Maven.
Configura la variable de entorno M2_HOME apuntando al directorio de instalación de Maven.
Agrega el binario de Maven a la variable de entorno PATH.
Configurar el Proyecto en IntelliJ IDEA:

Abre IntelliJ IDEA.
Importa el proyecto como un proyecto Maven
Asegúrate de que todas las dependencias se resuelvan correctamente.


Configuración del Proyecto Karate
Agregar Dependencias: Asegúrate de que tu archivo pom.xml  incluya las dependencias necesarias para Karate
<dependencies>
    <dependency>
        <groupId>com.intuit.karate</groupId>
        <artifactId>karate-junit5</artifactId>
        <version>1.2.0</version>
        <scope>test</scope>
    </dependency>
</dependencies>


Ejecutar Pruebas:

mvn test
o por test:mvn clean test -Dtest=AddPetRunner
mvn clean test -Dtest=GetPetRunner
mvn clean test -Dtest=GetPetByStatusRunner
mvn clean test -Dtest=UpdatePetRunner

Ejecutar Pruebas de Karate:

Navega al archivo .feature en IntelliJ IDEA.
Haz clic derecho sobre el archivo y selecciona "Run 'PetStoreTests.feature'".
Ver Resultados:

Los resultados de las pruebas se mostrarán en la pestaña de "Run" de IntelliJ IDEA.
Notas
Asegúrate de que tu conexión a Internet esté activa para poder acceder a la API de PetStore durante las pruebas.
Ajusta las versiones de las dependencias en el archivo de configuración según sea necesario.


