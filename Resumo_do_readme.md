# Azure OpenAI no Playground - Resumo da Aula Pablo Lopes (Microsoft)

Este documento resume os principais pontos da aula sobre Azure OpenAI no Playground, ensinada pelo Pablo Lopes da Microsoft.

## Tópico 1: Deploy no Azure AI Services

* O deploy é específico para cada modelo OpenAI.
* O custo é determinado pelo modelo utilizado (tokens processados), não pela quantidade de instâncias.
* O foco está na capacidade do modelo, em vez da escalabilidade tradicional de instâncias.

## Tópico 2: Explorando a Base do Azure AI Foundy e o Playground

### 2.1 Azure AI Foundy (Base de Modelos):

* Acesso a diversos modelos da OpenAI (texto e fala, texto e imagem, chatbots, etc.).
* A precificação varia conforme o modelo e o uso de tokens (inferência).

### 2.2 Playground: Interface interativa para desenvolvimento de prompts e configurações.

* **Chat:** Interação conversacional com os modelos, configuração do deploy e segurança.
* **Assistentes:** Conceito avançado de agentes e fluxos de trabalho (não detalhado na aula).
* **Áudio em Tempo Real:** Interface para transcrição e geração de fala (visão geral).
* **Imagens:** Interface para geração e manipulação de imagens (visão geral).
* **Conclusão:** Histórico das interações para revisão e iteração de prompts.

### 2.3 Estocasticidade:

* Os modelos são inerentemente randômicos; a mesma entrada pode gerar diferentes saídas.
* Os resultados são influenciados pelos parâmetros configurados.
* Um ajuste adequado dos parâmetros é crucial para garantir consistência e relevância nas respostas.

## Tópico 3: Tokenização

* É o processo de dividir o texto em unidades menores chamadas tokens.
* O português tende a gerar mais tokens por palavra em comparação com o inglês, devido à origem dos modelos GPT.
* Números geralmente são agrupados em até 3 dígitos por token.
* Emojis podem consumir um número significativo de tokens.
* A ferramenta `tiktoken` no VS Code permite a conversão entre texto e tokens.

## Tópico 4: Parâmetros de Geração

### 4.1 Texto:

A geração de texto é controlada por parâmetros como:

* **Temperatura vs. Top P:** Controlam a aleatoriedade e a probabilidade das palavras geradas.
* **Tokens Máximos:** Define o limite para o comprimento da resposta.
* **Penalidade (Presença vs. Frequência):** Influenciam a repetição de palavras na saída.

### 4.2 Imagem:

* **Multimodalidade:** Modelos como o DALL-E podem gerar imagens a partir de descrições textuais.
* Para obter bons resultados na geração de imagens, o prompt deve ter clareza, especificidade, contexto e estrutura.
* A origem da IA pode, por vezes, ser evidente na imagem gerada.

## Encerrando o Resumo da Aula e Próximos Passos

Para aqueles interessados em aprofundar seus conhecimentos, é recomendado participar do bootcamp em andamento na DIO (Digital Innovation One).

**Link do Bootcamp:** [https://web.dio.me/track/microsoft-azure-open-ai]
