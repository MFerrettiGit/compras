# Compras — Estoque & Reposição (M. Ferretti)

Painel visual de apoio à decisão de compra, alimentado pela planilha `ESTOQUE.xls` da filial 01.

**Site:** https://mferrettigit.github.io/compras/

## O que o painel mostra
- **Visão Geral** — responde de cara as perguntas-chave do comprador (estoque baixo sem pedido, zerados em linha, fornecedores a pedir, estoque alto, pouca qtd com muitos dias).
- **Estoque e detalhes** — base completa com busca, filtros (fornecedor, curva ABC, situação), ordenação e exportação CSV. Clique numa linha para ver todos os 54 campos do item.
- **Compra por Fornecedor** — total do pedido sugerido por fornecedor; verde = aconselhado pedir.
- **Atenção — Compra** — onde falta produto (repor, gerar pedido, zerados).
- **Atenção — Venda** — onde sobra produto (estoque alto, capital parado, giro lento).

## Atualização dos dados
Hoje os dados vêm da planilha. O arquivo `dados/estoque.js` é gerado a partir do `ESTOQUE.xls`
(NPOI, 264 produtos / 54 colunas). Futuramente será substituído por uma query direta ao banco.

Linha 2 da planilha = descrição de cada coluna; linha 3 = nome técnico (TOTVS); dados a partir da linha 4.
