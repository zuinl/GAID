# Manifesto GAID – Guarded AI Development

# Nomenclatura

GAID (*Guarded AI Development*) em tradução livre é **Desenvolvimento IA com Governança**. O nome foi pensado de forma a transparecer que a metodologia **promove e incentiva o uso de agentes de IA Generativa** especializados em desenvolvimento de software mas desde que haja **governança e método** nesse uso.

# Definição

O GAID é uma metodologia pensada em “remar a favor” do que muitos profissionais já estão fazendo: **utilizar IA para o desenvolvimento de software**. O GAID propõe **formalizar o uso de IA** através da **validação orientada a testes (TDD)** feito por humanos e revisão arquitetural crítica.

Em resumo, **o GAID nasceu pra trazer o controle do desenvolvimento de software de volta para os humanos usarem IA, e não o contrário**.

[Manifesto GAID.pdf](Manifesto%20GAID%20%E2%80%93%20Guarded%20AI%20Development/Manifesto_GAID.pdf)

# Os Pilares do GAID

## 1️⃣ *Human-First*

A prioridade máxima do GAID é **manter os humanos no controle** de todas as etapas de desenvolvimento. Aqui, a IA é apenas uma assistente.

## 2️⃣ TDD como Contrato

A GAID exige a validação via *Test Driven Development* (TDD, desenvolvimento orientado por testes). Os testes serão o **guia base** para que os agentes de IA criem apenas o necessário (nem mais, nem menos) e para que os humanos do time revisem e validem o código com base no que foi **definido pelos próprios humanos, não por IA**.

## 3️⃣ Uma metodologia agnóstica

O GAID propõe todo o fluxo de desenvolvimento, partindo do levantamento de requisitos, passando pelo planejamento e codificação até chegar na etapa final de entrega em produção. Mas nós **NÃO definimos como os testes devem ser escritos e nem qual agente de IA deve ser usado**. O time de humanos tem a liberdade e o controle de decidir isso por conta própria e aplicar o GAID encima do que escolherem.

## 4️⃣ IA executa, mas não decide

A IA transforma requisitos e testes em código, mas nunca define regras de negócio ou arquitetura por conta própria.

## Toda função é segregada

Quem solicita a execução à IA (Prompter) não deve ser o único a validar o resultado final. A revisão cruzada é a base da segurança.

# *Flags* de Autonomia Assistida

O uso de *Flags* de Autonomia Assistida estabelece uma classificação clara do grau de participação de agentes de IA durante todas as Etapas do GAID.

| Nível | Descrição |
| --- | --- |
| Nível 0 - Manual | IA totalmente ausente |
| Nível 1 - Consulta | IA usada para pesquisa/estudo. O código é 100% humano |
| Nível 2 - Coprodução | IA gera rascunhos e sugestões sob supervisão constante |
| Nível 3 - Execução assistida | IA gera o artefato final com base em testes. Revisão humana obrigatória |

# Papéis no GAID

Os Papéis do GAID servem para elucidar as responsabilidades de cada membro do time durante as Etapas da metodologia. Os Papéis podem ser acumulativos, ou seja, o Roteirista de Teste pode também ser Validador de Saída, por exemplo. A exceção é o Prompter, que não pode ser Validador de Saída na mesma implementação.

Os Papéis do GAID devem ser rotativos, portanto é recomendado que a cada nova implementação planejada, o time realize um rodízio das atribuições anteriores.

### Roteiristas de Testes

- São os responsáveis por planejar e escrever as suítes e casos de teste da implementação;
- Atuam como protagonistas nas Etapas 2 e 3;
- Devem estar presentes nas Etapas 1 e 6.

### *Prompter*

- Responsável pela interação com os agentes de IA, principalmente na etapa de codificação principal da implementação;
- Atuam como protagonistas na Etapa 4;
- Devem estar presentes nas Etapas 1, 2 e 6.

### Validador de Saída

- Revisor e validador de saída de artefatos gerados por agentes de IA (documentos, código);
- O *Prompter* nunca deve ser Validador de Saída na mesma implementação;
- Atuam como protagonistas na Etapa 5;
- Devem estar presentes nas Etapas 1, 2 e 6.

# Fluxo do GAID

## 1. Domínio e Planejamento Técnico Humano (*Human Domain and Planning*)

**Nível de Autonomia:** Nível 1 - Consulta

**Quem atua?** Todo o time de humanos e IA

### Objetivos da etapa

- Garantir que todo o time compreenda:
    - o objetivo (”o quê”) da implementação;
    - a justificativa (”o porquê”) da implementação;
    - a relevância da implementação: como ela impacta positivamente o negócio como um todo.
- Elaborar requisitos de *software* (funcionais e não funcionais);
- Planejar e documentar a arquitetura da implementação: essencial para que os desenvolvedores escrevam seus *prompts* para IA;
- Aplicar o conceito de Revisão Adversarial para os requisitos e planejamentos realizados.

### Definição de pronto da Etapa 1

O time deve considerar a etapa de Domínio e Planejamento Técnico Humano concluída quando:

- todos forem capazes de compreender o objetivo, justificativa e relevância da implementação proposta;
- existir uma lista de requisitos claros e compreensíveis por todos os desenvolvedores;
- os Papéis do GAID necessários para a implementação estão definidos;
- foi feita a Revisão Adversarial com IA;
- a arquitetura proposta está documentada e compreendida por todos;

## 2. Planejamento Humano de Testes (*Human Planning Tests*)

**Nível de Autonomia:** Nível 1 - Consulta

**Quem atua?** Roteirista de Testes

### Objetivos da etapa

- Planejar as suítes de testes que serão criadas, considerando os possíveis cenários e casos de teste;
- Considerar os principais cenários de uso, caminhos alternativos e casos de borda da aplicação.

### Definição de pronto da Etapa 2

O time deve considerar a etapa de Planejamento Humano de Testes concluída quando:

- toda a arquitetura planejada na Etapa 1 tiver casos de teste devidamente planejados;
- houver documentação das suítes e casos de testes planejados, a fim de serem usados na escrita e revisão deles.

## 3. Escrita e Validação Humana de Testes (*Human Writing and Validating Tests*)

**Nível de Autonomia:** Nível 1 - Consulta

**Quem atua?** Roteirista de Testes

### **Quem atua?**

Apenas o time de desenvolvedores humanos.

### Objetivos da etapa

- Escrever os testes planejados na etapa anterior, usando as bibliotecas e arquitetura definidas pelo time;
- Validar os testes escritos (*code review*) com base no que foi planejado.

### Definição de pronto da Etapa 3

O time deve considerar a etapa de Escrita e Validação Humana de Testes concluída quando:

- os testes previamente planejados na Etapa 2 estiverem desenvolvidos e organizados no repositório de acordo com a arquitetura padrão do time;
- os testes terem sido validados via processo de *code review* do time.

## 4. Implementação de Código com IA (*AI Code Implementation)*

**Nível de Autonomia:** Nível 3 - Consulta

**Quem atua?** Prompter e IA

### Objetivos da etapa

- Implementação principal (codificação) da demanda;
- utilizar agente de IA para a codificação, tendo como leis os testes previamente planejados e escritos;
- Refatorar e reorganizar, quando preciso, o código gerado pelo agente de IA;
- testar a implementação final e enviar para revisão do time.

### Definição de pronto da Etapa 4

O time deve considerar a etapa de Implementação de Código com IA concluída quando:

- todos os testes previamente planejados e escritos passam com sucesso após implementação do agente de IA;
- o(s) desenvolvedor(es) humano(s) revisaram e, se necessário, refinaram o código gerado pela IA para atender aos parâmetros de boas práticas e arquiteturas definidas pelo time;
- a implementação final funciona em ambiente de testes atendendo aos critérios de aceitação definido pelo time de negócios;
- existe *Pull Request* criada e documentada de forma a permitir a revisão do código pelo time.

## 5. Validação Humana de Código (*Human Code Validation*)

**Nível de Autonomia:** Nível 0 - Manual

**Quem atua?** Validador de saída

### Objetivos da etapa

- Revisar todo o código gerado pelo agente de IA;
- Garantir a conformidade com os parâmetros de arquitetura do projeto;
- Solicitar e aplicar, quando necessário, ajustes finais na implementação da demanda.

### Definição de pronto da Etapa 5

O time deve considerar a etapa de Validação Humana de Código concluída quando:

- todo o código criado pelo agente de IA sob monitoramento dos desenvolvedores foi revisado pelos responsáveis técnicos do time;
- o código que está entrando na base principal do repositório segue os parâmetros de arquitetura, boas práticas e performances existentes do projeto;
- a implementação final funciona e atende aos critérios de aceitação definidos pelo time de negócio.

## 6. *Feedback Loop*

A etapa de *Feedback Loop* visa atender às eventuais necessidades de mudanças e/ou *bugs* após o processo inicial de desenvolvimento (Etapas 1 a 5). Em resumo, esta etapa tem por objetivo garantir o entendimento da nova necessidade e levar o time à Etapa 2 para o tratamento do caso.

**Nível de Autonomia:** Nível 2 - Coprodução

**Quem atua?** O time de humanos e IA

### Objetivos da etapa

- Direcionar corretamente as eventuais mudanças e/ou *bugs* que surjam após o desenvolvimento inicial;
- Garantir a circularidade do processo do GAID, onde toda iteração no repositório seja devidamente governada;
- Fazer uso de agentes de IA para reprodução local de problemas, resumo e tradução técnica de documentos de mudança e até como diagnosticadora do problema raiz.

### Definição de pronto da Etapa 6

O time deve considerar a etapa de *Feedback Loop* concluída quando:

- após o registro de uma solicitação de mudança ou de um *bug* encontrado, o time técnico compreendeu o que é preciso ser alterado;
- com o entendimento tácito da mudança, o time deve iniciar o tratamento da mudança pela etapa 2 do GAID.