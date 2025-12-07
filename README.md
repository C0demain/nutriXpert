<img width="1500" height="250" alt="nutrixpert-banner (1)" src="https://github.com/user-attachments/assets/00bba542-eaaa-418a-88d0-a956762a2a60" />
<h1 align="center">
Projeto API - 6º Semestre
</h1>

## 🎯 Descrição do Desafio

O desafio é desenvolver um agente conversacional inteligente, baseado no modelo Gemini, para oferecer suporte personalizado em nutrição. Ele deverá interagir de forma natural com o usuário, coletando informações sobre saúde, hábitos alimentares, restrições e objetivos nutricionais. Nesse processo, busca também superar as principais dores do cliente, como a dificuldade em manter consistência alimentar, a falta de orientação prática e personalizada, a sobrecarga de informações contraditórias sobre nutrição e a insegurança em relação às escolhas feitas no dia a dia.

## 📋 Backlog do Produto

<details><summary>Visualize Aqui</summary>

| Rank | Prioridade | User Story                                                                                                                                          | Estimativa (h) | Story Points | Sprint | Critério de Aceitação                                                                                                                           |
| ---- | ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | -------------- | ------------ | ------ | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| 1    | Alta       | Como paciente, quero preencher dados básicos de saúde (altura, peso, hábitos e doenças), para que o agente me ofereça recomendações personalizadas. | 10             | 90           | 1      | O paciente consegue cadastrar altura, peso, hábitos e doenças, e o agente utiliza essas informações para fornecer recomendações personalizadas. |
| 2    | Alta       | Como paciente, desejo sanar minhas dúvidas sobre nutrição, para me alimentar melhor e desenvolver uma dieta adequada ao meu perfil.                 | 10             | 80           | 1      | O paciente pode enviar dúvidas nutricionais e o agente responde com orientações e explicações adequadas.                                        |
| 3    | Média      | Como novo paciente, quero criar uma conta na plataforma, para interagir com o agente e acessar minhas informações.                                  | 8              | 50           | 1      | O paciente consegue criar uma conta com e-mail e senha e visualizar seu perfil após o cadastro.                                                 |
| 4    | Média      | Como paciente, quero efetuar o login na plataforma de forma segura, para acessar meu perfil.                                                        | 8              | 40           | 1      | O login exige credenciais válidas e realiza autenticação segura com mensagens de erro apropriadas.                                              |
| 5    | Alta       | Como paciente, quero que meu histórico de conversas seja salvo, para que eu possa retomar o atendimento a qualquer momento.                         | 9              | 70           | 1      | O sistema armazena automaticamente todas as conversas e permite retomar o histórico completo.                                                   |
| 6    | Média      | Como paciente, quero corrigir meus dados, para que o agente não use informações desatualizadas.                                                     | 7              | 40           | 1      | O paciente consegue editar seus dados de perfil e o sistema atualiza as informações no banco.                                                   |
| 7    | Baixa      | Como paciente, quero conversar com o agente em uma interface semelhante ao WhatsApp, para ter uma experiência familiar e simples.                   | 6              | 30           | 1      | A interface do chat apresenta layout similar ao WhatsApp, com bolhas de mensagem, horário e identificação.                                      |
| 8    | Baixa      | Como paciente, quero um menu de navegação fácil e intuitivo, para melhorar a experiência como usuário.                                              | 5              | 20           | 1      | O menu apresenta ícones e rotas claras, permitindo acessar as principais funcionalidades com poucos cliques.                                    |
| 9    | Alta       | Como paciente, desejo inserir meus objetivos nutricionais, para receber dietas personalizadas.                                                      | 9              | 80           | 2      | O paciente define metas nutricionais e o agente ajusta recomendações de acordo com os objetivos.                                                |
| 10   | Alta       | Como paciente, quero registrar minhas refeições para que o sistema calcule minha ingestão diária.                                                   | 9              | 80           | 2      | O paciente registra refeições e o sistema apresenta o total de calorias e macronutrientes consumidos.                                           |
| 11   | Alta       | Como nutricionista, quero um acesso diferente do usuário padrão, para acompanhar os pacientes.                                                      | 8              | 60           | 2      | O nutricionista acessa painel exclusivo com lista de pacientes, dados e relatórios de progresso.                                                |
| 12   | Alta       | Como usuário, quero ter uma página de login e cadastro mais intuitiva e visualmente agradável.                                                      | 7              | 50           | 2      | As telas de login e cadastro seguem design responsivo e visual limpo com feedbacks claros de erro.                                              |
| 13   | Alta       | Como paciente, quero preencher minha anamnese em um formulário claro e estruturado, conforme orientações da nutricionista.                          | 9              | 70           | 2      | O formulário exibe campos padronizados (doenças, hábitos, metas) e salva corretamente os dados no sistema.                                      |
| 14   | Média      | Como usuário, quero visualizar as conversas com identificação clara de quem enviou as mensagens e horários bem formatados.                          | 7              | 50           | 2      | Cada mensagem exibe remetente, horário e formatação clara no histórico de conversas.                                                            |
| 15   | Média      | Como usuário, quero que toda a interface siga um padrão visual consistente.                                                                         | 6              | 40           | 2      | Todos os elementos seguem a identidade visual definida (cores, fontes, espaçamentos e botões).                                                  |
| 16   | Alta       | Como desenvolvedor backend, quero adicionar novos campos da anamnese ao banco de dados.                                                             | 8              | 60           | 2      | O banco de dados inclui novos campos clínicos e o backend processa corretamente as novas informações.                                           |
| 17   | Média      | Como paciente, quero avaliar a qualidade das respostas, para que o sistema melhore continuamente.                                                   | 6              | 40           | 2      | O paciente pode avaliar mensagens com estrelas e o feedback é armazenado para análise posterior.                                                |
| 18   | Baixa      | Como paciente, quero que o agente sugira combinações de refeições balanceadas, para ter opções práticas.                                            | 5              | 40           | 2      | O agente oferece sugestões de combinações de refeições completas (ex.: almoço + jantar).                                                        |
| 19   | Alta       | Como paciente, quero preencher a anamnese diretamente no chat, para envio de informações no primeiro contato.                                       | 10             | 90           | 3      | O agente solicita e registra informações básicas de anamnese diretamente durante o chat inicial.                                                |
| 20   | Alta       | Como paciente, quero que o agente reformule minha dieta conforme minha ingestão semanal.                                                            | 9              | 80           | 3      | O agente analisa registros de refeições e gera nova dieta ajustada ao comportamento alimentar.                                                  |
| 21   | Alta       | Como paciente, quero que o agente gere uma dieta completa com os alimentos do meu dia ou semana.                                                    | 9              | 80           | 3      | O agente apresenta plano alimentar diário ou semanal com porções e horários sugeridos.                                                          |
| 22   | Alta       | Como paciente, quero poder comparar diferentes planos gerados, para escolher o mais adequado.                                                       | 8              | 70           | 3      | O paciente visualiza planos lado a lado com resumo de calorias e macronutrientes para comparação.                                               |
| 23   | Média      | Como paciente, quero que o agente estime a distribuição de macronutrientes com base nos meus registros.                                             | 7              | 70           | 3      | O sistema calcula e exibe proporção de carboidratos, proteínas e gorduras com gráficos ilustrativos.                                            |
| 24   | Média      | Como paciente, quero um resumo semanal de progresso, para ver minha evolução.                                                                       | 6              | 60           | 3      | O paciente recebe relatório semanal com resumo de peso, calorias e metas atingidas.                                                             |
| 25   | Média      | Como paciente, quero receber insights automáticos sobre meus avanços (ex.: redução de açúcar).                                                      | 5              | 40           | 3      | O sistema envia mensagens automáticas destacando melhorias no comportamento alimentar.                                                          |
| 26   | Baixa      | Como paciente, quero anexar foto da refeição e que o agente calcule automaticamente os macronutrientes.                                             | 9              | 90           | 3      | O sistema permite upload de imagem e exibe estimativa de macronutrientes com base na foto.                                                      |
| 27   | Baixa      | Como paciente, quero exportar meu progresso em PDF com gráficos e análises para compartilhar com o nutricionista.                                   | 5              | 30           | 3      | O paciente pode gerar arquivo PDF contendo gráficos e informações consolidadas do progresso.                                                    |

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
  <a href="https://drive.google.com/file/d/1yrMEe427b8veCaSCSqBffnHH3a21yh0p/view">Vídeo da Aplicação</a><br> <br>


| Rank   | Prioridade | User Story                                                                                                                                                                                           | Estimativa | Sprint | Meta da Sprint |
| ------ | ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ------ | -------------- |
| **9**  | Alta       | Como paciente, desejo inserir meus objetivos nutricionais, para receber dietas personalizadas ou dicas de alimentação.                                                                               | 80         | 2      | ✅             |
| **10** | Alta       | Como paciente, quero registrar minhas refeições para que o sistema calcule minha ingestão diária.                                                                                                    | 80         | 2      | ✅             |
| **11** | Alta       | Como nutricionista, quero um acesso diferente do usuário padrão, para acompanhamento dos pacientes.                                                                                                  | 60         | 2      | ✅             |
| **12** | Alta       | Como usuário, quero ter uma página de login e cadastro mais intuitiva e visualmente agradável para facilitar meu acesso e registro na plataforma.                                                    | 50         | 2      | ✅             |
| **13** | Alta       | Como paciente, quero preencher minha anamnese em um formulário claro e estruturado conforme orientações da nutricionista para garantir que minhas informações de saúde sejam coletadas corretamente. | 70         | 2      | ✅             |
| **14** | Média      | Como usuário, quero visualizar as conversas com identificação clara de quem enviou as mensagens e horários bem formatados para compreender facilmente o histórico dos atendimentos.                  | 50         | 2      | ❌             |
| **15** | Média      | Como usuário, quero que toda a interface siga um padrão visual consistente para ter uma experiência mais agradável e profissional ao navegar pela plataforma.                                        | 40         | 2      | ❌             |
| **16** | Alta       | Como desenvolvedor backend, quero adicionar novos campos da anamnese ao banco de dados para armazenar todas as informações clínicas relevantes enviadas pelo paciente.                               | 60         | 2      | ❌             |
| **17** | Média      | Como paciente, quero avaliar a qualidade das respostas (com estrelas ou feedback) para que o sistema melhore continuamente.                                                                          | 40         | 2      | ❌             |
| **18** | Baixa      | Como paciente, quero que o agente sugira combinações de refeições (almoço + jantar balanceados), para ter opções práticas no dia a dia.                                                              | 40         | 2      | ❌             |

</details>

<details><summary>Sprint 3 (03.11 | 20.11)</summary>

<div align="center">
<a href="https://www.youtube.com/watch?v=6N9nwSJFzzg">Vídeo da Aplicação</a><br> <br>
  
|Rank|Prioridade|User Story|Estimativa|Sprint|Meta da Sprint|
| -------- |-------- |-------- |-------- |-------- |-------- | 
|**19**|Alta|Como paciente, quero preencher a anamnese diretamente no chat, para envio de informações no primeiro contato e para atualizações.|90|3|✅| 
|**20**|Alta|Como paciente, quero que o agente reformule a minha dieta, de acordo com a ingestão de alimentos ao longo da minha semana.|80|3|✅| 
|**21**|Alta|Como paciente, quero que o agente gere uma dieta completa com os alimentos que devo comer no meu dia ou ao longo da semana.|80|3|✅| 
|**22**|Alta|Como paciente, quero poder comparar diferentes planos gerados, para escolher aquele que mais se adapta à minha rotina.|70|3|✅| 
|**23**|Média|Como paciente, quero que o agente estime a distribuição de macronutrientes (carboidratos, proteínas, gorduras) a partir dos meus registros, para avaliar se minha dieta está equilibrada.|70|3|✅| 
|**24**|Média|Como paciente, quero um resumo semanal de progresso, para que eu veja minha evolução em ciclos curtos.|60|3|✅| 
|**25**|Média|Como paciente, quero receber insights automáticos (ex.: “você reduziu o consumo de açúcar nesta semana”), para ter clareza sobre meus avanços.|40|3|✅|
|**26**|Baixa|Como paciente, quero anexar uma foto da minha refeição e quero que o agente calcule automaticamente a quantidade de macronutrientes presentes no prato.|90|3|❌| 
|**27**|Baixa|Como paciente, quero exportar meu progresso em PDF com gráficos e análises, para compartilhar com meu nutricionista.|30|3|❌|

</div>
  </details>

## 🗓️ Planejamento de Entregas

![nutriXpert-planejamento](https://github.com/user-attachments/assets/1f6f67c0-ff87-4736-8340-a21576b54fee)

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

| Sprint      | Período       | Documentação                                       |
| ----------- | ------------- | -------------------------------------------------- |
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

| Repositório           | Descrição                                                                                                           |
| --------------------- | ------------------------------------------------------------------------------------------------------------------- |
| `nutriXpert-agent`    | Agente conversacional em Python, utilizando modelo Gemini. Responsável pela inteligência do sistema.          |
| `nutriXpert-backend`  | API REST construída em Java com Spring Boot, garantindo segurança, persistência de dados e integração com o agente. |
| `nutriXpert-frontend` | Interface web desenvolvida em Vue.js (SPA), voltada para interação do usuário e visualização dos resultados.        |

## 🎯 Estratégia de Branch

**Branches principais:**

- `main`→ versão estável e pronta para produção.
- `dev` → branch de integração, recebe funcionalidades testadas.
- `feat/<nome-da-funcionalidade>` → para cada User Story ou tarefa específica.

## 💻 Workflow Sistema

<img width="2607" height="866" alt="wokflow-sistema" src="https://github.com/user-attachments/assets/d07a87f3-5b6a-419c-b299-eac0a5151507" />

## 📘 Manual do Usuário

Para garantir a melhor experiência de interação com os agentes e entender o fluxo do sistema, disponibilizamos um guia prático.

| Documento             | Descrição                                                                                | Link                                                         |
| --------------------- | ---------------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| **Manual NutriXpert** | Explicação detalhada sobre os agentes, comandos, anamnese e interpretação das respostas. | [📖 Acessar Manual](./documentacao/manual_usuario/README.md) |

## 💻 Manual de Instalação
Guia completo para instalar, configurar e executar todo o ambiente do nutriXpert de forma rápida e padronizada.

| Documento                | Descrição                                                                                  | Link                                                                |
| ------------------------ | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| **Manual de Instalação** | Passo a passo completo para instalar, configurar e executar os módulos do nutriXpert.      | [📦 Acessar Manual](./documentacao/manual_instalacao/README.md)     |


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
