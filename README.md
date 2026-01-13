🚀 Desarrollo y Distribución de una Aplicación JavaFX para Windows
📌 Descripción del proyecto

Este repositorio contiene el desarrollo completo del Supuesto Práctico: “Desarrollo y Distribución de una Aplicación”, cuyo objetivo es simular un entorno profesional real en el que una empresa necesita distribuir una aplicación de escritorio JavaFX lista para instalar en sistemas Windows.

El proyecto abarca todo el proceso: desde la generación del JAR ejecutable hasta la creación de un instalador profesional para Windows, asegurando que la aplicación funcione incluso en equipos sin Java instalado previamente.

🛠️ Tecnologías y herramientas utilizadas

Java JDK

JavaFX

Maven

Maven Shade Plugin

Launch4j

Inno Setup

Windows

📂 Estructura del repositorio
📁 proyecto/
├── 📁 jar/
│   └── aplicacion.jar
├── 📁 exe/
│   └── aplicacion.exe
├── 📁 installer/
│   └── instalador.exe
├── 📁 jre/
│   └── (JRE incluido)
├── 📁 resources/
│   └── iconos y recursos
├── pom.xml
└── README.md

🔄 Proceso de desarrollo y distribución
1️⃣ Configuración del proyecto Maven

Se partió de una aplicación JavaFX completamente funcional.
Para generar un JAR ejecutable con todas las dependencias, se modificó el archivo pom.xml añadiendo el Maven Shade Plugin, configurando correctamente la clase principal (Main).

2️⃣ Generación y comprobación del JAR

Una vez configurado Maven, se generó el JAR ejecutable y se verificó su correcto funcionamiento ejecutándolo desde consola:

java -jar aplicacion.jar


Este paso es imprescindible para asegurar que la aplicación funciona correctamente antes de continuar con el empaquetado.

3️⃣ Preparación del JRE

Para permitir la ejecución de la aplicación en equipos sin Java instalado, se extrajo el JRE incluido en el JDK utilizado durante el desarrollo.
Este JRE se añadió posteriormente al ejecutable final.

4️⃣ Creación del ejecutable (.exe) con Launch4j

Se utilizó Launch4j para convertir el JAR en un archivo ejecutable de Windows.
Durante la configuración se realizaron los siguientes pasos:

Selección del JAR generado

Asignación de un icono personalizado

Configuración del JRE incluido

Desactivación de la consola (aplicación gráfica)

El resultado fue un archivo .exe totalmente funcional.

5️⃣ Creación del instalador con Inno Setup

A partir del ejecutable generado, se creó un instalador para Windows utilizando Inno Setup, el cual:

Copia la aplicación en una ruta adecuada del sistema

Crea accesos directos en el escritorio y menú inicio

Permite la desinstalación completa del programa

Incluye textos e iconos personalizados

Se prestó especial atención a la experiencia del usuario final.

6️⃣ Pruebas finales

Antes de la entrega se realizaron pruebas completas para verificar que:

El instalador se ejecuta sin errores

La aplicación se instala correctamente

El programa se inicia y funciona correctamente

La desinstalación elimina todos los archivos sin dejar restos

📦 Entrega

La entrega final consta de:

✅ Instalador final para Windows

✅ JAR ejecutable

✅ Ejecutable .exe

✅ Recursos necesarios (JRE, iconos)

✅ Documentación del proceso
