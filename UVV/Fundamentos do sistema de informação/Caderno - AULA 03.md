Aula ao vivo 

O modelo geral da computação é um sistema (sistema aberto)

![[Pasted image 20240228192554.png]]

Para poder resolver um problema, é necessário de alguma forma pegar a informação e representá-la. Para isso é necessário saber como o computador representa dados. 

A forma da representação de dados demonstra a quantidade de dados que você pode representar 

OBS: com os dedos de uma mão vc pode contar até 32 (0 - 31), com 2 mãos vc pode contar até 1024 (0 - 1023);

Ao mudar a representação do problema: 
- podemos fazer mais com menos 
- podemos utilizar algoritmos mais adequedos
- temos mais flexibilidade da entrada e da saída 


*Representação de dados numéricos*
- Pegar o Slide com esse nome com

*Noção intuitiva do sistema binário*
O sistema binário funciona como um hodômetro de um carro. normalmente, com o sistema decimal (10 algarismos, do 0 ao 9), temos o seguinte:
 - pegar no slide


Para saber qual é o maior número que vc consegue representar com uma quantidade de bits (2 ^ nº de bits - 1); para saber a quantidade de números é (2 ^ nº de bits)

Os computadores usam binário pois é mais fácil criar os sistemas elétricos dentro do computador com o sistema binário. (circuito sem energia = 0; circuito com energia = 1)

Quem cria os 0 e 1 dentro dos computadores são os transístor (responsável pelos 0s e 1s; 0: quando interrompe a passagem de energia; 1: quando permite a passagem de energia)

Os 0s e 1s não existem! são uma abstração, você tem energia e não energia.

OBS: o CDrom armazenar 0 e 1 com buracos na superfície dele, aonde não tem é 0, aonde tem é 1.

O HD representa o 0 e 1 conforme a representação do campo magnético.

As memórias utilizam transitors.

A fibra-ótica utiliza a representação do 0 e 1 com luz..

O sistema octal tem 8 algarismo para representar os números (0 a 7).

O sistema hexadecimal de 16 algarismo, vai do 0 a F ( 0, 1 2, 3, 4, 5, 6, 7, 8, 9,  A, B, C, D, E, F)

![[Pasted image 20240229143546.png]]

Nos computadores não se trabalha com bit, pois ser muito pequeno, ou se trabalha com nibble ou byte, normalmente é byte

1 byte é um conjunto de 8 bits. é necessário 1 byte para se armazenar uma letra.

O nibble se utiliza muito pouco, é um conjunto de 4 bytes.

![[Pasted image 20240229143826.png]]

![[Pasted image 20240229144059.png]]


Para transformar bits em letras é utilizado o enconding (mapeamento)

![[Pasted image 20240229145021.png]]

O padrão utilizado no Brasil é o ASCII 

![[Pasted image 20240229145432.png]]

Os caracteres da duas primeiras colunas da esquerda são chamados de "caracteres não-imprimíveis" pois não são visualizados.

O ASCII utiliza até 8 bits para fazer o mapeamento.

Hoje em dia os computadores não utilizam o ASCII em razão de suas limitações. Utilizam o UNICODE

![[Pasted image 20240229150149.png]]

![[Pasted image 20240229150050.png]]
![[Pasted image 20240229150105.png]]

O UNICODE é um catálogo de letras, e cada letra possui um ID.

![[Pasted image 20240229151454.png]]

O encode para cores que foi criado é o RGB, que é utilizado como padrão.

![[Pasted image 20240229152204.png]]

No padrão RGB cada cor é representada por 1 byte,  e cada cor individual pode assumir 256 valores. o 0 é o preto e 255 é o máximo dessa cor.

Imagens são representadas da seguintes forma:
- cada imagem é formada de milhares de pixels 
- e cada pixel tem 1 e apenas 1 cor.
- assim é só armazenar a cor de cada ponto da imagem.
![[Pasted image 20240229153220.png]]

Uma imagem é armazenada através de mecanismos de compreensão sem perda. 

Também a métodos de compreensão com perda, que diminuem o tamanho da imagem

Para representar áudio há duas maneiras?
- sintetização (utiliza a partitura, e no computador ficar a representação da partitura, e o computador gera o áudio, o nome do formato é o MIDI)
- gravação (o problema para gravar é que por ser sinal analógico ele varia indefinitivamente durante um intervalo, por isso se faz amostras desse intervalo.)


![[Pasted image 20240229155227.png]]

- video

![[Pasted image 20240229155613.png]]

um vídeo é um formato de arquivo com um monte de fotos que são passados rapidamente.

![[Pasted image 20240229155809.png]]


---

Aula Gravada

INTRODUÇÃO 

Até o presente momento, vislumbramos de forma intensa os conceitos dos Sistemas de Informação e discutimos, ainda de forma preliminar, os conceitos associados a alguns de seus elementos, em especial, às Tecnologias da Informação que subsidiam esses sistemas. Discutimos, por exemplo, as Redes de Computadores, Softwares e Hardwares de forma introdutória, bem como os conceitos de arquitetura e organização dos computadores sem, porém, nos adentrar em seus elementos. Passaremos agora a um aprofundamento desses tópicos, para que você possa estar bem fundamentado nos aspectos técnicos que são tão importantes em sua profissão e atuação no mercado de trabalho. Não basta somente esse perfil de profissional saber o que são tais elementos, mas tem um grau de aprofundamento maior para propor soluções melhores.  Iremos abordar temas como Sistemas de Numeração (binário e hexadecimal), que explicam como dados são lidos, reconhecidos e processados em um computador (chamemos inicialmente de um sistema de computação), o hardware e software envolvidos em tudo isso e suas aplicações aos sistemas de processamento de dados. Em seguida, iremos entender como os recursos amplamente utilizados na Internet colaboram para as organizações no uso de Sistemas de Informações. Ao final serão apresentadas atividades que o ajudarão na sua aprendizagem, através de um desafio, o qual o levará a propor respostas a questões práticas associadas aos sistemas de computação associados a um SI, e, como aplicação prática, identificar tecnologias inovadoras e essenciais ao papel do SI nas empresas. Elas são muito importantes para seu entendimento.  Ótimos Estudos! Palavra-Chave: Sistemas de Informação. Tecnologias da Informação. Sistemas de Computação. Sistemas de Numeração.

--- 
vídeo - como funciona a internet

A internet faz uso da mesma infraestrutura da telefonia e televisão

um protocolo é um conjunto de regras para os dispositivos conversarem entre si

O protocolo IP funciona da seguinte forma:
- identifica cada dispositivo na rede
- divide a informação em pacotes 

O IP funciona entre diversos tipos de aplicaçãoes.

Comutação de pacotes: dividir a informação em diversos pacotes pequenos de informação. sendo enviados da origem ao destino de forma independente, não sendo necessário reservar previamente recursos, eles podem ser compartilhados, por isso a menos desperdício e menor custo.

---

## texto - Conceitos e aplicações de Tecnologias da Informação

 - Introdução

Até o momento, realizamos um estudo preliminar sobre as tecnologias de informação e comunicação mais importantes no apoio aos Sistemas de Informação, dando foco nos Bancos de Dados, Redes de Computadores, Software e Hardware. ==Conforme definido por Laudon (2011, p. 105), a infraestrutura de TI (tecnologia da informação) é composta por cinco elementos principais: hardware, software, tecnologias de rede e telecomunicações, tecnologias de gestão de dados (ou simplesmente Banco de Dados) e serviços de tecnologias.== Nesta unidade, iremos nos atentar aos três primeiros elementos.

Quanto ao aspecto do hardware, precisamos entender melhor como os dados são representados em um computador, afinal, estamos falando de um dispositivo eletrônico que funciona a base de energia elétrica. Precisamos compreender como os dispositivos eletrônicos estão organizados e quais são suas funções. De acordo com Prado (2014, p.78):

> **Arquitetura** e **organização** são termos relacionados à forma com que os computadores são projetados, embora possuam significados diferentes. ==**Arquitetura** se relaciona aos atributos de um sistema que são visíveis para o programador ou, em outras palavras, aos que têm impacto direto sobre a execução lógica de um programa. O termo **organização** diz respeito à maneira com que as unidades operacionais e seus sistemas de interconexões implementam a arquitetura.==

Em especial, ==uma arquitetura de computadores possui vários elementos, mas os principais são a memória principal, que armazenava dados e instruções, a unidade lógica e aritmética (ULA), capaz de realizar operações com dados binários (veremos esse conceito mais à frente), a unidade de controle, que interpretava e executava instruções armazenadas na memória e os Dispositivos de entrada e saída (E/S), operados pela unidade de controle PRADO (2014, p.78).==

Conforme descrito, ==o elemento ULA – Unidade Lógica Aritmética – é o componente de hardware da unidade de processamento (UP) responsável pelo processamento de cálculos e expressões lógicas (expressões que devem obter uma avaliação verdadeira ou falsa, nada mais, p.ex., 2+2 = 4 (V) e 2-1= 5 (F)).== Mas, como os números são representados em um ambiente eletrônico?

Para responder a isso, vamos primeiramente entender ==como números podem ser representados de forma geral, o que chamamos de **Sistemas de Numeração**==. Conforme definido por Gonçalves (2020, p.3), ==um **Sistema de Numeração** é o conjunto de símbolos utilizados para representar quantidades e as regras que definem a forma de representação. ==Conforme definido pelo autor, ==todo sistema de numeração é determinado fundamentalmente pela sua **BASE**, que indica a quantidade de símbolos e o valor de cada símbolo.== Vejamos alguns dos principais sistemas de Numeração:

==a) Sistema de Numeração Decimal== (base 10); 0, 1, 2, 3, 4, 5, 6, 7, 8, 9;

b) ==Sistema de Numeração Binário ==(base 2): 0,1;

c) ==Sistema de Numeração Octal ==(base 8): 0, 1, 2, 3, 4, 5, 6, 7;

d) ==Sistema de Numeração Hexadecimal ==(base 16): 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F.

 Por enquanto, apenas entenda que ==estamos representando números em algum formato, cuja base representa a quantidade de elementos representáveis==. O sistema de numeração natural que aprendemos desde cedo é o Decimal. Qualquer número, até agora, era representado por um dos 10 símbolos desse sistema (0 a 9), correto? Por exemplo: o número 13.447 é um decimal contendo 4 símbolos (1,2,4,7) do sistema decimal, correto? Nos sistemas eletrônicos de um computador, não é possível utilizar esse sistema de numeração. Foi necessário buscar uma forma de representar nos circuitos eletrônicos algum conjunto de números. ==Esse sistema de numeração possível para isso é o **Sistema de Numeração Binário**.==

E não é difícil entendermos essa necessidade. Por hora, entenda que os ==computadores digitais trabalham internamente com dois níveis de tensão elétrica, obrigando que seu sistema de numeração interno seja binário, simbolicamente representando que 1 = aceso e 0 = apagado== ou, ainda, conforme descrito por Gonçalves (2020), o==s símbolos 0 e 1 correspondem a qualquer conjunto dual, como não e sim; falso e verdadeiro verdadeiro; desligado e ligado; negativo e positivo, etc.== ==Nos circuitos lógicos, 0 e 1 representam respectivamente níveis de tensão baixa e alto ou estados de saturação e corte de transistores==. O que temos de entender, por hora, é que, uma vez construídos esses circuitos eletrônicos numa placa de um hardware, o que irá trafegar dentro desses circuitos é energia elétrica, correto?

Entenda por enquanto que, nesses circuitos (que, no hardware, são eletrônicos), há passagem de corrente elétrica e, dependendo da forma como esses circuitos estarão organizados, haverá a representação de uma sequência de bits que, por sua vez, representam números (binários). ==O entendimento dos sistemas de numeração Binário é importante para entendermos o funcionamento dos principais elementos que compõem a Unidade Central de Processamento – CPU, em especial, aqueles por onde trafegam dados (na forma de bits).==

Da mesma forma que pelo Hardware do sistema de computação há um conjunto de bits trafegando (coleta, armazenamento, processamento e distribuição), lembremos que são os softwares os elementos da tecnologia responsáveis para dar a esses bits algum sentido (lógica), que representa regras e procedimentos de interesse de seus usuários. Por exemplo: ao digitar a palavra “avião” no teclado (hardware), cada letra é apenas um sinal elétrico capturado, mas que, por alguma regra previamente programada num software (editor de texto), surge na tela (hardware) com algo que faz sentido na língua portuguesa. Imagine que, ao você digitar a letra ‘a’ no teclado, surgisse na tela para você o símbolo 11100110. Não faria qualquer sentido para o propósito do editor de texto entregar esses símbolos para você, correto?  Nas próximas seções, iremos detalhar mais esses elementos, partindo do sistema de numeração Binário e estudando os principais dispositivos de hardware, software e comunicação de dados (em especial, a Internet).

	No texto aqui referenciado, está um excelente material adicional para seus estudos a respeito dos Sistemas de Numeração com uma aplicação em circuitos lógicos. Não é necessário qualquer aprofundamento nos conteúdos associados aos circuitos, mas apenas um breve entendimento de como eles se relacionam com o sistema binário.
	
	Boa leitura!
	
	Fonte: CAMARA (2020)


- Sistemas De Numeração

Conforme descrito por Scotti (2020), ==um sistema de numeração, (ou sistema numeral) é um sistema em que um conjunto de números são representados por numerais de uma forma consistente.== Pode ser visto como o contexto que permite ao numeral “11” ser interpretado como o numeral romano para dois, o numeral binário para três ou o numeral decimal para onze. Obviamente que não precisaremos estudar todos os sistemas de numeração existentes. Conforme definido por Gonçalves (2020), a base 10 é importante por ser a que manipulamos cotidianamente. Já a base 2 é útil por conta dos circuitos lógicos, porém, documentar números grandes apenas com 0 e 1s é complicado. Assim, podemos utilizar as bases 8 (sistema octal) e 16 (sistema hexadecimal) para representar grandes números binários, pois compactam significativamente a sua representação.

---
==Os computadores entendem impulsos elétricos, positivos ou negativos, que são representados por 1 ou 0. A cada impulso elétrico dá-se o nome de bit (BInary digiT). Um conjunto de 8 bits reunidos como uma única unidade forma um byte.== Nos computadores, representar 256 números binários é suficiente para que se possa lidar a contento com estas máquinas. ==Assim, os bytes possuem 8 bits. Como um bit representa dois tipos de valores (1 ou 0) e um byte representa 8 bits, basta fazer 2 (do bit) elevado a 8 (do byte) que é igual a 256.== ==Os bytes representam todas as letras (maiúsculas e minúsculas), sinais de pontuação, acentos, caracteres especiais e até informações que não podemos ver, mas que servem para comandar o computador e que podem inclusive ser enviados pelo teclado ou por outro dispositivo de entrada de dados e instruções.==

Fonte: COSTA (2020)

---


Lembremos que, ==no sistema Binário, utilizamos apenas 2 dígitos: **0** e **1**.== E isso tem relação direta com o fato de termos internamente nos computadores os circuitos eletrônicos funcionando com correntes elétricas (e uma variação de tensão dessa energia). Nesse sistema BINÁRIO, vamos chamar cada um de seus símbolos de **BIT**, que significa um Dígito Binário (_Binary Digit_). Assim, no sistema binário, teremos 2 bits: 0 e 1. Quando agrupamos 8 Bits, estamos representando um **Byte**. Assim:

           **1 bit ≈ 0 ou 1**

           1 Byte **≈** 8 bits **≈** sequência de 8 bits. (por ex.: 11000101)

==Quando estamos interessados em representar números binários muito grandes, seria inviável utilizar uma sequência grande de 0s e 1s. Ao invés disso, podemos utilizar duas outras formas de representação: a Octal (8 símbolos, 0 a 7) chamada de **Hexadecimal** (base 16), logo, 16 símbolos (0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F) para representar os números.  Vamos entender melhor esse sistema binário.==

De acordo com Scotti (2020), ==o sistema binário permite fazer operações lógicas e aritméticas usando-se apenas dois dígitos ou dois estados (sim e não, falso e verdadeiro, tudo ou nada, 1 ou 0, ligado e desligado).== Toda a eletrônica digital e computação está baseada nesse sistema binário, que permite representar por circuitos eletrônicos digitais (portas lógicas) os números, caracteres, realizar operações lógicas e aritméticas. Já que em um computador digital, os dados estão representados na forma de bits (zeros e uns). ==Vamos entender melhor como os números que conhecemos (sistema de numeração decimal) podem ser representados por bits. Temos, então, de utilizar de uma conversão de sistemas de decimais, partindo de um número decimal e gerando seu número binário associado. A forma de se fazer isso é dividindo-se sucessivamente o número decimal por 2 até que que cheguemos no dividendo 2.== ==O número binário associado será o último quociente seguido de todos os restos das divisões.== Vejamos exemplos:

==- Qual o número binário associado ao decimal 8?

![](https://ceadconteudo.uvv.br/wp-content/uploads/2023/09/20230920-aula_ecolog_top03_img01.jpg)

- ==Assim, o número binário correspondente ao decimal 2 será obtido pelo último quociente e a sequência de restos, de baixo para cima, correspondendo ao binário 1000.==

Vamos ver isso de outra forma, transformando o número decimal 25 em binário. ==A partir do decimal 25, são feitas divisões sucessivas por 2, até que o quociente obtido seja 1 (3 /2). A partir daí o binário correspondente é obtido tomando esse quociente na última divisão (1), seguido dos restos obtidos das últimas divisões até a primeira (de baixo para cima).==

Veja:

![](https://ceadconteudo.uvv.br/wp-content/uploads/2023/09/20230920-aula_ecolog_top03_img02.jpg)

Operação de conversão decimal para binário

==Vamos a um segundo exemplo: qual o número binário associado ao decimal 19? Vamos seguir a regra feita anteriormente:

![](https://ceadconteudo.uvv.br/wp-content/uploads/2023/09/20230920-aula_ecolog_top03_img03.jpg)

==Assim, o número binário correspondente ao decimal 19 é **10011**==. Fácil não é?! ==E o processo inverso, isto é, como converter um binário em decimal? Vamos considerar primeiro que o bit mais à direita do número binário está na posição zero.== O próximo bit está na posição 1, e assim por diante. Assim, no número binário 10011 (correspondente ao número decimal 19), teremos as seguintes posições:

![[Pasted image 20240229103235.png]]

==Para obtermos o correspondente decimal do binário acima, vamos escrever cada bit do número binário multiplicado pela base do sistema (base=2), elevado à posição que ocupa. ==A soma de cada multiplicação de cada dígito binário pelo valor das potências resulta no número real representado. Vamos ver isso:

**1** x 2^4 + **0** x 2^3 + **0** x 2^2 + **1** x 2^1 + **1** x 2^0 = 19.

Observe que, em negrito, está cada um dos bits do número binário e a potência na base 2 é sua posição naquele número, percebeu? Por exemplo: o bit mais à esquerda (1) está na posição 4, logo, ele foi multiplicado pela potência 2 elevado a 4. Vamos a outros exemplos:

a) Converter o decimal 53 para binário:

![](https://ceadconteudo.uvv.br/wp-content/uploads/2023/09/20230920-aula_ecolog_top03_img04.jpg)

==Assim, o número 53 (decimal) equivale a 110101 binário, ou, em outra notação, 53D = 0110101B.==

==b) Converter o binário **11011** para decimal:

**1** x 2^4 + **1** x 2^3 + **0** x 2^2 + **1** x 2^1 + **1** x 2^0 = 27

Assim, o número 11011 (binário) equivale a 27 (decimal), ou, em outra notação, 11011B  = 27D. Observe que, em cada potência 2, está representada a posição na qual o bit associado aparece na sequência (lembre-se de que o primeiro bit à direita inicia na posição 0). Verifique, por exemplo, que o número 45 (decimal) equivale a 101101 binário, ou, em outra notação, 45D = 101101B.

J==á o sistema de numeração **Hexadecimal** é um sistema de numeração que representa números em base 16, logo, possui 16 símbolos para representar qualquer número. Esses 16 símbolos são: **0 1 2 3 4 5 6 7 8 9 A B C D E F**. As letras **A, B, C, D, E e F** correspondem aos decimais 11, 12,13,14 e 15 respectivamente.== O principal propósito do sistema de numeração (notação) Hexadecimal é permitir exprimir grandes sequências de bits (binário) numa forma mais, digamos, “enxuta”. Antes de qualquer coisa, ==podemos visualizar cada símbolo da notação Hexadecimal (0 1 2 3 4 5 6 7 8 9 A B C D E F) como seu correspondente binário e decimal, ==assim:

|**Decimal**|**Binário**|**Hexadecimal**|
|---|---|---|
|0|0000|0|
|1|0001|1|
|2|0010|2|
|3|0011|3|
|4|0100|4|
|5|0101|5|
|6|0110|6|
|7|0111|7|
|8|1000|8|
|9|1001|9|
|10|1010|A|
|11|1011|B|
|12|1100|C|
|13|1101|D|
|14|1110|E|
|15|1111|F|

==Essa tabela será importante para nos auxiliar na conversão entre números decimais, binários e hexadecimais. ==Veremos isso mais a frente. Exemplos de números na notação Hexadecimal são: 2F, 15CA e 2AF. Parece estranho, não? Calma que iremos mostrar como esses números são gerados pela conversão de números decimais ou binários. Importante ressaltar que a notação Hexadecimal está muito associada à forma de representação de dados em um computador, em sua memória. Por exemplo: o binário 10011100, o qual poderia representar um dado na memória do computador é, de forma mais racional, representado pelo Hexadecimal 9C. O sistema de conversão da notação decimal para hexadecimal é bem parecido com a conversão de decimal para binário, porém, ao invés de usar a base 2, usaremos a base 16. Vamos aos exemplos:

![](https://ceadconteudo.uvv.br/wp-content/uploads/2023/09/20230920-aula_ecolog_top03_img05-680x556.jpg)

==Observe que o decimal 12 (resto de 12412/16) em Hexadecimal não existe na tabela anterior, mas está associado à letra C. Assim, teremos            12412D = **307C**H. ==Toda vez que um resto dessa conversão para hexadecimal for maior que 9, você terá de utilizar a tabela anterior para corresponder a letra em Hexadecimal, ok?!

==c) converter 10024D para Hexadecimal:==

![](https://ceadconteudo.uvv.br/wp-content/uploads/2023/09/20230920-aula_ecolog_top03_img06.jpg)

Observe que nenhum resto foi maior que 9, logo, não precisaremos utilizar qualquer letra da notação hexadecimal. Assim, 10024D = **2728**H.

==c) converter 1237D para Hexadecimal:==

![](https://ceadconteudo.uvv.br/wp-content/uploads/2023/09/20230920-aula_ecolog_top03_img07.jpg)

Observe que, agora, temos um resto maior que 9 (o 13), logo, precisaremos utilizar uma letra da notação hexadecimal (ver na tabela anterior o símbolo hexadecimal que corresponde ao 13). Assim, 1237D = **4D5**H. Já na conversão de Hexadecimal para decimal, precisaremos, primeiro, transformar cada dígito hexadecimal em decimal. Assim, por exemplo: o C será convertido para 12 (ver tabela). Em seguida, multiplicamos cada número decimal convertido por 16N, onde N é a casa decimal onde ele se encontra (lembrar que o dígito mais à direita está na posição 0). Ao final, somamos os valores. Vejamos alguns exemplos.

e) ==Transformar **7C12**H para decimal (observe que o digito 2 está na posição 0): ==Primeiro, vamos converter o símbolo C para decimal (ver tabela). Assim, 7C12 = 7(12)12. Agora, geramos as potências na base 16:

![[Pasted image 20240229103829.png]]

A conversão de Hexadecimal para binário também irá utilizar a tabela anterior. Primeiro, vamos separar o número binário em grupos de 4 dígitos, da direita para a esquerda, e, então, realizar a conversão de cada um desses grupos conforme a tabela. Caso a quantidade de 1s ou 0s não seja múltipla de 4, completar com 0s(zeros) a esquerda. Por exemplo: o binário 100 ficaria 0100. Vamos ver algumas conversões de binário para Hexadecimal.

==f) Transformar 1010111001010B para Hexadecimal: ==vamos agrupar de 4 em 4 bits, da direita para a esquerda: **0001, 0101, 1100, 1010**. Observe que os bits sublinhados foram completados. Assim, consultando a tabela anterior para cada conjunto de bits, teremos 1010111001010B = 15CAH.

==g) Transformar 1011011110010B para Hexadecimal:== vamos agrupar de 4 em 4 bits, da direita para a esquerda, gerando os seguintes grupos: **0001, 0110, 1111, 0010**. Observe que os bits sublinhados foram adicionados ao dígito 1. Assim, consultando a tabela anterior para cada conjunto de bits, teremos 1010111001010B  = 16F2H.

---
O material aqui referenciado apresenta um breve histórico da evolução dos computadores digitais modernos e todos os seus elementos, como hardware e software. Além disso, descreve como os conceitos de bits estão ligados ao funcionamento eletrônico daqueles dispositivos. É um texto muito interessante e que permite a você compreender melhor esse mundo digital. Boa leitura!

Fonte: DUARTE (2020)

---

- Hardware E Software – Aplicações Aos Sistemas De Informação

Como já estudamos anteriormente, os Sistemas de Informação utilizam dispositivos eletrônicos para realizar uma grande parte das tarefas de coleta, armazenamento, processamento e distribuição de dados. Estamos falando dos dispositivos de Hardware de um computador. ==Laudon (2011, p. 105) afirma que o **Hardware** consiste na tecnologia para processamento computacional, armazenamento, entrada e saída de dados. Para Stallings (2003, p. 7), as funções básicas que um computador pode desempenhar são o **Processamento, Armazenamento, Transferência** e **Controle dos dados**.==

Especificamente em um computador eletrônico, temos um conjunto de elementos organizados, compondo uma ==**arquitetura de computação**. Uma arquitetura de computador comum é composta de uma **memória principal**, que armazenava dados e instruções, uma **unidade lógica e aritmética (ULA)**, capaz de realizar operações com dados binários, uma **unidade de controle**, que interpretava e executava instruções armazenadas na memória e **dispositivos de entrada e saída (E/S)**, operados pela unidade de controle.== A figura a seguir ilustra esses elementos.

![](https://ceadconteudo.uvv.br/wp-content/uploads/2023/09/20230920-aula_ecolog_top03_img08-768x373-1-680x330.jpg)

Componentes da Arquitetura de Computadores de Von Neuman.

Vamos descrever melhor esses elementos. ==Do ponto de vista das memórias, conforme descreve Prado (2014, p.78), temos pequenas memórias, chamadas de **registradores do processador**, que são o tipo de memória mais rápido presente nos equipamentos de hoje, porém, sua capacidade de armazenamento é a menor de todas. Eles armazenam apenas pequenas quantidades de dados (uma palavra da memória RAM) ou instruções que devem ser executadas pelo processador.

Já outro tipo de memória, chamada de ==**memória principal**, ou memória de acesso aleatório (em inglês, _Random Access Memory_ – RAM), é volátil, pois seu conteúdo é apagado quando o computador é desligado.== Por isso, presta a armazenar programas e dados que estão em uso pela CPU. Assim, quando estamos desenvolvendo programas de computador, os dados que serão coletados pelos comandos do programa serão referenciados em alguma posição de memória RAM. Quando determinada função ou mesmo o programa tem sua operação finalizada, aquela posição anteriormente ocupada pelo dado ficará à disposição para novos dados, até manipulados por outros programas.

Assim, essa memória é a mais importante do ponto de vista da execução de programas, pois, sendo muito limitada, impedirá que um maior conjunto de programas estejam em execução ao mesmo tempo. A figura abaixo, extraída de programa Gerenciador de Tarefas do Windows descreve, nas caixas em vermelho, a utilização do recurso de Memória Principal em um computador.

![](https://ceadconteudo.uvv.br/wp-content/uploads/2023/09/20230920-aula_ecolog_top03_img09v2.jpg)

Utilização da memória RAM e Cache em um computador.

As caixas em vermelho apresentam de que forma a memória RAM está sendo utilizada pelos programas em execução no computador. Na caixa mais à esquerda, podemos visualizar a memória rápida (Cache) disponível. Conforme já discutido, essa memória é mais rápida que a RAM, mas com espaço mais restrito para os dados.

O acesso aleatório significa que cada posição de memória possui um endereço fixo e fisicamente conectado a ela via hardware. Dessa forma, para qualquer posição de memória, o tempo de acesso é sempre constante. ==Outro tipo de memória é a **cache**, que possui alta velocidade de gravação e leitura e fica posicionada entre a CPU e a memória principal. Conforme Prado (2014, p.78), seu objetivo é melhorar o desempenho da CPU, tendo em vista que a memória principal consiste em várias ordens de grandeza mais lenta que a CPU, tornando-se, com facilidade, um gargalo para o computador como um todo.==

Por fim, dentre os principais tipos de memórias, temos as ==memórias **Secundárias**, que são do tipo não volátil, ou seja, seu conteúdo não é perdido quando o computador é desligado.== O disco rígido (HD – hard disk) é o exemplo de memória secundária, possuindo acesso direto aos dados nele armazenados. ==Um **Barramento,** conforme descrito por Prado (2014, p.78), é um caminho de comunicação entre dois ou mais dispositivos. Ele pode ser considerado um meio de transmissão compartilhado. Diversos dispositivos podem ser conectados a um barramento, possibilitando que um sinal transmitido por qualquer um dos dispositivos seja recebido por todos os outros conectados ao barramento==. Já os componentes de ==**Entrada e Saída (E/S),** de acordo com Prado (2014, p.78), são projetados para permitir um controle sistemático da interação com o mundo exterior e fornecer ao sistema operacional as informações necessárias para gerenciar a atividade de E/S de maneira efetiva.==

Outro componente fundamental no apoio aos Sistemas de Informação é o ==**software**==. Para Laudon (2011, p. 105), s==oftwares podem ser classificados como softwares aplicativos (no suporte aos usuários finais) ou tipos de software de sistema, que auxiliam o funcionamento de outros softwares e administram os recursos e atividades de um computador.== Em Cardoso (2020), ==um software de sistema é definido como Software Básico e é um conjunto de programas que define o padrão de comportamento do equipamento, tornando-o utilizável, ou seja, são os programas usados para permitir o funcionamento do hardware.==

De acordo com Prado (2014, p. 79), ==o software de sistema (Básico) mais importante é o Sistema Operacional (SO). Um SO é um programa que gerencia os recursos computacionais (hardware/software) do computador==. Ele também fornece uma base para os programas aplicativos e atua como intermediário entre os usuários e o hardware do computador. Os SOs mais conhecidos no mercado são o Windows e Linux, para computadores de pequeno porte e máquinas servidoras, e Android e IoS, para dispositivos móveis. A figura a seguir ilustra bem como os elementos hardware, software e dispositivos de E/S interagem entre si.

O sistema operacional não surgiu juntamente com a computação, não era algo tão indissociável como encaramos hoje. Na verdade, o desenvolvimento de sistemas modernos, que podem ser vistos como antecessores diretos do que temos hoje, foi iniciado nos anos 60, com o CTSS (MIT), o OS/360 (IBM) e Multics (MIT, GE e Bell Labs). O primeiro sistema operacional a ter uma interface gráfica foi o Macintosh OS 1.0, lançado pela Apple em 1984. Como efeito complementar, recomendo que você dê uma lida neste outro artigo em nosso site que conta um causo bem engraçado, uma briga entre Steve Jobs e Bill Gates, sobre a lendária rivalidade em torno da interface gráfica em sistemas operacionais.

[Clique aqui e saiba mais](https://www.hardware.com.br/artigos/o-que-e-um-sistema-operacional)

![](https://ceadconteudo.uvv.br/wp-content/uploads/2023/05/20230531-image-17-680x566.png)

Relações entre hardware, SO, aplicativos e usuários.

==Outro elemento de extrema importância para o funcionamento dos Sistemas de Informação são as redes de computadores, em especial, uma rede de longa distância (WAN – _Wide Area Network_) chamada de Internet==. Segundo Prado (2014, p. 80), ==os equipamentos que se conectam à internet são denominados hospedeiros ou sistemas finais.== Os ==hospedeiros são conectados entre si por meio de enlaces de comunicação.==Os mais populares encontrados na internet são conhecidos como ==**roteadores** e **switches**.== ==Roteadores são dispositivos responsáveis por criar a rota que os pacotes devem seguir, sendo um dispositivo da camada de rede da internet. Sendo assim, um sistema final A consegue enviar uma mensagem ao sistema final B, seguindo a rota determinada pelos roteadores. Um switch é um dispositivo da camada (uma rede de computadores pode ser vista como um conjunto de camadas de componentes) enlace da internet que determina para qual das portas de saída os dados devem ir, deixando as outras portas livres para serem usadas.==

O vídeo a seguir ilustra de forma bem divertida o funcionamento da Internet. São apresentados conceitos importantes como endereçamento IP, protocolos, roteamento, etc. Não se preocupe por enquanto com os detalhes técnicos, mas apenas perceba os recursos utilizados numa conexão de Internet.

https://ceadgraduacao.uvv.br/conteudo.php?aula=conceitos-e-aplicacoes-de-tecnologias-da-informacao&dcp=fundamentos-de-sistemas-de-informacao&topic=3#section-1

- Conclusão

Ao final desta unidade, foi possível perceber como funciona uma aritmética digital, entendendo o que são sistemas de numeração e como os sistemas binário e hexadecimal se aplicam aos conceitos de um computador moderno. Vimos, em seguida, com maiores detalhes, os elementos que compõem hardware e softwares dos computadores modernos. Por fim, entendemos que a Internet, como uma rede de computadores de âmbito mundial, utiliza também daqueles recursos de hardware e software para comunicar milhões de computadores pelo mundo. Esses conceitos são todos aplicáveis aos contextos dos sistemas de informação. A partir de agora, iremos ter uma visão ampla de como os sistemas de informação por profissionais da tecnologia e quais processos, ferramentas e técnicas são utilizadas.

---

Aula gravada 01 

![[Pasted image 20240229112311.png]]

Unidades do processador 

- ULA - Unidade Lógica Aritmética, responsável por manipular os dados e processa-los 
- Unidade de controle - busca os dados e disponibiliza eles para a memória principal 

Os dados precisam ficar organizados lá dentro.

A arquitetura é como o sistema é visto.

![[Pasted image 20240229113014.png]]

O bit é a representação do menor tipo possivel de um dado, pode ser 0 ou 1.

![[Pasted image 20240229113732.png]]

Não importando a forma de representação, eles serão transformados em bits.

A base hexadecimal é uma forma mais enxuta de representar uma base binária 

![[Pasted image 20240229113853.png]]
![[Pasted image 20240229114002.png]]
![[Pasted image 20240229114012.png]]

 ![[Pasted image 20240229114256.png]]
![[Pasted image 20240229115616.png]]
![[Pasted image 20240229115913.png]]
![[Pasted image 20240229120012.png]]![[Pasted image 20240229120211.png]]
![[Pasted image 20240229120323.png]]
para converter de binário para hexadecimal é necessário separar os bits em bloco de 4 bits.



Aula gravada 02

![[Pasted image 20240229121708.png]]![[Pasted image 20240229121844.png]]
![[Pasted image 20240229121855.png]]
![[Pasted image 20240229121917.png]]
O sistema operacional que faz a iteração entre os usuários e os recursos de hardware.

![[Pasted image 20240229122044.png]]
![[Pasted image 20240229122140.png]]

---
Exercicios 

Os computadores, em geral, usam a base binária para representar os números, onde as posições, chamadas de bits, assumem as condições “verdadeiro” ou “falso”. Os computadores representam os números com uma quantidade fixa de bits, o que se traduz em um conjunto finito de números representáveis. Geralmente, para associar números do cotidiano das pessoas com as representações em um computador, utilizamos operações de conversões numéricas. Conversões numéricas são utilizadas em muitos casos na computação. Isso porque nós somos acostumados com a base numérica decimal (0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, ...), mas, no mundo da tecnologia digital, os dispositivos eletrônicos trabalham em baixo nível com a base numérica binária (0 ou 1), pois os números binários são facilmente representados na eletrônica através de pulsos elétricos. Além desses dois, as bases numéricas octal e hexadecimal também são muito utilizadas pela fácil representação. A base numérica representa a quantidade de símbolos possíveis para representar um determinado número. A tabela a seguir apresenta os símbolos que podem ser utilizados em cada sistema de numeração. 

|   |   |
|---|---|
|Base Numérica|Símbolos|
|Decimal|0, 1, 2, 3, 4, 5, 6, 7, 8 e 9|
|Binário|0 e 1|
|Octal|0, 1, 2, 3, 4, 5, 6 e 7|
|Hexadecimal|0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E e F|

Tendo em vista as informações apresentadas acima e os conteúdos vistos na unidade, faça o que se pede: Faça a conversão do número decimal 3445 para seu correspondente binário; Faça a conversão do número Binário 11010101101 para seu correspondente Hexadecimal; Faça a conversão do número Hexadecimal A81 para seu correspondente Binário; Faça a conversão do número Binário 101101 para seu correspondente decimal; Faça a conversão do número decimal 2123 para seu correspondente Hexadecimal.  Obs.: Não é necessário o envio de material.


---
chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/https://www.inf.ufsc.br/~bosco.sobral/extensao/sistemas-de-numeracao.pdf

chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/http://professores.dcc.ufla.br/~monserrat/icc/Introducao_internet.pdf

https://www.minhaconexao.com.br/blog/internet/como-funciona-internet