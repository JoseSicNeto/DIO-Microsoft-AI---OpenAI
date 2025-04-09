# Azure OpenAI no Playground - Resumo da Aula Pablo Lopes (Microsoft)

Este documento resume os principais tópicos abordados na aula sobre Azure OpenAI no Playground, ensinada por Pablo Nunes Lopes da Microsoft (https://www.linkedin.com/in/pablonuneslopes/).

## Tópico 1: Criação de Deploy no Azure AI Services

A criação de uma implantação (deploy) no Azure AI Services é feita por modelo. O custo de utilização é determinado pelo modelo escolhido, e não pela quantidade de instâncias provisionadas.

**Entendendo Melhor:**

* **Deploy por Modelo:** Seleciona-se um modelo específico da OpenAI para criar uma implantação dedicada.
* **Custo Baseado no Modelo:** A precificação varia por modelo, geralmente baseada no número de tokens processados (entrada e saída). Modelos mais poderosos têm custo por token mais elevado.
* **Capacidade, Não Instância:** O foco é na capacidade do modelo implantado. Para mais capacidade, considere um modelo mais robusto ou otimize seus prompts.

## Tópico 2: Explorando a Base do Azure AI Foundy e o Playground

### 2.1 Azure AI Foundy (Base de Modelos):

O Azure OpenAI oferece acesso aos modelos da OpenAI, abrangendo diversas capacidades com precificações distintas.

**Entendendo Melhor:**

* **Foco em OpenAI:** Acesso exclusivo aos modelos desenvolvidos pela OpenAI.
* **Catálogo de Modelos:** Variedade de modelos para:
    * **Texto e Fala:** Geração e compreensão de linguagem natural em texto e, às vezes, fala.
    * **Texto e Imagem:** Geração de imagens a partir de texto e outras tarefas relacionadas.
    * **Text Bots (Chatbots):** Modelos otimizados para conversação.
    * **Outros:** Novas capacidades são constantemente adicionadas.
* **Inferência (Previsão de Tokens):** Geração de respostas através da previsão sequencial de tokens. A saída é probabilística.
* **Precificação:** Verifique os custos de cada modelo antes de usar.

### 2.2 Playground:

Interface interativa no Azure OpenAI para desenvolvimento de prompts, preparação de modelos e alteração de configurações visuais.

#### 2.2.1 Chat:

* **Funcionalidades:** Interação conversacional com modelos de linguagem.
* **Configurações:** Permite mudar a implantação, importar/exportar configurações de prompts e ajustar segurança.

#### 2.2.2 Assistentes:

* **Conceito Avançado:** Envolve agentes autônomos e fluxos de trabalho complexos (não detalhado na aula).

#### 2.2.3 Áudio em Tempo Real:

* **Interface:** Para experimentar transcrição de fala para texto e geração de fala a partir de texto (apenas visão geral).

#### 2.2.4 Imagens:

* **Interface:** Para interagir com modelos de geração e manipulação de imagens (apenas visão geral).

#### 2.2.5 Conclusão (Histórico de Perguntas e Respostas):

* Mantém um histórico das interações para revisão e comparação de resultados.

### 2.3 Estocasticidade:

Modelos de linguagem são estocásticos (randômicos), dependendo dos parâmetros configurados. Um bom ajuste é crucial para resultados consistentes.

**Entendendo Melhor:**

* **Processos Randômicos:** A geração de texto não é determinística; a mesma entrada pode gerar saídas diferentes.
* **Dependência de Parâmetros:** Vários parâmetros controlam a aleatoriedade e outros aspectos da geração.
* **Bom Ajuste (Tuning):** Essencial para o caso de uso específico; ajuste inadequado pode levar a respostas ruins.

**Lembre-se:** O mesmo prompt pode gerar diferentes respostas devido à natureza estocástica dos modelos.

## Tópico 3: Entendendo a Tokenização em Modelos de Linguagem

### 3.1 Tokenização:

Processo fundamental de dividir texto em unidades menores (tokens) para processamento pelos modelos. Essencial para otimizar prompts e entender custos.

### 3.2 Ferramentas de Tokenização:

* **Tokenizador (VS Code - Tiktoken):** Extensão para VS Code que permite visualizar a tokenização por diferentes modelos da OpenAI, convertendo texto em tokens e vice-versa.

**Entendendo Melhor:**

* **Unidades de Processamento:** Modelos processam tokens, não diretamente palavras ou caracteres.
* **Visualização de Caracteres e Tokens:** Permite inspecionar a composição de palavras e frases em termos de caracteres e tokens.
* **Desvantagem do Português (Histórica):** Português tendia a ser menos eficiente na tokenização em modelos iniciais (mais tokens por palavra que em inglês), impactando custo e contexto. Modelos recentes melhoraram isso.
* **Tokenização de Números:** Números frequentemente são tokenizados em grupos de dígitos (ex: "normalmente números pegam 3 por vez").
* **Custo de Emojis:** Emojis podem usar um número relativamente grande de tokens, aumentando o custo se usados excessivamente.

## Tópico 5: Parâmetros para Controlar a Geração de Texto

Ajustar parâmetros permite controlar a criatividade, aleatoriedade e extensão das respostas.

**Entendendo Melhor:**

* **Sistema de Mensagens:** Define o papel/persona do modelo no prompt, influenciando o estilo.
* **Temperatura vs. Top P:** Controlam a aleatoriedade da saída.
    * **Temperatura:** Mais alta = mais aleatório/criativo; mais baixa = mais determinístico/focado.
    * **Top P:** Mais baixo = escolha restrita aos tokens mais prováveis (mais coerente/previsível).
* **Tokens Máximos:** Limite do número de tokens na resposta.
* **Penalidade (Presença vs. Frequência):** Reduzem a repetição.
    * **Penalidade de Presença:** Penaliza tokens já presentes no prompt/resposta (incentiva novos tópicos).
    * **Penalidade de Frequência:** Penaliza tokens usados frequentemente na resposta (promove diversidade).

## Tópico Adicional: Multimodalidade

Modelos modernos (como os do Azure AI) podem lidar com outras modalidades além de texto, como imagens.

**Entendendo Melhor:**

* **Capacidade Além do Texto:** Expande as aplicações da IA.
* **DALL-E:** Exemplo de modelo multimodal para gerar imagens a partir de texto.
* **Requisitos para Geração de Imagens Eficaz:**
    * Boa Clareza
    * Boa Especificidade
    * Bom Contexto
    * Boa Estrutura

## Encerrando o Resumo da Aula e Próximos Passos

Para aprofundar o conhecimento, participe do bootcamp em andamento na DIO (Digital Innovation One).

**Link do Bootcamp:** [https://web.dio.me/track/microsoft-azure-open-ai]
