
# Jogador Automático de Forca

Este projeto implementa um jogador automático para o jogo de forca. O objetivo é maximizar o número de vitórias do jogador, que dispõe de apenas 5 vidas para adivinhar uma palavra secreta. A estratégia principal deste jogador automático é baseada em conceitos de **teoria da informação** e **álgebra linear**, explorando a entropia das palavras e a probabilidade de ocorrência das letras para maximizar as chances de sucesso em cada jogo.

## Descrição Geral

O jogo de forca é uma atividade clássica onde um jogador tenta adivinhar uma palavra secreta escolhendo letras. Cada escolha correta revela as posições das letras na palavra; escolhas incorretas resultam em perda de vidas. O jogador vence ao adivinhar a palavra completa ou perde ao esgotar todas as suas vidas. Nesta implementação, um objeto `JogoDeForca` é instanciado com uma lista de palavras sem acentos em português.

## Abordagem do Projeto

A estratégia do jogador automático baseia-se em **teoria da informação**, em que a entropia é utilizada para calcular a probabilidade de uma letra estar presente em uma palavra de um dado comprimento. A ideia é escolher letras que maximizem a **redução de incerteza** (ou seja, revelem mais informações sobre a palavra) com cada tentativa. Essa abordagem ajuda a selecionar letras que são mais informativas, aumentando as chances de adivinhar a palavra com menos tentativas.

A implementação utiliza **álgebra linear** para representar e manipular as frequências e probabilidades das letras em cada posição. Essa estrutura permite:
1. **Análise das letras mais prováveis**: calcular a entropia para cada letra e selecionar aquela que reduzirá mais a incerteza.
2. **Atualização dinâmica do vocabulário**: o conjunto de palavras possíveis é reduzido a cada tentativa, refinando a previsão com base nos acertos e erros.

## Estrutura do Projeto

1. **Arquivo `demo.ipynb`**: Um notebook Jupyter que executa os testes para avaliar o desempenho do jogador automático. Este notebook está totalmente comentado e explica, passo a passo, cada parte do código e a importância dos conceitos aplicados.
2. **README.md**: Explica a abordagem adotada, descreve como a entropia e álgebra linear foram aplicadas e resume os resultados obtidos.
3. **Código Principal**: A classe `JogoDeForca` e a lógica do jogador automático, implementados diretamente no notebook.

## Conceitos Teóricos Utilizados

### Teoria da Informação
A entropia, medida da incerteza, é usada para calcular a probabilidade de uma letra aparecer em uma palavra de um determinado comprimento, dada a lista de palavras. Esse cálculo permite ao jogador automático focar em letras que potencialmente revelam mais da palavra secreta, maximizando a eficiência das tentativas.

### Álgebra Linear
Vetores são utilizados para representar as probabilidades de cada letra em cada posição da palavra. Essa estrutura permite operações matemáticas eficientes para atualizar as probabilidades a cada tentativa e reduzir o conjunto de palavras possíveis.

## Resultados

O desempenho do jogador automático foi avaliado em 100 jogos diferentes. O notebook `demo.ipynb` inclui um relatório da probabilidade de vitória do jogador com base nas 100 tentativas e analisa os casos em que o jogador falhou, oferecendo insights sobre os desafios enfrentados.

## Execução do Projeto

Para reproduzir os resultados:

1. Clone este repositório.
2. Instale os requisitos necessários (caso haja dependências).
3. Abra o notebook `demo.ipynb` e visualize os resultados já gerados.

Para mais informações, consulte o notebook comentado e o código no repositório.