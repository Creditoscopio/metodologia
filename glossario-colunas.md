# Indicadores

Cada número é da **instituição (entidade da fonte)** ou da **modalidade**, nunca de uma oferta ou de um contrato.

- **Taxa publicada**: média das taxas das operações que a instituição contratou na janela, ponderada pelo valor contratado, em % ao mês e % ao ano compostos. Segundo a documentação do Banco Central, é o custo efetivo médio, com os juros acrescidos de "encargos fiscais e operacionais" sem detalhar quais. Não é a taxa que a instituição cobra de todos os clientes, não é a oferta que você receberia e não é o CET.
- **Janela**: cinco dias úteis (no financiamento imobiliário, o mês). Janelas consecutivas se sobrepõem, então os pontos do histórico usam uma janela por mês, a primeira.
- **Mediana das instituições com dados disponíveis no período**: mediana das taxas mensais das instituições com dado na janela. Cada instituição pesa 1, grande ou pequena. Não é "média do mercado".
- **n**: quantas instituições entraram no cálculo. O conjunto muda de um período para outro.
- **P25 e P75**: quartis, por interpolação linear entre os valores ordenados.
- **Posição**: "acima de X% das instituições" é a proporção de instituições com taxa menor, contando empates pela metade. É uma posição na distribuição, não uma nota.
- **Posição no ranking de juros**: a ordem da instituição na lista da modalidade, da menor para a maior taxa mensal, entre as instituições com taxa maior que zero no período; empate na taxa publicada divide a posição (1, 2, 2, 4) e, abaixo das duas casas, vale a ordem do Banco Central. É a mesma ordem que o Banco Central publica, salvo nas raras janelas em que a ordem da fonte não segue a taxa publicada: aí vale a taxa. Uma lista por modalidade com janela de cinco dias úteis e pelo menos 10 instituições, num ranking para pessoa física e noutro, separado, para empresas; não junta modalidades nem pessoa física com empresas.
- **Diferença para a mediana**: (taxa da instituição − mediana) ÷ mediana. Abaixo de 0,05% da mediana aparece como "igual à mediana".
- **Referência oficial do mercado (SGS)**: taxa média mensal das novas operações de crédito livre do sistema financeiro inteiro, ponderada pelo valor das concessões. Medida diferente da mediana, sempre em gráfico separado, nunca usada para posicionar instituição.
- **Inadimplência (SGS)**: percentual da carteira de crédito livre com parcela em atraso há mais de 90 dias. Não é taxa de juros nem medida de instituição.
- **Índice de reclamações**: (reclamações reguladas procedentes × 1.000.000) ÷ clientes, do ranking trimestral do Banco Central. Desde o 2º trimestre de 2024 as procedentes são estimativa por amostragem; só esses trimestres são exibidos.
- **Entidade, marca e tipo**: a entidade é a pessoa jurídica da fonte (raiz do CNPJ); a marca agrupa o nome que o consumidor conhece e só ganha página quando a ligação com a entidade foi confirmada; o tipo (bancos públicos, grandes bancos privados, bancos digitais e fintechs, bancos de montadoras, bancos médios e de investimento, financeiras e crédito do varejo) é classificação editorial do Creditoscópio, não do Banco Central.

Instituições diferentes têm carteiras diferentes (perfil de cliente, prazo, garantia). Uma taxa maior ou menor não indica, por si só, que uma instituição seja melhor ou pior.
