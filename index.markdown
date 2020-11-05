---
layout: default
title: Tools for remote working
---

<script src="https://kit.fontawesome.com/2b48dbc3a6.js" crossorigin="anonymous"></script>
{% assign windows="<i class='fab fa-windows'></i>" %}
{% assign osx="<i class='fab fa-apple'></i>" %}
{% assign linux="<i class='fab fa-linux'></i>" %}
{% assign web="<i class='fas fa-globe'></i>" %}
{% assign android="<i class='fab fa-google-play'></i>" %}
{% assign iphone="<i class='fab fa-app-store-ios'></i>" %}
{% assign lock="<i class='fas fa-lock'></i>" %}

{% assign inserm="<span title='INSERM' style='color: #e74011;'><b>Ⓘ</b></span>" %}
{% assign cnrs="<span title='CNRS' style='color: #62c4dd;'><b>Ⓒ</b></span>" %}
{% assign sorbonne="<span title='Sorbonne Université' style='color: #ffb500;'><b>Ⓢ</b></span>" %}
<style>
#legend {
  position: fixed;
  bottom: 0;
  right: 0;
  border: 3px solid #73AD21;
}
</style>
<details id="legend">
<summary>Legend</summary>
<dl>
<dt>S</dt>
<dd>Sorbonne University</dd>
<dt>C</dt>
<dd>CNRS</dd>
<dt>Ⓘ</dt>
<dd>INSERM</dd>
</dl>
</details>

## Video-conferencing (*Zoom*-like)

## File storage/sharing (*Dropbox*-like)
{% capture all-compat %}{{windows}}&thinsp;{{osx}}&thinsp;{{linux}}&thinsp;{{web}}&thinsp;{{android}}&thinsp;{{iphone}}{% endcapture %}

{% include software_box.html service-name="iBox" service-provider=inserm
   software-compatibility=all-compat software-name="Nextcloud" software-link="https://nextcloud.com/files/" free-name="Quota" free-value="25&nbsp;GB"
   links="<a href='https://ibox.inserm.fr'>Web interface</a>&nbsp;<i class='fas fa-lock'></i> &ndash; <a href='https://nextcloud.com/support/'>Nextcloud documentation</a> &ndash; <a href='https://intranet.inserm.fr/services-et-support-informatique/Documents/ibox-utilisateurs-v3.pdf'>INSERM documentation&nbsp;<i class='fas fa-lock'></i></a>" %}

{% include software_box.html service-name="MyCore" service-provider=cnrs
   software-compatibility=all-compat software-name="ownCloud" software-link="https://owncloud.com/" free-name="Quota" free-value="100&nbsp;GB"
   links="<a href='https://mycore.core-cloud.net/index.php/login'>Web interface&nbsp;<i class='fas fa-lock'></i></a> &ndash; <a href='https://owncloud.com/docs-guides/'>ownCloud documentation</a> &ndash; <a href='https://confluence.cnrs.fr/confluence/pages/viewpage.action?spaceKey=ODSCORE&title=Aide+utilisateur'>CNRS documentation&nbsp;<i class='fas fa-lock'></i></a>" %}

{% include software_box.html service-name="DropSU" service-provider=sorbonne
   software-compatibility=all-compat software-name="Nextcloud" software-link="https://nextcloud.com/files/" free-name="Quota" free-value="100&nbsp;GB"
   links="<a href='https://dropsu.sorbonne-universite.fr/'>Web interface</a>&nbsp;<i class='fas fa-lock'></i> &ndash; <a href='https://nextcloud.com/support/'>Nextcloud documentation</a> &ndash; <a href='https://intranet.sorbonne-universite.fr/fr/procedures-et-services/informatique/outils-documentaires-collaboratifs.html'>Sorbonne documentation&nbsp;<i class='fas fa-lock'></i></a>" %}
   
## Chat + file sharing (*Slack*-like)

## Publication access

## Software access


