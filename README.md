# P1-Comando-de-Docker


Crea un novo repositorio público en git, coo nome da tarefa, clónao e engade un arquivo readme2.md en local que poña unha frase á túa elección.

Facendo uso de VScode, Docker e a imaxe de ubuntu da práctica anterior, describe no arquivo readme.md, cun formato claro, os pasos e comandos para:

1. Descargar e comprobar que unha imaxe está no teu equipo

**Para poder descargar e comprobar as imaxes podemos utilizar os seguintes comandos:**
```
docker pull "nome da imaxe"
docker images
```
**Con estos dous comandos podemos descargar e ver todas as imaxes que xa utilizamos e tamen aparece informacion sobre estas imaxes.**

2. Crear un contenedor sen nome, queda arrincado?, cómo obtés o nome?

  **Para poder comezar un contenedor sen nome podemos utilizar o comando:** 
```
 docker run -d nginx.
```
**Este quedara directamente acendido ata que o apaguemos e o nome e asignado aleatoriamente por Docker, se queremos coñecer o nome podemos utilzar o seguinte comando:**
```
docker ps -a
```
**Nos apareceran todos os contenedores que tengamos que esten ou non arrincados e nunha das columnas poderemos observar os nomes dos contenedores**

3. Crea un contenedor coo nome 'u1', cómo accedes a el?

**Para crear o contenedor utilizamos o comando**
```
docker run -d --name u1 nginx
```
**Podemos acceder desde Vcodestudio facendo click dereito y seleccionar Attach ou tamén a través da terminal co comando:**
```
docker exec -it u1 /ruta
```
**Con isto podemos acceder a o contenedor de varias formas**

4. Comproba a súa ip e fai ping a google.com

**Para comprobar a IP e para facer ping a google.com utilizaremos os seguintes comandos**
```
ifconfig
ping google.com
```
**Se algun destos da algun problema poderia solucionarse facendo un updtate**

5. Crea un contenedor coo nome 'bono', pódes facer ping entre os contenedores?

**Para crear o contenedor utilizaremos o comando**
```
docker run -d --name bono nginx
```
**Para facer ping a o outro contenedor tense que cumplir que os dous contenedores pertezcan a misma red se no non poden comunicarse e non faran o ping, o comando que utilziaremos é:**
```
ping {IP do outro contenedor}
```

6. Se pechas as terminales, qué pasa coo contenedor?

**Mentres nos non pechemos os contenedor estes aunque pechemos a nosa terminal continuaran funcionando en segundo plano, esto podese comprobar co comando**
```
docker ps
```


7. Cánta memoria no disco duro ocupaches? usa docker para calculalo

**Para saber canta memoria xa hemos utilizados executaremos o comando**
```
docker system df
```
**No meu caso aparece que se utilizaron 278.83MB de memoria**

8. Cánta RAM ocupan os contenedores? Crea varios para calculalo

**Para poder comprobar canta RAM ocupan os contenedores que se atopan en execución podemos utilizar o comando**
```
docker stats
```
**No meu caso tendo en conta que teño unha máquina con 12GB de memoria RAM estan ocupando con tres contenedores ao mesmo tempo un 0.18% da memoria**

9. Cómo fixeches para clonar o repositorio

**Para clonar o repositorio utilicei o comando**
```
git clone "DireccionDelRepositorio"
```

10. Cómo engades o arquivo readme2.md

**Para engadir o arquivo readme2.md primeiro o creamos co seguinte comando dentro do directorio no que se atopa o repositorio**
```
echo "Texto" > readme2.md
```
**Logo para engadirlo utilizamos o comando**
```
git add -A readme2.md
```


11. Os pasos a seguir para subir o arquivo que estás editando e o arquivo readme2.md

**Despois de realizar o paso anterior primeiro deberemos de utilizar o comando**
```
git add "NomeDoArquivo"
```
**Este comando e para que se actualice o arquivo e non atope ningun erro de porque non esta actualizado, despois utilizaremos o comando**
```
git commit -m "Texto para saber cando é que se actualizó
```
**E por ultimó utilizaremos o comando para subir e confirmar os cambios no repositorio**
```
git push
```

12. Cómo comprobarías que existen diferencias entre o teu repositorio local e o remote.

**Para comprobar estas diferencias entre os repositorios existe o seguinte comando:**
```
git diff origin/main
```


Entrega a tarefa enviando na resposta a dirección do teu repositorio coas respostas.

