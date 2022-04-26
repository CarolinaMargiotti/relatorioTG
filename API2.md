# Carolina Margiotti de Abreu

# Tabela de conteúdo
   - [Em 2020-2 (Minha Jornada) 2º Semestre](#em-2020-2-minhajornada-2º-semestre)
        - [Empresa](#empresa)
        - [Problema](#problema)
        - [Solução](#solução)
        - [Tecnologias utilizadas](#tecnologias-utilizadas)
        - [Contribuições Pessoais](#contribuições-pessoais)
            - [Hard Skills](#hard-skills)
            - [Soft Skills](#soft-skills)

# Em 2020-2 (Minha Jornada) 2º Semestre
[Github Minha Jornada](https://github.com/CarolinaMargiotti/Minha-Jornada)
<p align="center">
<img alt="Logo minha jornada" src="./imagens/api2/Capa.gif" height="250">
</p>

## Empresa
<p align="justify">
A IACIT foi fundada em 1986 no Brasil, possui sede em São José dos Campos e é um importante centro para a indústria aeroespacial do Brasil, com certificação dada pelo Ministério da Defesa de Empresa de estratégia de Defesa. Ela desenvolve projetos e sistemas para o auxílio do controle e do tráfego aéreo e marítimo, defesa e segurança pública, meteorologia, pesquisa e telemetria.
</p>

## Problema
<p align="justify">
Grande parte do transporte de mercadorias no Brasil é feito por caminhões, isso põem muita pressão em empresas para as entregas serem entregas corretamente. Para garantir o maior controle possível a empresa quer ter as informações de registro das jornadas de trabalho, repousos, horários de alimentação e horas extra dos seus caminhoneiros na logística.
</p>

## Solução
<p align="justify">
O Minha Jornada é um software que oferece registro da jornada de trabalho do motorista que transporta entregas, ajustando-se ao acordo coletivo sindical do usuário, além de permitir o controle e visualização dos registros pela empresa de logística, assim como permite coletar dados para a folha de pagamento.
</p>

Nesse projeto a carga de atividades foi melhor distribuída comparado ao primeiro projeto integrador, minhas contribuições para a solução mais significativas foram as abaixo.

### Modelo conceitual e lógico.
Eu desenhei os dois modelos para ajudar no desenvolvimento do projeto.
#### Modelo Conceitual
<p align="center">
<img alt="modelo conceitual" src="./imagens/api2/Modelo Conceitual.png" height="450">
</p>

#### Modelo Lógico
<p align="center">
<img alt="modelo lógico" src="./imagens/api2/Modelo Lógico.png" height="450">
</p>

### CRUD de veiculos
<p align="justify">
Criei a página de veículos, nele há uma tabela que você pode visualizar a lista de veículos com os dados deles de ID, chassi, ID de integração, marca do rastreador e versão do rastreador. Na tabela você pode além de visualizar, também pode criar um veículo, editar um veículo especifico ou deletar um veículo, com cada uma dessas opções indo para uma página diferente que eu também criei.
</p>

### Alteração de senha
Uma tela de alteração de senha foi criada por mim junto de um endpoint para efetuar isso no back-end.

### A pagina de visualizar o banco de horas de um caminhoneiro especifico.
<p align="justify">
Programei a tela com a tabela para visualizar o banco de horas dos caminhoneiros, criei um objeto para jornada possuindo além do id da jornada, o id do caminhoneiro, data dessa jornada em especifico, o tempo de almoço, horas totais de serviço, e horas de descanso. Depois de criar o objeto fiz o endpoint que pega eles do banco para a listagem.
</p>
Além disso adicionei ao CRUD de caminhoneiros a opção de ir visualizar o banco de horas do clicado em especifico, que redireciona para essa pagina.

<p align="center">
<img alt="tela de visualizar horas numeradas" src="./imagens/api2/tela visualizar horas numerado.png" height="450">
</p>

1. Nome do caminhoneiro que foi selecionado
2. Input para filtrar datas que aparecem na tabela.
3. ID da jornada.
4. Horas totais de serviço.
5. Minutos totais de almoço.
6. Minutos totais de descanso.


## Tecnologias Utilizadas
- Java \
Usado tanto para Back e Front-End.
   - Spring \
   Um framework Java para auxiliar desenvolvimento de aplicações.
   - Hibernate \
   Framework de persistência de dados usado no Java para implementar o conceito de mapeamento objeto-relacional, funcionando em conjunto do banco de dados.
- HTML \
Define a estrutura do conteúdo da web da forma mais básica.
- CSS \
Adiciona estilo á uma pagina web.
- Postgres \
Banco de dados relacional.
- Figma \
Um editor gráfico de vetor e prototipagem de projetos de design.

## Contribuições Pessoais

### Hard Skills
- Java, Spring, Hibernate:
<p align="justify">
Desenvolvi mais o conhecimento em Java que já havia adquirido no ensino técnico, sendo apresentada a um framework java e framework de persistência de dados pela primeira vez, não dominei completamente essas tecnologias, mas tive um conhecimento mais sólido de como funcionam que me ajudaram em projetos com essas tecnologias que vieram no futuro em outras matérias.
</p>

- Postgres:
<p align="justify">
Não havia tido contato com postgres antes, foi minha primeira vez e agora consigo usá-lo com relativa facilidade.
</p>

- Figma:
<p align="justify">
 Também me foi apresentado Figma pela primeira vez, aprendi facilmente e me lembro sem dificuldade com o que aprendi, agora no quinto semestre tive que auxiliar no figma do projeto integrador e pude trabalhar sem recorrer a tutoriais na internet ou outros conteúdos para me lembrar de como funciona.
</p>

### Soft Skills
- Flexibilidade no trabalho:
<p align="justify">
Ajudei com o que precisava ser feito na equipe, mesmo com coisas que eu não estava confiante que conseguiria fazer inicialmente (os modelos por exemplo).
</p>

- Resiliencia:
<p align="justify">
Troquei mensagens várias vezes com a professora de banco de dados para garantir que os modelos estavam corretos, pedindo a opinião dela inúmeras vezes e tirando dúvidas.
</p>

- Honestidade:
<p align="justify">
Nos gargalos que encontrei na programação admiti minhas dificuldades a equipe e recebi ajuda de acordo, podendo terminar minhas tarefas com uma maior agilidade.
</p>


