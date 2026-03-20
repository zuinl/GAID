# 📜 Manifesto GAID – _Guarded AI Development_

## 🔤 Nomenclatura

GAID (*Guarded AI Development*) em tradução livre é **Desenvolvimento IA com Governança**. O nome foi pensado de forma a deixar claro que a metodologia **promove e incentiva o uso de agentes de IA Generativa** especializados em desenvolvimento de software mas desde que haja **governança e método** nesse uso.

## 📍 Definição

O GAID é uma metodologia pensada em “remar a favor” do que muitos profissionais já estão fazendo: **utilizar IA generativa para o desenvolvimento de software**. O GAID propõe **formalizar o uso de IA** através da **validação orientada a testes (TDD)** feito por humanos e revisão arquitetural crítica.

Em resumo, **o GAID nasceu pra trazer o controle do desenvolvimento de software de volta para os humanos usarem IA, e não o contrário**.

### 🤔 Quando faz sentido adotar o GAID?

A metodologia GAID pode ser usada como **complemento no método de trabalho de qualquer time**, pois seu foco principal é a formalização e governança do uso de IA através da validação centrada no TDD.

No entanto, para o GAID venha para somar e não cause efeitos negativos no seu time, recomenda-se observar estes pontos:

1. **O time, como um todo, já possui um processo geral bem definido**: pode ser uma metodologia ágil como o Kanban ou o Scrum, ou qualquer outro método que já está maduro e funcional no time (produto, desenvolvimento, qualidade). Isso garante que o GAID seja como um _plugin_ instalado no time e que possa ser removido a qualquer momento sem prejuízos;
2. **Existe o hábito de teste de _software_**: não é obrigatório que já se faça uso do TDD, mas é importante que os desenvolvedores envolvidos já tenham um bom domínio de bibliotecas de teste. Isso reduz a curva de adaptação à metodologia, uma vez que o GAID **é agnóstico e deixa à escolha do time a decisão tecnológica**;
3. **Há diversidade de senioridade**: o GAID se baseia em revisão contínua e, para isso, é importante que exista **ao menos um membro do time com um alto conhecimento do negócio** e da _stack_ tecnológica. Por outro lado, se houverem apenas membros de alta senioridade, o GAID pode não trazer os resultados esperados. **O GAID pode ser muito mais aproveitado em times diversos**, permitindo compartilhamento de conhecimento e aprendizado contínuo entre os desenvolvedores.

### 🚫 O que o GAID **NÃO É**
- O GAID **não é** um substitut e/ou alternativa para metodologias ágeis (como SCRUM ou Kanban). Não existe organização de cerimônias, gestão de _backlog_ e entregas. O GAID atua como complemento a métodos já instalados no time;
- **não é** um _framework_ de arquitetura nem padrão de implementação, pois não define estrtura arquitetural, linguagem a ser usada, bibliotecas, árvore de diretórios, ferramentas de CI/CD, etc. **O GAID não inclui o "como desenvolver"**, apenas implementa governança;
- **não é "carta verde" para uso de qualquer modelo de IA**. Apesar de ser uma metodologia agnóstica, o GAID recomenda fortemente que haja políticas bem definidas de quais agentes de IA o time deverá usar e como;
- **o GAID não é _vibe coding_** pois rejeita qualquer proposta de construção de _software_ rápida sem comportamento claramente planejado. A IA acelera o processo, mas **os donos da _vibe_ ainda são os humanos**;
- **não é uma política corporativa de normas de uso de IA** pois seu foco é exclusivamente o processo de desenvolvimento de _software_ e não substitui normas organizacionais de segurança e _compliance_ em relação ao uso de IA.

## 🏛️ Os Pilares do GAID

### 1️⃣ *Human-First*

A prioridade máxima do GAID é **manter os humanos no controle** de todas as etapas de desenvolvimento. Aqui, a IA é apenas uma assistente.

### 2️⃣ TDD como Contrato

A GAID exige a validação via *Test Driven Development* (TDD, desenvolvimento orientado por testes). Os testes serão o **guia base** para que os agentes de IA criem apenas o necessário (nem mais, nem menos) e para que os humanos do time revisem e validem o código com base no que foi **definido pelos próprios humanos, não por IA**.

### 3️⃣ Uma metodologia agnóstica

O GAID propõe todo o fluxo de desenvolvimento, partindo do levantamento de requisitos, passando pelo planejamento e codificação até a possível regressão para correção de _bugs_. Mas nós **NÃO definimos como os testes devem ser escritos e nem qual agente de IA deve ser usado**. O time de humanos tem a liberdade e o controle de decidir isso por conta própria e aplicar o GAID encima do que escolherem.

### 4️⃣ IA executa, mas não decide

A IA transforma requisitos e testes em código, mas nunca define regras de negócio ou arquitetura por conta própria.

### 5️⃣ Toda função é segregada

Quem solicita a execução à IA (_Prompter_) não deve validar o resultado final. A revisão cruzada é a base da segurança.

## 🚩 *Flags* de Autonomia Assistida

O uso de *Flags* de Autonomia Assistida estabelece uma classificação clara do grau de participação de agentes de IA durante todas as Etapas do GAID.

| Nível | Descrição |
| --- | --- |
| 🔴 Nível 0 - Manual | IA totalmente ausente |
| 🟠 Nível 1 - Consulta | IA usada para pesquisa/estudo. O código é 100% humano |
| 🔵 Nível 2 - Coprodução | IA gera rascunhos e sugestões sob supervisão constante |
| 🟢 Nível 3 - Execução assistida | IA gera o artefato final com base em testes. Revisão humana obrigatória |

## 👥 Funções no GAID

As Funções do GAID servem para elucidar as responsabilidades de cada membro do time durante as Etapas da metodologia. As Funções podem ser acumuladas, ou seja, o Roteirista de Testes pode também ser Validador de Saída, por exemplo. A exceção é o _Prompter_, que **não pode ser Validador de Saída**.

As Funções do GAID devem ser rotativas, portanto é recomendado que a cada nova implementação planejada, o time realize um rodízio das atribuições anteriores.

**IMPORTANTE:** na metodologia GAID, usamos as Funções como guias para recomendar organização de atribuições e responsabilidades do time. Mas o GAID **não incentiva** mudanças disruptivas na cultura do time, como cerimônias e reuniões pré existentes. Em outras palavras: quando dizemos, por exemplo, que na Etapa 2 deve participar o Roteirista de Testes, isso **não significa que apenas ele cuidará da etapa**. A regra de ouro que segue valendo é: o GAID é agnóstico e deve se adaptar à cultura atual do time.

### Planejador da Implementação

- Planeja e documenta os requisitos da implementação de acordo com as regras de negócio. Garante que a arquitetura e boas práticas definidas pelo time sejam seguidas;
- Atua como protagonista na Etapa 1;
- Presença obrigatória na Etapa 6.

### Roteirista de Testes

- Planeja e escreve as suítes e casos de teste da implementação;
- Atua como protagonista nas Etapas 2 e 3;
- Presença obrigatório nas Etapas 1 e 6.

### *Prompter*

- Interage com os agentes de IA, principalmente na etapa de codificação principal da implementação;
- Atua como protagonista na Etapa 4;
- Presença obrigatória nas Etapas 1, 2 e 6.

### Validador de Saída

- Revisa e valida a saída de artefatos gerados por agentes de IA (documentos, código);
- Nunca deve ser Validador de Saída;
- Atua como protagonista na Etapa 5;
- Presença obrigatória nas Etapas 1, 2 e 6.

## Revisão Adversarial

TODO

## Etapas do GAID

### 1. Domínio e Planejamento Técnico Humano (*Human Domain and Planning*)

**Nível de Autonomia:** 🟠 Nível 1 - Consulta

**Protagonista:** Planejador da Implementação

**Quem participa?** Planejador da Implementação, Roteirista de Testes, _Prompter_ e Validador de Saída

**Objetivos da Etapa 1**

- Garantir que todo o time compreenda:
    - o objetivo (”o quê”) da implementação;
    - a justificativa (”o porquê”) da implementação;
    - a relevância da implementação: como ela impacta positivamente o negócio como um todo.
- Elaborar requisitos de *software* (funcionais e não funcionais);
- Planejar e documentar a arquitetura da implementação: essencial para que os desenvolvedores escrevam seus *prompts* para IA;
- Aplicar o conceito de Revisão Adversarial para os requisitos e planejamentos realizados.

**Definição de pronto da Etapa 1**

O time deve considerar a etapa de Domínio e Planejamento Técnico Humano concluída quando:

- todos forem capazes de compreender o objetivo, justificativa e relevância da implementação proposta;
- existir uma lista de requisitos claros e compreensíveis por todos os desenvolvedores;
- as Funções do GAID necessárias para a implementação estão definidos;
- foi feita a Revisão Adversarial com IA;
- a arquitetura proposta está documentada e compreendida por todos.

### 2. Planejamento Humano de Testes (*Human Planning Tests*)

**Nível de Autonomia:** 🟠 Nível 1 - Consulta

**Protagonista:** Roteirista de Testes

**Quem participa?** Roteirista de Testes

**Objetivos da Etapa 2**

- Planejar as suítes de testes que serão criadas, considerando os possíveis cenários e casos de teste;
- Considerar os principais cenários de uso, caminhos alternativos e casos de borda da aplicação.

**Definição de pronto da Etapa 2**

O time deve considerar a etapa de Planejamento Humano de Testes concluída quando:

- toda a arquitetura planejada na Etapa 1 tiver casos de teste devidamente planejados;
- houver documentação das suítes e casos de testes planejados, a fim de serem usados na escrita e revisão deles;
- os testes escritos foram validados pelos outros membros a fim de detecção de _gaps_ e inconsistências.

### 3. Escrita e Validação Humana de Testes (*Human Writing and Validating Tests*)

**Nível de Autonomia:** 🟠 Nível 1 - Consulta

**Protagonista:** Roteirista de Testes

**Quem participa?** Roteirista de Testes

**Objetivos da Etapa 3**

- Escrever os testes planejados na etapa anterior, usando as bibliotecas e arquitetura definidas pelo time;
- Validar os testes escritos (*code review*) com base no que foi planejado.

**Definição de pronto da Etapa 3**

O time deve considerar a etapa de Escrita e Validação Humana de Testes concluída quando:

- os testes previamente planejados na Etapa 2 estiverem desenvolvidos e organizados no repositório de acordo com a arquitetura padrão do time;
- os testes terem sido validados via processo de *code review* do time.

### 4. Implementação de Código com IA (*AI Code Implementation)*

**Nível de Autonomia:** 🟢 Nível 3 - Execução Assistida

**Protagonista:** _Prompter_

**Quem participa?** _Prompter_

**Objetivos da Etapa 4**

- Implementação principal (codificação) da demanda;
- utilizar agente de IA para a codificação, tendo como leis os testes previamente planejados e escritos;
- Refatorar e reorganizar, quando preciso, o código gerado pelo agente de IA;
- testar a implementação final e enviar para revisão do time.

**Definição de pronto da Etapa 4**

O time deve considerar a etapa de Implementação de Código com IA concluída quando:

- todos os testes previamente planejados e escritos passam com sucesso após implementação do agente de IA;
- os desenvolvedores humanos revisaram e, se necessário, refinaram o código gerado pela IA para atender aos parâmetros de boas práticas e arquiteturas definidas pelo time;
- a implementação final funciona em ambiente de testes atendendo aos critérios de aceitação definido pelo time de negócios;
- existe *Pull Request* criada e documentada de forma a permitir a revisão do código pelo time.

### 5. Validação Humana de Código (*Human Code Validation*)

**Nível de Autonomia:** 🔴 Nível 0 - Manual

**Protagonista:** Validador de Saída

**Quem participa?** Planejador da Implementação e Validador de Saída.

**Objetivos da Etapa 5**

- Revisar todo o código gerado pelo agente de IA;
- Garantir a conformidade com os parâmetros de arquitetura do projeto e planejamento realizado na Etapa 1;
- Solicitar e aplicar, quando necessário, ajustes finais na implementação da demanda.

**Definição de pronto da Etapa 5**

O time deve considerar a etapa de Validação Humana de Código concluída quando:

- todo o código criado pelo agente de IA sob monitoramento dos desenvolvedores foi revisado pelo do time;
- o código que está entrando na base principal do repositório segue os parâmetros de arquitetura, boas práticas e performances existentes do projeto;
- a implementação final funciona e atende aos critérios de aceitação definidos pelo time de negócio.

### 6. *Feedback Loop*

A etapa de *Feedback Loop* visa atender às eventuais necessidades de mudanças e/ou *bugs* após o processo inicial de desenvolvimento (Etapas 1 a 5). Em resumo, esta etapa tem por objetivo garantir o entendimento da nova necessidade e devolver o time à Etapa 2 para o tratamento do caso.

**Nível de Autonomia:** 🔵 Nível 2 - Coprodução

**Protagonista:** Planejador da Implementação

**Quem participa?** Planejador da Implementação

**Objetivos da Etapa 6**

- Direcionar corretamente as eventuais mudanças e/ou *bugs* que surjam após o desenvolvimento inicial;
- Garantir a circularidade do processo do GAID, onde toda iteração no repositório seja devidamente governada;
- Fazer uso de agentes de IA para reprodução local de problemas, resumo e tradução técnica de documentos de mudança e até como diagnosticadora do problema raiz.

**Definição de pronto da Etapa 6**

O time deve considerar a etapa de *Feedback Loop* concluída quando:

- após o registro de uma solicitação de mudança ou de um *bug* encontrado, o time técnico compreendeu o que é preciso ser alterado;
- com o entendimento tácito da mudança, o time deve iniciar o tratamento da mudança pela etapa 2 do GAID.
