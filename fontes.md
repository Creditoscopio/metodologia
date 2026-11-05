# Fontes

Todos os números de taxa vêm de bases do Banco Central do Brasil.

| Base | O que traz |
|---|---|
| Taxas de juros de operações de crédito por instituição financeira (médias dos últimos 5 dias) | Taxa média por instituição e modalidade, em % ao mês e % ao ano; é a fonte principal |
| Cadastro de instituições em funcionamento | Nome, conglomerado e CNPJ, usado para identificar a instituição pela raiz do CNPJ |
| SGS (Sistema Gerenciador de Séries Temporais) | Taxa média mensal do sistema financeiro, inadimplência da carteira, Selic e agregados nacionais, de pessoas físicas e de pessoas jurídicas, sempre em bloco separado |
| Ranking de Instituições por Índice de Reclamações | Índice trimestral de reclamações, reproduzido na ficha de algumas instituições |

O site mostra a fonte e o período ao lado de cada número. A página [creditoscopio.com.br/fontes](https://creditoscopio.com.br/fontes/) traz, para cada modalidade, o código oficial, o período mais recente e o identificador SHA-256 da cópia exata da resposta do Banco Central que o site usa. Se o Banco Central republicar um período com valores diferentes, o identificador muda e a alteração fica registrada.

## Modalidades publicadas

Segmento de pessoas físicas. Janela de referência de cinco dias úteis, exceto no financiamento imobiliário, em que o Banco Central publica só a média mensal.

| Modalidade no site | Nome na fonte | Código |
|---|---|---|
| Cartão rotativo | Cartão de crédito – rotativo total – Prefixado | 204101 |
| Cartão de crédito parcelado | Cartão de crédito – parcelado – Prefixado | 215101 |
| Cheque especial | Cheque especial – Prefixado | 216101 |
| Crédito pessoal (sem consignado) | Crédito pessoal não consignado – Prefixado | 221101 |
| Crédito consignado INSS | Crédito pessoal consignado INSS – Prefixado | 218101 |
| Crédito consignado público | Crédito pessoal consignado público – Prefixado | 220101 |
| Crédito consignado privado | Crédito pessoal consignado privado – Prefixado | 219101 |
| Financiamento de veículos | Aquisição de veículos – Prefixado | 401101 |
| Aquisição de outros bens | Aquisição de outros bens – Prefixado | 402101 |
| Financiamento imobiliário, taxas de mercado, pós-fixado em TR (mensal) | Financiamento imobiliário com taxas de mercado – Pós-fixado referenciado em TR | 903201 |
| Financiamento imobiliário, taxas reguladas, pós-fixado em TR (mensal) | Financiamento imobiliário com taxas reguladas – Pós-fixado referenciado em TR | 905201 |

O histórico mensal vem desde 2012 na maior parte das modalidades e desde 2015 nos cartões.

## Crédito para empresas

Segmento de pessoas jurídicas da mesma base, em seção própria do site ([creditoscopio.com.br/empresas](https://creditoscopio.com.br/empresas/)). Janela de cinco dias úteis, histórico desde janeiro de 2012. Só as modalidades prefixadas com dado de pelo menos 20 instituições:

| Modalidade no site | Nome na fonte | Código |
|---|---|---|
| Capital de giro com prazo até 365 dias | Capital de giro com prazo até 365 dias – Prefixado | 210101 |
| Capital de giro com prazo acima de 365 dias | Capital de giro com prazo superior a 365 dias – Prefixado | 211101 |
| Desconto de duplicatas | Desconto de duplicatas – Prefixado | 301101 |
| Cheque especial para empresas | Cheque especial – Prefixado | 216101 |
| Conta garantida | Conta garantida – Prefixado | 217101 |

O cheque especial tem o mesmo código nos dois segmentos; no site, o de pessoas jurídicas tem página própria e nunca aparece ao lado do de pessoas físicas. Ficam fora as modalidades pós-fixadas, o adiantamento sobre contratos de câmbio e as que têm menos de 20 instituições.

### Séries do SGS de pessoas jurídicas

Cada modalidade de empresas mostra, em blocos separados da mediana das instituições, a taxa média do mercado e a inadimplência da carteira publicadas pelo Banco Central, e a Selic (série 4189) no mesmo período. O conceito de cada série é o mesmo das séries de pessoas físicas usadas no site.

| Modalidade no site | Taxa média mensal (% ao mês) | Inadimplência (% da carteira) |
|---|---|---|
| Capital de giro com prazo até 365 dias | 25441 | 21090 |
| Capital de giro com prazo acima de 365 dias | 25442 | 21091 |
| Desconto de duplicatas | 25438 ("Desconto de duplicatas e recebíveis") | 21087 |
| Cheque especial para empresas | 25446 | 21095 |
| Conta garantida | 25445 | 21094 |

As séries são de recursos livres e de todas as pessoas jurídicas. A tabela por instituição usa só as operações prefixadas; o SGS não informa se a série inclui as pós-fixadas, e o Banco Central não afirma que as duas medidas sejam equivalentes. Por isso o site não compara a série com a mediana nem com nenhuma instituição. As séries por porte da empresa não são usadas.

### Onde a escolha da instituição mais pesa

A página de empresas compara as modalidades entre si: primeiro quartil (P25), mediana e terceiro quartil (P75) de cada uma e a distância entre os quartis, em pontos percentuais ao mês, só nas modalidades com 10 ou mais instituições. A diferença em reais aparece só no capital de giro, em que o contrato estabelece o prazo: a conta supõe uma dívida de R$ 1.000 paga em parcelas iguais (tabela Price), em 12 meses no capital de giro até 365 dias e em 24 meses no acima de 365 dias, sem IOF, tarifas nem seguros. A forma de pagamento é hipótese do cálculo. No desconto de duplicatas, na conta garantida e no cheque especial, o custo em reais depende do valor e do tempo de uso, que a fonte não informa, e a comparação fica só em pontos percentuais.

### Atualizações mensais

[creditoscopio.com.br/empresas/atualizacoes](https://creditoscopio.com.br/empresas/atualizacoes/) mostra, para cada mês, a mediana de cada modalidade de empresas na primeira janela de cinco dias úteis do mês, comparada à do mês de calendário anterior (sem ponto no mês anterior, não se compara), e quantas instituições tiveram taxa maior, menor ou igual. Não lista nominalmente as maiores altas e quedas, e não atribui causa à variação. Há feeds Atom com as mesmas frases: um geral e um por modalidade.

## Datas

A página de fontes do site mostra duas datas por modalidade: o **período coberto**, que é a janela das operações informada pelo Banco Central, e a data em que o Creditoscópio **carregou** a cópia da fonte usada nesse período. Ela só muda quando chega uma cópia nova. O Banco Central publica cada janela depois que ela termina, então as duas datas são diferentes.

## O que a fonte não informa

- O volume de operações de cada instituição: por isso não há média ponderada entre instituições.
- IOF, tarifas e seguros: a taxa publicada não equivale ao Custo Efetivo Total (CET) de uma oferta.
- A marca comercial: a fonte traz a entidade jurídica, e uma marca pode operar por mais de uma.
- O porte e o setor das empresas no crédito para empresas: cada taxa reúne operações com pessoas jurídicas de todos os tamanhos, e o site não diz qual taxa vale para uma empresa de determinado porte.
- A documentação do Banco Central não define o tomador do consignado privado, a esfera do tomador do consignado público, o que entra em "aquisição de outros bens" nem o que são as "taxas de mercado" e "taxas reguladas" do financiamento imobiliário. O site não afirma nada disso.
