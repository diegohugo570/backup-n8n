# 🤖 Portfólio de Automações com n8n + IA

Este repositório reúne **workflows avançados desenvolvidos no n8n**, com foco em **automação inteligente, agentes de IA, marketing digital e integração entre plataformas**.

Os fluxos aqui apresentados representam **casos reais de uso**, prontos para estudo, adaptação ou implementação em ambientes produtivos.

---

## 🚀 O que você vai encontrar aqui

### 🧠 Agentes de IA & Multi-Agent
- **Agentes de IA com n8n**
- **Arquiteturas Multi-Agent**
- Integração com LLMs (OpenAI / similares)
- Orquestração de decisões automáticas

---

### 📣 Marketing Digital Automatizado
- **Automação de LinkedIn com IA**
  - Criação, resposta e interação automatizada
- **Instagram com IA**
  - Responder comentários automaticamente
  - Templates inteligentes de interação
- **Geradores de conteúdo automatizados**

---

### 📲 Mensageria & Notificações
- **Registro de faturas no Telegram**
- Alertas automáticos
- Integração entre sistemas internos e canais de comunicação

---

### ⚙️ Infraestrutura & Templates
- Templates reutilizáveis de automação
- Estruturas base para novos projetos
- Backup e versionamento de workflows n8n no GitHub

---

## 🛠️ Tecnologias Utilizadas
- n8n  
- APIs REST  
- Webhooks  
- OpenAI / LLMs  
- Instagram API  
- LinkedIn Automation  
- Telegram Bot API  
- JSON / HTTP / OAuth  

---

## 🎯 Objetivo do Repositório
Este repositório tem como finalidade:
- Servir como **portfólio técnico**
- Demonstrar **capacidade de automação real**
- Acelerar novos projetos com **templates prontos**
- Compartilhar boas práticas em automações com IA

---

## 📂 Projetos em Destaque

### 🤖 Potto Flow – Agente de Atendimento Inteligente (WhatsApp)

![Potto Flow – Agente de Atendimento](assets/agente-de-atendimento.png)

**Descrição:**  
Workflow completo de **Agente de Atendimento com IA**, desenvolvido no **n8n**, projetado para **responder clientes automaticamente via WhatsApp**, simulando o comportamento de uma **secretária humana**, com contexto, memória e integração com sistemas externos.

Este agente é ideal para **clínicas, consultórios, empresas de serviços e atendimento comercial**, realizando triagem inicial, respostas inteligentes e direcionamento correto das solicitações.

**O que esse agente faz na prática:**
- Recebe mensagens via **Webhook (WhatsApp API)**
- Filtra mensagens inválidas:
  - Grupos
  - Newsletters
  - Mensagens editadas
  - Mensagens enviadas pelo próprio número
- Normaliza e simplifica dados do usuário:
  - Nome
  - WhatsApp
  - Conteúdo da mensagem
- Busca ou cria automaticamente o cliente no **Supabase**
- Identifica o tipo de mensagem recebida:
  - 💬 Texto
  - 🎙️ Áudio (com transcrição automática via IA)
  - 🖼️ Imagem (resposta contextual orientando o usuário)
- Utiliza **Agente de IA (LLM)** com:
  - Prompt estruturado
  - Memória por usuário (histórico da conversa)
  - Tool Calling (Google Docs como base de conhecimento)
- Responde de forma **educada, natural e contextual**
- Envia mensagens automaticamente via **WhatsApp (Z-API)**

📁 **Workflow incluso:**  
`Potto_Flow___Agente_de_atendimento.json`

---

### 🤖 Potto Flow – Agente com Follow Up Inteligente (WhatsApp)

![Potto Flow – Agente com Follow Up](assets/potto-flow-agente-follow-up.png)

**Descrição:**  
Workflow avançado de **Agente de IA com Follow Up automático**, desenvolvido no **n8n**, focado em **atendimento, qualificação e reengajamento de leads via WhatsApp**.

Este projeto simula um **assistente humano**, com **memória de conversa, entendimento de intenção do usuário e automações de acompanhamento temporal**, sendo ideal para clínicas, vendas, suporte ou pré-atendimento.

**O que esse agente faz na prática:**
- Recebe mensagens via **Webhook (WhatsApp API)**
- Filtra mensagens inválidas (grupos, newsletters, edições)
- Cria ou recupera usuários automaticamente no **Supabase**
- Processa **texto, áudio e imagem**
  - Áudio → transcrição automática via IA
- Utiliza **Agente de IA (LLM)** com:
  - Prompt estruturado
  - Memória por usuário
  - Tool Calling com banco de dados
- Identifica **intenção/desejo do usuário**
- Responde via **WhatsApp** de forma contextual
- Atualiza histórico e estágio do lead
- Executa **Follow Ups automáticos**:
  - ⏱️ 10 minutos
  - ⏱️ 24 horas
  - ⏱️ 3 dias

📁 **Workflow incluso:**  
`Potto_Flow___Agente_com_Follow_Up.json`

---

### 📄 Potto Flow – Geração Automática de Contratos com IA (WhatsApp)

![Potto Flow – Gerar Contrato](assets/fluxo-gerar-contrato.png)

**Descrição:**  
Workflow de **geração automática de contratos**, desenvolvido no **n8n**, que transforma dados enviados via **Webhook** em um **contrato personalizado em PDF**, utilizando **Google Docs como template**, e envia o documento final diretamente ao cliente via **WhatsApp**.

Este fluxo é ideal para **prestadores de serviço, consultorias, agências e empresas**, eliminando processos manuais de criação de contratos, reduzindo erros e acelerando o fechamento com o cliente.

**O que esse workflow faz na prática:**
- Recebe dados do cliente via **Webhook (POST)**:
  - Nome
  - CPF/CNPJ
  - Endereço
  - Telefone
  - E-mail
- Normaliza e organiza os dados automaticamente
- Cria uma **cópia de um contrato modelo** no **Google Drive**
- Substitui campos dinâmicos no **Google Docs**:
  - `{nome-cliente}`
  - `{cpf-cnpj}`
  - `{endereco-cliente}`
  - `{telefone-cliente}`
  - `{email-cliente}`
- Converte o contrato automaticamente para **PDF**
- Transforma o arquivo em **Base64**
- Envia o contrato final via **WhatsApp**, utilizando **Evolution API**
- Mensagem automática de entrega para aprovação do cliente

📁 **Workflow incluso:**  
`Gerar contrato - Potto Flow.json`

---

### 📧 Potto Flow – Resumo Inteligente de E-mails com IA (Gmail)

![Potto Flow – Resumo de E-mail](assets/fluxo-resumo-email.png)

**Descrição:**  
Workflow de **resumo automático de e-mails**, desenvolvido no **n8n**, que coleta mensagens recebidas no **Gmail**, analisa o conteúdo com **Inteligência Artificial** e envia diariamente um **resumo estruturado com pontos-chave e ações recomendadas**.

Este projeto é ideal para **gestores, executivos, equipes comerciais e operações**, reduzindo tempo de leitura, evitando perda de informações importantes e facilitando a tomada de decisão diária.

**O que esse workflow faz na prática:**
- Executa automaticamente via **Schedule Trigger** (horário programado)
- Busca e-mails recebidos no **Gmail** dentro de um intervalo de tempo definido
- Agrega e normaliza os dados das mensagens:
  - Remetente
  - Destinatários
  - Conteúdo resumido
- Envia os dados para um **Agente de IA (OpenAI / LLM)** que:
  - Identifica os **principais pontos dos e-mails**
  - Extrai **problemas, decisões e informações relevantes**
  - Gera uma lista clara de **itens de ação**, associados a pessoas quando possível
- Retorna o resultado em **JSON estruturado**
- Envia automaticamente um **e-mail formatado em HTML**, contendo:
  - 📌 Resumo dos e-mails
  - ✅ Lista de ações recomendadas
- Facilita acompanhamento diário sem necessidade de leitura manual de múltiplos e-mails

📁 **Workflow incluso:**  
`Potto_Flow___Resumo_de_e_mail.json`

---

## 👤 Autor
**Diego Hugo**  
Especialista em Inteligência Artificial com foco em **Automações Inteligentes, Agentes Autônomos e Python**

📌 Áreas de atuação:
- IA Generativa  
- Agentes Autônomos (LangGraph)  
- RAG  
- Automação Inteligente (Python / n8n)  
- Aplicações reais de IA para empresas

🔹 Especialidades:
- Automação Inteligente
- Agentes Autônomos
- n8n avançado
- IA aplicada a marketing e operações

---

## ⚠️ Observações Importantes
- Os arquivos representam **exports de workflows do n8n**
- Alguns fluxos podem exigir:
  - Credenciais (APIs)
  - Ajustes de variáveis de ambiente
- Recomenda-se importar os workflows em ambiente de teste antes de produção

---

🚀 Sinta-se à vontade para explorar, adaptar e evoluir essas automações.
