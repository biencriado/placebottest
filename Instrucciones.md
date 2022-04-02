# placebottest
Bot para visualizar el escudo de Gran Colombia en r/place

![imagen](https://user-images.githubusercontent.com/102851218/161374349-053f10f1-a58f-4a84-b5b2-cc6c14e95b13.png)


Instrucciones 

1. Instalar  
En Chrome/Opera (Tampermonkey)[https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo?hl=en]
o Firefox (Violentmonkey)[https://addons.mozilla.org/en-US/firefox/addon/violentmonkey/]
Yo uso firefox y funciona bien, necesito gente que me reporte si funciona bien en chrome


2. Click en la extension/Añadir nuevo script (+) 

![imagen](https://user-images.githubusercontent.com/102851218/161374456-6f84ae29-0994-4aef-a63d-63ea55eee323.png)

3. Pegar el script 

```
// ==UserScript==
// @name         GranColombiaEscudo
// @namespace    http://tampermonkey.net/
// @version      0.1
// @description  Escudo y estrellas
// @author       oralekin
// @match        https://hot-potato.reddit.com/embed*
// @icon         https://www.google.com/s2/favicons?sz=64&domain=reddit.com
// @grant        none
// ==/UserScript==
if (window.top !== window.self) {
    window.addEventListener('load', () => {
            document.getElementsByTagName("mona-lisa-embed")[0].shadowRoot.children[0].getElementsByTagName("mona-lisa-canvas")[0].shadowRoot.children[0].appendChild(
        (function () {
            const i = document.createElement("img");
            i.src = "https://raw.githubusercontent.com/biencriado/placebottest/main/escudoplacetemplate.png";
            i.style = "position: absolute;left: 0;top: 0;image-rendering: pixelated;width: 1000px;height: 1000px;";
            console.log(i);
            return i;
        })())

    }, false);
    
  }
```

4. Asignar un nombre y guardar y cerrar 

![imagen](https://user-images.githubusercontent.com/102851218/161374574-2f837d5c-43f9-4401-8ec3-9111d2f0c8fb.png)

5. Actualizar la pagina de r/place y sobre la bandera, debe aparecer la guia de dibujo 

![imagen](https://user-images.githubusercontent.com/102851218/161374623-bd77d3ee-d92d-4c19-a4d8-9e4ca43ee599.png)
