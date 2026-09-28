# Aprofundamento de Formação — versão final

Miniaplicativo estático para disponibilizar filmes, séries, documentários e leituras depois de uma formação ou pregação.

## Estrutura

- `index.html` — aplicação
- `conteudos.csv` — base de conteúdo
- `.nojekyll` — evita processamento desnecessário pelo Jekyll no GitHub Pages
- `README.md` — este arquivo

## URL por formação

O aplicativo lê o parâmetro `contexto` da URL.

Exemplo:

`https://SEU-USUARIO.github.io/aprofundamento-formacao/?contexto=atos`

O dropdown continua disponível para navegar entre futuras formações.

## Como adicionar outra formação

Acrescente novas linhas no `conteudos.csv`.

Use um novo `contexto_id`, por exemplo:

- `joao`
- `eucaristia`
- `oracao`
- `paulo`

Repita o mesmo `contexto_nome` e `contexto_subtitulo` em todas as linhas daquele contexto.

Tipos suportados:
- `Filme`
- `Série`
- `Documentário`
- `Leitura`

A nova formação aparecerá automaticamente no dropdown.

## Publicação no GitHub Pages

### 1. Crie um repositório
Sugestão de nome: `aprofundamento-formacao`.

### 2. Envie estes quatro arquivos para a raiz do repositório
- index.html
- conteudos.csv
- .nojekyll
- README.md

### 3. Ative o GitHub Pages
No repositório:
`Settings` → `Pages`

Em `Build and deployment`:
- Source: `Deploy from a branch`
- Branch: `main`
- Folder: `/(root)`
- Save

### 4. Acesse
A URL normalmente será:

`https://SEU-USUARIO.github.io/aprofundamento-formacao/`

Para Atos:

`https://SEU-USUARIO.github.io/aprofundamento-formacao/?contexto=atos`

Use esta última URL no QR Code da formação de Atos.

## Atualizações

Para acrescentar ou alterar recomendações, normalmente basta editar `conteudos.csv` no GitHub e salvar/commit.

Não é necessário alterar o código da página.

## Teste local

Como o navegador precisa carregar o CSV por HTTP, evite testar abrindo `index.html` diretamente pelo Windows Explorer.

Dentro da pasta, rode:

`python -m http.server 8000`

Depois abra:

`http://localhost:8000/?contexto=atos`
