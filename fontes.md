# Fontes

Todos os números de taxa vêm de bases do Banco Central do Brasil.

| Base | O que traz |
|---|---|
| Taxas de juros de operações de crédito por instituição financeira (médias dos últimos 5 dias) | Taxa média por instituição e modalidade, em % ao mês e % ao ano; é a fonte principal |
| Cadastro de instituições em funcionamento | Nome, conglomerado e CNPJ, usado para identificar a instituição pela raiz do CNPJ |
| SGS (Sistema Gerenciador de Séries Temporais) | Taxa média mensal do sistema financeiro, inadimplência da carteira e agregados nacionais, sempre em bloco separado |
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

## O que a fonte não informa

- O volume de operações de cada instituição: por isso não há média ponderada entre instituições.
- IOF, tarifas e seguros: a taxa publicada não equivale ao Custo Efetivo Total (CET) de uma oferta.
- A marca comercial: a fonte traz a entidade jurídica, e uma marca pode operar por mais de uma.
- A documentação do Banco Central não define o tomador do consignado privado, a esfera do tomador do consignado público, o que entra em "aquisição de outros bens" nem o que são as "taxas de mercado" e "taxas reguladas" do financiamento imobiliário. O site não afirma nada disso.
