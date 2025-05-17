# dio-ia

**Teste de chat**
![Imagem do teste do chat ia feito no Azure AI Foundry](https://live.staticflickr.com/65535/54524673584_ec866b9da7_b.jpg)

**Índice de busca vetorial**
![Imagem do índice gerado para a busca do no pdf](https://live.staticflickr.com/65535/54524673584_ec866b9da7_b.jpg)

# Relatório Técnico do Projeto de IA com Busca Vetorial

## 🎯 Objetivo do Projeto

Este projeto tem como finalidade proporcionar uma plataforma interativa com capacidade de entendimento contextual baseada em documentos carregados pelo usuário. As principais funcionalidades implementadas são:

✅ Carregamento de arquivos PDF contendo informações relevantes para estudo ou projeto.  
✅ Implementação de um sistema de busca vetorial para indexação e recuperação de informações.  
✅ Uso de inteligência artificial para gerar respostas fundamentadas nos conteúdos carregados.  
✅ Desenvolvimento de um chat interativo para perguntas e respostas com base no conteúdo dos arquivos.

## 🧠 Tecnologias e Conceitos Utilizados

- **IA Generativa**: Utilização de modelos da família OpenAI para geração de respostas naturais.
- **Embeddings**: Conversão de textos em vetores semânticos usando o modelo `text-embedding-ada-002`.
- **Buscas Vetorizadas**: Indexação e recuperação de vetores usando Azure AI Search.
- **Azure AI Foundry**: Plataforma que integra e orquestra os serviços de IA e busca vetorial.

## ⚙️ Configuração Técnica

### 🔹 Geração de Embeddings

Os embeddings foram gerados utilizando:

- API Base: `https://iadio0603107097.openai.azure.com`
- Modelo: `text-embedding-ada-002`
- Dimensão dos vetores: `1536`
- Tipo de conexão: `workspace_connection` via Azure Machine Learning

### 🔹 Indexação em Azure AI Search

A indexação foi realizada com as seguintes configurações:

- Endpoint: `https://search-dio-ia.search.windows.net/`
- Nome do índice: `keen-cart-ywnwf2fd2v`
- Mapeamento dos campos:
  - Texto: `content`
  - Vetores: `contentVector`
  - Nome do arquivo: `filepath`
  - Metadados: `meta_json_string`
  - Título: `title`
  - URL: `url`

### 🔒 Conexões

Foram utilizadas conexões gerenciadas dentro do Azure Machine Learning Workspace:

- Conexão com Azure OpenAI: `iadio0603107097_aoai`
- Conexão com Azure AI Search: `searchdioia`
