# BioBridge Tech

## Descrição do Projeto
Conecta bioinformatas (não biólogos) à biologia, com explicações objetivas, rápidas e de fácil entendimento para estes profissionais, auxiliando e otimizando a rotina de trabalho.

## Objetivo do Projeto no Bootcamp
Demonstrar o uso da API Google Gemini e conceitos da 3ª Imersão IA da Alura/Google para criar uma ferramenta útil na tradução de conhecimento complexo.

## Funcionalidades Implementadas (Neste MVP)
- Recebe um termo de biologia (gene, proteína, organismo, etc.) do usuário.
- Envia o termo para a API Google Gemini.
- Retorna uma explicação simples, analogias com TI, e sugestões de exemplos de URLs para bancos de dados científicos, indicando onde buscar conteúdo mais completo.
- Exibe a resposta da IA, com esses 3 itens, para o usuário.
- A interação é via linha de comando/input no Google Colab neste MVP.

## Como Atende às Exigências do Bootcamp
- O projeto se comunica diretamente com a API Google Gemini para gerar as explicações e analogias numa linguagem que o usuário absorva com mais rapidez a explicação.
- Foi utilizado requisições HTTP com `requests` devido ao problema de instalação da biblioteca oficial 'google-generative-ai', demonstrando conhecimento na interação com APIs web.
- Relação com as Aulas 4 e/ou 5:
    - Foi utilizado prompts cuidadosamente elaborados (Prompt Engineering - Aula 4) para instruir a IA a gerar explicações simples e fazer analogias de TI.
    - A interação com uma API externa (Gemini API) foi demonstrada fazendo requisições HTTP (`requests`), o que é um conceito chave (Interação com APIs / Uso de Ferramentas - Aula 5) sobre conectar modelos a sistemas externos/dados.
    - Embora não implementado no MVP atual (focado na explicação textual via requisições HTTP), a funcionalidade planejada para o futuro de buscar dados biológicos reais (expressão, variações, mapas) em bancos de dados externos demonstra a aplicação de um conceito chave do Function Calling (Aula 5).
- Publicação no GitHub: O código-fonte completo está disponível neste repositório público.

## Tecnologias Utilizadas
- Python
- Biblioteca `requests` (para requisições HTTP à API Gemini)
- API Google Gemini

## Como Configurar e Executar
1. Clone este repositório para sua máquina local ou abra o notebook diretamente no Google Colab.
2. Obtenha sua API Key: Siga as instruções no Google AI Studio ([https://aistudio.google.com/](https://aistudio.google.com/)) para obter sua API Key.
3. Configure a API Key:
   - **No Google Colab:** Use o recurso Secrets (menu de chave na lateral esquerda) ou a caixa de input seguro (`getpass.getpass`) na primeira célula para inserir sua chave. **NUNCA cole a chave diretamente no código que irá para o GitHub.**
   - **Em ambiente local:** Configure uma variável de ambiente chamada `GOOGLE_API_KEY` com sua chave.
4. Se estiver rodando localmente ou se `requests` não estiver no Colab, execute: `pip install requests`. (No Colab, a primeira célula do notebook já faz isso).
5. **Execute o Notebook no Google Colab:** Abra o arquivo `.ipynb` no Colab e execute as células na ordem (Célula 1, Célula 2, Célula 3, Célula 4, Célula 5).
6. Interaja com o chatbot na área de output da Célula 5, digitando os termos de biologia quando solicitado.

## Escopo Futuro (Ideias para Próximas Versões)
- Implementar uma interface gráfica (GUI) mais amigável (usando Streamlit, Gradio, Flask, etc.).
- Conectar a APIs de bancos de dados biológicos reais (NCBI, UniProt, etc.) para buscar dados de expressão, variações, etc., e exibir essas informações (Implementação de Function Calling/Uso de Ferramentas - Aula 5).
- Melhorar as sugestões de análise e visualização, talvez gerando snippets de código básicos.
- Incorporar a funcionalidade de sugestoes de analise exploratoria R/Python.
- Funcionalidade para marcar explicações como "importante" ou "uso recorrente" para salvá-las localmente e permitir reconsultas rápidas sem precisar chamar a API novamente (Persistência de Dados).

## Autor
Paula Bruno
github.com/paula-bruno/biobridge-tech
http://www.linkedin.com/in/paulabrunno

## Licença
Este projeto está sob a [MIT License](https://opensource.org/licenses/MIT). Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## Disclaimer
Esta ferramenta de IA é projetada apenas para fins educacionais e informativos. As explicações e analogias são geradas por um modelo de linguagem e não substituem o aconselhamento profissional de biólogos, médicos, ou bioinformatas especializados. Os exemplos de links são ilustrativos e a consulta a bases de dados oficiais é indicada para informações elaboradas e validadas.
