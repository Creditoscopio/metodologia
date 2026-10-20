# Regras e ferramentas

## Regras que valem no site

- Nenhum número sem período e fonte.
- Ausência é declarada: "sem dado no período", nunca zero. Taxa igual a zero na fonte não entra em mediana, quartil, mínimo ou máximo.
- Sem ranking de "melhores", sem "melhor/pior" e sem recomendação de instituição.
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

As ferramentas orientam. Não confirmam o que consta do seu contrato.
