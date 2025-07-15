### 1. Propósito do desafio

Desenvolver **um mini‑assistente conversacional** (RAG‑based) que orquestra múltiplas _tools_ via **LangChain + LangGraph** e oferece **interface gráfica** para o usuário final.  
A entrega será avaliada pelo nosso time de engenharia durante uma entrevista técnica.

---

### 2. Requisitos funcionais (obrigatórios)

| Cenário | O agente deve ser capaz de… | Sugestões de implementação |
|---------|----------------------------|----------------------------|
| **Busca na Web** | Receber perguntas no chat, executar buscas no Google e retornar informações consolidadas com links‑fonte. | SerpAPI, Tavily ou Google CSE wrapper do LangChain |
| **Base vetorial** | Fazer _similarity search_ em embeddings previamente carregados (docs ou FAQs). | Chroma, Qdrant ou Azure AI Search (se optar por Foundry) |
| **PostgreSQL** | Executar queries parametrizadas e retornar resultados formatados. | `SQLDatabaseToolkit` do LangChain |
| **Previsão do tempo** | Consultar uma API pública (ex. OpenWeatherMap) e responder em linguagem natural. | HTTP tool via LangChain |

Todas as funções devem ser **evocadas pelo modelo** conforme o _prompt_ do usuário, sem botões dedicados.

---

### 3. Requisitos não‑funcionais (obrigatórios)

1. **Organização do código**  
