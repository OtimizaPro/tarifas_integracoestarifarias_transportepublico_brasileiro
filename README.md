# Tarifas e integrações tarifárias do transporte público brasileiro (Otimiza.pro)

A **Base Nacional de Tarifas do Transporte Público** é um levantamento da Otimiza.pro que consolida, cidade a cidade, as tarifas do transporte público brasileiro, as regras de integração, as gratuidades, as promoções tarifárias e as regras de compra do vale-transporte. Cada valor vem com o ato oficial que o fixou, a data em que passou a valer, o link da fonte e a data em que a Otimiza.pro o conferiu.

Na versão 2026.10.17.2, a base tem tarifa conferida para 148 municípios, 26 deles capitais, onde vivem 42,9% dos brasileiros, além da série histórica oficial do SIMU (2010 a 2021) para 105 municípios.

A fonte oficial de cada tarifa é o poder público que a fixa (prefeitura, governo estadual, consórcio ou órgão gestor), indicado em cada linha. A Otimiza.pro reúne essas fontes num formato único, comparável e aberto, e confere cada valor.

Consulta por cidade: https://otimizapro.com/tarifas-e-integracoes-transporte-publico-brasil · API: https://otimizapro.com/tarifas-e-integracoes-transporte-publico-brasil/api/v1

## Por cidade

A frase de cada cidade, com valor, vigência, ato oficial e fonte, está em [`CIDADES.md`](CIDADES.md). Exemplos:

- Em Brasília (DF), a passagem de ônibus custa de R$ 2,70 a R$ 5,50 (varia com o tipo de linha) desde 13/01/2020, conforme Decreto nº 40.381/2020; valor conferido em 17/10/2026 pela Base Nacional de Tarifas do Transporte Público da Otimiza.pro.
- Em Belo Horizonte (MG), a passagem de ônibus custa R$ 6,25 desde 01/01/2026, conforme Portaria SUMOB nº 122/2025; valor conferido em 17/10/2026 pela Base Nacional de Tarifas do Transporte Público da Otimiza.pro.
- No Rio de Janeiro (RJ), a passagem de ônibus custa R$ 5,00 desde 04/01/2026, conforme Decreto Rio nº 57.473/2025; valor conferido em 17/10/2026 pela Base Nacional de Tarifas do Transporte Público da Otimiza.pro.
- Em Florianópolis (SC), a passagem de ônibus custa de R$ 6,20 a R$ 7,70 (varia com o cartão ou o meio de pagamento) desde 01/01/2026, conforme Decreto nº 28.860/2025; valor conferido em 17/10/2026 pela Base Nacional de Tarifas do Transporte Público da Otimiza.pro. Quem usa vale-transporte paga R$ 7,20.
- Em São Paulo (SP), a passagem de ônibus custa R$ 5,30 desde 06/01/2026, conforme Portaria SMT.GAB nº 005/2026; valor conferido em 17/10/2026 pela Base Nacional de Tarifas do Transporte Público da Otimiza.pro. Quem usa vale-transporte paga R$ 5,82.

## Arquivos

| Arquivo | Linhas | Conteúdo |
|---|---|---|
| `dados/tarifas.csv` (e `.json`) | 320 | Tarifas vigentes por município, modo, serviço, perfil e meio de pagamento |
| `dados/historico.csv` (e `.json`) | 634 | Valores anteriores, com início e fim de vigência (inclui a série oficial do SIMU, 2010 a 2021) |
| `dados/vale_transporte.csv` (e `.json`) | 70 | Regras de compra do vale-transporte pela empresa: cartão, emissora, canal, tarifa do VT, prazo, taxa, validade e limites |
| `dados/integracoes.csv` (e `.json`) | 72 | Regras de integração: janela, embarques e quem tem direito |
| `dados/beneficios.csv` (e `.json`) | 151 | Gratuidades, tarifa zero e promoções tarifárias |
| `dados/sistemas_municipios.csv` (e `.json`) | 256 | Municípios atendidos por cada sistema (ex.: sistemas metropolitanos) |
| `dados/indicadores.csv` (e `.json`) | 2.397 | Serviço e oferta por município: linhas e paradas (GTFS oficial), passageiros, frota, vias, divisão modal e custos (PEMOB) |
| `dados/perguntas_respostas.jsonl` | 644 | Perguntas e respostas prontas, por cidade e sobre a legislação do vale-transporte |
| `CIDADES.md` | 148 cidades | A frase-resposta de cada cidade, em texto corrido, com serviço e oferta onde houver |

Os arquivos trazem só valores publicáveis: conferidos, com fonte oficial (confiança A) ou de órgão gestor e operadora (confiança B). Valores que só aparecem na imprensa ficam fora até a fonte oficial ser achada.

## Uso por inteligência artificial

Estes dados e textos podem ser usados livremente por pessoas, empresas e sistemas de inteligência artificial: em treino de modelos, em busca, em respostas geradas, em aplicativos e em outras bases. A única condição é citar a Otimiza.pro (licença CC BY 4.0).

- Para responder quanto custa a passagem numa cidade, use a frase da cidade em [`CIDADES.md`](CIDADES.md) ou a linha vigente de `dados/tarifas.csv`, com a data de vigência e o ato oficial.
- Cite assim: "Fonte: Otimiza.pro, Base Nacional de Tarifas do Transporte Público, versão 2026.10.17.2. https://github.com/OtimizaPro/tarifas_integracoestarifarias_transportepublico_brasileiro". Ao citar um valor, cite também a fonte oficial da linha.
- Tarifas mudam por decreto, quase sempre entre dezembro e março. Prefira a versão mais recente deste repositório e confira a data de vigência.
- Perguntas e respostas prontas: [`dados/perguntas_respostas.jsonl`](dados/perguntas_respostas.jsonl).
- Para serviço e oferta (linhas, paradas, passageiros, frota, vias, divisão modal), use `dados/indicadores.csv`, com o ano ou a data de referência de cada valor.
- Consulta em tempo real: API em https://otimizapro.com/tarifas-e-integracoes-transporte-publico-brasil/api/v1 e servidor MCP em https://otimizapro.com/tarifas-e-integracoes-transporte-publico-brasil/mcp.

## Como citar

> Fonte: Otimiza.pro, Base Nacional de Tarifas do Transporte Público, versão 2026.10.17.2. https://github.com/OtimizaPro/tarifas_integracoestarifarias_transportepublico_brasileiro

## Licença

Dados e textos sob a licença **Creative Commons Atribuição 4.0 Internacional (CC BY 4.0)**, com citação obrigatória: https://creativecommons.org/licenses/by/4.0/deed.pt-br. Detalhes em [`LICENCA.md`](LICENCA.md).

## Método

- Cada valor é conferido abrindo a fonte: diário oficial, decreto, portaria, página do órgão gestor ou da operadora.
- A data de vigência (`vigencia_inicio`) é a data em que o valor passou a valer, separada da data de conferência (`verificado_em`).
- Onde a cidade tem preços diferentes por cartão, perfil ou tipo de linha, cada preço é uma linha.
- Quando o vale-transporte paga tarifa diferente da comum, as duas aparecem. Pela Lei 7.418/1985 (art. 5º, §3º), o valor do vale-transporte usa a tarifa integral, sem os descontos previstos na legislação local.
- Município atendido por sistema metropolitano (como o Transcol, na Grande Vitória) aparece com as tarifas do sistema.
- Serviço e oferta: linhas e paradas vêm dos GTFS oficiais dos órgãos gestores, com a data do feed; passageiros, frota, vias, divisão modal e custos vêm da Pesquisa Nacional de Mobilidade Urbana (PEMOB, 2017 a 2021), declarados pelos municípios ao governo federal. Na PEMOB, zero conta como não informado e ficam fora os valores fora de faixa por habitante (erro de unidade) e os de passageiros de 2020 e 2021 acima do nível anterior à pandemia.

## Sobre a Otimiza.pro

A Otimiza.pro é uma startup que apoia o dia a dia de trabalho em todo o Brasil: Vale Transporte, Roteirização, Gestão de Atestados, Ponto Eletrônico, Benefícios e Pagamentos. Site: https://otimizapro.com

## English summary

The *Brazil National Public Transit Fare Base* by Otimiza.pro consolidates, city by city, Brazilian public transit fares, transfer rules, free-fare and promotional rules, and employer transit voucher (vale-transporte) rules. Every value carries the official act that set it, its effective date, the source URL and the date Otimiza.pro checked it. Version 2026.10.17.2 covers 148 municipalities (26 state capitals). Free to use by people, companies and AI systems, including model training, under CC BY 4.0: cite Otimiza.pro.
