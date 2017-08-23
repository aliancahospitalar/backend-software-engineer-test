# Teste Data Engineeer - Aliança Hospitalar


```
Aliança Hospitalar
tecnologia@aliancahospitalar.com
(11) 95977-0090
```

Vamos desenvolver uma aplicação que provê estatísticas sobre avaliações de filmes. Para isso teremos acesso a uma base-de-dados que chamaremos de Transacional. Essa base é uma base SQLite tem a seguinte estrutura:

![](https://raw.githubusercontent.com/aliancahospitalar/backend-software-engineer-test/master/movies.png "Logo Title Text 1")

## Parte 1 - Obtendo os dados

Baixe a base de dados aqui (http://bit.ly/2tiG9lK).

## Parte 2 - Transformando os dados
Vamos assumir que nossa base Transacional é muito lenta e não apropriada para análises complexas, por isso, em qualquer linguagem ou tecnologia de sua escolha, desenvolva um ou mais pipelines de transformação que, a partir da base Transacional, insira dados numa nova base de dados (Análise).

Essa nova base de dados deve ser otimizada para consultas - seja pelo modelo de dados, seja pelo esquema ou seja pela tecnologia escolhida em si.

Pode ser utilizada qualquer base-de-dados a sua escolha desde que seja:
Não-relacional
Gratuita para usar (Open-source, community edition etc)

O pipeline, o modelo de dados da nova base e os dados nela contidos devem possibilitar responder às seguintes perguntas:
* Quais os filmes com melhor avaliação média?
* Quais os gêneros com melhor avaliação média?
* Quais os gêneros com mais filmes?
* Qual a avaliação média por gênero?
* Qual a avaliação média por ano?
* Qual a distribuição do número de filmes produzidos por ano?
* Qual a distribuição do número de filmes produzidos por década?

Sempre que dados forem inseridos no banco Transacional, a base de Análise deve ser atualizada.

## Parte 3 - Provendo acesso aos dados
Em qualquer linguagem ou tecnologia da sua escolha, exponha uma API REST que retorne resultados para as perguntas acima.

O design da API, endpoints e formato de resposta fica a seu critério.

Ex.: Quais os filmes com melhor avaliação média?

Request:

`GET /movies/best`

Response:
```
[
{
	id: “5513770”,
		title: “Kung Fu Panda: Secrets of the Scroll (2016)”,
		year: “2016”,
		avg_rating: “6.9”,
		genres: [ “Short”, “Action”, “Animation”]
       	},
	...
]
```
## Parte 4 - A entrega
A sua aplicação, bem como o banco de dados de Análise devem estar em Docker, um ou mais containers, para  que seja mais fácil executarmos.
Se possível, toda a sua stack deve subir com um único comando: docker-compose up
Suba seu código num repositório Git e mande o link pra nós. Pode ser no github, bitbucket, gitlab. Não importa, desde que tenhamos acesso para clonar seu repositório.
Adicione um Readme.md com as instruções para setup e execução do seu código.
Adicione um pequeno diagrama explicando sua arquitetura: módulos e como se comunicam.
Depois da entrega conversaremos sobre a sua solução. Você então poderá explicar melhor sua abordagem, a modelagem dos dados, as tecnologias e a arquitetura que você escolheu.
Considerações finais
O prazo é flexível e fica a seu critério, mas acreditamos que em 2 semanas dá pra resolver um problema dessa complexidade.
Você pode arquitetar sua solução como quiser e utilizar mais de uma linguagem de programação se julgar necessário. Ex.: Pode fazer o extrator com Go, o pipeline com Python e a API com Node.js.
Se você precisar fazer ajustes na base Transacional, adicionar views, triggers, índices, chaves etc, fique à vontade - só não esqueça de explicar o que fez, o porquê e os scripts para fazermos a mesma coisa na nossa base ;)

## Referências
Dataset original: https://github.com/sidooms/MovieTweetings
