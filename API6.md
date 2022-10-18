# Carolina Margiotti de Abreu

# Tabela de conteúdo

-   [Em 2022-2 (Soyia) 5º Semestre](#em-2022-2-soyia-6º-semestre)
    -   [Empresa](#empresa)
    -   [Problema](#problema)
    -   [Solução](#solução)
        -   [Client](#client)
        -   [Server](#server)
    -   [Tecnologias utilizadas](#tecnologias-utilizadas)
    -   [Contribuições Pessoais](#contribuições-pessoais)
        -   [Hard Skills](#hard-skills)
        -   [Soft Skills](#soft-skills)

# Em 2022-2 (Soyia) 6º Semestre
<p align="center">
<img alt="logo soia" src="./imagens/api6/logo.png" height="200">   
</p>
[Github Soyia](https://github.com/medrenan/SoyIA)


## Empresa

<p align="justify">
A Visiona é uma empresa de atividade espacial que oferece integrações de sistemas espaciais, oferecendo através dos dados de satélites que a Embraer coleta do INPE, soluções para as necessidades civis e militares do Brasil.
</p>

## Problema
<p align="justify">
A empresa parceira Visiona possui um aplicativo para registro e administração de cultivos de soja, nele o agricultor pode registrar suas plantas e receber estatisticas sobre sua plantação, mas para o registro de amostras era exigido que ele fosse á campo, colhesse três amostras e contasse manualmente cada vagem e sentimento dessas plantas para o preenchimento de dados no aplicativo, isso levava em torno de 15 minutos para o agricultor e tornava o uso do aplicativo não tão conveniente. Vendo uma oportunidade de melhoria nesse aspecto, a Visiona veio a nós pedir para criar uma nova feature para a aplicação: Uma inteligência artificial que dava uma estimativa das vagens e sementes por planta apartir de uma foto da mesma, facilitando e agilizando seu trabalho.
</p>

## Solução

<p align="justify">
Foi feito um fork dos repositórios de front e back-end do aplicativo original para facilitar no desenvolvimento das nossas mudanças e criado um segundo back-end para isolar as funcionalides de IA do outro.
</p>

### Client

#### ESoja Mobile

##### Reordenação da tela de upload de imagem para o meio do registro e não o fim.
##### Criei modal com instruções de como tirar a imagem para facilitar a relação usuario e inteligencia artificial.
<img alt="png do modal" src="./imagens/api6/modal.png" height="500">   

##### Integrei a api criada por nós com o aplicativo
##### Programei para os dados recebidos pela api da contagem de sementes ser atribuida automaticamente nos campos.
<img alt="gif upload da imagem e atribuição" src="./imagens/api6/chamada-endpoint-atribuicao.gif" height="500">

##### Conserto de bugs do aplicativo
- Bug que o datepicker não pegava a data inserida.
- Bug que causava erro ao criar uma propriedade.
- Bug que causava erro ao tentar criar uma amostra.

### Server

#### Esoja-api

#### Soyia-api

#### Estruturar o projeto em flask
##### Script para resize e padding de imagem
Resultado de um padding e resize:

<img alt="foto soja resized com padding" src="./imagens/api6/newSoja.jpg" height="500">   


### Infraestrutura
Tivemos muitos problemas para fazer o aplicativo rodar pela falta de documentação, eu acabei resolvendo todos eles.

#### Back
- Consertei o arquivo env para conseguir levantar o docker.
- Descobri que ja ter um postgres instalado localmente no sistema confundia o servidor.
- Criei um script para fazer o servidor abrir adequadamente.
- Descobri quais eram as urls de request e como chama-las.
- Descobri como fazer autenticação para adquirir o token para os requests avançados.

#### Front
- Descobri como configurar o emulador do Android Studio para rodar as mudanças locais para o desenvolvimento.
- Descobri que precisava por os ips da maquina local no arquivo de api para o aplicativo no emulador mobile encontrar o servidor.

#### Armazenamento de imagens
- Configurei o firebase para conseguirmos armazernamos as imagens.

## Tecnologias Utilizadas
- React Native \
Uma biblioteca do React para desenvolvimento mobile.
- Typescript \
Superset do javascript.
- Python \
Linguagem de programação.
    - Flask \
Microframework web do Python, utilizado para as rotas de serviço.
- Firebase \
Banco de dados NoSQL escolhido para armazenar as imagens.
- Node.js \
Software open source para ambiente de server.
- Prisma \
Um ORM para typescript e node.js.
- Docker \
Virtualização de nível de sistema operacional para uso de contêineres.

## Contribuições Pessoais

### Hard Skills
- React Native: Sei fazer com certa autonomia.
- Python, Flask: Sei fazer com autonomia.

### Soft Skills

