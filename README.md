# OrientadorVocacional_Dify 🎯

Um chatbot inteligente e personalizado desenvolvido para auxiliar usuários na escolha do curso ideal com base em suas habilidades, conhecimentos prévios e interesses pessoais. 

Este projeto foi construído utilizando a plataforma **Dify**, integrando técnicas de **RAG (Retrieval-Augmented Generation)** para consulta a uma base de dados oficial de cursos e utilizando o modelo **Gemini 2.5 Flash** para a orquestração e geração das respostas.

---

## 🚀 Funcionalidades

- **Mapeamento de Perfil:** O chatbot conduz uma conversa amigável para entender os interesses, pontos fortes e objetivos do usuário.
- **Consulta à Base de Dados Oficial (RAG):** A IA não alucina sobre os cursos disponíveis; ela consulta diretamente uma base de dados que contém o portfólio oficial de cursos, pré-requisitos e descrições sucintas.
- **Recomendação Personalizada:** Cruza os dados do usuário com a base de conhecimento para sugerir os cursos mais adequados, justificando o motivo da escolha.

---

## 🛠️ Tecnologias e Ferramentas

- **[Dify](https://dify.ai/):** Plataforma de desenvolvimento de aplicações de LLM (Orquestração do fluxo e gerenciamento de conhecimento).
- **Google Gemini 2.5 Flash:** Modelo de linguagem de última geração utilizado via API, escolhido pelo excelente custo-benefício, velocidade de resposta e grande janela de contexto.
- **RAG (Vetorização de Documentos):** Base de conhecimento interna alimentada com o portfólio oficial de cursos.

---

## 📐 Arquitetura do Fluxo no Dify

O projeto foi estruturado utilizando a seguinte lógica:

1. **Input do Usuário:** Coleta das preferências e histórico do usuário.
2. **Contexto / RAG:** O nó de Conhecimento do Dify realiza uma busca semântica na base de dados de cursos usando os termos e interesses chave citados.
3. **Prompt Engine / LLM:** O Gemini 2.5 Flash recebe o perfil do usuário + as descrições dos cursos encontrados na base de dados.
4. **Output:** Apresentação formatada das melhores opções de cursos e orientações sobre os próximos passos.



---

## 📁 Estrutura do Repositório

- `/dify-dsl/`: Contém o arquivo `.yml` de exportação do aplicativo.
- `README.md`: Documentação do projeto.

---

## ⚙️ Como Replicar este Projeto

Se você deseja rodar ou testar este fluxo na sua própria conta do Dify:

1. Faça o download do arquivo `Orientador Vocacional .yml` presente neste repositório.
2. Acesse o seu painel do **Dify**.
3. Clique em **Create from Blank** (Criar do zero) e escolha a opção **Import DSL file**.
4. Configure suas credenciais da API do Google AI Studio para habilitar o modelo **Gemini 2.5 Flash**.
5. Na aba **Knowledge** (Conhecimento), crie uma nova base de dados e faça o upload do catálogo de cursos (você pode usar um arquivo .txt, .csv ou .pdf com a lista de cursos e pré-requisitos).
6. Vincule essa nova Base de Conhecimento ao nó de contexto do chatbot.

---

## 👤 Felipe 
