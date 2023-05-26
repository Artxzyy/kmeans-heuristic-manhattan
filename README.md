# kmeans-heuristic-manhattan

Essa é uma versão provisória do projeto sendo desenvolvido. Futuramente, a escrita do artigo deve ser revisada e complementada, além de possuir tradução para o inglês.

Em relação aos códigos, tudo é melhor explicado no artigo (mesmo que em versão provisória).

## code_part_1

Proposta de heurística customizada baseada no cálculo da Distância de Manhattan para o algoritmo K-Means, testes realizados em um contexto de problema real do Brasil, com comparação com resultados da implementação padrão do Scikit-learn, com os mesmos hiper parâmetros.

Utiliza os dados, especificamente os pontos (longitude, latitude) (x, y) das cidades do estado de Minas Gerais, disponíveis em https://github.com/kelvins/Municipios-Brasileiros, ou na cópia exisitente nesse repositório.

## code_part_2

Proposta de solução do problema de descarte de lixo não conforme com a lei 12.305/2010 (Política Nacional de Resíduos Sólidos, PNRS) para o estado de Minas Gerais. Utiliza-se, para isso, além dos pontos (longitude, latitude) disponíveis no link acima, o porte das cidades, sendo classificado como, Pequeno I, Pequeno II, Médio, Grande e Metrópole. Cada uma dessas classes para porte torna-se um peso que é usado como uma "terceira dimensão" para o cálculo dos centróides. Quanto maior o porte, maior o peso, sendo que, no momento, os pesos são, respectivamente: 50, 50, 300, 700, 2800. Com isso, os centróides gerados se concentram mais nas regiões com maior concentração populacional.

Além do mesmo dataset da parte anterior, há também a concatenação com os dados de população e porte de cada cidade, disponível em http://blog.mds.gov.br/redesuas/wp-content/uploads/2018/06/Lista_Munic%C3%ADpios_com_IBGE_Brasil_Versao_CSV.csv, ou na cópia existente nesse repositório.
