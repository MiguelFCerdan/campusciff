# campusciff: EJERCICIOS


## 2.1 REPOSITORIO CAMPUSCIFF (I)

1. Crear un repositorio en vuestro GitHub llamado __campusciff__.

Se ha seleccionado la opción "New repository" disponible en GitHub.

!(/img/Paso_2.1.png)


## 2.2 REPOSITORIO CAMPUSCIFF (II)

1. Clonar vuestro repositorio en local.

```
git clone git@github.com:MiguelCerdan/campusciff.git
```

(../img/Paso_2.2.png)


## 2.3 README

1. Crear (si no lo habéis creado ya) en vuestro repositorio local un documento __README.md__.

Ya fue creado al hacer el repositorio en GitHub marcando el checkbox "Initialize this repository with a README".


## 2.4 COMMIT INICIAL

1. Añadir al README.md los comandos utilizados hasta ahora y hacer un commit inicial con el mensaje __commit inicial__.

```
git add .
git commit -m "commit inicial"
```


## 2.5 PUSH INICIAL

1. Subir los cambios al repositorio remoto.

```
git push origin master
```


## 2.6 IGNORAR ARCHIVOS (I)
* Crear en el repositorio local un fichero llamado __privado.txt__.

```
touch privado.txt
```

* Crear en el repositorio local una carpeta llamada __privada__.

```
mkdir privada
```


## 2.7 IGNORAR ARCHIVOS (II)
1. Realizar los cambios oportunos para que tanto el archivo como la carpeta sean ignorados por git.

```
vi .gitignore
```

Se añaden las excepciones al archivo .gitignore:

(imagen Paso_2.7.png)

Se escribe en VI ':q' para salir tras haber escrito con ':w'.

```
git add .
git commit -m "archivo .gitignore"
```

## 2.8 AÑADIR FICHERO 1.TXT
1. Añadir fichero __1.txt__ al repositorio local.

```
touch 1.txt
git add .
git commit -m "añadido 1.txt"
```

## 2.9 CREAR EL TAG V0.1
1. Crear un tag __v0.1__.

```
git tag v0.1
```

## 2.10 SUBIR EL TAG V0.1
1. Subir los cambios al repositorio remoto.

```
git push --tag origin master
```

## 2.11 CREAR UNA RAMA V0.2
* Crear una rama __v0.2__.

```
git branch v0.2
```

* Posiciona tu carpeta de trabajo en esta rama.

```
git checkout v0.2
```

También podría haberse hecho en un solo paso:

```
git checkout -b v0.2
```

## 2.12 AÑADIR FICHERO 1.TXT
1. Añadir un fichero __2.txt__ en la rama __v0.2__.

```
touch 2.txt
git add .
git commit -m "añadido 2.txt"
```

## 2.13 CREAR RAMA REMOTA V0.2
1. Subir los cambios al reposiorio remoto.

```
git push origin v0.2
```

## 2.14 MERGE DIRECTO
* Posicionarse en la rama __master__.

```
git checkout master
```

* Hacer un merge de la rama __v0.2__ en la rama __master__.

```
git merge v0.2 ESTO PODRIA SOBRAR: -m "fusion (merge) v0.2 en master"
```

## 2.15 MERGE CON CONFLICTO (I)
1. En la rama __master__ poner _Hola_ en el fichero __1.txt__ y hacer commit.

```
echo "Hola" >> 1.txt
git add .
git commit -m "añadido Hola a 1.txt"
```

## 2.16 MERGE CON CONFLICTO (II)
1. Posicionarse en la rama __v0.2__ y poner _Adios_ en el fichero __1.txt__ y hacer commit.

```
git checkout v0.2
echo "Adios" >> 1.txt
git add .
git commit -m "añadido Adios a 1.txt"
```

## 2.17 MERGE CON CONFLICTO (III)
1. Posicionarse de nuevo en la rama __master__ y hacer un merge con la rama __v0.2__.

```
git checkout master
git merge v0.2 -m "segunda fusion (merge) v0.2 en master"
```

## 2.18 LISTADO DE RAMAS
1. Listar las ramas con merge y las ramas sin merge.

```
git branch --merged
git branch --no-merged
```

## 2.19 ARREGLAR CONFLICTO
1. Arreglar el conflicto anterior y hacer un commit.

```
vi 1.txt
```

Se soluciona el conflicto mediante VI:

(imagen Paso_2.19.png)

```
git add .
git commit -m "conflicto resuelto"
```

## 2.20 BORRAR RAMA
* Crear un tag __v0.2__.

```
git tag v0.2
```

* Borrar la rama __v0.2__.

```
git branch -d v0.2
```

## 2.21 LISTADO DE CAMBIOS
1. Listar los distintos commits con sus ramas y sus tags.

```
git log --oneline --decorate --graph --all
```

## 2.22 CUENTA DE GITHUB
* Poner una foto en vuestro perfil de GitHub.

Desde la página del perfil, en la columna "Personal Settings", pestaña de "Profile", se puede editar llegando a la siguiente página:

(imagen Paso_2.22.1.png)

En ella se puede subir una foto en "Upload new picture".
Al acabar, hay que clicar en "Update profile".

* Poner el doble factor de autentificación en vuestra cuenta de GitHub.

En la misma página de edición del perfil, en la columna de "Personal settings", se selecciona la pestaña "Security". Se activa la "Two-factor authentication":

(imagen Paso_2.22.2.png)

Se siguen los pasos. En este caso se ha elegido la opción de recibir la segunda contraseña via SMS.

* Añadir (si no lo habéis hecho ya) la clave pública que se corresponde a tu ordenador.

La clave pública fue añadida anteriormente, como puede observarse en la pestaña "SSH keys":

(imagen Paso_2.22.3.png)

## 2.23 USO SOCIAL DE GITHUB
1. Preguntar los nombres de usuario de GitHub de tus compañeros de clase, búscalos, y sigueles.

Estoy siguiendo a los siguientes compañeros de clase:
- Javier Enríquez de Salamanca
- ciffSara
- Eduardociff
- cabreracanal
- Adolfo Sanz de Diego
- Alejandro Diaz
- sergiotorrespalomino
- Jose Dios
- PalomaCiffBigData
- Danielobit
- macarenagaranena
- Miriam Asenjo
- Cristóbal Rodríguez Fraile

(imagen Paso_2.23.1.png)

2. Seguir los repositorios __campusciff__ del resto de tus compañeros.

Se sigue un repositorio mediante el boton "Watch".

(imagen Paso_2.23.2.png)

Se ha realizado en los siguientes compañeros:
- ciffSara
- cabreracanal
- Alejandro Diaz
- PalomaCiffBigData
- Danielobit
- macarenagaranena
- Miriam Asenjo
- Cristobal Rodríguez Fraile

3. Añadir una estrella a los repositorios __campusciff__ del resto de tus compañeros.

Se ha añadido una estrella a todos los repositorios campusciff de los compañeros mencionados antes.

## 2.24 CREAR UNA TABLA
1. Crear una tabla de este estilo en el fichero README.md con la información de varios de tus 

compañeros de clase:

| NOMBRE                      | GITHUB                                               |
| --------------------------- | ---------------------------------------------------: |
|  ciffSara                   |  [link perfil](http://github.com/ciffSara)           |
|  cabreracanal               |  [link perfil](http://github.com/elelement)          |
|  Alejandro Diaz             |  [link perfil](http://github.com/adiazgalache)       |
|  PalomaCiffBigData          |  [link perfil](http://github.com/PalomaCiffBigData)  |
|  Danielobit                 |  [link perfil](http://github.com/Danielobit)         |
|  macarenagaranena           |  [link perfil](http://github.com/macarenagaranena)   |
|  Miriam Asenjo              |  [link perfil](http://github.com/Miriam-Asenjo)      |
|  Cristobal Rodríguez Fraile |  [link perfil](http://github.com/crisrodfra)         |

## 2.25 COLABORADORES
1. Poner a [github.com/asanzdiego](http://github.com/asanzdiego) como colaborador del repositorio __campusciff__.

(imagen Paso_2.25.png)

## 2.26 CREAR UNA ORGANIZACIÓN
1. Crear una organización llamada __campuscifftunombredeusuariodegithub__.

(imagen Paso_2.26.png)

## 2.27 CREAR EQUIPOS
* Crear 2 equipos en la organización __campuscifftunombredeusuariodegithub__, uno llamado __administradores__ con más permisos y otro __colaboradores__ con menos permisos.

(imagen Paso_2.27.1.png)

* Meter a [github.com/asanzdiego](http://github.com/asanzdiego) y a 2 de vuestros compañeros de clase en el equipo __administradores__.

(imagen Paso_2.27.2.png)

3. Meter a [github.com/asanzdiego](http://github.com/asanzdiego) y a otros 2 de vuestros compañeros de clase en el equipo __colaboradores__.

(imagen Paso_2.27.3.png)

## 2.28 CREAR UN INDEX.HTML
1. Crear un index.html que se pueda ver como página web en la organización.

Se crea un repositorio en la organización. Se crea el archivo html y se sube al repositorio:

```
git clone git@github.com:campusciff-MiguelCerdan/campusciff-MiguelCerdan.github.io.git
cd campusciff-MiguelCerdan.github.io
touch index.html
git add index.html
git commit -m "subido index.html"
git push origin master
```

Se puede ver aquí: [http://campusciff-MiguelCerdan.github.io](http://campusciff-MiguelCerdan.github.io)

## 2.29 CREAR PULL-REQUESTS
* Hacer 2 forks de 2 repositorios __campuscifftunombredeusuariodegithub.github.io__ de 2 organizaciones de las que no seais ni administradores ni colaboradores.

Hago fork a los repositorios:
- [http://campusciff-goaluix.github.io](http://campusciff-goaluix.github.io)
- [http://campusciff-edugago.github.io](http://campusciff-edugago.github.io)

(Imagen Paso_2.29.1.png)

Clono los repositorios en repositorio local:

```
git clone git@github.com:MiguelCerdan/campusciff-goaluix.github.io.git
git clone git@github.com:MiguelCerdan/campusciff-edugago.github.io.git
```

* Crearos una rama en cada fork.

Para cada uno:

```
cd campusciff-goaluix.github.io
git branch rama_MiguelCerdan
```

* En cada rama modificar el fichero index.html añadiendo vuestro nombre.

```
git checkout rama_MiguelCerdan
echo "Saludos fisicos." >> index.html
echo "Miguel Cerdan" >> index.html
```

Subo los cambios al repositorio:

```
git add .
git commit -m "Miguel Cerdán"
git push origin rama_MiguelCerdan
cd ..

```

Se repiten los mismos pasos con campusciff-edugago.github.io

* Con cada rama hacer un pull-request.

Solicito pull request en "Compare & pull request" sobre la rama que yo mismo he creado:

(Imagen Paso_2.29.4.png)

Los compañeros aceptan mis pull request:

(Imagen Paso_2.29.4b.png)

## 2.30 GESTIONAR PULL-REQUESTS
1. Aceptar los pull-request que lleguen a los repositorios de tu organización.

Todavía no hay solicitudes de pull request.
