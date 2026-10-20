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
3. **Estatística**: mediana das instituições com dado no período, quartis (P25 e P75), mínimo, máximo e a quantidade de instituições (n). Quartis e posição só aparecem com n de pelo menos 10.
4. **Marca e entidade**: a fonte traz a entidade jurídica; uma página de marca só existe quando a ligação entre a marca e a entidade foi confirmada.
5. **Atualização** a cada novo período publicado pelo Banco Central; o período aparece em cada página.

## Como citar

> Creditoscópio. *Título da página*. Dados: Banco Central do Brasil, período. https://creditoscopio.com.br/… Acesso em AAAA-MM-DD.

Cite sempre o período do número.

## Correções

Encontrou um erro? contato@creditoscopio.com.br, com o link da página e o que viu na fonte.
