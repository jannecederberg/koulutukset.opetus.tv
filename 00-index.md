---
layout: default
title: Etusivu
permalink: /
jarjestys: 1
ikoni: home
---


<div class="row">
	<div class="hero-unit text-centered">
		<h1>DigabiOS-koulutukset</h1>
		<p>
			Opetus.tv tarjoaa koulutuksia ylioppilaskokeisiin käyttöön tulevaan Digabi-käyttöjärjestelmään liittyen; yli 1500 opetusvideon ja yli kahden miljoonan videokatselun kokemuksella!
		</p>
		<p style="text-align: center;">
			<a href="/tilaa-koulutus" class="btn btn-warning btn-large">Tilaa koulutus</a> tai
			<a href="/listaus/" class="btn btn-large">Tarkastele koulutuksia</a>
		</p>
	</div>

	<div class="span12">
		<h2>Uusimmat koulutukset</h2>

		<table class="table">
			<tr>
				<th>Päivämäärä</th>
				<!--th>Aika</th-->
				<th>Otsikko</th>
				<th>Koulutuspaikka</th>
				<!--th>Kouluttaja(t)</th-->
			</tr>

			{% for koulutus in site.categories.koulutukset limit:3 %}
			<tr>
				<td>{{ koulutus.date | date:"%d.%m.%Y" }}</td>
				<!--td>{{ koulutus.aika }}</td-->
		    	<td><a href="{{ koulutus.url }}">{{ koulutus.title }}</a></td>
		    	<td>{{ koulutus.paikka }}</td>
		    	<!--td>{{ koulutus.kouluttaja }}</td-->
		    </tr>
			{% endfor %}

		</table>
	</div>
</div>