# Internet Sem Limites

[![Join the chat at https://gitter.im/InternetSemLimites/InternetSemLimites](https://badges.gitter.im/InternetSemLimites/InternetSemLimites.svg)](https://gitter.im/InternetSemLimites/InternetSemLimites?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Repositório que busca catalogar e organizar os provedores de internet que não limitarão o tráfego de dados.

Para cadastrar um novo provedor utilize [esse formulário](https://internetsemlimites.herokuapp.com/new/).

Os dados estão disponíveis também em uma [API pública](http://github.com/cuducos/InternetSemLimitesCMS). Se você pensa em fazer algo, um site, um app, um SPA com os dados, [junte-se a nós](https://github.com/jlcarvalho/InternetSemLimites/issues/9).

---
This repo is focused on creating an open catalog of companies [who are not adhering to data cap in Brazil](http://www.zdnet.com/article/brazilians-protest-against-fixed-broadband-data-cap/).

---
{% for state, providers in states %}
## {{ state }}

| Provedor | Fonte | Observações |
|----------|-------|-------------|{% for provider in providers %}
| [{{ provider.name }}]({{ provider.url }}) | {{ provider.source }} | {{ provider.other|default:"&nbsp;" }} |{% endfor %}
{% endfor %}

# Painel da Vergonha

[Provedores de internet que irão limitar o tráfego de dados](HALL_OF_SHAME.md).
