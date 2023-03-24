# Gastos Abertos: Histórico resumido

1. Coleta dos dados pra análise

 https://github.com/okfn-brasil/gastos_abertos_dados

 * Coletado de diferentes fontes, vejam os arquivos 'source'.
 * Scripts pra limpeza dos dados e conversão dos dados:
     
   https://github.com/okfn-brasil/gastos_abertos_dados/tree/master/utils
     
 * Estudo dos dados do orçamento aprovado:
      
   http://nbviewer.ipython.org/github/okfn-brasil/gastos_abertos_dados/blob/master/notebooks/Aprovado%202014.ipynb

 * Análise comparando diferentes fontes dos dados de planejamento:
      
   http://nbviewer.ipython.org/github/okfn-brasil/gastos_abertos_dados/blob/master/notebooks/Comparando%20dados%20de%20planejamento.ipynb
      
 * Início do wiki para o projeto:
      
   http://pt.wikiversity.org/wiki/Gastos_Abertos
      
 * Início do glossário para o tema orçamento público:
      
   http://pt.wikiversity.org/wiki/Gastos_Abertos/Gloss%C3%A1rio

2. Telas e estrutura do site

* Mockup da página principal com acesso as diferentes areas planejadas para explorarmos

   http://app.mockflow.com/view/1ce113609b3260d0a412865e9d87bef9#/page/d5471361367b4641bab1f6129e595844

3. Página para visualizção dos dados da Receita

* Imagem desktop

  http://i.imgur.com/U4mNER2.png

* Imagem mobile

  http://i.imgur.com/IINIA3J.png

4. Trabalho realizado para análise dos dados da Receita

* Download dos dados via Selenium

  https://github.com/okfn-brasil/gastos_abertos_dados/blob/master/utils/revenue_downloader.py

* Limpeza dos dados

  https://github.com/okfn-brasil/gastos_abertos_dados/blob/master/utils/convert_xml.py

* Descobrimos que os dados exportados possuem linhas duplicadas e levamos um tempo para entender o porquê.

  https://github.com/okfn-brasil/gastos_abertos_dados/blob/master/utils/show_replications.py

Ao entender a razão, baixamos novamente os dados de forma a não obter tais duplicações:
    
  https://github.com/okfn-brasil/gastos_abertos_dados/tree/master/Orcamento/receitas

* Experimentos com gráficos estilo Treemap que foi um dos gráficos sugeridos pelos grupos no workshop:
    
   http://vaz.io/gastos_abertos/
    
Não gostamos muito dos resultados devido as grandes diferenças nos tipos, gerando retângulos ou muito grandes 
ou muito pequenos. Exploramos então uma outra forma de visualização:
    
   http://jsfiddle.net/upeqzrua/embedded/result/

Onde também é possível navegar nos diferentes níveis de um tipo de receita clicando em uma das barras.

* Implementação de uma API para os dados da receita:
    
  https://github.com/okfn-brasil/gastos_abertos

Essa api já encontra-se disponível para acesso aqui:
    
  http://demo.gastosabertos.org
    
E sua documentação está aqui:
    
  https://github.com/okfn-brasil/gastos_abertos/wiki/API

Utilizando essa API implementamos a página de acordo com o design:
    
   http://site.gastosabertos.org/receitas/
