<img width="1500" height="250" alt="nutrixpert-banner (1)" src="https://github.com/user-attachments/assets/00bba542-eaaa-418a-88d0-a956762a2a60" />
<h1 align="center">
Projeto API - 6º Semestre
</h1>

## 🎯 Descrição do Desafio
O desafio é desenvolver um agente conversacional inteligente, baseado no modelo LLM medGemma, para oferecer suporte personalizado em nutrição. Ele deverá interagir de forma natural com o usuário, coletando informações sobre saúde, hábitos alimentares, restrições e objetivos nutricionais. Nesse processo, busca também superar as principais dores do cliente, como a dificuldade em manter consistência alimentar, a falta de orientação prática e personalizada, a sobrecarga de informações contraditórias sobre nutrição e a insegurança em relação às escolhas feitas no dia a dia.


## 📋 Backlog do Produto
<details><summary>Visualize Aqui</summary>

| Rank | Prioridade | User Story | Estimativa (h) | Story Points | Sprint | Critério de Aceitação |
|------|------------|------------|----------------|--------------|--------|------------------------|
| 1  | ALTA   | Como paciente, quero preencher dados básicos de saúde (altura, peso, hábitos e doenças), para que o agente me ofereça recomendações personalizadas. | 10 | 90 | 1 | O paciente consegue cadastrar altura, peso, hábitos e doenças, e o agente utiliza essas informações para fornecer recomendações personalizadas. |
| 2  | ALTA   | Como paciente, quero criar uma conta na plataforma, para interagir com o agente e ter acesso às minhas informações. | 12 | 80 | 1 | O agente responde corretamente às perguntas do paciente sobre nutrição, usando dados cadastrados e base de conhecimento. |
| 3  | MÉDIA  | Como paciente, quero criar uma conta na plataforma, para interagir com o agente e ter acesso às minhas informações. | 5  | 50 | 1 | O paciente consegue criar uma conta, com validação de e-mail, e acessar seu perfil. |
| 4  | MÉDIA  | Como paciente, quero efetuar o login na plataforma de forma segura, para acessar meu perfil. | 4  | 40 | 1 | O paciente consegue logar com usuário e senha, e suas credenciais são protegidas. |
| 5  | ALTA   | Como paciente, quero que meu histórico de conversas seja salvo, para que eu possa retomar o atendimento em qualquer momento. | 6  | 70 | 1 | As conversas são armazenadas no sistema e podem ser acessadas pelo paciente a qualquer momento. |
| 6  | MÉDIA  | Como paciente, quero corrigir meus dados, para que o agente não acesse informações desatualizadas. | 3  | 40 | 1 | O paciente consegue editar dados pessoais e de saúde, e o agente usa sempre os dados atualizados. |
| 7  | BAIXA  | Como paciente, quero conversar com o agente em uma interface semelhante ao WhatsApp, para que eu tenha uma experiência familiar e simples. | 8  | 30 | 1 | O paciente consegue enviar e receber mensagens do agente em um chat com interface intuitiva tipo WhatsApp. |
| 8  | BAIXA  | Como paciente, quero um menu de navegação fácil e intuitivo, para melhorar a minha experiência como usuário. | 4  | 20 | 1 | O paciente consegue acessar todas as funcionalidades principais através de menus claros e intuitivos. |
| 9  | ALTA   | Como paciente, desejo inserir meus objetivos nutricionais, para receber dietas personalizadas ou dicas de alimentação. | 6  | 80 | 2 | O paciente consegue cadastrar objetivos nutricionais, e o agente utiliza esses dados para recomendações. |
| 10 | ALTA   | Como paciente, quero registrar minhas refeições para que o sistema calcule minha ingestão diária. | 8  | 80 | 2 | O paciente cadastra refeições, e o sistema calcula automaticamente calorias e macronutrientes consumidos. |
| 11 | ALTA   | Como nutricionista, quero um acesso diferente do usuário padrão, para conseguir monitorar os pacientes. | 5  | 60 | 2 | O nutricionista consegue acessar painel com pacientes, visualizar informações e histórico de interações. |
| 12 | ALTA   | Como nutricionista, quero revisar respostas do agente para que a confiabilidade seja garantida. | 4  | 50 | 2 | O nutricionista consegue avaliar respostas do agente e aprová-las ou corrigi-las antes do envio ao paciente. |
| 13 | MÉDIA  | Como paciente, quero avaliar a qualidade das respostas (com estrelas ou feedback) para que o sistema melhore continuamente. | 3  | 40 | 2 | O paciente consegue avaliar respostas do agente com estrelas ou comentários, e essas avaliações são armazenadas. |
| 14 | BAIXA  | Como paciente, quero que o agente sugira combinações de refeições (almoço + jantar balanceados), para ter opções práticas no dia a dia. | 5  | 40 | 2 | O agente sugere combinações de refeições balanceadas com base nos registros e objetivos do paciente. |
| 15 | BAIXA  | Como nutricionista, quero poder adicionar anotações personalizadas ao perfil de cada paciente, para registrar observações clínicas e recomendações complementares. | 3  | 30 | 2 | O nutricionista consegue adicionar anotações ao perfil do paciente, visíveis apenas para ele e para o paciente conforme permissões. |
| 16 | ALTA   | Como paciente, quero que o agente estime a distribuição de macronutrientes (carboidratos, proteínas, gorduras) a partir dos meus registros, para avaliar se minha dieta está equilibrada. | 8  | 90 | 3 | O sistema calcula automaticamente a distribuição de macronutrientes com base nas refeições cadastradas pelo paciente. |
| 17 | ALTA   | Como paciente, quero poder comparar diferentes planos gerados, para escolher aquele que mais se adapta à minha rotina. | 4  | 50 | 3 | O paciente consegue visualizar e comparar planos alimentares gerados pelo sistema. |
| 18 | ALTA   | Como paciente, quero um resumo semanal de progresso, para que eu veja minha evolução em ciclos curtos. | 5  | 50 | 3 | O paciente recebe um resumo semanal com gráficos de progresso e evolução dos indicadores nutricionais. |
| 19 | MÉDIA  | Como paciente, quero exportar meu progresso em PDF com gráficos e análises, para compartilhar com meu nutricionista. | 3  | 30 | 3 | O paciente consegue exportar relatórios em PDF com gráficos e análises do progresso. |
| 20 | BAIXA  | Como paciente, quero receber uma introdução interativa (tour da plataforma), para entender como usar as funcionalidades principais desde o primeiro acesso. | 4  | 60 | 3 | O paciente é guiado em um tour interativo, conseguindo identificar todas as funcionalidades principais. |
| 21 | BAIXA  | Como paciente, quero receber insights automáticos (ex.: “você reduziu o consumo de açúcar nesta semana”), para ter clareza sobre meus avanços. | 3  | 20 | 3 | O sistema gera insights automáticos baseados nos registros do paciente e os exibe de forma clara. |
| 22 | BAIXA  | Como paciente, quero anexar meu exame de sangue, para que o agente me dê dicas de como melhorar os resultados com mudanças na alimentação e hábitos de saúde. | 6  | 80 | 3 | O paciente consegue anexar exames, e o agente utiliza os dados para fornecer recomendações personalizadas. |
</details>
  
## 🏃 Sprint Backlog
  
</div>

<details><summary>Sprint 1 (08.09 | 28.09)</summary>

<div align="center">
  <a href="https://onedrive.live.com/?qt=allmyphotos&photosData=%2Fshare%2F7EB0B94C6DED4A70%21s80109a5e4ed24a688434052c138e964a%3Fithint%3Dvideo%26migratedtospo%3Dtrue&cid=7EB0B94C6DED4A70&id=7EB0B94C6DED4A70%21s80109a5e4ed24a688434052c138e964a&redeem=aHR0cHM6Ly8xZHJ2Lm1zL3YvYy83ZWIwYjk0YzZkZWQ0YTcwL0VWNmFFSURTVG1oS2hEUUZMQk9PbGtvQl9sM1c0UmstX2hkT2t0clc3Mkxzbmc&v=photos">Vídeo da Aplicação</a><br> <br>
</div>
  
|Rank|Prioridade|User Story|Estimativa|Sprint|Meta da Sprint|
| -------- |-------- |-------- |-------- |-------- |-------- | 
|**1**|Alta|Como paciente, quero preencher dados básicos de saúde (altura, peso, hábitos e doenças), para que o agente me ofereça recomendações personalizadas.|90|1|✅|
|**2**|Alta|Como paciente, desejo sanar minhas dúvidas sobre nutrição, para me alimentar melhor e para que me auxilie a desenvolver uma dieta que se adeque ao meu perfil.|80|1|✅|
|**3**|Média|Como novo paciente, quero criar uma conta na plataforma, para interagir com o agente e ter acesso as minhas informações.|50|1|✅|
|**4**|Média|Como paciente, quero efetuar o login na plataforma de forma segura, para acessar meu perfil.|40|1|✅|
|**5**|Alta|Como paciente, quero que meu histórico de conversas seja salvo, para que eu possa retomar o atendimento em qualquer momento.|70|1|❌|
|**6**|Média|Como paciente, quero corrigir meus dados, para que o agente não use informações desatualizadas.|40|1|❌|
|**7**|Baixa|Como paciente, quero conversar com o agente em uma interface semelhante ao WhatsApp, para que eu tenha uma experiência familiar e simples.|30|1|❌|
|**8**|Baixa|Como paciente, quero um menu de navegação fácil e intuitivo, para melhorar a minha experiência como usuário.|20|1|❌|

</details>

<details><summary>Sprint 2 (06.10 | 26.10)</summary>

<div align="center">
<br> YouTube <br><br>
  
|Rank|Prioridade|User Story|Estimativa|Sprint|Meta da Sprint|
| -------- |-------- |-------- |-------- |-------- |-------- | 
|**9**|Alta|Como paciente, desejo inserir meus objetivos nutricionais, para receber dietas personalizadas ou dicas de alimentação.|80|2|✅| 
|**10**|Alta|Como paciente, quero registrar minhas refeições para que o sistema calcule minha ingestão diária.|80|2|✅| 
|**11**|Alta|Como nutricionista, quero um acesso diferente do usuário padrão, para acompanhamento dos pacientes.|60|2|✅| 
|**12**|Alta|Como nutricionista, quero revisar respostas do agente para que a confiabilidade seja garantida.|50|2|✅| 
|**13**|Média|Como paciente, quero avaliar a qualidade das respostas (com estrelas ou feedback) para que o sistema melhore continuamente.|40|2|❌|
|**14**|Baixa|Como paciente, quero que o agente sugira combinações de refeições (almoço + jantar balanceados), para ter opções práticas no dia a dia.|40|2|❌|
|**15**|Baixa|Como nutricionista, quero poder adicionar anotações personalizadas ao perfil de cada paciente, para registrar observações clínicas e recomendações complementares.|30|2|❌|
</details>  

<details><summary>Sprint 3 (03.11 | 20.11)</summary>

<div align="center">
<br>YouTube <br><br>
  
|Rank|Prioridade|User Story|Estimativa|Sprint|Meta da Sprint|
| -------- |-------- |-------- |-------- |-------- |-------- | 
|**16**|Alta|Como paciente, quero que o agente estime a distribuição de macronutrientes (carboidratos, proteínas, gorduras) a partir dos meus registros, para avaliar se minha dieta está equilibrada.|90|3|✅| 
|**17**|Alta|Como paciente, quero poder comparar diferentes planos gerados, para escolher aquele que mais se adapta à minha rotina.|50|3|✅| 
|**18**|Alta|Como paciente, quero um resumo semanal de progresso, para que eu veja minha evolução em ciclos curtos.|50|3|✅| 
|**19**|Média|Como paciente, quero exportar meu progresso em PDF com gráficos e análises, para compartilhar com meu nutricionista.|30|3|✅| 
|**20**|Baixa|Como paciente, quero receber uma introdução interativa (tour da plataforma), para entender como usar as funcionalidades principais desde o primeiro acesso.|60|3|✅| 
|**21**|Baixa|Como paciente, quero receber insights automáticos (ex.: “você reduziu o consumo de açúcar nesta semana”), para ter clareza sobre meus avanços.|20|3|❌|
|**22**|Baixa|Como paciente, quero anexar meu exame de sangue, para que o agente me dê dicas de como melhorar os resultados com mudanças na alimentação e hábitos de saúde.|80|3|❌|

</details>  
  

## 🗓️ Planejamento de Entregas
<img width="1920" height="1080" alt="nutriXpert-planejamento" src="https://github.com/user-attachments/assets/467379a7-2b4c-44db-a17a-39e49e3c2de1" />


## 🚩 DoR - Definition of Ready
- Critérios de aceitação bem definidos e mensuráveis
- Estimativa de esforço realizada pela equipe
- Compreensão validada com todos os membros do time
- Modelagem do Banco de Dados
- Banco de Dados Vetorizado do Cliente
- Diagrama de Rotas
- Design no Figma

## 🧩 DoD - Definition of Done
- Segue padrões de codificação e boas práticas do time
- Testes unitários implementados e passando
- Testes funcionais/aceitação executados e aprovados
- Documentação de código atualizada (comentários, README, API docs)
- Manual ou guia de usuário atualizado
- Configurações de ambiente e variáveis documentadas
- Todos os bugs críticos identificados resolvidos

  
## 🗓️ Cronograma de Sprints

| Sprint      | Período       | Documentação       |
|------------|---------------|------------------|
| 🚀 SPRINT 1 | 08.09 - 28.09 | [Sprint 1 Docs](./documentacao/sprint-1/README.md) |
| 🚀 SPRINT 2 | 06.10 - 26.10 | [Sprint 2 Docs](./documentacao/sprint-2/README.md) |
| 🚀 SPRINT 3 | 03.11 - 23.11 | [Sprint 3 Docs](./documentacao/sprint-3/README.md) |


## 🧰 Tecnologias Utilizadas
### 🚹 Agent
- Python
- Chroma DB
- Google ADK
- Fast API

### 🧱 Backend
- Java
- Spring Boot
- Postgres

### 💻 Frontend
- Vue.JS

### 🧪 Testes e Outros
- Postman (testes de API)
- Notion (documentação)
- Jira (users stories, sprints e tarefas)
- Figma (design das telas)
- Canva (materiais visuais)

## 🧩 Estrutura do Projeto

O projeto foi dividido em **três repositórios independentes**, refletindo a arquitetura desacoplada da solução:

| Repositório       | Descrição                                                                 |
|-------------------|---------------------------------------------------------------------------|
| `nutriXpert-agent`    | Agente conversacional em Python, utilizando modelo LLM medGemma. Responsável pela inteligência do sistema.|
| `nutriXpert-backend`  | API REST construída em Java com Spring Boot, garantindo segurança, persistência de dados e integração com o agente.|
| `nutriXpert-frontend` | Interface web desenvolvida em Vue.js (SPA), voltada para interação do usuário e visualização dos resultados.|


## 🎯 Estratégia de Branch
**Branches principais:**

- `main`→ versão estável e pronta para produção.
- `dev` → branch de integração, recebe funcionalidades testadas.
- `feat/<nome-da-funcionalidade>` → para cada User Story ou tarefa específica.


## 👨‍💻 Integrantes da Equipe

<div align="center">
  
|Nome|Função|GitHub|Linkedin|
| -------- |-------- |-------- |-------- |
|**Erick Hideki**|Product Owner|[@GitHub](https://github.com/erickhoawata)|[@Linkedin](http://linkedin.com/in/érick-awata)
|**Pedro Kajiya**|Scrum Master|[@GitHub](https://github.com/kajiyap)|[@Linkedin](https://www.linkedin.com/in/pedro-santos-kajiya-65763b260/)
|**Bruno Silvério**|Desenvolvedor|[@GitHub](https://github.com/BrunoVieira30)|[@Linkedin](https://www.linkedin.com/in/bruno-vieira-b999a2224/)
|**Cauã Dezidera**|Desenvolvedor|[@GitHub](https://github.com/CauaDezidera)|[@Linkedin](https://www.linkedin.com/in/cauã-dezidera-375736275/) 
|**Mateus Madeira**|Desenvolvedor|[@GitHub](https://github.com/mafemad)|[@Linkedin](https://www.linkedin.com/in/mateus-ferreira-madeira)
|**Abner Machado**|Desenvolvedor|[@GitHub](https://github.com/abnerdouglas)|[@Linkedin](https://www.linkedin.com/in/abner-douglas-a70a9b199/)
|**Ryan Seiji Wakugawa**|Desenvolvedor|[@GitHub](https://github.com/ryan-wakugawa)|[@Linkedin](https://www.linkedin.com/in/ryan-wakugawa-526bbb27a)

<br>  
  
</div>
