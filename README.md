# Assistente de Chat - Gerência de Infraestrutura do CIn

Este projeto usa a API da OpenAI para responder perguntas com base em documentos PDF da Coordenação de Infraestrutura do CIn/UFPE. A interface é feita com Gradio e roda direto no Google Colab.

### Pré-requisitos
- Conta na OpenAI com acesso à API.
- Chave de API da OpenAI salva no ambiente do Colab.

### Etapas para usar
1. Instalar dependências
- Execute o comando abaixo no início do notebook
- !pip install openai gradio tqdm

2. Configurar o ambiente
- Execute a célula com os import, definição do caminho para os PDFs e instanciação do cliente da OpenAI.

3. Criar vector store e enviar PDFs
- Execute a célula que cria o vector store e envia os pdfs que você colocou em uma pasta chamada input_pdfs.
- Fazer upload dos PDFs para o vector store.

4. Função de resposta
- A função response_output(query, history) utiliza a ferramenta de busca em arquivos (via vector store) para responder com base nos documentos.
- Execute essa célula pra deixar a função pronta para o uso.

5. Iniciar interface Gradio
- Execute a última célula para abrir a interface gráfica de chat.
- Um link será gerado para você interagir com o assistente.

### Como interagir
- Faça perguntas sobre a Coordenação de Infraestrutura do CIn.
- O assistente responde com base nos PDFs enviados.
- Se a pergunta for ambígua ou fora do escopo, ele avisará que não pode responder.
