# Seminario de Deep Learning
**Ingeligencia Artificial - Universidad Pablo de Olavide** 

*Impartido por: José F. Torres AKA Pepe*

----
¡Hola a tod@s!

Antes de nada, me gustaría daros la bienvenida y animaros en estos momentos en los que seguro tenéis una carga de trabajo considerable entre todas las clases, entregas y exámenes parciales, pero pensad en que todo esfuerzo tiene su recompensa, y antes o después os daréis cuenta que todo este esfuerzo habrá merecido la pena :stuck_out_tongue_winking_eye:

Como ya sabréis, esta "practica" no es evaluable, pero si es muy interesante que conozcáis de qué va la historia y sobre todo familiarizaros un poco con cómo se trabaja en esto, porque fuera de la universidad se está demandando, y mucho (podemos discutirlo en el descanso o en un café :innocent:).

## ¿Qué vamos a ver?
Principalmente, lo que vamos a hacer una pequeña introducción a *Deep Learning*, cubriendo:
- Principales diferencias con las redes neuronales tradicionales.
- Teoría de arquitecturas recurrentes y convolucionales a muy alto nivel.
- Práctica ANN VS CNN, donde implementaremos dos modelos para clasificar si una fotografía es de un :dog: o de un :cat:.

## ¿Qué vamos a necesitar?
En la práctica trabajaremos fundamentalmente con Tensorflow: una librería de código abierto desarrollada por Google que nos permite implementar redes neuronales de forma realmente sencilla. Por encima de tensorFlow usaremos Keras, que es otra librería apoyada sobre la anterior, simplificando la sintaxis y haciendo que implementar las redes sea mucho más fácil.

Además, necesitaremos una serie de librerías y paquetes que nos facilitarán la tarea de trabajar con imágenes, operaciones matriciales y otras herramientas.

En resumen, para poder seguir la práctica vamos a necesitar tres recursos fundamentalmente:

### 1. Lo más importante: Los datos
Obviamente, sin datos no podemos trabajar. Mi intención es acercanos lo máximo posible a un problema del mundo real, por lo que no vamos a partir de datos ya procesados, lo vamos a hacer nosotros (o intentarlo :innocent:).

Vamos a partir de un conjunto de imágenes, que cuenta con **25.000 fotografías** de perros y gatos (la mitad de cada uno).

Dentro de la carpeta ```src/dataset/``` de este repositorio hay disponible algunas de las imágenes a modo de ejemplo, pero **el conjunto de datos completo lo debéis descargar desde [aquí](https://upolavide-my.sharepoint.com/:u:/g/personal/jftormal_upo_es/ETUU1VU8cI1NhWpnjPkzPgIBn0NyBIPtZjeLUdUQKIPVoQ?e=ubtnSw).**

### 2. Fuente de los cuadernos Jupyter
Como entorno de desarrollo vamos a usar Jupyter notebook (ya debéis saber lo que es :wink:). Os he preparado unas plantillas de los cuatro notebooks que vamos a usar, que lo podéis descargar desde esta misma página:

1. **PARTE I - INTRODUCCIÓN.ipynb**: Una breve introducción a Jupyter para aquell@s que no sepan todavía lo que es y no estén familiarizados.
2. **PARTE II - PERROS VS GATOS ANN.ipynb**: Aquí implementaremos nuestra red neuronal simple, llamada perceptrón multicapa (el que habéis visto en clase), para resolver el problema que planteamos.
3. **PARTE III - CONVOLUCION.ipynb**: Haremos un ejemplo de convolución y veremos cómo podemos extraer información de utilidad de una imagen aplicando una serie de filtros.
4. **PARTE IV - PERROS VS GATOS CNN.ipynb**: ¡Lo bueno se hace esperar! Desarrollamos nuestro modelo usando redes convolucionales, y compararemos los resultados con los obtenidos en el apartado 2.

### 3. Máquina virtual disponible
Para no extendernos demasiado en el tiempo del seminario y tener que configurar todo el entorno e instalar los paquetes que vamos a necesitar, he creado una **máquina virtual** en VirtualBox con *Linux Mint*, que tenéis disponible en [este enlace](https://upolavide-my.sharepoint.com/:u:/g/personal/jftormal_upo_es/ET7qm2nyhghLhuocpTT2glMBI503FYBLusu8f3rB-biLPg?e=rIXr5Q). Con descargar la máquina virtual y abrirla en VirtualBox tendréis lo necesario para seguir el seminario, ya que los datos y los archivos que vais a necesitar están todos dentro del directorio ```/home/ia/seminario ``` de dicha máquina.

¿Qué?, ¿que no sabéis el usuario y la contraseña? Os lo digo en clase, aunque seguro que la mayoría sois capaces de sacarlo sin problemas :smirk:

:bangbang: **IMPORTANTE**: La máquina virtual ocupa unos 20GB y está configurada para que use unos 5GB de memoria RAM, por lo que debéis estar seguros que tenéis recursos suficientes para soportar la VM.

### * ¿Prefieres usar tu máquina directamente? ¡Aquí te explico como!
Si por el contrario quieres utilizar toda la potencia de tu máquina y tener el entorno preparado para futuras experimentaciones, os dejo una pequeña guía de los pasos que necesitáis ejecutar desde un terminal para tener el entorno en un sistema basado en Ubuntu (no me voy a parar a explicar qué significa cada una de las sentencias):

#### Descargar e instalar Anaconda
```
cd /tmp 
curl -O https://repo.anaconda.com/archive/Anaconda3-2019.03-Linux-x86_64.sh
sha256sum Anaconda3-2019.03-Linux-x86_64.sh
bash Anaconda3-2019.03-Linux-x86_64.sh
```
La secuencia de comandos anterior descargará el instalador de [Anaconda](https://www.anaconda.com/distribution/). Al ejecutarlo pedirá varias confirmaciones, y nosotros haremos lo mismo de siempre: *siguiente, siguiente y siguiente*.
``` 
cd 
source .bashrc
```

#### Creación del entorno virtual de python e instalación de librerías
```
conda create --name iaenv python=3.6.0
conda activate iaenv

sudo apt-get install python3-pip
sudo apt  install jupyter-core
sudo apt-get install jupyter
sudo apt-get install python3-setuptools

pip3 install numpy=1.16.4
pip3 install sklearn
pip install imutils
conda install tensorflow
conda install keras
conda install opencv
conda install matplotlib
conda install pillow
```

Fácil, ¿no? si tienes alguna duda o problema y quieres que te eche una mano, te intento ayudar en lo que pueda. 
Solo tienes que escribirme a jftormal@upo.es

:bangbang:**NOTA IMPORTANTE:** ¡Cuidado con la compatibilidad de las versiones! :bangbang:

