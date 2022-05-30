# Carolina Margiotti de Abreu

# Tabela de conteúdo

-   [Em 2021-2 (AirplaneDocGenerator) 4º Semestre](#em-2021-2-airplanedocgenerator-4º-semestre)
    -   [Empresa](#empresa)
    -   [Problema](#problema)
    -   [Solução](#solução)
        -   [Client](#client)
        -   [Server](#server)
    -   [Tecnologias utilizadas](#tecnologias-utilizadas)
    -   [Contribuições Pessoais](#contribuições-pessoais)
        -   [Hard Skills](#hard-skills)
        -   [Soft Skills](#soft-skills)

# Em 2021-2 (AirplaneDocGenerator) 4º Semestre

<p align="center">
<img src="./imagens/api4/Crab.png" alt="logo equipe" height="200">
</p>

[Github AirplaneDocGenerator](https://github.com/CarolinaMargiotti/AirplaneDocGenerator)

## Empresa

<p align="justify">
Embraer é uma empresa da área aeroespacial, trabalhando na fabricação de aviões e peças aeroespaciais, além de oferecer outros tipos de suporte.
</p>

## Problema

<p align="justify">
Nosso cliente possui a necessidade de automatizar a geração de manuais para as suas aeronaves, pois, atualmente, o processo é feito de forma manual, o que pode tomar muito tempo em razão da complexidade para a montagem deles e, também, pode aumentar as chances de erros. Nossa aplicação tem como objetivo resolver esses problemas através de uma interface simples e intuitiva que agilizará o processo.
</p>

## Solução

<p align="justify">
Foi criado dois projetos diferente, um server para o back-end responsável pelos serviços e um client para front-end cuidando do que é visível para o usuário. 
</p>

### Client

Desenvolvido com electron, react e tailwind, permitia a visualização dos manuais e a interface de filtragem e criação deles.

#### Filtros

Eu programei os filtros para pesquisa e o sistema de filtrar dos manuais na pesquisa deles.

<p align="center">
<img src="./imagens/api4/filtro.png">
</p>

#### Criar nova linha

Os manuais eram formados por linhas que apontavam para uma página do manual, eu programei o botão e o modal para adicionar uma linha nova ao manual.

<p align="center">
<img src="./imagens/api4/nova_linha.png">
</p>
<p align="center">
<img src="./imagens/api4/linha.png">
</p>

#### Tooltips

Criei o componente de tooltip e programei sua funcionalidade, permitindo facilmente uso dele na programação para mostrar dicas e explicações de funcionalidades.

<p align="center">
<img src="./imagens/api4/tooltip.png">
</p>

#### Pagina de criar manuais

Programei o esqueleto da página de criar manuais, embora não com as funcionalidades completas o visual estava 100% funcional e só foi necessário outro membro depois trocar os logs de console para o chamar da função que criaram para tal.

<p align="center">
<img src="./imagens/api4/criar_manual.png">
</p>

#### CardHeader

Um componente criado por mim, fica no topo de todas as páginas do sistema para explicar seu objetivo e mostrar o nome da página.

<p align="center">
<img src="./imagens/api4/cardheader.png">
</p>

#### Criação do client

Eu criei a base do projeto de cliente, configurando o Electron e React para o desenvolvimento.

#### Estrutura da seleção de projeto

Programei a estrutura base que um dos colegas usou para a página de seleção de projeto.

#### Ajustes menores

-   Consertei algumas páginas para o visual ficar mais parecido com o idealizado no Figma.
-   Arrumei um bug na hora de criar o diretório onde ficaria os manuais quando baixados por um usuario.

### Server

#### Swagger

Swagger é uma ferramenta para documentação de APIs para agilizar o desenvolvimento. O configurei para o uso do projeto.

## Tecnologias Utilizadas

-   Electron.js \
    Para o desenvolvimento do aplicativo de desktop, utilizando linguagem de programação Javascript.
-   React \
    Framework para agilizar desenvolvimento com Javascript.
-   Tailwind CSS \
    Biblioteca de css para ajudar no desenvolvimento do front-end.
-   Spring Boot \
    Utilizado para o back-end, utilizando a linguagem de programação Java.
-   PostgresSQL
    Banco de dados.

## Contribuições Pessoais

### Hard Skills
- Electron.js: Fui introduzida.
- React: Sei fazer com autonomia.
- Tailwind CSS: Sei fazer com autonomia.
- Spring Boot: Consigo fazer com ajuda.
- PostgresSQL: Consigo fazer com ajuda.

### Soft Skills
- Trabalho em equipe
<p align="justify">
    Neste API passei bastante tempo em chamada de voz ajudando outros membros com impedimentos no desenvolvimento ou os ajudando na lógica de suas tarefas.
</p>

- Responsabilidade
<p align="justify">
    Aparência nas reuniões semanais e mais de um dia da semana conseguia tempo para produzir e auxiliar a equipe.
</p>
