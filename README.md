transporte-cargo-ai
===================


#### TODO
- Explicação extensa das 2 soluções;
- Uma explicação clara da modelagem de estados;
- As justificativas para as escolhas dos métodos de busca;

## Cenário
  
Necessidade de transportar containers pela plataforma de transporte do porto
em menor viagens possíveis para o navio cargueiro.

## Especificação do Problema

A plataforma de transporte possue restrições quanto ao peso máximo
transportado. Os containers variam em seus pesos.

Temos de buscar a melhor combinação entre os containers transportados por
uma determinada vez na plataforma, de forma que sempre sejam transportados
o maior número possível dos mesmos, garantindo um menor número de
viagens da plataforma e a segurança no transporte da mesma, isto é, não
podem ser ultrapassados a carga máxima especificados
pela plataforma de transporte.

Não há vantagem em transportar primeiro os containers mais leves,
deixando os mais pesados por último, pois no começo transportaremos o maior 
número possível de containers mas, no final, somente um pequeno número de
containers será transportado em função do excesso de peso.

## Implementação 

### Busca Não Informada

Consiste em fazer uma Busca em Largura em todas as possíveis combinações
dos grupos de containers. Achar a permutação que não viola a restrição de peso
máximo em cada grupo e tem o menor número de grupos de containers (plataformas).

### Busca Heurística

Usando algoritmo do Best First.

Ver vídeo para entender: https://www.youtube.com/watch?v=vUxhAmfXs2o

### Como rodar

Linguagem: **prolog**

Compilador: **swi-prolog**

Em ambiente GNU/Unix com swipl instalado, rode:

```
swipl -f busca_heuristica.pl
swipl -f busca_nao_informada.pl
```

