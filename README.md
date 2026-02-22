# Análise da um quarto de suspensão de um carro

Parte da análise de confortabilidade de um veículo se passa por analisar o quão estável o veículo é quando passa por terrenos sinuosos. Para isso, deve-se analisar o sistema de suspensão e seus componentes para que o carro obtenha a maior estabilidade possível.

<img width="185" height="331" alt="QUARTO-DE-CARRO-PADRÃO" src="https://github.com/user-attachments/assets/99348af4-6f26-4188-810f-7ebd50e0728c" /> 

Exemplificação do sistema de suspenção abstraido, contendo:
- Massa suspensa [Ms](Chassi do carro)
- Massa não suspensa [Mu](Massa do sistema de suspensão)
- Mola da suspensão [ks]
- Mola da roda[kt](Mola referente a elasticidade das rodas)
- Amortecedor do sistema de suspensão[cs]

## Objetivo

Partindo de um modelo já estudado e testado no MATLAB, tentar aplicador um novo modelo desse sistema em JAVA, usando a biblioteca gráfica JavaFX para obter os gráficos.

## Tecnologias Utilizadas

- Linguagem: **Java, MATLAB**
- Biblioteca: **JavaFX**

## Conceitos aplicados

Programação
- Programação orientada a objetos
- UML
Engenharia
- Modelo de um quarto de carro
- Modelo massa-mola-amortecedor
- Conforto veicular
Matemática
- Equações diferenciais de 2 ordem
- Matriz de espaço de estados
- Equações de Runge-Kutta

## Como foi feito

<img width="990" height="620" alt="UML1 2" src="https://github.com/user-attachments/assets/c043504a-dc4e-4549-b41d-6901200f49db" />

Criou-se um UML básico, para ter uma base para quais seriam as classes usadas no programa. A partir daí, foram criadas as classes principais, e os atributos de cada uma dessas classes. A maioria das classes tem algum tipo de relação com o sistema de suspensão, no qual serão feitos todos os cálculos do programa.
Em termos de cálculo, a análise de um sistema dinâmico feita no MATLAB é mais fácil, já que existem funções próprias para analisar um sistema dinâmico que não existem no Java. Dessa forma, todo cálculo feito em Java foi desenvolvido do zero, criando a matriz de 2 ordem do sistema de suspensão (0 ordem - Deslocamento | 1 ordem - Velocidade | 2 ordem - Aceleração[Todas variaveis referentes a massa suspensa]) e aplicando as condições de contorno do problema.

## Como usar

O programa possui uma interface básica na qual o usuario digita os valores referentes ao sistema de suspensão

<img width="337" height="228" alt="image" src="https://github.com/user-attachments/assets/cc864453-b0b5-4461-b893-435569c69371" />

Depois disso, o programa se inicia gerando gráficos do deslocamento da massa suspensa, deslocamento da massa não suspensa e aceleração da massa suspensa em função do tempo. A partir daí, é necessário fazer uma análise dos gráficos para ter uma boa noção dos resultados. Abaixo estão alguns exemplos criados com dados de carros de verdade, em laranja estão os gráficos gerados em Java, em azul estão os gráficos gerados pelo MATLAB (apenas para comparação dos resultados).

<img width="600" height="285" alt="image" src="https://github.com/user-attachments/assets/a0c8749e-2caa-421e-bd4a-39d37d151934" />

<img width="600" height="285" alt="image" src="https://github.com/user-attachments/assets/c9001b8e-39eb-4ee0-a67c-acea21c4128b" />

<img width="600" height="285" alt="image" src="https://github.com/user-attachments/assets/4ce5d75d-b61d-417d-b5b5-36432cd5c346" />

<img width="600" height="285" alt="image" src="https://github.com/user-attachments/assets/e74c0a10-67b8-41cd-be37-01a7f0ab80bf" />

<img width="600" height="285" alt="image" src="https://github.com/user-attachments/assets/f759c850-3d53-4e8d-ac67-b7efbf0d32dc" />
