# Giga de teste de forno
## Objetivo
Criar giga de teste capaz de simular condições dentro dos fornos para aperfeiçoar o processo de secagem das peças.

## 1 - Partes do produto

### 1.1 - Estrutura
   Feita para conter todas as demais partes. 
   
   A estrutura deverá ser a de um forno em miniatura.
   
### 1.2 - Balança
   Feita para pesar a peça durante a secagem. 
   
   Conforme a peça se torna mais leve sabemos quanta água evaporou e em quanto tempo.
   
### 1.3 - Mesa
   Parte onde a peça que deve ser secada deve ser colocada. 
   
   A mesa deve se apoiar sobre a balança pra permitir a pesagem da peça.
   
### 1.4 - Contra-peso
   Para calibrar a balança, reduz (elimina) o peso da mesa.
   
### 1.5 - Aquecedores
   Os mesmos elementos aquecedores usados no forno da empresa.
   
### 1.6 - Carros
   Onde os aquecedores são presos. 
   
   Permitem aumentar ou diminuir a distancia entre os aquecedores e a mesa.
   
### 1.7 - Sistema de ar
   Para permitir ventilar o interior da giga e simular as condições de ventilação do forno.
   
### 1.8 - Controlador
   Sistema que permite controlar todos os elementos e fazer medidas (temperatura, umidade, etc). 
   
   Todos os sensores necessários fazem parte da controladora.
   
   A controladora é um computador, e a giga será operada via IoT (Internet of Things, Internet das Coisas).

## Descrição das partes

### 2.1 - Estrutura
   Deve ser uma caixa capaz de suportar a temperatura do forno (135oC) e capaz de dar suporte para as demais peças.
   
   Atualmente é uma estrutura de folha de aço retirada de uma geladeira, isolada termicamente.

### 2.2 - Balança
   É de um pequeno sensor de deformação mecanica capaz de pesar até 1 quilograma.
   
   A balança não suporta a temperatura de 135oC, entao deve ser colocada numa área isolada termicamente dentro da estrutura.
   
<img src="https://images-na.ssl-images-amazon.com/images/I/719H3CSVRwL._AC_SL1500_.jpg" width=400 />

### 2.3 - Mesa
   Ainda deve ser projetada. Ela deve:

  * apoiar a peça a ser seca
  * permitir a passagem de ar
  * ser apoiada no sensor de peso

### 2.4 - Contra-peso
Ainda deve ser projetado. Ela deve:

  * ser ajustável (permitir variar o peso)
  * ser afixado na mesa
  * não atrapalhar a passagem de ar

### 2.5 - Aquecedores
Os mesmos ja utilizados no forno. Serão dois, um fixado num carro acima e outro num carro abaixo da peça.

(O de baixo pode ser colocado dentro da peça que será a mesa, mas ainda deve estar no carro que permita mudar a sua posição)

Para eles um sistema elétrico e de controle deve ser montado.

O sistema elétrico e de controle deve ser ligado na controladora, mas deve também permitir controle manual.

### 2.6 - Carros
Ainda devem ser projetados.

O carro de cima fica suspenso acima da mesa.

O carro de baixo pode ficar abaixo da mesa, ou embutido dentro da mesa.

O importante para o carro de baixo é permitir aproximar ou afastar o aquecedor da peça na mesma medida que for possivel para o aquecedor de cima.

### 2.7 - Sistema de ar
Ainda deve ser projetado.

Ele deve permitir variar os pontos por onde o ar entra e sai da estrutura.

Ele deve permitir que o ar entre por um unico ponto e saia por um unico ponto, ou que entre por mais pontos e/ou saia por mais pontos.

### 2.8 - Controladora
Vamos usar um Raspberry Pi Zero W ou um Raspberry Pi Pico, o que for adequado para o processamento.

<img src="https://uploads.filipeflop.com/2017/03/DESCRITIVO_ITENS1.png" />

Teremos sensores para medir a temperatura da peça, idealmente em varios pontos. Os sensores poderão ser termo-pares, ou talvez algo mais avançado como uma camera termica.

A balança é um sensor de peso que enviará dados para a controladora.

Pode-se incluir um sensor de umidade (mas o sensor deve suportar a temperatura do forno).

Pode-se incluir sensores de vazão de ar.

## 3 - Primeiro esboço do projeto

### 3.3 - Mesa

<img src="https://github.com/casson-projects-2020/carbon-garage/blob/main/mesa.png" />

Sugestão da mesa montada como uma caixa de perfis de aço. Ela deve ser coberta com uma chapa perfurada ou algo equivalente.

As peças vermelhas sao os isolantes termicos dentro da estrutura.

Note a parte de baixo da estrutura, isolada termicamente. A balança será colocada nessa parte de baixo.

A mesa não pode ficar apoiada no fundo da estrutura: se isso acontecer, ela não vai transferir o peso da peça para a balança.

Não é possivel ver na imagem, mas temos um furo no isolante abaixo da mesa, e uma pequena barra que apoia a mesa em cima da balança.

Para estabilizar a mesa, ela pode utilizar um sistema de trilhos (sugeridos na imagem).

Ela no entanto tem que estar perfeitamente balanceada: se tombar para um lado, a leitura de peso terá erro.

### 3.4 - Contra-peso

Para o contra-peso a ideia inicial foi uma caixa de aço com alavancas que empurrariam a balança pra cima.

No entanto, talvez um sistema com cabos e polias seja mais simples.

A equipe precisa discutir e chegar na melhor solução.

### 3.6 - Carros

<img src="https://github.com/casson-projects-2020/carbon-garage/blob/main/carrosup.png" />

Sugestão do carro superior como uma caixa de perfis de aço.

O item em laranja é o aquecedor.

Para realizar o movimento de subir e descer do carro, ele poderia correr em trilhos como sugerido no desenho, ou pode-se pensar num sistema em que o carro esteja pendurado 
por cabos de aço.

<img src="https://github.com/casson-projects-2020/carbon-garage/blob/main/carroinf.png" />

Sugestão do carro inferior montado dentro da mesa, correndo nos mesmos trilhos.

Note que o carro superior é uma copia do inferior, mas isso não é obrigatorio: o carro superior pode ser maior.

### 3.7 - Sistema de ar
Ainda deve ser projetado.

Nas imagens aparece somente como dois furos no isolamento.

No entanto, é possivel um sistema melhor, por exemplo montado com junções em "t" como abaixo:

# TODO: imagem da sugestao

As sugestoes de carro nao estão levando em conta esse sistema, então talvez os carros e a mesa tenham que ser mais estreitos ou terem um espaço no meio para permitir
a passagem desses canos.


