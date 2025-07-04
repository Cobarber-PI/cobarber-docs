# Cobarber

Um modelo para o desenvolvimento do Projeto Integrador do Curso de Técnico em Desenvolvimento de Sistemas para a Internet Integrado ao Ensino Médio do IFC - Campus Araquari.

*O sistema Cobarber é uma plataforma web/mobile que intermediará a comunicação de barbeiros/cabelereiros com seus clientes, com o objetivo de oferecer uma solução prática, moderna e eficiente para o agendamento de serviços. Através de uma interface amigável e intuitiva, os barbeiros poderão cadastrar seus horários disponíveis, gerenciar sua agenda, cadastrar serviços oferecidos (como corte, barba, sobrancelha, entre outros), além de acompanhar estatísticas de atendimentos. Por outro lado, os clientes poderão visualizar horários disponíveis, realizar agendamentos e receber notificações automáticas para o seu compromisso.*

## IMPORTANTE: link do projeto: (https://github.com/Cobarber-PI)

Professor: [Marco André Mendes](github.com/marcoandre)

Equipe:
- [Henrique Dias Belboni Silva](https://github.com/Henrique0330)
- [Marco Antonio Peruzzo](https://github.com/MarcoPeruzzocmd)
- [Eduardo Gustavo Bomsenhor](https://github.com/goodsir6)

Links do projeto:
-   Documentação: [esse documento](https://github.com/Cobarber-PI/cobarber-docs)
-   Backend: [Repositório](https://github.com/Cobarber-PI/cobarber-backend) e [Publicação] ainda não disponível
-   Frontend: [Repositório](https://github.com/Cobarber-PI/cobarber-frontend) e [Publicação] ainda não disponível

# 1. Desenvolvimento

**1.1.3 Ordem de Serviço (O.S.)**

O sistema de agendamento de horários para barbeiros permitirá que trabalhadores e donos do estabelecimento tenham suas agendas preenchidas automaticamente, com base nos horários e serviços disponíveis predefinidos pelo mesmo. Além de gerar relatórios diários/mensais para consulta ao faturamento da empresa. Por outo lado, o cliente poderá agendar seu horário, após se cadastrar informando seu email e telefone, sem se preocupar em ter que receber algum retorno (como o barbeiro precisar atender sua ligação), e receber notificações para o compromisso. O agendamento será enviado automaticamente para o sistema do prestador de serviço, registrando-se na agenda com dia, horário, serviço e preferências do cliente. Após finalizar o dia, o sistema reinicia automaticamente os horários, deixando-os disponíveis para novos agendamentos.

# 2. Situação Problema

A Berto e Reis é uma barbearia de pequeno porte fundada em 2020 pelo barbeiro João Berto, localizada em um bairro residencial da cidade. Inicialmente, João atendia sozinho em um pequeno espaço improvisado, mas, com o tempo e a fidelização dos clientes, o negócio cresceu e atualmente conta com quatro profissionais no atendimento e uma clientela ampla e variada. Com isso, a demanda por cortes, barba e demais serviços aumentou significativamente, fazendo com que a organização da agenda se tornasse uma tarefa cada vez mais desafiadora.
 Atualmente, os serviços da barbearia são agendados por meio de mensagens em redes sociais ou ligações para os barbeiros, o que torna o processo lento e desorganizado. Muitas vezes, a comunicação é feita utillizando o contato pessoal do trabalhador, exigindo que o profissional pare suas atividades e responda fora de hora, ou até mesmo misturando seus clientes com contatos pessoais. Além disso, é comum o agendamento ser esquecido, mal anotado ou sobreposto a outros compromissos, o que gera transtornos tanto para os clientes quanto para os profissionais. Outro problema é a dificuldade do barbeiro em gerir o controle da movimentação financeira e de clientes durante o mês, sem saber ao certo quais dias são mais movimentados ou lucrativos.
 A partir da análise da situação atual, é possível identificar que a barbearia enfrenta desafios relacionados à organização dos agendamentos, falta de automatização, baixa eficiência na comunicação com o cliente e ausência do controle de dados financeiros. Nosso objetivo é criar uma forma de comunicação única e agilizada entre o cliente e o barbeiro, sem a necessidade da disponibilidade de ambos ao mesmo tempo. Além de automatizar os agendamentos, exibir horários disponíveis em tempo real e centralizar o controle da agenda de todos os profissionais. Ademais a isso, o sistema contribuirá com a gestão da berbearia, gerando relatórios para o controle financeiro.

# 3. Descrição da proposta

O Cobarber é um sistema focado na agilidade de comunicação de cliente para profissional, utilizando-se de horários e serviços predefinidos pelos barbeiros, com foco em liberdade e independência de ambos os lados. Os trabalhadores do local (que também administrarão o sistema da sua barbearia) serão cadastrados e definirão serviços e horários disponíveis em cada dia da semana, fazendo assim com que os clientes que se cadastrarem possam escolher determinado tipo de serviço, horário e o barbeiro de sua preferência, além de receber notificações automáticas para o seu compromisso.

# 4. Modelagem de Dados

![image](https://github.com/user-attachments/assets/fb952fae-3a44-464c-9918-6cddfcfdda01)



# 4. Regras de negócio

**RN001 – Cadastro de Usuário:** O sistema deve permitir o cadastro de clientes e barbeiros com nome, e-mail, senha, número de celular, data de nascimento e CPF.  

**RN002 – Níveis de Acesso:** O sistema deve diferenciar os acessos de cliente, barbeiro(administrador).

**RN003 – Agendamento de Horário:** Apenas clientes registrados podem agendar horários disponíveis com barbeiros.

**RN004 – Horários Disponíveis:** Barbeiros podem cadastrar, editar e excluir seus horários disponíveis.  

**RN005 – Cancelamento de Agendamento:** Clientes podem cancelar seus agendamentos antes da data marcada.

**RN006 – Multa de cancelamento:** O cliente será cobrado uma taxa de R$10,00 caso cancele o agendamento com 3 horas ou menos de antecedência. 

**RN007 – Avaliação de Atendimento:** Clientes podem deixar uma avaliação sobre o barbeiro após o serviço.  

**RN008 – Confirmação por E-mail:** O sistema deve enviar e-mails confirmando agendamentos e suas informações.  

**RN009 – Visualização de Agenda:** Barbeiros podem visualizar todos os agendamentos feitos com eles.  

**RN0010 – Comentários Visíveis:** Comentários dos clientes ficam públicos no perfil do barbeiro.  


# 5. Requisitos funcionais

**Entradas:**

**RF001 – Cadastro de Usuário:** O sistema deve permitir o cadastro de clientes e barbeiros, diferenciando-os pelo nível de acesso.  
  **Dados:** Nome, e-mail, senha, nível de acesso (cliente ou barbeiro).  

**RF002 – Login:** O sistema deve permitir que usuários entrem com e-mail e senha cadastrados.  
  **Dados:** E-mail, senha.  

**RF003 – Cadastro de Horários:** O sistema deve permitir que barbeiros cadastrem horários disponíveis para o atendimento.  
  **Dados:** Data, hora, barbeiro.  

**RF004 – Agendamento de Horário:** O sistema deve permitir que clientes escolham um barbeiro e agendem um horário disponível.  
  **Dados:** Data, hora, barbeiro, cliente.  

**RF005 – Avaliação do Atendimento:** O sistema deve permitir que o cliente avalie o barbeiro após o atendimento.  
  **Dados:** Nota (1 a 5), comentário, cliente, barbeiro.  


**Processamento:**

**RF006 – Verificação de Horários:** O sistema deve verificar se á horario disponível antes de realizar o agendamento.  
  **Dados:** Data, hora, barbeiro.  

**RF007 – Confirmação por E-mail:** O sistema deve enviar um e-mail automático ao cliente confirmando o agendamento.  
  **Dados:** Nome do cliente, nome do barbeiro, data, hora, e-mail.  

**RF008 – Cancelamento de Agendamento:** O sistema deve permitir que o cliente cancele um agendamento já feito.  
  **Dados:** Data, hora, barbeiro, taxa, cliente,   

**RF009 – Notificação agendamento:** O sistema deve enviar um e-mail para o barbeiro quando houver cancelamento de um corte.  
  **Dados:** Lista de agendamentos, datas, horários, nomes dos clientes.  

**RF0010 – Reabrir horário após cancelamento:** Quando o cliente cancelar um agendamento de corte, o sistema deve reabrir o horário para ser agendado por outro cliente.  
  **Dados:** Datas, horários, barbeiro.  

**RF0011 – Exibição da Agenda:** O sistema deve mostrar ao barbeiro sua agenda com todos os agendamentos marcados.  
  **Dados:** Lista de agendamentos, datas, horários, nomes dos clientes.  


**Saídas:**

**RF010 – Listagem de Barbeiros:*** O sistema deve exibir todos os barbeiros disponíveis para o cliente escolher.  
  **Dados:** Nome, especialidade, avaliações.  

**RF011 – Exibição de Comentários:** O sistema deve exibir avaliações e comentários de clientes nos perfis dos barbeiros.  
  **Dados:** Nome do cliente, nota, comentário.  

**RF012 – Notificações por E-mail:** O sistema deve notificar os usuários sobre alterações nos agendamentos.  
  **Dados:** E-mail do usuário, tipo de notificação (cancelamento, alteração), data, hora.  


# 6. Requisitos não funcionais


**RNF001 – O backend do sistema deve ser feito com o framework Django.**  
**RNF002 – O frontend do sistema deve ser feito com o framework Vue.js.**  
**RNF003 – O sistema deve ser hospedado no GitHub.**

**RNF004 – O sistema deve ser intuitivo e simples.**

# 7. Diagrama de Caso de Uso

**7.1 Introdução**

O diagrama de caso de uso é uma ferramenta de modelagem que descreve o comportamento de um sistema a partir da perspectiva do usuário. Ele é usado para capturar os requisitos funcionais de um sistema.

- Especificam a visão externa do sistema.
- Descrevem como o sistema é percebido por seus usuários.
- Descrevem as interações entre os usuários e o sistema.

![Diagrama de Caso de Uso](img/dcu1.png "Diagrama de Caso de Uso")

**Os casos de uso:**
- Descrevem como os **usuários interagem com o sistema** (as funcionalidades do sistema)
- Facilitam a **organização dos requisitos** de um sistema.
- Dão uma **visão externa** do sistema
- O conjunto de casos de uso deve ser capaz de comunicar a **funcionalidade** e o **comportamento** do sistema para o cliente.
- Descrevem **o que** o sistema faz, mas **não** especificam **como** isso deve ser feito.

**7.2 Elementos do diagrama de caso de uso**

7.2.1 **Atores**

- Representam os papéis desempenhados por **elementos externos** ao sistema
  - Ex: humano (usuário), dispositivo de hardware ou outro sistema (cliente)
- Elementos que **interagem** com o sistema

Notação:

![Atores Notação](img/dcu_atores_notacao.png "Atores Notação")

**Exemplo: Loja de CDs**

**Identificando os atores**
- Uma loja de CDs possui discos para venda. Um cliente pode comprar uma quantidade ilimitada de discos para isto ele deve se dirigir à loja.
- A loja possui um **atendente** cuja função é atender os clientes durante a venda dos discos. A loja também possui um **gerente** cuja função é administrar o estoque para que não faltem discos. Além disso é ele quem dá folga ao atendente, ou seja, ele também atende os clientes durante a venda dos discos.

![Identificando os atores](img/dcu_identificando_atores.png "Identificando os atores")

**E o cliente?**
- Não é ator pois ele **não interage** com o sistema!

**7.2.2 Casos de uso**

- Representam **funcionalidades** do sistema (requisitos funcionais).
- São iniciados por **atores** ou por outros casos de uso.

> **Dica**: nomeie os casos de uso com **verbos** no **infinitivo**.

Notação:

![Casos de uso Notação](img/dcu_casos_de_uso_notacao.png "Casos de uso Notação")

**Exemplo: Loja de CDs**

**Identificando os casos de uso**

- Uma loja de CDs possui discos para venda. Um cliente pode comprar uma quantidade ilimitada de discos para isto ele deve se dirigir à loja. A loja possui um atendente cuja função é atender os clientes durante a **venda dos discos**.
- A loja também possui um gerente cuja função é **administrar o estoque** para que não faltem discos. Além disso é ele quem dá folga ao atendente, ou seja, ele também atende os clientes durante a **venda dos discos**.

![Identificando os casos de uso](img/dcu_identificando_casos_de_uso.png "Identificando os casos de uso")

**7.2.3 Relacionamentos**

**7.2.3.1 Relacionamento de associação**

- Indica que um ator **participa** de um caso de uso, ou seja, o ator **interage** (comunica-se) com o caso de uso.
- É representado por uma **linha sólida**.
- Um ator pode se relacionar com **um ou mais casos de uso**.

> Dicas:
> - Não use setas nas linhas de associação.
> - Associações não representam fluxo de informação.

![Relacionamento de associação](img/dcu_relacionamento_de_associacao.png "Relacionamento de associação")

**Exemplo: Loja de CDs**

**Identificando os relacionamentos de associação**

- Uma loja de CDs possui discos para venda. Um cliente pode comprar uma quantidade ilimitada de discos para isto ele deve se dirigir à loja. A loja possui um _atendente_ cuja função é atender os clientes durante a **venda dos discos**.
- A loja também possui um _gerente_ cuja função é **administrar o estoque** para que não faltem discos. Além disso é ele quem dá folga ao _atendente_, ou seja, ele também atende os clientes durante a **venda dos discos**.

![Identificando os relacionamentos de associação](img/dcu_identificando_relacionamentos_de_associacao.png "Identificando os relacionamentos de associação")

**7.2.3.2 Relacionamento de generalização/especialização**

**Generalização de atores**

- Quando dois ou mais atores podem se **comunicar com o mesmo conjunto de casos de uso**.
- Indica que um ator **herda** as características de outro ator.
– Um filho (herdeiro) pode se comunicar com todos os casos de uso que seu pai se comunica.

> **Dica:** coloque os herdeiros **embaixo**.

**Notação:**

![Relacionamento de generalização/especialização de atores - notação](img/dcu_relacionamento_de_generalizacao_especializacao_notacao_de_atores.png "Relacionamento de generalização/especialização de atores - notação")

**Exemplo: Loja de CDs**

**Identificando os relacionamentos de generalização/especialização de atores**

![Identificando os relacionamentos de generalização/especialização de atores](img/dcu_identificando_relacionamentos_de_generalizacao_especializacao_de_atores.png "Identificando os relacionamentos de generalização/especialização de atores")

**Generalização de casos de uso**

– O caso de uso filho herda o comportamento e o significado do caso de uso pai.
– O caso de uso filho pode incluir ou sobrescrever o comportamento do caso de uso pai.
– O caso de uso filho pode substituir o caso de uso pai em qualquer lugar que ele apareça.

> **Dica:** deve ser aplicada quando uma condição resulta na definição de
diversos fluxos alternativos.

Notação:

![Relacionamento de generalização/especialização de casos de uso - notação](img/dcu_relacionamento_de_generalizacao_especializacao_notacao_de_casos_de_uso.png "Relacionamento de generalização/especialização de casos de uso - notação")

**Exemplo: Loja de CDs**

**Identificando os relacionamentos de generalização/especialização de casos de uso**

**Novos requisitos:**

- As vendas podem ser **à vista** ou **a prazo**. Em ambos os casos o estoque é
atualizado e uma nota fiscal, entregue ao consumidor.
- No caso de uma **venda à vista**, clientes cadastrados na loja e que compram mais de 5 CDs de uma só vez ganham um desconto de 1% para cada ano de cadastro.
- No caso de uma **venda a prazo**, ela pode ser parcelada em 2 pagamentos com um
acréscimo de 20%. As vendas a prazo podem ser pagas no **cartão** ou no **boleto**.
  - Para pagamento com **boleto**, são gerados boletos bancários que são entregues ao cliente e armazenados no sistema para lançamento posterior no caixa.
  - Para pagamento com **cartão**, os clientes com mais de 10 anos de cadastro na loja ganham o mesmo desconto das compras à vista.

![Identificando os relacionamentos de generalização/especialização de casos de uso](img/dcu_identificando_relacionamentos_de_generalizacao_especializacao_de_casos_de_uso.png "Identificando os relacionamentos de generalização/especialização de casos de uso")

**Identificando mais relacionamentos de generalização/especialização de casos de uso**

![Identificando mais relacionamentos de generalização/especialização de casos de uso](img/dcu_identificando_mais_relacionamentos_de_generalizacao_especializacao_de_casos_de_uso.png "Identificando mais relacionamentos de generalização/especialização de casos de uso")

**7.2.3.3 Relacionamento de dependência**

**Extensão**

- Representa uma variação/extensão do comportamento do caso de uso base.
- O caso de uso estendido só é executado sob certas circunstâncias.
- Separa partes obrigatórias de partes opcionais.
  - Partes obrigatórias: caso de uso base.
  - Partes opcionais: caso de uso estendido.
- Fatorar comportamentos variantes do sistema (podendo reusar este comportamento
em outros casos de uso).

**Notação:**

![Relacionamento de dependência (extensão) - notação](img/dcu_relacionamento_de_dependencia_extensao_notacao.png "Relacionamento de dependência (extensão) - notação")

**Exemplo: Loja de CDs**

**Identificando os relacionamentos de dependência (extensão)**

**Novos requisitos:**
- No caso de uma venda à vista, clientes cadastrados na loja e que compram mais
de 5 CDs de uma só vez ganham um **desconto** de 1% para cada ano de cadastro.
- No caso de uma venda a prazo...
  - ...Para pagamento com cartão, os clientes com mais de 10 anos de cadastro na loja ganham o mesmo **desconto** das compras à vista.

![Identificando os relacionamentos de dependência (extensão)](img/dcu_identificando_relacionamentos_de_dependencia_extensao.png "Identificando os relacionamentos de dependência (extensão)")

**Inclusão**

- Evita repetição ao fatorar uma atividade
comum a dois ou mais casos de uso.
- Um caso de uso pode incluir vários casos de uso.

**Notação:**

![Relacionamento de dependência (inclusão) - notação](img/dcu_relacionamento_de_dependencia_inclusao_notacao.png "Relacionamento de dependência (inclusão) - notação")

**Exemplo: Loja de CDs**

**Novos requisitos:**
Para efetuar vendas ou administrar estoque, atendentes e gerentes terão que **validar** suas respectivas senhas de
acesso ao sistema.

![Identificando os relacionamentos de dependência (inclusão)](img/dcu_identificando_relacionamentos_de_dependencia_inclusao.png "Identificando os relacionamentos de dependência (inclusão)")

**7.2.4 Fronteira do sistema**

- Elemento opcional (mas essencial para um bom
entendimento).
- Serve para definir a área de atuação do sistema, ou seja, seus limites.

**Identificando a fronteira do sistema**

![Identificando a fronteira do sistema](img/dcu_identificando_a_fronteira_do_sistema.png "Identificando a fronteira do sistema")

---



