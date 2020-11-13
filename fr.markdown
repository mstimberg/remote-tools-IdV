---
lang: fr
layout: default
title: Outils pour travail à distance
---

<script src="https://kit.fontawesome.com/2b48dbc3a6.js" crossorigin="anonymous"></script>
{% assign windows="<i class='fab fa-windows'></i>" %}
{% assign osx="<i class='fab fa-apple'></i>" %}
{% assign linux="<i class='fab fa-linux'></i>" %}
{% assign web="<i class='fas fa-globe'></i>" %}
{% assign android="<i class='fab fa-google-play'></i>" %}
{% assign iphone="<i class='fab fa-app-store-ios'></i>" %}
{% assign lock="<i class='fas fa-lock'></i>" %}

{% assign inserm="<span title='INSERM' style='color: #e74011;'><b>🅘</b></span>" %}
​⃰{% assign inserm-eu="<span title='INSERM (compte .eu)' style='color: #e74011;'><b>🅘¹</b></span>" %}
{% assign cnrs="<span title='CNRS' style='color: #62c4dd;'><b>🅒</b></span>" %}
{% assign sorbonne="<span title='Sorbonne Université' style='color: #ffb500;'><b>🅢</b></span>" %}
{% capture renater %}
{{inserm}}&thinsp;{{cnrs}}&thinsp;{{sorbonne}}
{% endcapture %}

<div class="container">
<h1>Outils pour travail à distance</h1>
<div class="row">
<div class="col md-4">{{ inserm}} INSERM</div>
<div class="col md-4">{{ cnrs}} CNRS</div>
<div class="col md-4">{{ sorbonne}} Sorbonne Université</div>
</div>
<div class="row">
<div class="col md-12">
<h3 class="mt-2">Table des matières</h3>
</div>
</div>
<div class="row justify-content-left">
<div class="col-3">
<ul>
<li><a href="#video">Visio-conférence</a></li>
<li><a href="#storage">Stockage/partage de fichiers</a></li>
<li><a href="#chat">Chat + partage de fichier</a></li>
</ul>
</div>
<div class="col-3"></div>
<ul>
<li><a href="#publication">Accès aux publications</a></li>
<li><a href="#software">Logiciels</a></li>
</ul>
</div>
<section id="video">
<h2 class="mt-5"><i class="fas fa-video"></i>&nbsp; Visio-conférence (<q>comme <i>Zoom</i></q>)</h2>
{% capture web-mobile-compat %}{{web}}&thinsp;{{android}}&thinsp;{{iphone}}{% endcapture %}
{% capture all-but-web %}{{windows}}&thinsp;{{osx}}&thinsp;{{linux}}&thinsp;{{android}}&thinsp;{{iphone}}{% endcapture %}
{% capture all-but-linux %}{{windows}}&thinsp;{{osx}}&thinsp;{{web}}&thinsp;{{android}}&thinsp;{{iphone}}{% endcapture %}
{% capture all-compat %}{{windows}}&thinsp;{{osx}}&thinsp;{{linux}}&thinsp;{{web}}&thinsp;{{android}}&thinsp;{{iphone}}{% endcapture %}
{% capture all-desktop %}{{windows}}&thinsp;{{osx}}&thinsp;{{linux}}{% endcapture %}

{% include software_box.html service-name="Teams" service-provider=inserm-eu
   software-compatibility=all-compat software-name="Microsoft Teams" software-link="https://teams.microsoft.com/"
   links="<a href='https://teams.microsoft.com/' class='btn btn-primary'>Web interface &nbsp;<i class='fas fa-lock'></i></a>|<a href='https://intranet.inserm.fr/actualites/Pages/detail.aspx?news_id=284'  class='btn btn-primary'>INSERM documentation</a>" free-text="<span style='color: #e74011;'>¹</span>&nbsp; Nécessite un compte <code>@inserm.eu</code>. Les identifants ont été envoyé par mail en mars 2020. En cas de besoin, contactez <a href='https://siou.inserm.fr/'>siou.inserm.fr</a>." %}

{% include software_box.html service-name="Rendez-Vous" service-provider=renater
   software-compatibility=web-mobile-compat software-name="Jitsi Meet" software-link="https://jitsi.org/jitsi-meet/"
   links="<a href='https://rendez-vous.renater.fr/home/' class='btn btn-primary'>Web interface &nbsp;<i class='fas fa-lock'></i></a>|<a href='https://jitsi.github.io/handbook/docs/intro'  class='btn btn-primary'>Jitsi documentation</a>|<a href='https://services.renater.fr/voix_et_image/rdv/user_guide' class='btn btn-primary'>RENATER documentation</a>" free-text="Nombre maximale de participants en simultané: 5 to 10 (seulement audio), 4 to 5 (vidéo)" %}

{% include software_box.html service-name="Tixeo" service-provider=cnrs
   software-compatibility=all-but-web software-name="Tixeo" software-link="https://www.tixeo.com/"
   links="<a href='https://tixeo.cnrs.fr' class='btn btn-primary'>Interface web&nbsp;<i class='fas fa-lock'></i></a>|<a href='https://aide.core-cloud.net/si/tixeo/SitePages/Accueil.aspx' class='btn btn-primary'>Documentation CNRS</a>" %}

</section>
<section id="storage">
<h2 class="mt-5"><i class="far fa-hdd"></i>&nbsp; Stockage/partage de fichiers (<q>comme <i>Dropbox</i></q>)</h2>
{% include software_box.html service-name="DropSU" service-provider=sorbonne
   software-compatibility=all-compat software-name="Nextcloud" software-link="https://nextcloud.com/files/" free-text="Offre 100&nbsp;Go d'espace; Documents/fichiers peuvent être partagés avec des utilisateurs externes sans compte; Installation OnlyOffice pour édition collaboratif des documents MS Office"
   links="<a href='https://dropsu.sorbonne-universite.fr/' class='btn btn-primary'> Interface web&nbsp;<i class='fas fa-lock'></i></a>|<a href='https://nextcloud.support/com/' class='btn btn-primary'>Documentation Nextcloud</a>|<a href='https://intranet.sorbonne-universite.fr/fr/procedures-et-services/informatique/outils-documentaires-collaboratifs.html' class='btn btn-primary'>Documentation Sorbonne&nbsp;<i class='fas fa-lock'></i></a>" %}

{% include software_box.html service-name="MyCore" service-provider=cnrs
   software-compatibility=all-compat software-name="ownCloud" software-link="https://owncloud.com/" free-text="Offre 100&nbsp;Go d'espace; Documents/fichiers peuvent être partagés avec des utilisateurs externes sans compte"
   links="<a href='https://mycore.core-cloud.net/index.php/login' class='btn btn-primary'>Interface web&nbsp;<i class='fas fa-lock'></i></a>|<a href='https://owncloud.com/docs-guides/' class='btn btn-primary'>Documentation ownCloud</a>|<a href='https://confluence.cnrs.fr/confluence/pages/viewpage.action?spaceKey=ODSCORE&title=Aide+utilisateur' class='btn btn-primary'>Documentation CNRS&nbsp;<i class='fas fa-lock'></i></a>" %}

{% include software_box.html service-name="iBox" service-provider=inserm
   software-compatibility=all-compat software-name="Nextcloud" software-link="https://nextcloud.com/files/" free-text="Offre 25&nbsp;Go d'espace; Documents/fichiers peuvent être partagés avec des utilisateurs externes sans compte"
   links="<a href='https://ibox.inserm.fr' class='btn btn-primary'>Web interface&nbsp;<i class='fas fa-lock'></i></a>|<a href='https://nextcloud.com/support/' class='btn btn-primary'>Documentation Nextcloud</a>|<a href='https://intranet.inserm.fr/services-et-support-informatique/Documents/ibox-utilisateurs-v3.pdf' class='btn btn-primary'>Documentation INSERM&nbsp;<i class='fas fa-lock'></i></a>" %}
</section>
<section id="chat">
<h2 class="mt-5"><i class="far fa-comment-dots"></i>&nbsp; Chat + partage de fichier (<q>comme <i>Slack</i></q>)</h2>
{% include software_box.html service-name="Citadel" service-provider=cnrs
   software-compatibility=all-but-linux software-name="Citadel Team" software-link="https://citadel.team/" free-text="Fonctionalité assez basique"
   links="<a href='https://cnrs.citadel.team/' class='btn btn-primary'>Interface web&nbsp;<i class='fas fa-lock'></i></a>|<a href='https://support.citadel.team/kb' class='btn btn-primary'>Citadel support</a>|<a href='https://aide.core-cloud.net/si/citadel/SitePages/Accueil.aspx' class='btn btn-primary'>Documentation CNRS&nbsp;<i class='fas fa-lock'></i></a>" %}
</section>
<section id="publication">
<h2 class="mt-5"><i class="far fa-newspaper"></i>&nbsp; Accès aux publications</h2>
<p>La méthode d'accès décrit ci-dessous peut être automatisé par un module
complémentaire de navigateur comme <i>ezProxy</i> (<a href="https://addons.mozilla.org/en-US/firefox/addon/ezproxy-redirect-foxified/"><i class="fas fa-download"></i>&nbsp;Firefox Add-On</a>, <a href="https://chrome.google.com/webstore/detail/ezproxy-redirect/gfhnhcbpnnnlefhobdnmhenofhfnnfhi"><i class="fas fa-download"></i>&nbsp;Chrome Extension</a>).</p>
{% include biblio_box.html service-name="Inserm biblio" service-provider=inserm portal-url="insermbiblio.inist.fr/" direct-url="proxy.insermbiblio.inist.fr/login?url=" %}

{% include biblio_box.html service-name="insb bib cnrs" service-provider=cnrs portal-url="bib.cnrs.fr" direct-url="insb.bib.cnrs.fr/login?url=" %}

{% include biblio_box.html service-name="Sorbonne Portail Documentaire" service-provider=sorbonne portal-url="documentation.sorbonne-universites.fr/ressources/ressources-electroniques.html" direct-url="proxy.insermbiblio.inist.fr/login?url=" %}
</section>
<section id="software">
<h2 class="mt-5"><i class="fas fa-laptop-code"></i>&nbsp; Logiciels</h2>
<p>Licences <q>Campus</q> pour tous les membres de Sorbonne Université</p>

{% include software_box.html service-name="Antivirus (Kapersky)" service-provider=sorbonne software-name="Kapersky Anti-Virus" software-link="https://www.kaspersky.fr/antivirus" software-compatibility=all-desktop links="<a href='http://logiciels.upmc.fr/fr/marches_conclus_par_l_upmc/antivirus.html' class='btn btn-primary'>Sorbonne Campus Licence&nbsp;<i class='fas fa-lock'></i></a>"%}


{% include software_box.html service-name="Matlab" service-provider=sorbonne software-name="Matlab" software-link="https://fr.mathworks.com/" software-compatibility=all-desktop links="<a href='http://logiciels.upmc.fr/fr/marches_conclus_par_l_upmc/matlab/lic_standalone_personnel.html' class='btn btn-primary'>Licence employé&nbsp;<i class='fas fa-lock'></i></a>|<a href='http://logiciels.upmc.fr/fr/marches_conclus_par_l_upmc/matlab/lic_standalone_etudiant.html' class='btn btn-primary'>Licence étudiant&nbsp;<i class='fas fa-lock'></i></a>"%}

{% include software_box.html service-name="Mathematica" service-provider=sorbonne software-name="Mathematica" software-link="https://www.wolfram.com/mathematica/" software-compatibility=all-desktop links="<a href='http://logiciels.upmc.fr/fr/marches_conclus_par_l_upmc/mathematica.html' class='btn btn-primary'>Sorbonne Campus Licence&nbsp;<i class='fas fa-lock'></i></a>"%}

{% include software_box.html service-name="Maple" service-provider=sorbonne software-name="Maple" software-link="https://www.maplesoft.com/" software-compatibility=all-desktop links="<a href='http://logiciels.upmc.fr/fr/marches_conclus_par_l_upmc/maple.html' class='btn btn-primary'>Sorbonne Campus Licence&nbsp;<i class='fas fa-lock'></i></a>"%}
</section>
</div>
