# Seminario de Deep Learning
**Ingeligencia Artificial - Universidad Pablo de Olavide** 

*Impartido por: José F. Torres AKA Pepe*

===
¡Hola a tod@s!

Antes de nada, quería daros la bienvenida y animaros en estos momentos en los que seguro tenéis una carga de trabajo considerable entre todas las clases, exámenes parciales y entregas. Todo esfuerzo tiene su recompensa, y antes o después os daréis cuenta que todo este esfuerzo merece la pena :stuck_out_tongue_winking_eye:

## ¿Qué vamos a ver?
Principalmente, lo que vamos a hacer una pequeña introducción a *Deep Learning*, cubriendo:
- Principales diferencias con las redes neuronales tradicionales.
- Teoría de arquitecturas recurrentes y convolucionales a muy alto nivel.
- Práctica ANN VS CNN, donde implementaremos dos modelos para clasificar si una fotografía es de un perro o de un gato.

## ¿Qué vamos a necesitar?
En este seminario trabajaremos fundamentalmente con Tensorflow: una librería de código abierto desarrollada por Google que nos permite implementar redes neuronales de forma realmente sencilla. por encima de tensorFlow, trabajaremos con Keras, que es otra librería apoyada sobre la anterior, de forma que simplifica aun más su uso. 

Además, necesitaremos una serie de librerías y paquetes que nos facilitarán la tarea de trabajar con imágenes y otras operaciones.

### Lo más importante: Datos
Obviamente, sin datos no podemos trabajar. Mi intención en este seminario es acercanos lo máximo posible a un problema del mundo real, por lo que no vamos a partir de datos ya procesados, lo vamos a hacer nosotros (o intentarlo :innocent:).

Vamos a trabajar con imágenes, concretamente con un conjunto de datos de **25.000 imágenes** de perros y gatos (la mitad de ellas de :dog2: y la otra mitad de :cat2:).

En este repositorio hay disponible 


### Máquina virtual disponible
Para no extendernos demasiado en el tiempo del seminario y estar configurando todo el entorno e instalando los paquetes que vamos a necesitar, he creado una **máquina virtual** en VirtualBox con un *Linux Mint*, que tenéis disponible en [este enlace](https://www.google.com). Con descargar la máquina virtual y abrirla en VirtualBox tendréis lo necesario para seguir el seminario, ya que los datos y los archivos que váis a necesitar están todos dentro del directorio ```/home/ia/seminario ```

**IMPORTANTE**: La máquina virtual ocupa unos 20GB y está configurada para que use unos 5GB de memoria RAM, por lo que debéis de estar seguros que tenéis recursos suficientes para soportar la VM.

### ¿Prefieres usar tu máquina directamente? ¡Aquí te explico como!

Para el desarrollo del seminario, se tiene disponible una máquina virtual en VirtualBox con el entorno preparado y listo para ser usado. La máquina se puede descargar a través de: 

Esta máquina virtual ocupa unos 20Gb de tamaño en disco, y está configurada para hacer uso de unos 5Gb de memoria RAM.
