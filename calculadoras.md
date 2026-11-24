# Regras e ferramentas

## Regras que valem no site

- Nenhum número sem período e fonte.
- Ausência é declarada: "sem dado no período", nunca zero. Taxa igual a zero na fonte não entra em mediana, quartil, mínimo ou máximo.
- Sem "melhor/pior", nota, selo ou recomendação de instituição. O ranking de juros só repete a ordem publicada pelo Banco Central, da menor para a maior taxa, com a lista completa e a mediana ao lado.
- Dado parcial nunca sobrescreve dado bom: a publicação é recusada se uma modalidade ficar sem dados, uma tabela ficar vazia ou o período recuar.
- Diferença entre instituições é descrita como fato, em pontos percentuais, sem atribuir causa.
- A taxa publicada nunca é comparada ao CET nem a teto de juros.

## Cálculos financeiros

Funções puras, sem IA, validadas pelos mesmos vetores de teste nas três implementações (Python, JavaScript e PHP).

- Juros compostos com capitalização mensal; conversão `anual = ((1 + mensal/100)^12 − 1) × 100`.
- Dívida que cresce sem pagamento: `M = P·(1+i)^n`.
- Parcelas (Price): `PMT = P·i / (1 − (1+i)^−n)`; também SAC, taxa implícita, prazo de quitação e valor presente.
- Premissa explícita em toda ferramenta: sem IOF, tarifas, seguros nem atrasos, salvo quando a pessoa os informa.

## Ferramentas

- **Custo do crédito**: quanto uma dívida cresce ou custa em parcelas a determinada taxa.
- **Compare a sua taxa**: a taxa da proposta contra a mediana da modalidade e, se a pessoa escolher, a referência da instituição. CET ou "não sei" não compara.
- **Troca de dívida**: mesmo saldo e prazo, taxa atual contra taxa nova, com custos somados ao saldo e taxa de equilíbrio.
- **Comparar instituições**: 2 ou 3 marcas, nas modalidades em que todas têm dado, sem vencedor.
- **Explorar o histórico**: até 4 séries mensais sobrepostas desde 2012, com tabela e "como citar".
- **Margem do consignado**: a pessoa informa a própria margem; o site não afirma a esfera do tomador nem aplica percentual legal ao consignado público e ao privado. No INSS usa a margem de 35% (Lei 10.820/2003, art. 6º, § 5º).
- **Raio-x do pedido de crédito**: lê o pedido por sinais de regra fixa, sem nota e sem chance de aprovação.
- **Simulador de financiamento imobiliário**: a conta em reais usa só os números da proposta (taxa ao ano efetiva ou nominal, TR suposta pela pessoa e mantida constante, seguros MIP e DFI e tarifa), em SAC e Price. A cada mês o saldo é corrigido pela TR antes dos juros; no SAC a amortização é o saldo corrigido dividido pelos meses restantes, na Price a parcela é recalculada sobre o saldo corrigido. A mediana das modalidades em TR aparece à parte e não entra na conta, porque o Banco Central não informa se a taxa publicada dessas modalidades inclui a TR. O total não é chamado de CET.

## Gráficos de posição e de contexto

- **Instituição contra a mediana, até 10 anos**: na página de cada instituição por modalidade, a linha da referência da entidade e a da mediana das instituições com dado em cada mês, nos últimos 120 meses (a história inteira se for menor). Cada mês em que a referência ficou acima da mediana ganha uma faixa de fundo (tom âmbar) e cada mês abaixo, outra (azul); diferença menor que 0,05% da mediana conta como igual e não ganha faixa. Abaixo do gráfico, a contagem de meses acima, abaixo e iguais na mesma janela, só com 12 meses ou mais. Mês sem dado da entidade quebra a linha e nunca vira zero. É descrição de posição ao longo do tempo: não indica causa, tendência nem "melhor/pior".
- **Juros e inadimplência no mesmo período**: nas modalidades de pessoa física de cinco dias úteis que têm série de inadimplência da carteira (SGS), dois gráficos empilhados com o mesmo eixo de tempo: em cima a mediana das instituições (% ao mês), embaixo a inadimplência (% da carteira). Cada um tem a própria escala vertical, porque medem coisas diferentes; as linhas nunca se sobrepõem. O período é o da série de inadimplência, e mês sem dado quebra a linha. Os gráficos não servem para comparar instituições nem afirmam causa entre as duas medidas.

As ferramentas orientam. Não confirmam o que consta do seu contrato.
