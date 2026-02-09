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

### 🧑‍💼 Potto Flow – Triagem Inteligente de Currículos com IA (RH)

![Potto Flow – Triagem de Currículo RH](assets/triagem-curriculo-rh.png)

**Descrição:**  
Workflow completo de **triagem automatizada de currículos**, desenvolvido no **n8n**, que utiliza **Inteligência Artificial** para analisar currículos em **PDF**, comparar com uma **descrição de vaga específica** e gerar uma **avaliação estruturada do candidato**, pronta para decisão de RH.

Este projeto é ideal para **times de Recursos Humanos, recrutadores, consultorias de RH e empresas**, reduzindo drasticamente o tempo de análise manual e aumentando a consistência e qualidade das decisões de contratação.

**O que esse workflow faz na prática:**
- Monitora automaticamente uma **pasta no Google Drive**
- Detecta quando um **novo currículo em PDF** é adicionado
- Faz o **download automático do arquivo**
- Extrai o texto completo do currículo (**PDF → texto**)
- Injeta dinamicamente:
  - 📄 Descrição detalhada da vaga  
  - 🎯 Prompt de avaliação rigoroso de recrutador  
- Utiliza um **Agente de IA (OpenAI / LLM)** para:
  - Avaliar aderência do candidato à vaga
  - Identificar pontos fortes e fracos
  - Detectar possíveis **job hoppers**
  - Gerar um **percentual de compatibilidade**
- Retorna a análise em **formato estruturado**
- Normaliza os dados via **Code Node**
- Registra automaticamente os resultados em uma **planilha do Google Sheets**, incluindo:
  - Nome do candidato
  - Contato
  - Percentual de compatibilidade
  - Resumo do perfil
  - Razões para contratar
  - Razões para não contratar

Este fluxo cria um **pipeline de recrutamento inteligente**, escalável e auditável, pronto para uso em ambientes reais de RH.

📁 **Workflow incluso:**  
`Triagem de Currículo RH - Potto Flow.json`

---

### 🛒 Potto Flow – Infoproduto com Recuperação de Checkout (WhatsApp)

![Potto Flow – Infoproduto e Recuperação de Checkout](assets/fluxo-infoproduto-e-recuperacao-checkout.png)

**Descrição:**  
Workflow avançado de **automação de vendas de infoprodutos**, desenvolvido no **n8n**, focado em **atendimento automatizado, recuperação de checkout abandonado e follow up inteligente via WhatsApp**.

Este projeto foi desenhado para **produtores digitais, lançadores, afiliados e infoprodutores**, automatizando o contato com leads, aumentando taxa de conversão e reduzindo esforço manual no pós-clique.

**O que esse workflow faz na prática:**
- Recebe eventos via **Webhook** (ex: lead, checkout iniciado, checkout abandonado)
- Normaliza e simplifica os dados do lead:
  - Nome
  - WhatsApp
  - Produto de interesse
  - Status do funil
- Identifica automaticamente o **estágio do lead**:
  - Novo lead
  - Checkout iniciado
  - Checkout abandonado
  - Compra finalizada
- Executa **fluxos condicionais** com **Switch + Regras**
- Envia mensagens personalizadas via **WhatsApp**, como:
  - Boas-vindas ao infoproduto
  - Lembrete de checkout abandonado
  - Reforço de benefícios do produto
  - Gatilhos de urgência e escassez
- Implementa **timers estratégicos** com **Wait Node**:
  - ⏱️ minutos após abandono
  - ⏱️ horas depois
  - ⏱️ novo follow up se não houver resposta
- Evita mensagens duplicadas ou spam com controle de fluxo
- Possui ramificação para:
  - Compra concluída → encerra automação
  - Sem resposta → encerra fluxo com segurança
- Estrutura preparada para integração com:
  - Plataformas de checkout
  - CRM
  - Banco de dados de leads

Este fluxo cria um **funil automatizado de vendas via WhatsApp**, focado em **conversão, escala e experiência do usuário**, pronto para ambientes reais de infoprodutos.

📁 **Workflow incluso:**  
`Infoproduto_Potto_Flow.json`

---

### 💰 Potto Flow – Agente Financeiro Inteligente com Supabase (Chat + IA)

![Potto Flow – Agente Financeiro Supabase](assets/agente-financeiro-supabase.png)

**Descrição:**  
Workflow de **Agente Financeiro Inteligente**, desenvolvido no **n8n**, que permite ao usuário **gerenciar gastos financeiros por chat**, utilizando **Inteligência Artificial, memória de contexto e Supabase como banco de dados**.

Este agente funciona como um **assistente financeiro conversacional**, capaz de registrar, consultar, atualizar, excluir e somar despesas de forma natural, segura e auditável, sendo ideal para **controle financeiro pessoal, familiar ou de pequenas empresas**.

**O que esse agente faz na prática:**
- Recebe mensagens via **Chat Trigger do n8n**
- Atua como **Assistente Financeiro Inteligente**, orientado por prompt estruturado
- Utiliza **LLM (OpenAI)** para entender comandos em linguagem natural
- Mantém **memória de conversa** para continuidade do atendimento
- Integra-se diretamente ao **Supabase** para persistência de dados
- Permite executar ações financeiras via chat:
  - 📊 **Visualizar gastos**
    - Lista nome, tipo e valor
    - Permite filtros por categoria ou período
  - ➕ **Adicionar novos gastos**
    - Classifica automaticamente o tipo se não informado
    - Categorias suportadas:
      - Mercado
      - Diversão
      - Comida
      - Educação
      - Assinatura
      - Transporte
  - ✏️ **Atualizar gastos existentes**
    - Confirma o registro antes de editar
    - Permite alterar nome, valor ou tipo
  - 🗑️ **Deletar gastos**
    - Confirmação obrigatória antes da exclusão
  - 🧮 **Somar gastos**
    - Total geral ou filtrado por tipo/período
- Evita ações incorretas com:
  - Confirmação de comandos críticos
  - Validação de registros existentes
- Retorna respostas **claras, organizadas e amigáveis**

Este fluxo cria um **sistema financeiro conversacional completo**, combinando **IA + banco de dados + automação**, pronto para uso real e escalável.

📁 **Workflow incluso:**  
`Potto_Flow___Agente_financeiro__supabase.json`

## 📈 Potto Flow – Agente Automatizado para Geração de Leads (Google Maps → Planilha)

![Potto Flow – Agente para Gerar Leads](assets/agente-para-gerar-leads.png)

**Descrição:**  
Workflow de **geração automática de leads**, desenvolvido no **n8n**, que realiza **prospecção ativa de empresas no Google Maps**, extrai dados relevantes via **Outscraper API**, trata e normaliza as informações e salva os leads de forma estruturada em uma **planilha do Google Sheets**.

Este projeto é ideal para **times comerciais, SDRs, agências de marketing, pré-vendas e outbound**, permitindo criar listas qualificadas de leads com rapidez, escala e baixo esforço manual.

**O que esse workflow faz na prática:**
- Inicia manualmente via **Manual Trigger**
- Define parâmetros de busca dinamicamente:
  - 🔍 Tipo de negócio (ex: clínica de estética)
  - 📍 Localização (cidade/região)
- Executa requisição **HTTP POST** para a **Outscraper API (Google Maps Search)**
- Coleta dados enriquecidos das empresas, como:
  - Nome da empresa
  - Endereço completo
  - Telefone
  - Website
  - E-mails (principal e secundário, quando disponíveis)
  - Avaliação (rating)
  - Número de reviews
  - Categoria
  - Horário de funcionamento
- Processa e normaliza os dados via **Code Node (JavaScript)**:
  - Remove caracteres inválidos
  - Ajusta formatos de telefone
  - Garante consistência dos campos
- Registra automaticamente os leads em uma **planilha do Google Sheets**, com colunas bem definidas
- Estrutura pronta para:
  - Enriquecimento adicional
  - Integração com CRM
  - Automação de contato (WhatsApp, e-mail, etc.)

Este fluxo cria uma **máquina de geração de leads B2B**, escalável, reutilizável e facilmente adaptável para diferentes nichos e regiões.

📁 **Workflow incluso:**  
`Potto_Flow___Agente_para_gerar_leads.json`

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
