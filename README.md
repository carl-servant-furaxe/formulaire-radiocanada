# Formulaire de concours Radio-Canada

## Valeurs a modifier pour chaques Concours
- Meta Title (ligne #4)
- H1 (ligne #21)
- Champs du mode de participation (lignes #93 a #96)
- Opt-in (lignes #102, #105 et #108)
- Url du reglement (ligne #120)

## Version au CSS
Il est preferable d'ajouter une valeur "?20190101" au lien qui appelle la feuille de style.
Cela force le navigateur a charger le version la plus a jour du code CSS.
Cela evite des problemes avec la cache des navigateurs des clients.

```
ex <link rel="stylesheet" type="text/css" href="assets/css/style.css?20190101" />
```

## Champs du mode de participation
Selon le type de concours, les champs peuvent changer. Il est important de respecter les codes mis a notre dispositions par Radio-Canada.
Dans le doute, contacter Ginette Delage.

Cette partie de code sera retravaillee par l'equipe Radio-Canada. Il ne faut donc pas appliquer de CSS a ces champs.
Si vous devez appliquer une style precis, il faut en discuter avec l'equipe avant de commencer le travail.

### Champs Indice
Utiliser champs "reponseIndice".
```
<label for="reponseIndice">Notez l'indice sur <a href="https://ici.exploratv.ca/" target="_blank">ICI EXPLORA</a> <span class="req">*</span></label>
<input type="text" name="reponseIndice" id="reponseIndice" size="32" maxlength="256" required />
```

### Champs texte sur une ligne
```
<div id="divQuestion_1" class="classQuestion"><span class="Num">1. </span>De quelle couleur etait la chemise de l'animateur?</div>
<div id="divReponse_1_1" class="classReponse"><input type="text" id="reponse_1" size="30" name="reponse_6239" maxlength="128"></div>
```

### Champs texte sur plusieurs lignes
```
<div id="divQuestion_1" class="classQuestion"><span class="Num">1. </span>Identifiez le nom de l'artiste et le titre de sa performance musicale :</div>
<div id="divReponse_1_1" class="classReponse"><textarea id="reponse_1" cols="50" rows="7" name="reponse_6241"></textarea></div>
```

### Champs choix deroulant (select)
```
<div id="divQuestion_1" class="classQuestion"><span class="Num">1. </span>Pour la diffusion du ??</div>
<div id="divReponse_1_1" class="classReponse">
	<select id="reponse_1" name="reponse_6240">
		<option value="0">Selectionnez...</option>
		<option value="36166">lundi 28 juillet (rediff. mardi 29 juillet)</option>
		<option value="36167">mardi 29 juillet (rediff. mercredi 30 juillet)</option>
		<option value="36168">mercredi 30 juillet (rediff. jeudi 31 juillet)</option>
		<option value="36169">jeudi 31 juillet (rediff. vendredi 1er juillet)</option>
	</select>
</div>
```

### Champs cases a cocher (checkbox)
```
<div id="divQuestion_1" class="classQuestion"><span class="Num">1. </span>Cochez le nom des invites qui ont ete recus a l'emission entre le lundi 6&nbsp;juillet et le vendredi 10&nbsp;juillet&nbsp;:</div>
<div id="divReponse_1_1" class="classReponse"><input type="checkbox" id="reponse_1" name="reponse_6242" value="36173">Melissa Desormeaux-Poulin</div>
<div id="divReponse_1_2" class="classReponse"><input type="checkbox" id="reponse_2" name="reponse_6242" value="36174">Anne-Marie Cadieux</div>
<div id="divReponse_1_3" class="classReponse"><input type="checkbox" id="reponse_3" name="reponse_6242" value="36175">Philippe Fehmiu</div>
<div id="divReponse_1_4" class="classReponse"><input type="checkbox" id="reponse_4" name="reponse_6242" value="36176">Dany Turcotte</div>
<div id="divReponse_1_5" class="classReponse"><input type="checkbox" id="reponse_5" name="reponse_6242" value="36177">Julianne Cote</div>
```

### Champs cases a cocher choix unique (radio)
```
<div id="divQuestion_1" class="classQuestion"><span class="Num">1. </span>Indiquez votre forfait prefere parmi ceux a&nbsp;gagner&nbsp;:</div>
<div id="divReponse_1_1" class="classReponse"><input type="radio" id="reponse_1" name="reponse_6243" value="36178">Tourisme Wendake</div>
<div id="divReponse_1_2" class="classReponse"><input type="radio" id="reponse_2" name="reponse_6243" value="36179">Parc aventure Cap Jaseux</div>
<div id="divReponse_1_3" class="classReponse"><input type="radio" id="reponse_3" name="reponse_6243" value="36180">Parc Jean-Drapeau</div>
```

### Champs telechargement de fichier
```
<div class="uploadContainer_0">
	<div class="uploadNom">Photo:</div>
	<div class="uploadChamps">
		<INPUT TYPE="FILE" NAME="Photo">
		<div class="uploadExtensions">(.jpg;.jpeg;.pdf;.gif;.png;.bmp)</div>
	</div>
</div>
```

### Code Genere par Radio-Canada
Ginette precise : "Pour la boite texte ou le participant tape son histoire, on a deux options, et je te laisse choisir entre les deux, puisque du cote "fonctionnel" pour la gestion de ce concours-ci (stats, tirage et cie), ca ne fait pas de difference, mais pour que tu puisses mettre un decompte pour les caracteres, ca pourrait en faire une. "

#### faire une "question"
Avec cette option, on ne peut rien modifier aux div generes, ni en inserer d'autres entre eux, ou ajouter/modifier, ni class, ni id, ni name (le name du champs varie d'une option de reponse a l'autre et est attribue par l'Admin Concours); la seule partie editable, c'est ou on trouve le texte de la question)

```
<div id="divQuestion_1" class="classQuestion"><span class="Num">1. </span>Ton histoire en 200 mots ou moins</div> <div id="divReponse_1_1" class="classReponse"><textarea id="reponse_1" cols="50" rows="7" name="reponse_5965"></textarea></div
```

#### utiliser un champ du type "Autre
Dans la deuxieme option, on garde evidemment les name et id tels quels, mais sinon tu peux lui ajouter ce que tu veux, modifier son format : c'est un champ qui est dans le code html, comme les input Nom,  Prenom, Age...

```
<label for="autre1">Ton histoire en 200 mots ou moins</label>  <textarea name="autre1" id="autre1" cols="70" rows="5"></textarea
```



## Opt-in

### Declaration
Le premier optin qui declare que la personne a bien pris connaissance du reglement.
tres important de changer le URL du reglement

```
<div class="field field-declaration">
	<label for="declaration" class="label-checkbox"><input type="checkbox" name="declaration" id="declaration" /><span class="label-text">J'ai lu et j'accepte le <a href="https://ici.radio-canada.ca/concours-revelezvotrestyle/reglement.pdf" target="_blank" title="règlement du concours">règlement du concours</a>. <span class="req">*</span></span></label>
</div>
```

### Transmettre Info
Le premier opt-in est souvent celui reserve au communications de Radio-Canada.

```
<div class="field field-infolettre">
	<label for="transmettreInfo" class="label-checkbox"><input type="checkbox" name="transmettreInfo" id="transmettreInfo" /><span class="label-text">Je souhaite recevoir des offres et des communications de la part de Radio-Canada.</span></label>
</div>
```

### Transmettre Info #2
Le deuxieme opt-in est pour la plupart du temps reserve au partenaire.
```
<div class="field field-infolettre2">
	<label for="transmettreInfo2" class="label-checkbox"><input type="checkbox" name="transmettreInfo2" id="transmettreInfo2" />
	<span class="label-text">Je souhaite recevoir des offres et des communications de la part de Bota Bota, spa-sur-l'eau.</span></label>
</div>
```

### Transmettre Info #3
Il est possible que parfois un 3e optin soit demande. Son nom doit etre "transmettreInfo3"
```
<div class="field field-infolettre3">
	<label for="transmettreInfo3" class="label-checkbox"><input type="checkbox" name="transmettreInfo3" id="transmettreInfo3" />
	<span class="label-text">Texte de l'optin #3.</span></label>
</div>
```


## Url du reglement
Comme pour le css, je suggere fortement d'ajouter une valeur au url afin de *bypasser* la cache des navigateurs.
Soit en ajoutant "?20190101" ou en nommant le nom du fichier "reglement.pdf" par "reglement-20190101.pdf".
Mais dans le cas d'un changement de nom, s'assurer que le fichier existe sur le serveur et que le meme nom est utilise sur le site du concours.


## Livrer le travail
Il est important de livrer le formulaire le plus vite possible. C'est surtout par respect pour l'equipe Radio-Canada qui doit effectuer du travail sur le code une fois recu. Envoyer 1-2 jours avant la date de lancement du concours ou si possible, plus tot.

Le projet doit etre zippe et attache au courriel. 

*NOTE: Eviter d'ajouter des fichiers JS dans le formulaire. Si un de ces fichiers se retrouve dans le zip, il se pourrait que les filtres anti-spam de Radio-Canada refuse le courriel. Il faut donc rester avec HTML et CSS seulement. Sinon, utilisez Wetransfer pour livrer le travail.*

Les courriels a inclure sont:
- ginette.delage@radio-canada.ca (personne responsable des formulaires)
- studionumerique@radio-canada.ca (equipe de soutien si Ginette n'est pas disponible)
- info@furaxe.qc.ca (Stefan a mettre en CC dans toutes les communications)
- courriel de la chargee de projet
