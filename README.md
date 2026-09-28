# Aprofundamento de Formação — thumbnails reais

Esta versão usa imagens representativas reais das obras:
- pôsteres oficiais/promocionais para filmes e minisséries;
- arte do provedor para séries/documentários;
- capas reais da editora para livros;
- screenshot oficial do aplicativo Catho+.

As imagens são referenciadas por URL em `conteudos.csv`, na coluna `thumbnail_url`.
Há fallback visual automático se uma fonte externa estiver temporariamente indisponível.

Deploy:
1. substitua `index.html`;
2. substitua `conteudos.csv`;
3. faça Commit changes.

Não é necessária pasta `assets`.
