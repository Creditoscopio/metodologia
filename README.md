# Metodologia do Creditoscópio

Como o [Creditoscópio](https://creditoscopio.com.br/) obtém e calcula os números que mostra sobre as taxas de juros do crédito para pessoas físicas no Brasil. A versão de referência, navegável, é a página [creditoscopio.com.br/metodologia](https://creditoscopio.com.br/metodologia/). Este repositório guarda o texto em formato versionado, para quem precisa citar ou conferir uma versão específica.

Licença do texto: CC BY 4.0. Os dados de origem seguem os termos de cada portal e não são redistribuídos aqui.

## Conteúdo

- [fontes.md](fontes.md): as bases do Banco Central usadas e as modalidades publicadas
- [glossario-colunas.md](glossario-colunas.md): o que cada número do site significa
- [calculadoras.md](calculadoras.md): regras gerais e premissas das ferramentas
- [CHANGELOG.md](CHANGELOG.md): mudanças de método, com data

## Como o número é produzido, em resumo

1. **Coleta** das taxas por instituição publicadas pelo Banco Central, três vezes por semana, guardando a resposta bruta de cada coleta.
2. **Recorte**: só pessoas físicas, só taxas maiores que zero, uma entidade por raiz de CNPJ e sempre a mesma janela para todas as instituições.
3. **Estatística**: mediana das instituições com dado no período, quartis (P25 e P75), mínimo, máximo e a quantidade de instituições (n). Quartis e posição só aparecem com n de pelo menos 10. Esse corte é uma regra de publicação, para não descrever uma distribuição com poucos pontos; não é intervalo de confiança nem teste estatístico, e o site não calcula margem de erro para esses números.
4. **Marca e entidade**: a fonte traz a entidade jurídica; uma página de marca só existe quando a ligação entre a marca e a entidade foi confirmada.
5. **Atualização** a cada novo período publicado pelo Banco Central; o período aparece em cada página.

## O que é do Banco Central e o que é do Creditoscópio

- **Dado oficial do Banco Central, sem alteração:** a taxa média de cada instituição em cada modalidade e período (% ao mês e % ao ano), o nome e o código da modalidade, o nome e a raiz do CNPJ da entidade; as séries do SGS (taxa média do mercado, inadimplência e endividamento); o índice de reclamações.
- **Cálculo do Creditoscópio a partir desse dado:** mediana, quartis, posição entre as instituições, diferença para a mediana, mediana por tipo de instituição, a série mensal (uma janela por mês), as atualizações mensais e as contas das ferramentas.
- **Organização do Creditoscópio:** a marca comercial ligada a cada entidade, o tipo de instituição e os pares de comparação. Não são classificações do Banco Central.

## Como citar

> Creditoscópio. *Título da página*. Dados: Banco Central do Brasil, período. https://creditoscopio.com.br/… Acesso em AAAA-MM-DD.

Cite sempre o período do número.

## Correções

Encontrou um erro? contato@creditoscopio.com.br, com o link da página e o que viu na fonte.
