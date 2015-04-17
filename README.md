
<h2> CakePHP3-ImageHelper</h2>
L'objectif principal de ce Helper CakePHP est de vous donner la possibilité de redimensionner une image sans maux de tête.

<h2>Exigences</h2>
<ul>
	<li>
		CakePHP 3.x
	</li>
	<li>
		PHP Gd library
	</li>
</ul>

<h2>Installation</h2>
Chargez l'assistant au contrôleur désiré. Ou tout simplement au AppController.php

<pre>
	<code>	
		public $helpers = ['Image']; 
	</code>
</pre>

<h2>Utilisation</h2>
Remplacer la fonction standard de CakePHP:

<pre>
	<code>
		~~$this->Html->image('path/image.[png|jpg|gif]', 'options' => array());~~

		$this->Image->resize('path/image.[png|jpg|gif]', width, height, 'options' => array(), 'quality' => 100);

		// Va Générer une image dans path/image_widthxheight.[png|jpg|gif] (la transparence est gardé)
		// contenu géneré 

		<img src="path/image_widthxheight.[png|jpg|gif]" width="width" height="height"/>
	</code>
</pre>

Le 4ème paramètre est le même que le 2ème paramètre de HtmlHelper :: l'image ()

Le 5ème paramètre est la qualité d'image