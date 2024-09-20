{% assign imagesample = site.data[site.metadata] | where_exp: 'item','item.format contains "image"' | first %}
{% capture imagesampleid %}{{imagesample.objectid | default: "https://www.lib.uidaho.edu/collectionbuilder/demo-objects/mg101_b6_photographs_01.jpg"}}{% endcapture %}
{% assign pdfsample = site.data[site.metadata] | where_exp: 'item','item.format contains "pdf"' | first %}
{% capture pdfsampleid %}{{pdfsample.objectid | default: "https://www.lib.uidaho.edu/collectionbuilder/demo-objects/uiext21768.pdf"}}{% endcapture %}
{% assign videosample = site.data[site.metadata] | where_exp: 'item','item.format contains "video"' | first %}
{% capture videosampleid %}{{videosample.objectid | default: "https://cdil.lib.uidaho.edu/storying-extinction/objects/trailcams/videos/ballcreek-cedarrub-birdonpath.mp4"}}{% endcapture %}
{% assign audiosample = site.data[site.metadata] | where_exp: 'item','item.format contains "audio"' | first %}
{% capture audiosampleid %}{{audiosample.objectid | default: "https://www.lib.uidaho.edu/digital/mp3s/Clouds.mp3"}}{% endcapture %}

## ¿Qué es Bicinefilos? 

Bogotá ha sido el epicentro y locación de películas icónicas como La estrategia del Caracol o La gente de La Universal, sin embargo, es poco lo que se conoce sobre los lugares donde se han filmado y el valor histórico y arquitectónico que tienen. Bicinefilos es un mapa interactivo que destaca las locaciones icónicas de películas colombianas filmadas en Bogotá. Con esta cartografía buscamos mapear estos lugares que han quedado registrados en la pantalla, y reafirmar su importancia dentro de nuestro patrimonio cinematográfico.

Este proyecto busca desarrollar nuevas formas de interacción entre el público y el cine colombiano al incorporar las películas en la cotidianidad de los espectadores. Además, pretende abrir el diálogo a nuevos significados de los lugares emblemáticos de Bogotá como la Plaza de Bolívar que han sido retratados en la pantalla y cargados narrativamente. Estas interacciones con el público posibilitan una activación de las películas a través de un ejercicio del derecho a la ciudad y el fortalecimiento de las relaciones entre la ciudadanía y el espacio público.
 
Esta investigación, al contrastar el registro fílmico con el estado actual de estos espacios, permite evidenciar las transformaciones arquitectónicas y los procesos de renovación urbanización que ha presenciado Bogotá a lo largo de su historia.

## Tercer cine

Bicinéfilos es desarrollado por Tercer Cine, que es una plataforma creativa enfocada en la investigación y difusión del cine colombiano. Esta plataforma se especializa en generar reflexiones sobre las representaciones y la importancia histórica y social de dicho cine. Por tanto, Bicinéfilos es uno de estos proyectos investigativos que se enfoca en reconocer las trasformaciones del espacio público a través del patrimonio cinematográfico. Así, el cine y el reconocimiento de las locaciones donde se grabaron sus icónicas escenas, se vuelve parte crucial del proceso de apropiación del espacio público por parte de los espectadores. 

Si desea comprender más del trabajo que adelanta este equipo por el cine colombiano, puede consultar: INCLUIR BOTONES CON LINKS

Tercer cine está compuesto por un equipo interdisciplinar tales como:

Laura Arias, Politóloga e investigadora de cine;
Juliana Santana, Profesional en Cine y comunicación digital;
Jorge Rojas, Músico y productor musical;
Jonathan Hurtado, Politólogo y Magíster en Humanidades digitales;
Miguel Moyano, Artista y diseñador digital. 


We want to make engaging interpretive pages easier to create, so CollectionBuilder gives you tools to write *with* your collection content!

The template comes with a customizable "About" page layout designed for long form content with rich media embeds.
Content is written in [Markdown](https://guides.github.com/features/mastering-markdown/) and enhanced using "includes" that pull in collection content, external media, and [Bootstrap](https://getbootstrap.com/) features like cards and modals.
We hope this makes it easier for site builders to develop the collection AND add interesting and engaging contextual information. 

Each "include" file has several options, which are documented in the files themselves--copy the examples to see how it works with your content! 
In the demo below, we've given display widths of 25% and 50% to save space, but you can feature the entire image or document.

You can also see a page featuring [a bonanza of feature includes options](https://collectionbuilder.github.io/collectionbuilder-gh/feature_options.html) on our CollectionBuilder-GH demo site. 

{% include feature/button.html text="Feature *Includes* Bonanza page" link="https://collectionbuilder.github.io/collectionbuilder-gh/feature_options.html" color="primary" size="lg" centered=true %}

### Include Collection Items

The template provides includes to pull your collection objects and metadata into your interpretive page, allowing you to write with your materials directly embedded in the content.

#### Include an Image

- Image --> `{% raw %}{% include feature/image.html objectid="demo_001" width="75" %}{% endraw %}`

{% include feature/image.html objectid=imagesampleid width="75" %}

#### Include a PDF

- PDF -- > `{% raw %}{% include feature/pdf.html objectid="demo_002"  width="50" %}{% endraw %}`

{% include feature/pdf.html objectid=pdfsampleid width="50" %}

#### Include a Video

- Video: `{% raw %}{% include feature/video.html objectid="demo_004" %}{% endraw %}`

{% include feature/video.html objectid=videosampleid width="75" %}

#### Include an Audio File

- Audio: `{% raw %}{% include feature/audio.html objectid="demo_003" %}{% endraw %}`

{% include feature/audio.html objectid=audiosampleid  %}

### Include Bootstrap Features

The template also provides includes to make it easier to add [Bootstrap](https://getbootstrap.com/) components to your Markdown writing.
These features allow you to better organize and highlight your content.

#### Include a Card

- Card -- > `{% raw %}{% include feature/card.html header="This is a Card" text="The card features an image from the collection as a cap" objectid="demo004" width="25" centered=true %}{% endraw %}`

{% include feature/card.html header="This is a Card" text="The card features an image from the collection as a cap" objectid="demo_001" width="25" centered=true %}

#### Include a Button 

- Buttons -- > `{% raw %}{% include feature/button.html text="Button Link to Somewhere" link="https://collectionbuilder.github.io/" color="success" %}{% endraw %}`

{% include feature/button.html text="Button Link to Somewhere" link="https://collectionbuilder.github.io/" color="success" centered=true %}
  
#### Include an Alert

- Alerts -- > `{% raw %}{% include feature/alert.html text="this is an *alert* that 'warns' a user" color="warning" align="center" %}{% endraw %}`

{% include feature/alert.html text="This is an *alert* that 'warns' a user with centrally aligned text." color="warning" align="center"  %}

#### Include a Modal

- Modals -- > `{% raw %}{% include feature/modal.html button="This is a modal using a 'primary' colored button to invite clicking" title="when clicked:" text="A Modal will pop out a box with some more information" color="primary"  %}{% endraw %}`

{% include feature/modal.html button="This is a modal using a 'primary' colored button to invite clicking" title="When clicked:" text="A Modal will pop out a box with some more information" color="primary"  %} 
