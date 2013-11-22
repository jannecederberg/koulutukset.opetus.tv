---
layout: post
title: Koulutuslistaus
date: 2013-01-01 00:00:00
permalink: /listaus/
jarjestys: 10
ikoni: pencil

---

Koulutukset listattuna, uusin ylimpänä.

<table class="table">
	<tr>
		<th>Päivämäärä</th>
		<th>Aika</th>
		<th>Otsikko</th>
		<th>Koulutuspaikka</th>
		<th>Kouluttaja(t)</th>
	</tr>
	{% for koulutus in site.categories.koulutukset %}
	<tr>
		<td>{{ koulutus.date | date:"%d.%m.%Y" }}</td>
		<td>{{ koulutus.aika }}</td>
    	<td><a href="{{ koulutus.url }}">{{ koulutus.title }}</a></td>
    	<td>{{ koulutus.paikka }}</td>
    	<td>{{ koulutus.kouluttaja }}</td>
    </tr>
	{% endfor %}
</table>