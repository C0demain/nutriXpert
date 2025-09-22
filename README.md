<img width="1500" height="250" alt="nutrixpert-banner (1)" src="https://github.com/user-attachments/assets/00bba542-eaaa-418a-88d0-a956762a2a60" />

## 🎯 Explicação do Projeto
O desafio consiste no desenvolvimento de um agente conversacional inteligente, baseado no modelo LLM medGemma, com foco em fornecer suporte personalizado na área de nutrição. O sistema deverá interagir com o usuário de forma natural, coletando informações relevantes sobre saúde, hábitos alimentares, restriçoes e objetivos nutricionais.

## 🧩 Estrutura do Projeto

O projeto foi dividido em **três repositórios independentes**, refletindo a arquitetura desacoplada da solução:

| Repositório       | Descrição                                                                 |
|-------------------|---------------------------------------------------------------------------|
| `nutriXpert-agent`    | Agente conversacional em Python, utilizando modelo LLM medGemma. Responsável pela inteligência do sistema.|
| `nutriXpert-backend`  | API REST construída em Java com Spring Boot, garantindo segurança, persistência de dados e integração com o agente.|
| `nutriXpert-frontend` | Interface web desenvolvida em Vue.js (SPA), voltada para interação do usuário e visualização dos resultados.|

## 📋 Backlog do Produto
<details><summary>Ver Mais</summary>

<div align="center">
  
|Rank|Prioridade|User Story|Estimativa|Sprint
| -------- |-------- |-------- |-------- |-------- |
|**1**|Alta|Como paciente, quero preencher dados básicos de saúde (altura, peso, hábitos e doenças), para que o agente me ofereça recomendações personalizadas.|90|1|
|**2**|Alta|Como paciente, desejo sanar minhas dúvidas sobre nutrição, para me alimentar melhor e para que me auxilie a desenvolver uma dieta que se adeque ao meu perfil.|80|1|
|**3**|Média|Como novo paciente, quero criar uma conta na plataforma, para interagir com o agente e ter acesso as minhas informações.|50|1|
|**4**|Média|Como paciente, quero efetuar o login na plataforma de forma segura, para acessar meu perfil.|40|1|
|**5**|Alta|Como paciente, quero que meu histórico de conversas seja salvo, para que eu possa retomar o atendimento em qualquer momento.|70|1|
|**6**|Média|Como paciente, quero corrigir meus dados, para que o agente não use informações desatualizadas.|40|1|
|**7**|Baixa|Como paciente, quero conversar com o agente em uma interface semelhante ao WhatsApp, para que eu tenha uma experiência familiar e simples.|30|1|
|**8**|Baixa|Como paciente, quero um menu de navegação fácil e intuitivo, para melhorar a minha experiência como usuário.|20|1|
|**9**|Alta|Como paciente, desejo inserir meus objetivos nutricionais, para receber dietas personalizadas ou dicas de alimentação.|80|2|
|**10**|Alta|Como paciente, quero registrar minhas refeições para que o sistema calcule minha ingestão diária.|80|2|
|**11**|Alta|Como nutricionista, quero um acesso diferente do usuário padrão, para acompanhamento dos pacientes.|60|2|
|**12**|Alta|Como nutricionista, quero revisar respostas do agente para que a confiabilidade seja garantida.|50|2|
|**13**|Média|Como paciente, quero avaliar a qualidade das respostas (com estrelas ou feedback) para que o sistema melhore continuamente.|40|2|
|**14**|Baixa|Como paciente, quero que o agente sugira combinações de refeições (almoço + jantar balanceados), para ter opções práticas no dia a dia.|40|2|
|**15**|Baixa|Como nutricionista, quero poder adicionar anotações personalizadas ao perfil de cada paciente, para registrar observações clínicas e recomendações complementares.|30|2|
|**16**|Alta|Como paciente, quero que o agente estime a distribuição de macronutrientes (carboidratos, proteínas, gorduras) a partir dos meus registros, para avaliar se minha dieta está equilibrada.|90|3|
|**17**|Alta|Como paciente, quero poder comparar diferentes planos gerados, para escolher aquele que mais se adapta à minha rotina.|50|3|
|**18**|Alta|Como paciente, quero um resumo semanal de progresso, para que eu veja minha evolução em ciclos curtos.|50|3|
|**19**|Média|Como paciente, quero exportar meu progresso em PDF com gráficos e análises, para compartilhar com meu nutricionista.|30|3|
|**20**|Baixa|Como paciente, quero receber uma introdução interativa (tour da plataforma), para entender como usar as funcionalidades principais desde o primeiro acesso.|60|3|
|**21**|Baixa|Como paciente, quero receber insights automáticos (ex.: “você reduziu o consumo de açúcar nesta semana”), para ter clareza sobre meus avanços.|20|3|
|**22**|Baixa|Como paciente, quero anexar meu exame de sangue, para que o agente me dê dicas de como melhorar os resultados com mudanças na alimentação e hábitos de saúde.|80|3|

</details>  
  
</div>

## 📑 Backlog da Sprint
<details><summary>Sprint 1</summary>

<div align="center">
  
|Rank|Prioridade|User Story|Estimativa|Sprint|Status
| -------- |-------- |-------- |-------- |-------- |-------- | 
|**1**|Alta|Como paciente, quero preencher dados básicos de saúde (altura, peso, hábitos e doenças), para que o agente me ofereça recomendações personalizadas.|90|1|✅|
|**2**|Alta|Como paciente, desejo sanar minhas dúvidas sobre nutrição, para me alimentar melhor e para que me auxilie a desenvolver uma dieta que se adeque ao meu perfil.|80|1|✅|
|**3**|Média|Como novo paciente, quero criar uma conta na plataforma, para interagir com o agente e ter acesso as minhas informações.|50|1|
|**4**|Média|Como paciente, quero efetuar o login na plataforma de forma segura, para acessar meu perfil.|40|1|✅|
|**5**|Alta|Como paciente, quero que meu histórico de conversas seja salvo, para que eu possa retomar o atendimento em qualquer momento.|70|1|
|**6**|Média|Como paciente, quero corrigir meus dados, para que o agente não use informações desatualizadas.|40|1|
|**7**|Baixa|Como paciente, quero conversar com o agente em uma interface semelhante ao WhatsApp, para que eu tenha uma experiência familiar e simples.|30|1|
|**8**|Baixa|Como paciente, quero um menu de navegação fácil e intuitivo, para melhorar a minha experiência como usuário.|20|1|

</details>  
<details><summary>Sprint 2</summary>

<div align="center">
  
|Rank|Prioridade|User Story|Estimativa|Sprint|Status
| -------- |-------- |-------- |-------- |-------- |-------- | 
|**9**|Alta|Como paciente, desejo inserir meus objetivos nutricionais, para receber dietas personalizadas ou dicas de alimentação.|80|2|
|**10**|Alta|Como paciente, quero registrar minhas refeições para que o sistema calcule minha ingestão diária.|80|2|
|**11**|Alta|Como nutricionista, quero um acesso diferente do usuário padrão, para acompanhamento dos pacientes.|60|2|
|**12**|Alta|Como nutricionista, quero revisar respostas do agente para que a confiabilidade seja garantida.|50|2|
|**13**|Média|Como paciente, quero avaliar a qualidade das respostas (com estrelas ou feedback) para que o sistema melhore continuamente.|40|2|
|**14**|Baixa|Como paciente, quero que o agente sugira combinações de refeições (almoço + jantar balanceados), para ter opções práticas no dia a dia.|40|2|
|**15**|Baixa|Como nutricionista, quero poder adicionar anotações personalizadas ao perfil de cada paciente, para registrar observações clínicas e recomendações complementares.|30|2|
</details>  

<details><summary>Sprint 3</summary>

<div align="center">
  
|Rank|Prioridade|User Story|Estimativa|Sprint|Status
| -------- |-------- |-------- |-------- |-------- |-------- | 
|**16**|Alta|Como paciente, quero que o agente estime a distribuição de macronutrientes (carboidratos, proteínas, gorduras) a partir dos meus registros, para avaliar se minha dieta está equilibrada.|90|3|
|**17**|Alta|Como paciente, quero poder comparar diferentes planos gerados, para escolher aquele que mais se adapta à minha rotina.|50|3|
|**18**|Alta|Como paciente, quero um resumo semanal de progresso, para que eu veja minha evolução em ciclos curtos.|50|3|
|**19**|Média|Como paciente, quero exportar meu progresso em PDF com gráficos e análises, para compartilhar com meu nutricionista.|30|3|
|**20**|Baixa|Como paciente, quero receber uma introdução interativa (tour da plataforma), para entender como usar as funcionalidades principais desde o primeiro acesso.|60|3|
|**21**|Baixa|Como paciente, quero receber insights automáticos (ex.: “você reduziu o consumo de açúcar nesta semana”), para ter clareza sobre meus avanços.|20|3|
|**22**|Baixa|Como paciente, quero anexar meu exame de sangue, para que o agente me dê dicas de como melhorar os resultados com mudanças na alimentação e hábitos de saúde.|80|3|

</details>  
  
</div>

## 🧰 Tecnologias Utilizadas
### 🚹 Agent
- Python
- Chroma DB

### 🧱 Backend
- Java
- Spring Boot
- Postgres

### 💻 Frontend
- Vue.JS

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
