<p style="text-align: justify;"><span style='font-family: "Trebuchet MS", Helvetica, sans-serif; font-size: 24px; color: rgb(61, 142, 185);'><strong>&iquest;C&oacute;mo usar la LCD TFT ILI9163 con ESP32 ? &iexcl;Muy f&aacute;cil!</strong></span></p>
<p style="text-align: justify;"><span style="font-family: 'Trebuchet MS', Helvetica, sans-serif;">Para poder desarrollar este proyecto lo m&aacute;s concreto posible, debemos antes que nada hablar de la <a href="https://parsek.com.co/lcd-tft-144-128x128" rel="noopener noreferrer" target="_blank"><span style="color: rgb(61, 142, 185);">LCD TFT ILI9163</span></a>. Esta LCD es una gran opci&oacute;n si deseas tener una visualizaci&oacute;n m&aacute;s detallada de tus proyectos, puesto que cuenta con una resoluci&oacute;n de 128x128 pixeles y un tama&ntilde;o 1.44&rdquo;, lo que significa 2.6x2.6 cm. &nbsp;Con esta LCD somos capaces de mostrar hasta 262 mil colores diferentes y su comunicaci&oacute;n se realiza por SPI.&nbsp;</span></p>
<p style="text-align: justify;"><span style="font-family: 'Trebuchet MS', Helvetica, sans-serif;">En cuanto al sistema embebido de este proyecto se escogi&oacute; el microcontrolador ESP32, el cual cuenta con comunicaci&oacute;n SPI y su programaci&oacute;n puede ser desde el IDE de Arduino.</span></p>

------------

<p style="text-align: justify;"><span style='font-family: "Trebuchet MS", Helvetica, sans-serif; color: rgb(61, 142, 185);'><strong>PREPARACI&Oacute;N DEL ENTORNO DE DESARROLLO</strong></span></p>
<p style="text-align: justify;"><span style="font-family: 'Trebuchet MS', Helvetica, sans-serif;">Para empezar, debemos abrir el IDE de Arduino y agregar la siguiente URL que permitir&aacute; usar la placa ESP32. &nbsp;Para ello ve &nbsp;a <strong>File &gt; Preference</strong>&nbsp; y agrega la URL.</span></p>

`<link>` : https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json

<p align="center" width="100%">
    <img width="60%" src="https://parsek-pro-public-images-bucket.s3.us-east-2.amazonaws.com/large/428058821.png" alt="URLESP32"> 
</p>
<p style="text-align: justify;"><span style="font-family: 'Trebuchet MS', Helvetica, sans-serif;">Una vez realizado este paso, sigue la instalaci&oacute;n de la librer&iacute;a de la ESP32. Para ello ve a <strong>Tools&gt;Board&gt;Boards Manager</strong>,&nbsp;escribe ESP32 e instalas la primera opci&oacute;n esp32 by Espressif.</span></p>

<p align="center" width="100%">
    <img width="50%" src="https://parsek-pro-public-images-bucket.s3.us-east-2.amazonaws.com/large/2021105196.png" alt="LIBRERIAESP32"> 
</p>


<p style="text-align: justify;"><span style="font-family: 'Trebuchet MS', Helvetica, sans-serif;">Con esto tenemos listo el microcontrolador para usarlo sin ning&uacute;n problema. Para el caso de la LCD TFT basta con agregar la carpeta, la cual se puede descargar en el siguiente link, a la carpeta que se encuentra en tu computador con la siguiente dirección <strong>C:\Users\Documents\Arduino\libraries.</strong></span></p>

`<link>` : [libreria de la TFT ILI9163C](https://github.com/sumotoy/TFT_ILI9163C)

<p style="text-align: justify;"><span style="font-family: 'Trebuchet MS', Helvetica, sans-serif;">Una vez hayas copiado la carpeta en tu computador, dentro del entorno de Arduino podemos agregar la librer&iacute;a si vamos a <strong>Sketch&gt;include library&gt; Add .ZIP Library</strong> y seleccionamos la carpeta previamente descargada.</span></p>

<p align="center" width="100%">
    <img width="50%" src="https://parsek-pro-public-images-bucket.s3.us-east-2.amazonaws.com/large/4010512192.png" alt="LIBRERIATFT"> 
</p>

------------


<p style="text-align: justify;"><span style="font-family: 'Trebuchet MS', Helvetica, sans-serif;"><strong><span style="color: rgb(61, 142, 185);">CODIGO EN EL IDE ARDUINO</span></strong></span></p>
<p style="text-align: justify;"><span style="font-family: 'Trebuchet MS', Helvetica, sans-serif;">Para poder visualizar una imagen en la LCD, hacemos uso de un programa llamado &nbsp;&ldquo;LCD image Converter&rdquo; que convierte las im&aacute;genes de cualquier tama&ntilde;o a un vector hexadecimal que podemos leer desde el entorno de arduino. Es importante recordar que las im&aacute;genes que convirtamos deben estar en un tama&ntilde;o de 128x128 p&iacute;xeles para ajustarnos al tama&ntilde;o de la LCD y el formato que se debe configurar en el programa debe ser el de RGB565.</span></p>

`<link>` : [programa &ldquo;LCD image Converter&rdquo;](https://sourceforge.net/projects/lcd-image-converter/)

<p align="center" width="100%">
    <img width="50%" src="https://parsek-pro-public-images-bucket.s3.us-east-2.amazonaws.com/large/1852811696.png" alt="LCDCONVERTER"> 
</p>

<p style="text-align: justify;"><span style="font-family: 'Trebuchet MS', Helvetica, sans-serif;"><strong>Con esto estamos listos para programar !</strong></span></p>

------------

<p><span style="color: rgb(61, 142, 185);"><strong><span style="font-family: 'Trebuchet MS', Helvetica, sans-serif;">CONEXIONES</span></strong></span></p>
<p><span style="font-family: 'Trebuchet MS', Helvetica, sans-serif;">Para este proyecto puedes realizar las siguientes conexiones.</span></p>


<p align="center" width="100%">
    <img width="70%" src="https://parsek-pro-public-images-bucket.s3.us-east-2.amazonaws.com/large/2293711299.png" alt="LIBRERIAESP32"> 
</p>


<p><span style='font-size: 16px; font-family: "Trebuchet MS", Helvetica, sans-serif; color: rgb(0, 0, 0); background-color: transparent; font-weight: 400; font-style: normal; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;'>Con esto puedes agregar distintas im&aacute;genes y mejorar la visualizaci&oacute;n de tus proyectos! &nbsp;</span></p>


<p align="center" width="100%"><img width="60%" src="https://parsek-pro-public-images-bucket.s3.us-east-2.amazonaws.com/large/2021105196.jpg" alt="LCDTFTRES2"><img width="60%" src="https://parsek-pro-public-images-bucket.s3.us-east-2.amazonaws.com/large/2706773801.jpg" alt="LCDTFTRES1"></p>