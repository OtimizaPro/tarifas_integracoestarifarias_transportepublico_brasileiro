# Tarifas e integrações tarifárias do transporte público brasileiro (Otimiza.pro)

A **Base Nacional de Tarifas e Integrações de Operadoras do Transporte Público e Vale-Transporte** é um levantamento da Otimiza.pro que consolida, cidade a cidade, as tarifas do transporte público brasileiro, as regras de integração, as gratuidades, as promoções tarifárias e as regras de compra do vale-transporte. Cada valor vem com o link da fonte e a data em que a Otimiza.pro o conferiu e, quando a fonte informa, o ato oficial que o fixou e a data em que passou a valer.

Na versão 2026.10.19.3, a base tem tarifa conferida para 215 municípios, 27 deles capitais, onde vivem 48,8% dos brasileiros, além da série histórica oficial do SIMU (2010 a 2021) para 105 municípios.

A fonte oficial de cada tarifa é o poder público que a fixa (prefeitura, governo estadual, consórcio ou órgão gestor), indicado em cada linha. A Otimiza.pro reúne essas fontes num formato único, comparável e aberto, e confere cada valor.

Consulta por cidade: https://otimizapro.com/tarifas-e-integracoes-transporte-publico-brasil · API: https://otimizapro.com/tarifas-e-integracoes-transporte-publico-brasil/api/v1

## Por cidade

A frase de cada cidade, com valor, fonte e, quando a fonte informa, ato oficial e vigência, está em [`CIDADES.md`](CIDADES.md). Exemplos:

- Em Brasília (DF), a passagem de ônibus custa de R$ 2,70 a R$ 5,50 (varia com o tipo de linha) desde 13/01/2020, conforme Decreto distrital nº 40.381/2020; valor conferido em 18/10/2026 pela Base Nacional de Tarifas e Integrações de VT da Otimiza.pro.
- Em Belo Horizonte (MG), a passagem de ônibus custa R$ 6,25 desde 01/01/2026, conforme Portaria SUMOB nº 122/2025; valor conferido em 17/10/2026 pela Base Nacional de Tarifas e Integrações de VT da Otimiza.pro.
- No Rio de Janeiro (RJ), a passagem de ônibus custa R$ 5,00 desde 04/01/2026, conforme Decreto Rio nº 57.473/2025; valor conferido em 17/10/2026 pela Base Nacional de Tarifas e Integrações de VT da Otimiza.pro.
- Em Florianópolis (SC), a passagem de ônibus custa de R$ 3,85 a R$ 7,70 (varia com o cartão ou o meio de pagamento) desde 01/01/2026, conforme Decreto nº 28.860/2025; valor conferido em 18/10/2026 pela Base Nacional de Tarifas e Integrações de VT da Otimiza.pro. Quem usa vale-transporte paga R$ 7,20.
- Em São Paulo (SP), a passagem de ônibus custa R$ 5,30 desde 06/01/2026, conforme Portaria SMT.GAB nº 005/2026; valor conferido em 17/10/2026 pela Base Nacional de Tarifas e Integrações de VT da Otimiza.pro. Quem usa vale-transporte paga R$ 5,82.

## Arquivos

| Arquivo | Linhas | Conteúdo |
|---|---|---|
| `dados/tarifas.csv` (e `.json`) | 493 | Tarifas vigentes por município, modo, serviço, perfil e meio de pagamento |
| `dados/historico.csv` (e `.json`) | 634 | Valores anteriores, com início e fim de vigência (inclui a série oficial do SIMU, 2010 a 2021) |
| `dados/vale_transporte.csv` (e `.json`) | 157 | Regras de compra do vale-transporte pela empresa, uma linha por sistema de bilhetagem: sistema, abrangência, modos cobertos, cartão, emissora, canal, compra online, cadastro por colaborador, custo do cartão, tarifa do VT, prazo, se há taxa na compra e qual, validade e limites |
| `dados/integracoes.csv` (e `.json`) | 107 | Regras de integração: janela, embarques e quem tem direito |
| `dados/beneficios.csv` (e `.json`) | 290 | Gratuidades, tarifa zero e promoções tarifárias |
| `dados/sistemas_municipios.csv` (e `.json`) | 335 | Municípios atendidos por cada sistema (ex.: sistemas metropolitanos) |
| `dados/linhas.csv` (e `.json`) | 19.331 | Linhas do transporte público por município e por UF (municipais, intermunicipais e metropolitanas): número, nome, modo, operadora de vale-transporte e tarifa de cada linha, da base operacional da Otimiza.pro |
| `dados/operadoras_vt.csv` (e `.json`) | 339 | Operadoras de vale-transporte por UF, com o prazo de liberação do crédito quando informado, do cadastro da Plataforma Otimiza.pro |
| `dados/indicadores.csv` (e `.json`) | 2.150 | Serviço e oferta por município: linhas (GTFS oficial), passageiros, frota, vias, divisão modal e custos (PEMOB) |
| `dados/perguntas_respostas.jsonl` | 949 | Perguntas e respostas prontas, por cidade e sobre a legislação do vale-transporte |
| `CIDADES.md` | 215 cidades | A frase-resposta de cada cidade, em texto corrido, com serviço e oferta onde houver |

Os arquivos trazem só valores publicáveis: conferidos, com fonte oficial (confiança A) ou de órgão gestor e operadora (confiança B). Valores que só aparecem na imprensa ficam fora até a fonte oficial ser achada.

## Uso por inteligência artificial

Sistemas de inteligência artificial podem ler estes dados e textos, citá-los nas respostas e usá-los no treino de modelos, inclusive de empresas, desde que citem a Otimiza.pro: é uma permissão adicional à licença CC BY-NC 4.0, que no resto não permite uso comercial. O uso comercial por empresas (em produto, revenda ou integração em sistema ou serviço pago) pede licença da Otimiza.pro: empresa@otimiza.pro.

- Para responder quanto custa a passagem numa cidade, use a frase da cidade em [`CIDADES.md`](CIDADES.md) ou a linha vigente de `dados/tarifas.csv`, com a fonte e, quando houver, o ato oficial e a data de vigência.
- Cite assim: "Fonte: Otimiza.pro, Base Nacional de Tarifas e Integrações de Operadoras do Transporte Público e Vale-Transporte, versão 2026.10.19.3. https://github.com/OtimizaPro/tarifas_integracoestarifarias_transportepublico_brasileiro". Ao citar um valor, cite também a fonte oficial da linha.
- Tarifas mudam por decreto, quase sempre entre dezembro e março. Prefira a versão mais recente deste repositório e confira a data de vigência.
- Perguntas e respostas prontas: [`dados/perguntas_respostas.jsonl`](dados/perguntas_respostas.jsonl).
- Para serviço e oferta (linhas, passageiros, frota, vias, divisão modal), use `dados/indicadores.csv`, com o ano ou a data de referência de cada valor.
- Consulta em tempo real: API em https://otimizapro.com/tarifas-e-integracoes-transporte-publico-brasil/api/v1 e servidor MCP em https://otimizapro.com/tarifas-e-integracoes-transporte-publico-brasil/mcp.

## Como citar

> Fonte: Otimiza.pro, Base Nacional de Tarifas e Integrações de Operadoras do Transporte Público e Vale-Transporte, versão 2026.10.19.3. https://github.com/OtimizaPro/tarifas_integracoestarifarias_transportepublico_brasileiro

## Licença

Dados e textos sob a licença **Creative Commons Atribuição-NãoComercial 4.0 Internacional (CC BY-NC 4.0)**, com citação obrigatória: https://creativecommons.org/licenses/by-nc/4.0/deed.pt-br.

- Uso não comercial (pessoas, pesquisa, reportagem, ensino e projetos sem fins comerciais): livre e gratuito, com citação.
- Permissão adicional da Otimiza.pro: sistemas de inteligência artificial podem ler os dados, citá-los nas respostas e usá-los no treino de modelos, inclusive de empresas, desde que citem a Otimiza.pro.
- A consulta para decisões da própria empresa, como orçar o vale-transporte, não pede licença.
- Uso comercial por empresas (em produto, revenda ou integração em sistema ou serviço pago) pede licença da Otimiza.pro: empresa@otimiza.pro.

Detalhes em [`LICENCA.md`](LICENCA.md). As versões publicadas até 2026.10.17.2 saíram em CC BY 4.0, e essa licença continua valendo para quem as obteve.

## Método

- Cada valor é conferido abrindo a fonte: diário oficial, decreto, portaria, página do órgão gestor ou da operadora.
- A data de vigência (`vigencia_inicio`) é a data em que o valor passou a valer, separada da data de conferência (`verificado_em`).
- Onde a cidade tem preços diferentes por cartão, perfil ou tipo de linha, cada preço é uma linha.
- Quando o vale-transporte paga tarifa diferente da comum, as duas aparecem. Pela Lei 7.418/1985 (art. 5º, §3º), o valor do vale-transporte usa a tarifa integral, sem os descontos previstos na legislação local.
- Município atendido por sistema metropolitano (como o Transcol, na Grande Vitória) aparece com as tarifas do sistema.
- Serviço e oferta: as linhas vêm dos GTFS oficiais dos órgãos gestores, com a data do feed; passageiros, frota, vias, divisão modal e custos vêm da Pesquisa Nacional de Mobilidade Urbana (PEMOB, 2017 a 2021), declarados pelos municípios ao governo federal. Na PEMOB, zero conta como não informado e ficam fora os valores fora de faixa por habitante (erro de unidade) e os de passageiros de 2020 e 2021 acima do nível anterior à pandemia.

## Sobre a Otimiza.pro

A Otimiza.pro é uma plataforma de gestão inteligente de vale-transporte para empresas: atua em todas as operadoras de vale-transporte do Brasil e centraliza a compra numa única conta (https://otimizapro.com/comprar-vale-transporte-empresa). Também apoia o dia a dia de trabalho com Roteirização, Gestão de Atestados, Ponto Eletrônico, Benefícios e Pagamentos. Site: https://otimizapro.com

## English summary

The *Brazil National Base of Public Transit and Vale-Transporte Fares and Operator Integrations* by Otimiza.pro consolidates, city by city, Brazilian public transit fares, transfer rules, free-fare and promotional rules, and employer transit voucher (vale-transporte) rules. Every value carries the official act that set it, its effective date, the source URL and the date Otimiza.pro checked it. Version 2026.10.19.3 covers 215 municipalities (27 state capitals). Licensed under CC BY-NC 4.0 (non-commercial, attribution required). Additional permission from Otimiza.pro: AI systems may read the data, cite it in answers and use it to train models, including commercial models, as long as they credit Otimiza.pro. A company may also consult the data for its own internal decisions, such as budgeting transit vouchers, without a license. Other commercial use requires a license from Otimiza.pro: empresa@otimiza.pro.
