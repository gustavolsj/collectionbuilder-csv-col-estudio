{% comment %}
Find some sample images or use defaults for About demos
{% endcomment %}
{% assign imagesample = site.data[site.metadata] | where_exp: 'item','item.format contains "image"' | first %}
{% capture imagesampleid %}{{ imagesample.objectid | default: "https://www.lib.uidaho.edu/collectionbuilder/demo-objects/mg101_b6_photographs_01.jpg" }}{% endcapture %}
{% assign pdfsample = site.data[site.metadata] | where_exp: 'item','item.format contains "pdf"' | first %}
{% capture pdfsampleid %}{{ pdfsample.objectid | default: "https://www.lib.uidaho.edu/collectionbuilder/demo-objects/uiext21768.pdf" }}{% endcapture %}
{% assign videosample = site.data[site.metadata] | where_exp: 'item','item.format contains "video"' | first %}
{% capture videosampleid %}{{ videosample.objectid | default: "https://cdil.lib.uidaho.edu/storying-extinction/objects/trailcams/videos/ballcreek-cedarrub-birdonpath.mp4" }}{% endcapture %}
{% assign audiosample = site.data[site.metadata] | where_exp: 'item','item.format contains "audio"' | first %}
{% capture audiosampleid %}{{ audiosample.objectid | default: "https://www.lib.uidaho.edu/digital/mp3s/Clouds.mp3" }}{% endcapture %}

## Acerca de la página Acerca de

Queremos que las páginas interpretativas atractivas sean más fáciles de crear, así que CollectionBuilder te ofrece herramientas para escribir _con_ el contenido de tu colección.

La plantilla incluye un diseño personalizable para la página "Acerca de", pensado para contenidos largos con inserciones multimedia.
El contenido se escribe en [Markdown](https://guides.github.com/features/mastering-markdown/) y se enriquece mediante "includes" que incorporan contenido de la colección, medios externos y componentes de [Bootstrap](https://getbootstrap.com/) como tarjetas y modales.
Esperamos que esto facilite a quienes construyen el sitio desarrollar la colección y añadir información contextual interesante y atractiva.

Cada archivo "include" tiene varias opciones documentadas dentro del propio archivo. Copia los ejemplos para ver cómo funcionan con tu contenido.
En la demostración siguiente hemos usado anchos de visualización del 25% y 50% para ahorrar espacio, pero puedes destacar la imagen o el documento completo.

También puedes ver una página con [muchas opciones de includes de funciones](https://collectionbuilder.github.io/collectionbuilder-gh/feature_options.html) en nuestro sitio de demostración de CollectionBuilder-GH.

{% include feature/button.html text="Página de muestra de *includes*" link="https://collectionbuilder.github.io/collectionbuilder-gh/feature_options.html" color="primary" size="lg" centered=true %}

### Incluir objetos de la colección

La plantilla ofrece includes para incorporar los objetos y metadatos de la colección a tu página interpretativa, de modo que puedas escribir con los materiales incrustados directamente en el contenido.

#### Incluir una imagen

- Imagen --> `{% raw %}{% include feature/image.html objectid="demo_001" width="75" %}{% endraw %}`

{% include feature/image.html objectid=imagesampleid width="75" %}

#### Incluir un PDF

- PDF -- > `{% raw %}{% include feature/pdf.html objectid="demo_002"  width="50" %}{% endraw %}`

{% include feature/pdf.html objectid=pdfsampleid width="50" %}

#### Incluir un video

- Video: `{% raw %}{% include feature/video.html objectid="demo_004" %}{% endraw %}`

{% include feature/video.html objectid=videosampleid width="75" %}

#### Incluir un archivo de audio

- Audio: `{% raw %}{% include feature/audio.html objectid="demo_003" %}{% endraw %}`

{% include feature/audio.html objectid=audiosampleid  %}

### Incluir componentes de Bootstrap

La plantilla también proporciona includes para facilitar la incorporación de componentes de [Bootstrap](https://getbootstrap.com/) a tu escritura en Markdown.
Estas funciones te permiten organizar y resaltar mejor el contenido.

#### Incluir una tarjeta

- Tarjeta -- > `{% raw %}{% include feature/card.html header="Esta es una tarjeta" text="La tarjeta muestra una imagen de la colección como encabezado" objectid="demo004" width="25" centered=true %}{% endraw %}`

{% include feature/card.html header="Esta es una tarjeta" text="La tarjeta muestra una imagen de la colección como encabezado" objectid=imagesampleid width="50" centered=true %}

#### Incluir un botón

- Botones -- > `{% raw %}{% include feature/button.html text="Botón con enlace" link="https://collectionbuilder.github.io/" color="success" %}{% endraw %}`

{% include feature/button.html text="Botón con enlace" link="https://collectionbuilder.github.io/" color="success" centered=true %}

#### Incluir una alerta

- Alertas -- > `{% raw %}{% include feature/alert.html text="esta es una *alerta* que avisa al usuario" color="warning" align="center" %}{% endraw %}`

{% include feature/alert.html text="Esta es una *alerta* que avisa al usuario con texto centrado." color="warning" align="center"  %}

#### Incluir un modal

- Modales -- > `{% raw %}{% include feature/modal.html button="Este es un modal con un botón de color 'primary'" title="al hacer clic:" text="Se abrirá una ventana con información adicional" color="primary"  %}{% endraw %}`

{% include feature/modal.html button="Este es un modal con un botón de color 'primary'" title="Al hacer clic:" text="Se abrirá una ventana con información adicional" color="primary"  %}
