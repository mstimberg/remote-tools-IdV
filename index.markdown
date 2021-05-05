---
lang: en
layout: default
title: Tools for remote working
---

<script src="https://kit.fontawesome.com/2b48dbc3a6.js" crossorigin="anonymous"></script>
{% assign windows="<i class='fab fa-windows' title='Windows'></i>" %}
{% assign osx="<i class='fab fa-apple' title='OS X'></i>" %}
{% assign linux="<i class='fab fa-linux' title='Linux'></i>" %}
{% assign web="<i class='fas fa-globe' title='Web'></i>" %}
{% assign android="<i class='fab fa-google-play' title='Android'></i>" %}
{% assign iphone="<i class='fab fa-app-store-ios' title='iPhone'></i>" %}
{% assign lock="<i class='fas fa-lock'></i>" %}

{% assign inserm="<span title='INSERM' style='color: #e74011;'><b>🅘</b></span>" %}
​⃰{% assign inserm-eu="<span title='INSERM (.eu account)' style='color: #e74011;'><b>🅘¹</b></span>" %}
{% assign cnrs="<span title='CNRS' style='color: #62c4dd;'><b>🅒</b></span>" %}
{% assign sorbonne="<span title='Sorbonne Université' style='color: #ffb500;'><b>🅢</b></span>" %}
{% capture renater %}
{{inserm}}&thinsp;{{cnrs}}&thinsp;{{sorbonne}}
{% endcapture %}

<div class="container">
<h1>Tools for remote working</h1>
<div class="row">
<div class="col md-4">{{ inserm}} INSERM</div>
<div class="col md-4">{{ cnrs}} CNRS</div>
<div class="col md-4">{{ sorbonne}} Sorbonne Université</div>
</div>
<div class="row">
<div class="col md-12">
<h3 class="mt-2">Overview</h3>
</div>
</div>
<div class="row justify-content-left">
<div class="col-3">
<ul>
<li><a href="#video">Video conferencing</a></li>
<li><a href="#storage">File storage/sharing</a></li>
<li><a href="#chat">Chat + file sharing</a></li>
</ul>
</div>
<div class="col-3"></div>
<ul>
<li><a href="#publication">Publication access</a></li>
<li><a href="#software">Software licenses</a></li>
</ul>
</div>
<section id="video">
<h2 class="mt-5"><i class="fas fa-video"></i>&nbsp; Video-conferencing (<q><i>Zoom</i>-like</q>)</h2>
{% capture web-mobile-compat %}{{web}}&thinsp;{{android}}&thinsp;{{iphone}}{% endcapture %}
{% capture all-but-web %}{{windows}}&thinsp;{{osx}}&thinsp;{{linux}}&thinsp;{{android}}&thinsp;{{iphone}}{% endcapture %}
{% capture all-but-linux %}{{windows}}&thinsp;{{osx}}&thinsp;{{web}}&thinsp;{{android}}&thinsp;{{iphone}}{% endcapture %}
{% capture all-compat %}{{windows}}&thinsp;{{osx}}&thinsp;{{linux}}&thinsp;{{web}}&thinsp;{{android}}&thinsp;{{iphone}}{% endcapture %}
{% capture all-desktop %}{{windows}}&thinsp;{{osx}}&thinsp;{{linux}}{% endcapture %}

{% include software_box.html service-name="Teams" service-provider=inserm-eu
   software-compatibility=all-compat software-name="Microsoft Teams" software-link="https://teams.microsoft.com/"
   links="<a href='https://teams.microsoft.com/' class='btn btn-primary'>Web interface &nbsp;<i class='fas fa-lock'></i></a>|<a href='https://intranet.inserm.fr/wp-content/uploads/2020/08/MS-Teams-creer-visioconference.pdf'  class='btn btn-primary'>Creating a videoconference with Teams (INSERM)&nbsp;<i class='fas fa-lock'></i></a>" free-text="<span style='color: #e74011;'>¹</span>&nbsp; Needs an <code>@inserm.eu</code> account. Account details were sent via mail in March 2020. If you do not have one, request an account here: <a href='https://siou.inserm.fr/'>siou.inserm.fr</a>." %}

{% include software_box.html service-name="Rendez-Vous" service-provider=renater
   software-compatibility=web-mobile-compat software-name="Jitsi Meet" software-link="https://jitsi.org/jitsi-meet/"
   links="<a href='https://rendez-vous.renater.fr/home/' class='btn btn-primary'>Web interface&nbsp;<i class='fas fa-lock'></i></a>|<a href='https://jitsi.github.io/handbook/docs/intro'  class='btn btn-primary'>Jitsi documentation</a>|<a href='https://services.renater.fr/voix_et_image/rdv/user_guide' class='btn btn-primary'>RENATER documentation</a>" free-text="Limits for simultaneous participants: 5 to 10 (audio-only), 4 to 5 (video)" %}

{% include software_box.html service-name="Zoom" service-provider=cnrs
   software-compatibility=all-compat software-name="Zoom" software-link="https://cnrs.zoom.us/"
   links="<a href='https://cnrs.zoom.us/' class='btn btn-primary'>Web interface</a>|<a href='https://intranet.cnrs.fr/Cnrs_pratique/si/Pages/Zoom.aspx' class='btn btn-primary'>CNRS documentation&nbsp;<i class='fas fa-lock'></i></a>" free-text="For non-confidential topics only."%}

{% include software_box.html service-name="Zoom" service-provider=sorbonne
   software-compatibility=all-compat software-name="Zoom" software-link="https://zoom.us/"
   links="<a href='https://zoom.us/' class='btn btn-primary'>Web interface</a>|<a href='https://hotline.sorbonne-universite.fr/front/document.send.php?docid=2179' class='btn btn-primary'>Procedure to get account&nbsp;<i class='fas fa-lock'></i></a>" free-text="For time-limited use (e.g. for a conference/workshop) with many participants" %}

{% include software_box.html service-name="Tixeo" service-provider=cnrs
   software-compatibility=all-but-web software-name="Tixeo" software-link="https://www.tixeo.com/"
   links="<a href='https://tixeo.cnrs.fr' class='btn btn-primary'>Web interface &nbsp;<i class='fas fa-lock'></i></a>|<a href='https://aide.core-cloud.net/si/tixeo/SitePages/Accueil.aspx' class='btn btn-primary'>CNRS documentation</a>" %}

</section>
<section id="storage">
<h2 class="mt-5"><i class="far fa-hdd"></i>&nbsp; File storage/sharing (<q><i>Dropbox</i>-like</q>)</h2>
{% include software_box.html service-name="DropSU" service-provider=sorbonne
   software-compatibility=all-compat software-name="Nextcloud" software-link="https://nextcloud.com/files/" free-text="Offers 100&nbsp;GB of space; Documents/folders can be shared with external users without account; OnlyOffice installation for collaborative editing of MS Office documents"
   links="<a href='https://dropsu.sorbonne-universite.fr/' class='btn btn-primary'>Web interface&nbsp;<i class='fas fa-lock'></i></a>|<a href='https://nextcloud.com/support/' class='btn btn-primary'>Nextcloud documentation</a>|<a href='https://intranet.sorbonne-universite.fr/fr/procedures-et-services/informatique/outils-documentaires-collaboratifs.html' class='btn btn-primary'>Sorbonne documentation&nbsp;<i class='fas fa-lock'></i></a>" %}

{% include software_box.html service-name="MyCore" service-provider=cnrs
   software-compatibility=all-compat software-name="ownCloud" software-link="https://owncloud.com/" free-text="Offers 100&nbsp;GB of space;  Documents/folders can be shared with external users without account"
   links="<a href='https://mycore.core-cloud.net/index.php/login' class='btn btn-primary'>Web interface&nbsp;<i class='fas fa-lock'></i></a>|<a href='https://owncloud.com/docs-guides/' class='btn btn-primary'>ownCloud documentation</a>|<a href='https://confluence.cnrs.fr/confluence/pages/viewpage.action?spaceKey=ODSCORE&title=Aide+utilisateur' class='btn btn-primary'>CNRS documentation&nbsp;<i class='fas fa-lock'></i></a>" %}

{% include software_box.html service-name="iBox" service-provider=inserm
   software-compatibility=all-compat software-name="Nextcloud" software-link="https://nextcloud.com/files/" free-text="Offers 25&nbsp;GB of space;  Documents/folders can be shared with external users without account"
   links="<a href='https://ibox.inserm.fr' class='btn btn-primary'>Web interface&nbsp;<i class='fas fa-lock'></i></a>|<a href='https://nextcloud.com/support/' class='btn btn-primary'>Nextcloud documentation</a>" %}
</section>
<section id="chat">
<h2 class="mt-5"><i class="far fa-comment-dots"></i>&nbsp; Chat + file sharing (<q><i>Slack</i>-like</q>)</h2>
{% include software_box.html service-name="Citadel" service-provider=cnrs
   software-compatibility=all-but-linux software-name="Citadel Team" software-link="https://citadel.team/" free-text="Quite basic functionality"
   links="<a href='https://cnrs.citadel.team/' class='btn btn-primary'>Web interface&nbsp;<i class='fas fa-lock'></i></a>|<a href='https://support.citadel.team/kb' class='btn btn-primary'>Citadel support</a>|<a href='https://aide.core-cloud.net/si/citadel/SitePages/Accueil.aspx' class='btn btn-primary'>CNRS documentation&nbsp;<i class='fas fa-lock'></i></a>" %}
</section>
<section id="publication">
<h2 class="mt-5"><i class="far fa-newspaper"></i>&nbsp; Publication access</h2>
<p>The access described below can be made automatic with Browser plugins such as <i>ezProxy</i> (<a href="https://addons.mozilla.org/en-US/firefox/addon/ezproxy-redirect-foxified/"><i class="fas fa-download"></i>&nbsp;Firefox Add-On</a>, <a href="https://chrome.google.com/webstore/detail/ezproxy-redirect/gfhnhcbpnnnlefhobdnmhenofhfnnfhi"><i class="fas fa-download"></i>&nbsp;Chrome Extension</a>).</p>
{% include biblio_box.html service-name="Inserm biblio" service-provider=inserm portal-url="insermbiblio.inist.fr/" direct-url="proxy.insermbiblio.inist.fr/login?url=" %}

{% include biblio_box.html service-name="insb bib cnrs" service-provider=cnrs portal-url="bib.cnrs.fr" direct-url="insb.bib.cnrs.fr/login?url=" %}

{% include biblio_box.html service-name="Sorbonne Portail Documentaire" service-provider=sorbonne portal-url="sorbonne-universite.primo.exlibrisgroup.com/discovery/search?vid=33BSU_INST:33BSU" direct-url="accessdistant.sorbonne-universite.fr/?url=" %}
</section>
<section id="software">
<h2 class="mt-5"><i class="fas fa-laptop-code"></i>&nbsp; Software licences</h2>
<p>Campus licences for all members of Sorbonne University</p>

{% include software_box.html service-name="Antivirus (Kapersky)" service-provider=sorbonne software-name="Kapersky Anti-Virus" software-link="https://www.kaspersky.fr/antivirus" software-compatibility=all-desktop links="<a href='http://logiciels.upmc.fr/fr/marches_conclus_par_l_upmc/antivirus.html' class='btn btn-primary'>Sorbonne Campus Licence&nbsp;<i class='fas fa-lock'></i></a>"%}


{% include software_box.html service-name="Matlab" service-provider=sorbonne software-name="Matlab" software-link="https://fr.mathworks.com/" software-compatibility=all-desktop links="<a href='http://logiciels.upmc.fr/fr/marches_conclus_par_l_upmc/matlab/lic_standalone_personnel.html' class='btn btn-primary'>Employee licence&nbsp;<i class='fas fa-lock'></i></a>|<a href='http://logiciels.upmc.fr/fr/marches_conclus_par_l_upmc/matlab/lic_standalone_etudiant.html' class='btn btn-primary'>Student licence&nbsp;<i class='fas fa-lock'></i></a>"%}

{% include software_box.html service-name="Mathematica" service-provider=sorbonne software-name="Mathematica" software-link="https://www.wolfram.com/mathematica/" software-compatibility=all-desktop links="<a href='http://logiciels.upmc.fr/fr/marches_conclus_par_l_upmc/mathematica.html' class='btn btn-primary'>Sorbonne Campus Licence&nbsp;<i class='fas fa-lock'></i></a>"%}

{% include software_box.html service-name="Maple" service-provider=sorbonne software-name="Maple" software-link="https://www.maplesoft.com/" software-compatibility=all-desktop links="<a href='http://logiciels.upmc.fr/fr/marches_conclus_par_l_upmc/maple.html' class='btn btn-primary'>Sorbonne Campus Licence&nbsp;<i class='fas fa-lock'></i></a>"%}
</section>
</div>
