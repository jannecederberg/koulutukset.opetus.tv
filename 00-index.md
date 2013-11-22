---
layout: default
title: Etusivu
permalink: /
jarjestys: 1
ikoni: home
---


<div class="row">
	<div class="hero-unit text-centered">
		<h1>Koulutustarjonta</h1>
		<p>
			Opetus.tv tarjoaa pedagogisia koulutuksia uudenlaisista opetuskäytänteistä.
			Pedagogisten koulutusten lisäksi Opetus.tv tarjoaa koulutuksia tieto- ja viestintätekniikan hyödyntämisestä opetuskäytössä.
		</p>
		<p>
			Huomaa, että <a href="http://opetus.tv">Opetus.tv</a> ja <a href="http://maot.fi" title="Matematiikan opetuksen tulevaisuus">Maot.fi</a> toimivat tiivissä yhteistyössä ja osa toimijoista on samoja.
		</p>
		<p style="text-align: center;">
			<a href="/listaus/" class="btn btn-warning btn-large">Tarkastele koulutuksia</a> tai
			<a href="/tilaa-koulutus" class="btn btn-large">Tilaa koulutus</a>
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