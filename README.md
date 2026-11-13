Painel Financeiro

Painel pessoal de finanças em um único arquivo (index.html): contas, transações, contas mensais, dívidas, investimentos, metas e relatórios. HTML, CSS e JavaScript puro, sem build e sem dependências (só as fontes do Google Fonts).

Como usar

Abra o index.html no navegador ou publique no GitHub Pages. Não precisa instalar nada.

Na primeira abertura o painel mostra dados de exemplo (nada é gravado). No aviso do topo:

Começar do zero limpa os exemplos e cria as categorias padrão.
Manter estes exemplos grava os exemplos como seus dados.
Barra do topo
Controle	O que faz
‹ mês ›	Troca o mês de referência de todas as telas
Hoje	Volta para o mês atual
Olho	Oculta ou mostra os valores na tela
Sol/lua	Alterna o tema: automático, claro, escuro
Cadeado	Bloqueia o painel (aparece quando há PIN)
Novo	Atalho para criar qualquer tipo de registro
Módulos
Visão geral

Resumo do mês: patrimônio líquido, saldo em contas, receitas, despesas, resultado, investimentos, dívidas em aberto e contas a pagar. Gráficos de receitas x despesas (6 meses), saldo acumulado e despesas por categoria, além das próximas contas, últimos lançamentos e metas.

Patrimônio líquido = saldo das contas + valor atual dos investimentos − dívidas em aberto.
Transações

Lançamentos de receita, despesa e transferência entre contas. Filtros por mês, tipo, categoria e conta, mais busca por descrição.

Contas

Conta corrente, poupança, carteira, cartão de crédito etc.

Saldo = saldo inicial + receitas − despesas ± transferências.
"Somar no patrimônio líquido" define se a conta entra no cálculo do patrimônio.
Ver extrato abre as transações filtradas pela conta.
Contas mensais

Despesas fixas (aluguel, internet, assinaturas) com dia de vencimento. A situação é calculada sozinha: paga, vence hoje, vence em N dias ou atrasada.

Pagar marca a conta como paga no mês e cria a despesa correspondente.
Desfazer remove o pagamento e a despesa criada.
Contas desmarcadas como "Ativa" ficam pausadas e saem do total.
Dívidas

Financiamentos, empréstimos e parcelamentos, com juros ao mês e barra de quitação.

Em aberto = valor total − (parcelas pagas × valor da parcela).
Se o valor da parcela ficar em branco, o painel divide o total pelo número de parcelas.
Registrar parcela paga soma uma parcela e lança a despesa no mês selecionado.
Investimentos

Ativos com tipo, quantidade, preço médio e preço atual.

Investido = quantidade × preço médio.
Atual = quantidade × preço atual (sem preço atual, usa o preço médio).
O painel não busca cotações: atualize o preço atual editando o ativo.
Metas e orçamentos
Meta de reserva: valor alvo, quanto já foi guardado e prazo. O botão Guardar valor soma ao total.
Orçamento de categoria: teto mensal. O gasto é calculado pelas despesas do mês naquela categoria; a barra fica amarela a partir de 80% e vermelha ao estourar.
Relatórios

Período de 3, 6 ou 12 meses: médias de receita e despesa, sobra média, melhor mês, gráficos e maiores despesas. Copiar CSV do período gera as transações separadas por ; para colar em planilha.

Ajustes
Painel: nome, moeda, tema, tela inicial e cor de destaque.
Módulos visíveis: esconde as seções que você não usa.
Indicadores: escolhe quais cartões aparecem na visão geral.
Categorias: cria, edita e exclui categorias de receita e despesa.
Acesso: ocultar valores, PIN de 4 a 8 dígitos e bloqueio automático por inatividade.
Dados: exportar e importar JSON, ou apagar tudo.
Onde os dados ficam

Os dados são salvos no localStorage do navegador (chave painel-financeiro-v1).

Ficam só naquele navegador e aparelho; não sincronizam.
Somem se os dados do site forem limpos.
Faça backup em Ajustes → Exportar (copiar JSON) e restaure com Importar JSON.

Nenhum dado financeiro vai para o repositório: o arquivo contém apenas o código e os exemplos fictícios.

Segurança

O PIN é uma trava de tela. Ele é guardado como hash SHA-256 com salt, mas não criptografa os dados nem substitui um login: quem tiver acesso ao navegador consegue ler o localStorage. Não use em computador compartilhado.

Endereços das telas

#visao-geral · #transacoes · #contas · #mensais · #dividas · #investimentos · #metas · #relatorios · #ajustes
