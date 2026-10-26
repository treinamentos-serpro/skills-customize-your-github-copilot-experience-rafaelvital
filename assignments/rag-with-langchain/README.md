# 📘 Assignment: Building a Document Q&A Assistant with LangChain

## 🎯 Objective

Crie um assistente que responda perguntas usando informações de um pequeno conjunto de documentos. Você praticará preparação de documentos, busca semântica e geração aumentada por recuperação (RAG) com LangChain, incluindo respostas com fontes e tratamento de perguntas sem suporte nos documentos.

## 📝 Tasks

### 🛠️ Prepare and index the documents

#### Descrição
Escolha de 3 a 5 documentos públicos e curtos sobre um tema de seu interesse. Carregue-os com os document loaders do LangChain, divida o conteúdo em trechos e preserve os metadados necessários para identificar a origem de cada trecho.

#### Requisitos
O programa concluído deve:

- Carregar pelo menos 3 documentos e registrar o nome ou caminho de origem de cada um
- Dividir os documentos em trechos com tamanho e sobreposição configuráveis
- Preservar os metadados de origem nos trechos e exibir uma amostra do resultado
- Explicar como instalar as integrações do LangChain necessárias para os loaders escolhidos

### 🛠️ Build semantic retrieval

#### Descrição
Gere embeddings para os trechos e armazene-os em um vector store compatível com LangChain. Crie um retriever que encontre os trechos mais relevantes para uma pergunta e apresente os resultados junto com suas fontes.

#### Requisitos
O programa concluído deve:

- Gerar embeddings usando uma integração compatível com LangChain
- Armazenar os vetores em um vector store e permitir consultá-lo por similaridade
- Retornar até 3 trechos relevantes por pergunta, com metadados que identifiquem suas fontes
- Demonstrar uma pergunta respondível pelos documentos e explicar por que os trechos recuperados são relevantes

### 🛠️ Generate and evaluate grounded answers

#### Descrição
Conecte o retriever a um modelo de linguagem usando LangChain para construir um fluxo RAG. Instrua o assistente a responder somente com base no contexto recuperado, citar as fontes utilizadas e informar quando os documentos não contiverem a resposta.

#### Requisitos
O programa concluído deve:

- Receber uma pergunta e produzir uma resposta a partir dos trechos recuperados
- Exibir a resposta e as fontes correspondentes
- Testar uma pergunta respondível e uma pergunta cuja resposta não esteja nos documentos
- Para a pergunta sem suporte, informar claramente que não há informação suficiente, sem inventar fatos
- Manter credenciais em variáveis de ambiente, nunca em código ou nos documentos, e usar apenas conteúdo público ou autorizado
- Incluir instruções para configurar o provedor escolhido, definir as variáveis de ambiente e executar o programa
