# GAID Manifesto – Guarded AI Development

## Nomenclature

**GAID (Guarded AI Development)** can be freely translated as **AI Development with Governance**.  
The name was designed to make it clear that the methodology promotes and encourages the use of Generative AI agents specialized in software development — but only when that use is guided by governance and method.

## Definition

GAID is a methodology designed to work **with the reality of what many professionals are already doing**: using AI in software development.  
GAID proposes formalizing that use of AI through **human-led test-driven validation (TDD)** and **critical architectural review**.

In short, GAID was created to bring control of software development back to humans using AI — **not the other way around**.

## The Pillars of GAID

### 1️⃣ Human-First

GAID’s highest priority is to keep humans in control throughout every stage of development.  
Here, AI is only an assistant that takes on operational work.

### 2️⃣ Test-First Always

GAID requires validation through **Test Driven Development (TDD)**.  
Tests are the foundational guide that ensures AI agents create **only what is necessary** — no more, no less — and that the human team reviews and validates the code based on what was defined by humans themselves, not by AI.

### 3️⃣ A Flexible Methodology

GAID defines the overall development flow, from requirements gathering to planning, implementation, and final delivery into production.  
However, it does **not** define how tests must be written, nor which AI agent must be used.

The human team has the freedom and control to decide that for itself and apply GAID on top of those choices.

### 4️⃣ AI Only Writes Code

The AI agent only writes code based on the tests planned by the team and the prompts provided.  
It never makes decisions on its own. Never.

### 5️⃣ Segregation of Duties

The person responsible for implementing code with AI (the **Prompter**) must never be the same person who validates that implementation.

## Assisted Autonomy Levels

The use of **Assisted Autonomy Levels** establishes a clear classification of how much AI agents participate throughout the stages of GAID.

- **🔴 Level 0 (Manual):** complete absence of AI agents. Everything must be conceived, planned, and executed by humans.
- **🟠 Level 1 (Consultation):** AI agents may be used as a source of information or research, but the final content and decision must be 100% written by humans.
- **🔵 Level 2 (Co-creation):** AI may generate drafts and suggest changes (code, documentation, tests) under continuous human supervision. Nothing should be transferred directly from the AI agent without first going through human review and reorganization.
- **🟢 Level 3 (Assisted Execution):** the AI agent performs tasks with a high degree of autonomy. Final responsibility still remains under human review, but at this level it is acceptable for a result to be 100% produced by AI, as long as it is properly validated.

## Roles in GAID

- **Test Designer**
- **Prompter**
- **Output Validator**

## GAID Flow

### 1. Human Domain and Technical Planning

**Who is involved?**  
Only the human development team.

**Stage goals**
- Ensure the entire team understands:
  - the objective (**what**) of the implementation
  - the justification (**why**) of the implementation
  - the relevance of the implementation and how it positively impacts the business as a whole
- Define software requirements (functional and non-functional)
- Plan and document the implementation architecture, which is essential for developers to later write prompts for AI

**Definition of Done for Stage 1**  
The team should consider the Human Domain and Technical Planning stage complete when:
- everyone is able to understand the objective, justification, and relevance of the proposed implementation
- there is a list of clear requirements that all developers can understand
- the necessary GAID roles for the implementation have been defined
- the proposed architecture is documented and understood by everyone
- developers know which files must exist and what each one is responsible for

This depends on the stack the team uses, and it is not GAID’s role to prescribe architecture.  
What matters most is that developers clearly understand which files should exist and what their responsibilities are. This is essential because GAID tests are written based on the expected behavior of each architectural component.

### 2. Adversarial Review: AI versus Human

**Who is involved?**  
Humans and AI agents.

**Stage goals**
- Subject the requirements produced in Stage 1 to a stress test
- Identify logical flaws, exception scenarios, ambiguities, and incorrect assumptions that could compromise later stages
- Review both business requirements and technical requirements
- Use a “Devil’s Advocate” AI agent to challenge and raise discussion points about what the human team has refined

**Definition of Done for Stage 2**  
The team should consider the Adversarial Review stage complete when:
- the “Devil’s Advocate” AI agent has been given the full implementation context and asked to search for ambiguities or possible flaws
- the human team has considered, discussed, and, when necessary, rewritten the requirements that were demonstrably shown to be incorrect

### 3. Human Test Planning

In GAID, tests are not only about code coverage.  
They are the **behavioral contract** that will guide the work of AI agents during implementation.

**Who is involved?**  
Only the human development team.

**Stage goals**
- Plan the test suites that will be created, considering possible scenarios and test cases
- Consider the main usage scenarios, alternative paths, and edge cases of the application

**Artifacts**
- List of planned test suites
- List of test cases for each planned suite
- Identification of edge cases

**Definition of Done for Stage 3**  
The team should consider the Human Test Planning stage complete when:
- all architecture planned in Stage 1 has properly planned test cases
- the test suites and planned test cases are documented so they can be used in the writing and review stages

### 4. Human Test Writing and Validation

This is the stage that comes before an AI agent intervenes.  
Writing tests is the formal and technical contract for everything that was discussed and planned in Stages 1 and 2.

**Who is involved?**  
Only the human development team.

**Stage goals**
- Write the tests planned in the previous stage, using the libraries and architecture defined by the team
- Validate the written tests through code review, based on what was planned

**Artifacts**
- Pull Request(s) reviewed and approved according to team policies
- Test suites and test cases properly developed and available in the repository

**Definition of Done for Stage 4**  
The team should consider the Human Test Writing and Validation stage complete when:
- the tests previously planned in Stage 3 have been developed and organized in the repository according to the team’s standard architecture
- the tests have been validated through the team’s code review process

### 5. AI Code Implementation

At this point, the AI agent finally becomes the main actor.  
GAID was created as a methodology to formalize and manage the use of AI by developers, but it does not include recommendations or rules about which AI agents to use or how to use them.

**Who is involved?**  
The AI agent, monitored by human developers.

**Stage goals**
- Carry out the main implementation work (coding) for the requested change
- Use an AI agent for coding, with the previously planned and written tests acting as the rules
- Refactor and reorganize the code generated by the AI agent when necessary
- Test the final implementation and send it for team review

**Artifacts**
- Pull Request(s) created and properly described/documented, highlighting what was requested from the AI agent and what human interventions were made, if any

**Definition of Done for Stage 5**  
The team should consider the AI Code Implementation stage complete when:
- all previously planned and written tests pass successfully after the AI implementation
- the human developer(s) reviewed and, when necessary, refined the code generated by the AI to meet the team’s standards for best practices and architecture
- the final implementation works in a test environment and meets the acceptance criteria defined by the business team
- a Pull Request has been created and documented in a way that allows code review by the team

### 6. Human Code Validation

**Who is involved?**  
The human development team.

**Stage goals**
- Review all code generated by the AI agent
- Ensure compliance with the project’s architectural standards
- Request and apply final adjustments to the implementation whenever necessary

**Artifacts**
- Pull Request(s) approved and made available in the application’s main repository

**Definition of Done for Stage 6**  
The team should consider the Human Code Validation stage complete when:
- all code created by the AI agent under the monitoring of developers has been reviewed by the team’s technical owners
- the code entering the main repository follows the project’s existing standards for architecture, best practices, and performance
- the final implementation works and meets the acceptance criteria defined by the business team

### 7. Feedback Loop

The Feedback Loop stage exists to handle possible changes and/or bugs after the initial development process.  
In short, this stage ensures that the new need is properly understood and that the team is routed back to **Stage 2** to handle the case.

**Who is involved?**  
The human development team.

**Stage goals**
- Properly direct any changes and/or bugs that arise after the initial development
- Ensure the circular nature of the GAID process, where every repository iteration is properly governed

**Definition of Done for Stage 7**  
The team should consider the Feedback Loop stage complete when:
- after a change request or bug report is registered, the technical team understands what needs to be changed
- once the change is understood, the team starts handling it again from **Stage 2** of GAID
