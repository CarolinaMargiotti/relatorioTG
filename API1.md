# Carolina Margiotti de Abreu

# Tabela de conteúdo
   - [Em 2020-1 (LittlePet) 1º Semestre](#em-2020-1-littlepet-1º-semestre)
        - [Empresa](#empresa)
        - [Problema](#problema)
        - [Solução](#solução)
            - [Hardware](#hardware)
            - [Software](#aplicativo-mobile)
        - [Tecnologias utilizadas](#tecnologias-utilizadas)
        - [Contribuições Pessoais](#contribuições-pessoais)
            - [Hard Skills](#hard-skills)
            - [Soft Skills](#soft-skills)

# Em 2020-1 (LittlePet) 1º Semestre
<p align="center">
<img alt="Logo littlePet" src="./imagens/logo little pet.png" height="100">
</p>

## Empresa
<p align="justify">
As Fatecs são instituições importantes para o Brasil em ensino superior, sendo pioneiras na graduação de tecnólogos e localizadas em vÁrias cidades pelo estado de São Paulo. A unidade de São José dos Campos oferece um grande número de cursos para graduação de nível superior neles incluindo analise e desenvolvimento de sistemas, Banco de dados, manutenção de aeronaves entre outros.
</p>

<p align="justify">
Em 2020 foi iniciado o projeto integrador na Fatec, em que a faculdade fazia parceria com empresas para realizar um projeto em conjunto, os alunos recebiam o problema das empresas e elaboram uma solução que é apresentada em sprints e no fim há uma feira de soluções com cada grupo de alunos apresentando seus projetos.
</p>

<p align="justify">
No primeiro semestre os alunos decidem um próprio problema para resolver no decorrer do semestre.
</p>

## Problema
<p align="justify">
Os dispensadores automáticos de ração existentes hoje em dia no mercado foram feitos para trabalhar com ração de cachorros e gatos principalmente, um trabalho no qual ele faz muito bem, mas peca quando é usado com outros tipos de ração tipo o de roedores que é normalmente encontrado no formato cilíndrico, que muitas vezes empaca no dispensador entre outros inconvenientes. O projeto virava oferecer uma opção de dispensador de ração automático feito para roedores, contendo inclusive a possibilidade de se programar quando a ração será dispensada.
</p>

## Solução
<p align="justify">
Nosso grupo, que continha 6 elementos (comigo estando no time de desenvolvimento) teve a solução de fazer dois projetos, um com Arduino para cuidar da parte física do dispensador e o segundo um aplicativo mobile que cuidou da parte de agendamento prático para notificar a hora de dispensar ração, customizada pelo usuário.
</p>

### Hardware

O hardware foi feito por uma coléga do grupo, nele foram utilizados:
- Uma balança de carga 5kg

Usado para calcular o peso de ração presente no dispensador, para mandar um aviso quando está vazio e precisa ser reenchido.
<p align="center">
<img alt="balança de carga" src="./imagens/balança de carga.jpg" height="300" width="300">
</p>


- Um motor 12V 15KGF

Responsável pelo movimento de girar para derrubar ração.
<p align="center">
<img alt="motor" src="./imagens/motor.jpg" height="300">
</p>

- WI-FI Lora 915MHZ

Se conecta ao banco para enviar dados novos.
<p align="center">
<img alt="wifi lora" src="./imagens/wifi lora.jpg" height="300">
</p>

- Placa Arduino Bluetooth

Se comunica com outros componentes sendo utilizados.
<p align="center">
<img alt="placa arduino" src="./imagens/bluetooth.jpg" height="300">
</p>

- Placa HX711

Converte os valores de peso da balança para dados digitais.
<p align="center">
<img alt="hx711" src="./imagens/hx711.jpg" height="300">
</p>

Segue imagem do projeto abaixo com alguns itens visíveis demarcados:

<p align="center">
<img alt="hx711" src="./imagens/projeto hardware.png" height="500">
</p>

1. Motor
2. Placa Arduino
3. WI-FI Lora
4. Balança de carga
5. HX711


### Aplicativo Mobile

O aplicativo mobile eu fiz boa parte da codificação, com um outro membro auxiliando em certas partes dele.

Abaixo está a tela principal do aplicativo que será explicado de cima para baixo a seguir.

<p align="center">
<img alt="tela aplicativo de agendamento" src="./imagens/tela aplicativo little pet.png" height="500">
</p>

1. Um bloco informando qual usuário está conectado e o botão para deslogar o mesmo.
2. Um botão de seleção em que o usuário pode selecionar uma entre todas as conexões disponíveis ao redor.
3. Um texto informado se a conexão teve sucesso ou não.
4. A lista dos horários de dispensamento criados pelo usuário, quando não está informado quais os dias da semana o alarme será diariamente.
5. Botão para abrir um modal para seleção do horário para o agendamento (Aparece-se um texto embaixo informando qual o selecionado para confirmação).
6. Um array de botões, quando o usuário clica em um ele se torna verde informando que aquele dia será incluso na rotina para o horário selecionado do alarme.
7. Botão para confirmar a adição do horário novo.
8. Um texto adicionado para a etapa de desenvolvimento, informando onde o aparelho estava conectado, retirado na versão final.

A seguir explicarei alguns códigos principais do projeto e que eu fui responsavel por programar eles.


#### Notificação do alarme

O usuário poderia agendar horários nos quais a ração seria dispensada do dispensador, na mesma hora o aplicativo notificava o usuário.

<p align="center">
<img alt="código verificar alarme" src="./imagens/notificar alarme numerado.png" height="500">
</p>

1. É criado uma variavel que recebe qual horário é atualmente.
2. Numa lista que contém os horários agendados para o dia atual é verificado se a hora atual é um horário marcado para a dispensão da ração.
3. Caso sim entra-se em outra condição na qual é verificado se o alarme é semanal ou é de uso único.

Caso o horário é de uso único:

4. O horário atual é removido da lista de horários para se notificar do dia.
5. Da lista total de horários é removido o horário.
6. É reatribuido ao componente lista que é apresentado ao usuário a nova lista de horários, agora sem esse horário que ja foi concluido e não deve existir mais.
7. É enviado ao bluetooth o texto 1 que sinaliza o arduino para dispensar ração.
8. Uma notificação é enviada para o usuário informando que a ração foi dispensada.

Caso o horário seja semanal:

9. O horário atual é removido da lista de horários para se notificar do dia.
10. É enviado ao bluetooth o texto 1 que sinaliza o arduino para dispensar ração.
11. Uma notificação é enviada para o usuário informando que a ração foi dispensada.

#### Salvando os horários no banco
Aqui segue o código utilizado para salvar um horário para o dispensar da ração.

<p align="center">
<img alt="código salvando horário de alarme" src="./imagens/salvar horario numerado.png" height="500">
</p>

1. Primeiro se é verificado se o horário é semanal, se não tem valor na lista de dias da semana escolhidos assumi-se que não.

Caso o horário seja de uso único:

2. A hora é adicionada na lista demarcada para os alarmes de uso único.
3. Da mesma forma é adicionado na lista de horários á serem alertados hoje o horário escolhido.

Caso o horário deva se repetir:

4. Condição para se verificar se o horário criado hoje acontece de ser numa data que é para ser acionado.
5. Caso sim ele é adicionado na lista dos horários para serem acionados no dia.
6. Para cada dia da semana que foi selecionada para o horário acionar (Segunda, Quarta, Quinta por exemplo) o alarme, as ações 7 e 8 serão feitas.
7. Pede-se para o banco de dados guardar o horário no campo especificado na tag, sendo ele dentro da agenda do usuário logado e dentro da lista do dia da semana na agenda dele.
8. Um identificador que diferencia os horários é atribuido uma unidade a mais para o próximo valor não o substituir.



## Tecnologias Utilizadas
- Kodular

Para a programação mobile.

<img alt="Kodular" title="Kodular" src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fs3-eu-west-1.amazonaws.com%2Ftpd%2Flogos%2F5e0b334f707fc40001351cf8%2F0x0.png&f=1&nofb=1" height="75">

- Arduino

Para o uso em hardware.

<img alt="Arduino" src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Flogodownload.org%2Fwp-content%2Fuploads%2F2019%2F03%2Farduino-logo-0.png&f=1&nofb=1" height="75">

- Firebase

Banco de dados utilizado.

<img alt="Firebase" src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fpluspng.com%2Fimg-png%2Ffirebase-logo-png-firebase-logo-png-transparent-amp-svg-vector-pluspng-2400x3291.png&f=1&nofb=1" height="75">


## Contribuições Pessoais
### Hard Skills
- Lógica de programação: Eu tinha uma lógica de construção já bem forte por conta do ensino técnico antes da faculdade, fui responsável pela lógica da agenda, programei grande parte dela.
- Banco de dados: Já havia trabalhado com firebase antes no técnico, mas tive chance de poder aprender ele numa plataforma diferente da que estava acostumada e fiquei mais flexível com o uso dele.
- Kodular: Aprendi uma nova ferramenta para desenvolvimento mobile, anteriormente só tinha tido a chance de experimentar Android Studio, sendo uma ferramenta simples estou segura que se abrisse o kodular novamente poderia programar um aplicativo novamente sem grandes problemas.

### Soft Skills
- Liderança: Eu tive a ideia para o projeto e fui atrás de integrantes, falei da minha ideia para eles e aceitaram se juntando ao grupo.
- Comunicação e trabalho em equipe: Me comuniquei bastante do que fazia e como estava meu trabalho com os outros integrantes, além de levantando dúvidas pertinentes e ajudando em dificuldades de outros.




