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

### 📚 Potto Flow – RAG Automático com Google Drive + Supabase (IA)

![Potto Flow – RAG](assets/fluxo-rag.png)

**Descrição:**  
Workflow completo de **RAG (Retrieval-Augmented Generation)** desenvolvido no **n8n**, responsável por **ingerir documentos automaticamente**, gerar **embeddings com IA** e armazená-los em um **Vector Store no Supabase**, criando uma **base de conhecimento consultável por agentes de IA**.

Este projeto é ideal para **chatbots inteligentes, assistentes corporativos, bases de conhecimento internas, suporte técnico e aplicações educacionais**, permitindo que a IA responda com base em documentos reais e atualizados.

**O que esse workflow faz na prática:**
- Monitora automaticamente uma **pasta específica no Google Drive**
- Detecta quando um **novo arquivo é adicionado** (ex: PDFs)
- Normaliza os metadados do arquivo:
  - ID do arquivo
  - Tipo (MIME)
  - Data de criação
- Faz o **download automático do documento**
- Extrai o texto do arquivo (**PDF → texto**)
- Prepara o conteúdo para indexação:
  - Limpeza
  - Padronização de campos
- Fragmenta o texto com **Recursive Character Text Splitter**
  - Controle de chunk size para melhor recuperação semântica
- Gera **embeddings utilizando OpenAI**
- Armazena documentos e vetores no **Supabase Vector Store**
  - Com metadados para rastreabilidade
- Estrutura pronta para:
  - Consulta via agentes de IA
  - Chatbots com contexto documental
  - Sistemas RAG escaláveis e auditáveis

Este fluxo cria uma **pipeline completa de ingestão e indexação RAG**, totalmente automatizada, robusta e pronta para uso em produção.

📁 **Workflow incluso:**  
`Potto_Flow___RAG.json`

---

## 🧩 Potto Flow – Buscar ID de Grupos em Massa (Evolution API → Google Sheets)

![Potto Flow – Buscar ID de Grupos em Massa](assets/buscar-id-grupo-em-massa.png)

**Descrição:**  
Workflow utilitário desenvolvido no **n8n** para **listar e extrair automaticamente os IDs de todos os grupos** vinculados a uma instância da **Evolution API (WhatsApp)**, salvando essas informações de forma organizada em uma **planilha do Google Sheets**.

Este projeto é ideal para **operações de WhatsApp em escala**, times de automação, suporte técnico e desenvolvedores que precisam **mapear grupos ativos**, realizar auditorias, integrações posteriores ou preparar automações em massa baseadas em grupos.

**O que esse workflow faz na prática:**
- Inicia manualmente via **Manual Trigger** (modo teste ou execução controlada)
- Conecta-se à **Evolution API** utilizando credenciais configuradas
- Executa a operação **Fetch Groups** para buscar todos os grupos disponíveis na instância
- Retorna dados estruturados dos grupos, como:
  - 🆔 ID do grupo
  - 👥 Nome / assunto do grupo
- Realiza a separação dos registros com **Split Out**
- Processa os itens em lote com **Loop Over Items**
- Aplica controle de ritmo com **Wait Node** para evitar:
  - Limites de API
  - Bloqueios por excesso de requisições
- Registra automaticamente os dados em uma **planilha do Google Sheets**, com colunas:
  - `ID`
  - `Grupo`
- Fluxo seguro, simples e reutilizável para diferentes instâncias e contas

Este fluxo funciona como uma **ferramenta base de infraestrutura para automações com WhatsApp**, facilitando o gerenciamento, controle e uso estratégico de grupos em outros workflows.

📁 **Workflow incluso:**  
`Buscar_ID_grupo_em_massa_EVO___Potto_Flow.json`

---

## 🤖 Potto Flow – Agente SDR Inteligente com CRM (Notion + Supabase)

![Potto Flow – Agente SDR CRM](assets/Agente_SDR_CRM.png)

**Descrição:**  
Workflow de **Agente SDR Inteligente**, desenvolvido no **n8n**, responsável por **auxiliar o processo de pré-vendas e atendimento comercial**, integrando **Notion (CRM)** e **Supabase (banco de dados operacional)**.

Este agente atua como um **assistente de SDR**, organizando leads, atualizando status e mantendo os dados sincronizados entre CRM e banco de dados, garantindo **continuidade de atendimento e rastreabilidade das interações**.

**O que esse workflow faz na prática:**
- Centraliza a gestão de leads em um **CRM no Notion**
- Busca automaticamente todos os leads cadastrados:
  - Nome  
  - WhatsApp  
  - Status  
  - Resumo do atendimento
- Permite **qualificar leads**:
  - Atualiza status para **Atendimento Humano**
  - Registra resumo completo da conversa
  - Salva e-mail do lead
- Permite **encerrar leads perdidos**:
  - Atualiza status para **Perdido**
  - Registra resumo final da conversa
- Sincroniza informações críticas com o **Supabase**:
  - Status do lead
  - E-mail
- Mantém o histórico organizado para continuidade do processo comercial

Este fluxo é ideal para **times de SDR, pré-vendas, atendimento comercial e automações de CRM**, garantindo **processos claros, organizados e escaláveis**.

📁 **Workflow incluso:**  
`Agente SDR - CRM.json`

---

## 🧠 Potto Flow – Agente SDR com MCP (CRM Inteligente via Tools)

![Potto Flow – Agente SDR MCP CRM](assets/Agente_SDR_MCP_CRM.png)

**Descrição:**  
Workflow avançado de **Agente SDR com MCP (Model Context Protocol)**, desenvolvido no **n8n**, que expõe o CRM como **ferramentas (Tools)** para um **Agente de IA**, permitindo que o próprio agente **decida quando buscar, atualizar ou encerrar leads automaticamente**.

Este projeto representa uma **arquitetura moderna de automação orientada a agentes**, onde a IA possui **controle ativo sobre o CRM**, simulando o comportamento de um **SDR humano experiente**, com autonomia e lógica contextual.

**O que esse workflow faz na prática:**
- Expõe o CRM como **Tools via MCP Server Trigger**
- Permite que o **Agente de IA** execute ações como:
  - 🔍 Buscar todos os leads no CRM (Notion)
  - ✅ Qualificar leads automaticamente
  - ❌ Marcar leads como perdidos
  - ✏️ Atualizar e-mails e status no Supabase
- Mantém **sincronização bidirecional** entre:
  - Notion (CRM)
  - Supabase (banco operacional)
- Garante consistência dos dados em tempo real
- Facilita integração com:
  - Chatbots
  - Assistentes comerciais
  - Fluxos de atendimento automatizado

Este fluxo é ideal para **operações comerciais inteligentes**, **SDRs automatizados**, **assistentes de vendas com IA** e arquiteturas baseadas em **Agentic AI + MCP**, prontas para escala e produção.

📁 **Workflow incluso:**  
`Agende SDR MCP - CRM.json`

---

## 🚗 Potto Flow – Agente de Concessionária de Automóveis com IA (WhatsApp)

![Potto Flow – Agente de Concessionária Automóveis](assets/Agente_de_Concessionaria_Automoveis.png)

**Descrição:**  
Workflow completo de **Agente de Atendimento Inteligente para Concessionárias**, desenvolvido no **n8n**, projetado para **atender clientes interessados na compra de veículos via WhatsApp**, utilizando **Inteligência Artificial, banco de dados estruturado e envio automático de imagens**.

Este agente simula o comportamento de um **vendedor humano**, entendendo as necessidades do cliente, buscando veículos disponíveis e apresentando opções de forma clara, educada e contextual.

**O que esse workflow faz na prática:**
- Recebe mensagens via **Webhook (WhatsApp – Evolution API)**
- Normaliza dados do cliente:
  - Nome
  - WhatsApp
  - Mensagem enviada
- Busca ou cria automaticamente o cliente no **Supabase (CRM)**
- Identifica o tipo de mensagem recebida:
  - 💬 Texto
  - 🎙️ Áudio (com transcrição automática via IA)
- Utiliza **Agente de IA (LLM)** com:
  - Prompt especializado para vendas de automóveis
  - Memória por usuário (histórico de conversa)
  - Integração com **Tools MCP**
- Consulta veículos disponíveis conforme critérios do cliente:
  - Preço máximo
  - Modelo / marca
  - Ano
- Retorna lista de veículos disponíveis de forma clara
- Quando solicitado, envia **imagens reais dos veículos** automaticamente
- Responde via **WhatsApp**, com texto ou mídia, conforme o contexto

Este fluxo é ideal para **concessionárias, lojas de veículos e operações comerciais automotivas**, oferecendo **atendimento escalável, inteligente e orientado à conversão**.

📁 **Workflow incluso:**  
`Agente de Concessionária - Automóveis.json`

---

## 🧠 Potto Flow – MCP Concessionária (CRM Automotivo via Tools)

![Potto Flow – MCP Concessionária](assets/MCP_Concessionaria.png)

**Descrição:**  
Workflow de **MCP Server (Model Context Protocol)** para Concessionárias, desenvolvido no **n8n**, responsável por **expor o banco de dados automotivo como ferramentas (Tools)** para Agentes de IA.

Este projeto transforma o **CRM da concessionária em uma API inteligente**, permitindo que agentes tomem decisões autônomas sobre **busca de veículos e envio de imagens**, com base em critérios definidos pelo cliente.

**O que esse workflow faz na prática:**
- Cria um **MCP Server Trigger** no n8n
- Expõe o banco de dados de veículos no **Supabase** como Tools:
  - 🔍 **tool_buscar_carros**
    - Pesquisa veículos disponíveis por:
      - Valor
      - Modelo
      - Marca
      - Ano
  - 🖼️ **tool_imagens_carros**
    - Retorna **URLs diretas das imagens** dos veículos
- Garante que o agente:
  - Nunca invente preços ou modelos
  - Utilize apenas dados reais do banco
- Retorna **somente a URL da imagem** quando solicitado
- Estrutura preparada para integração com:
  - Agentes de IA conversacionais
  - Chatbots de vendas
  - Fluxos comerciais automatizados

Este fluxo representa uma **arquitetura moderna baseada em Agentic AI + MCP**, ideal para **operações comerciais avançadas**, CRM inteligente e automações orientadas a contexto.

📁 **Workflow incluso:**  
`MCP Concessionária.json`

---

## 📸 Potto Flow – Template de Atendimento Automático para Instagram com IA

![Potto Flow – Template Instagram](assets/Template_Fluxo_Instagram.png)

**Descrição:**  
Workflow template de **atendimento automatizado para Instagram**, desenvolvido no **n8n**, projetado para **receber, interpretar e responder mensagens diretas (DMs) automaticamente**, utilizando **Inteligência Artificial, memória de conversa e integração direta com a API do Instagram**.

Este projeto serve como **base reutilizável** para criação de **assistentes de atendimento, vendas ou engajamento em redes sociais**, permitindo rápida adaptação para diferentes nichos e estratégias.

**O que esse workflow faz na prática:**
- Recebe eventos do **Instagram Webhook** (mensagens diretas)
- Realiza validação inicial do webhook (GET + hub.challenge)
- Processa mensagens recebidas via **POST**
- Normaliza os dados da conversa:
  - ID do remetente
  - ID da conta do Instagram
  - Conteúdo da mensagem
- Filtra mensagens inválidas:
  - Mensagens enviadas pela própria conta
- Utiliza **Agente de IA (LLM)** com:
  - Prompt configurável por negócio
  - Memória por usuário (continuidade de conversa)
- Gera respostas automáticas:
  - Contextuais
  - Naturais
  - Alinhadas à estratégia definida no prompt
- Envia respostas diretamente para o **Instagram DM** via **HTTP Request**
- Estrutura modular pronta para:
  - Atendimento
  - Pré-vendas
  - Engajamento automático
  - Social Media com IA

Este template é ideal para **criadores de conteúdo, empresas, social medias e agências**, servindo como **ponto de partida profissional** para automações avançadas no Instagram com IA.

📁 **Workflow incluso:**  
`Template_Instagram___Potto_Flow.json`

---

## 💬 Potto Flow – Template de Resposta Automática a Comentários no Instagram com IA

![Potto Flow – Resposta Automática a Comentários Instagram](assets/template-fluxo-resposta-comentarios-instagram.png)

**Descrição:**  
Workflow template de **resposta automática a comentários no Instagram**, desenvolvido no **n8n**, projetado para **monitorar comentários em posts**, interpretar o conteúdo com **Inteligência Artificial** e **responder automaticamente de forma contextual**, mantendo engajamento ativo e imediato.

Este projeto é ideal para **marcas, criadores de conteúdo, infoprodutores, social medias e equipes de marketing**, permitindo escalar interações públicas no Instagram sem perder personalização ou timing.

**O que esse workflow faz na prática:**
- Recebe eventos do **Instagram Webhook** relacionados a novos comentários
- Realiza validações iniciais de segurança e origem do evento
- Normaliza os dados do comentário:
  - ID do post
  - ID do comentário
  - Texto do comentário
  - ID do usuário
- Aplica filtros para:
  - Evitar respostas duplicadas
  - Ignorar comentários da própria conta
- Utiliza **regras condicionais (Switch / If)** para classificar o tipo de comentário:
  - Dúvidas
  - Interesse em produto/serviço
  - Comentários genéricos
  - Engajamento simples (ex: “🔥”, “top”, “amei”)
- Gera respostas automáticas via **Agente de IA (LLM)**:
  - Linguagem natural
  - Alinhada ao posicionamento da marca
  - Personalizada conforme o contexto do comentário
- Envia a resposta diretamente como **reply ao comentário** via **Instagram Graph API**
- Estrutura pronta para:
  - CTA em comentários
  - Direcionamento para DM
  - Estratégias de engajamento e conversão

Este template cria uma **máquina de engajamento automático no Instagram**, aumentando alcance, relevância e velocidade de resposta, com **IA aplicada de forma estratégica e segura**.

📁 **Workflow incluso:**  
`Template Fluxo de resposta comentários no Instagram - Potto Flow copy.json`

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
