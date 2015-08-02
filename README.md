*Pasos para actualizar o crear el archivo  documento.json

*se abre una terminal 

*clona la wiki de libgdx o otra que sea github

*Organiza la jerarquia con carpetas

*se ubica en la carpeta anterior a los recursos
-tree -fJ libgdx.wiki/ > tree.json

*luego se elimina dentro del archivo todo lo que contenga el patron libdgc.wiki/ de la siguiente manera
-sed 's/libgdx.wiki\/// ' tree.json > treeD.json

*se mueve el archivo dentro de la carpeta libgdx.wiki
-mv tree.json libgdx.wiki/

*y listo cuando se abra el archivo index.html
-se examina el archivo creado para que carge los recursos

Posdata:
Es necesario realizar las siguientes modificaciones en el archivo js/personalizacion.js

*Linea 3
 -http.open("GET" ,"file:///home/erik/apis/wikiLibgdx/libgdx.wiki/"+e.getAttribute("direccion"),false);
 -http.open("GET" ,"file://ruta hasta la carpeta que contiene los markdown "+e.getAttribute("direccion"),false);

