## Aula 02 Conceitos e Elementos de um Sistema de informação 

Neste Tópico, iremos entender como os ==Sistemas de Informação utilizam tais recursos para desempenhar suas funções e entregar informação de qualidade, tempestiva e íntegra aos gestores.==  Nosso objetivo é ==compreender e detalhar as principais tecnologias de informação que apoiam esses sistemas.==  Também iremos ==abordar e detalhar a necessidade de integração de um SI com os demais processos organizacionais, estudando as arquiteturas de Integração entre SI e os demais sistemas da organização (internos e externos).== Para melhorar os resultados obtidos pelos SIs, iremos entender o ==conceito de governança de TI e sua importância da gestão de sistemas e dados para o alinhamento estratégico da organização.==  Ao final, serão apresentadas atividades que o ajudarão na sua aprendizagem, através de um desafio, o qual o levará a propor respostas a questões práticas associadas às tecnologias de um SI, e, como aplicação prática, identificar tecnologias emergentes utilizadas nas organizações como diferencial competitivo, com pesquisas na literatura. Por fim, os exercícios práticos testam seu conhecimento no conteúdo, com questões de múltipla escolha e discursivas. Elas são muito importantes para seu entendimento.  Ótimos Estudos! Palavra-Chave: Sistemas de Informação. Tecnologias da Informação. Governança.

---
Texto  -  Conceitos e elementos de um Sistema de Informação

1 - Introdução

Os Sistemas de Informação (SI) podem ser vistos como importante recurso dentro da organização. Seu principal produto é a informação, importante insumo para a obtenção de conhecimento e inovação para qualquer organização. ==Vimos também que um SI compreende 3 dimensões (**Pessoas, Organização e Tecnologias**)==, sendo que as Tecnologias compõem a estrutura de suporte ao funcionamento dos SI dentro da organização. Vimos os conceitos e alguns exemplos das tecnologias mais importantes, como Bancos de Dados, Redes de Computadores, Software e Hardware.  

Nesta unidade, avançaremos um pouco mais, detalhando tais tecnologias e entendendo como elas se integram e a outros sistemas também. Porém, não é nosso objetivo detalhar suas estruturas e funcionamento, conteúdos esses vistos em outras disciplinas. É importante que lembremos que ==as tecnologias são recursos da organização e, como tal, devem ser gerenciados no que chamamos de Governança de Tecnologias, cujo tema será também aqui abordado. ==Nesse sentido, entendendo as tecnologias como recursos, PRADO (2014, p. 6) afirma que:

> “O conceito holístico da ==TI é compreendido quando diferentes tecnologias e sistemas de informação usados em uma organização serão convergentes e resultarão em um processo coerente de tomada de decisão.== Este conceito significará hardware, software, design do sistema de informação que capturará dados transacionais, táticos e estratégicos, processando-os e que auxiliarão os gestores no processo de tomada de decisão. ==A TI também ajudará a automatizar processos de negócios que melhorarão na consistência e na previsibilidade das entradas e saídas, facilitando na construção do protocolo de comunicação”.==

O que percebemos é o papel (dentro de um sistema maior) das Tecnologias da Informação aplicadas para atingir os objetivos da organização. Novamente, percebemos que **==a TI é um meio e não um fim**.==  Prado (2014, p.6) salienta ainda que:

> “A evolução da TI, vista aqui de forma holística, propicia um barateamento nos custos de coleta, de armazenamento e da manipulação dos dados e um ganho na velocidade de transmissão da informação consolidada e distribuída para diferentes pontos locais geográficos. A informação obtida por meio da TI é originada em cada um dos processos de negócios, processada pelos vários canais componentes da estrutura organizacional e consolidada nos níveis táticos e estratégicos, com o objetivo de auxiliar a tomada de decisão”.

Nesse mesmo sentido, **enxergando a TI como importante recurso**, afirma Laudon (2011, p. 73), ==as organizações e gerências bem-sucedidas têm visto a TI como instrumento importante para suas ações, assumindo um papel de forma ativa no ajuste da função dessas tecnologias e avaliando seu impacto sobre as receitas e os lucros.== Ainda, Laudon (2011, p. 73) nos fornece um guia para melhor utilizar o recurso de TI:

> “- **Identifique a estratégia e metas de seu negócio; – Transforme essas metas estratégicas em atividades e processos concretos; – Defina de que maneira irá avaliar o progresso em direção às metas do negócio (ou seja, as métricas);** Pergunte-se: ‘como a tecnologia da informação pode me ajudar a progredir rumo às metas empresariais e de que maneira ela vai aprimorar os processos e as atividades de negócio?’; – avalie o desempenho atual. Deixe que os números falem”.

Ora, o texto acima fala a todo o momento em avaliação e efetividade da TI. Esse ponto deixa claro que a ==adoção de uma solução de TI deve passar por uma gestão, com contínua avaliação de seus resultados. É o que chamaremos de Governança em TI.== Ainda, Prado (2014, p.78) aponta os benefícios de um uso efetivo da TI para os negócios:

> ==“Os investimentos nos componentes da infraestrutura de TI, tanto em hardware (estações de trabalho, data center, impressoras, redes de longa e curta distância para voz e dados) quanto em software (aplicativos de segurança e sistemas de integração) possibilitam a criação de uma camada de recursos compartilhados para toda a organização, melhorando a qualidade dos serviços, aumentando a eficiência na comunicação, e agilizando as decisões.==O investimento nessa camada ==determina como todos os sistemas e serviços de TI da organização funcionam por determinado período de tempo.== Em geral, são investimentos de longo prazo, visando atender tanto a demanda atual quanto o crescimento dos negócios”.

==Nosso papel enquanto profissionais de tecnologia da informação é fornecer para o gestor um mapa, um direcionamento de como esses recursos importantes serão empregados (e evoluídos) dentro do ambiente da organização para prover maior vantagem competitiva (por exemplo: reduzindo custos operacionais).== Vamos, então, nos debruçar sobre esses temas.

Gottfried Wilhem von Leibniz (1646 – 1716) foi um matemático e filósofo alemão que desenvolveu o cálculo e a notação que hoje é utilizada. Contudo, ele nunca pensou no conceito de derivada como um limite. A revolução das máquinas de calcular ocorreu entre os anos de 1960 e 1970. Foi durante este período que elas passaram de mecânicas para eletrônicas. Já o computador parece ter derivado dos primeiros teares que começaram a utilizar cartões perfurados. Em 1834, Charles Babbage desenvolveu uma máquina que executava as operações básicas, somar, subtrair, multiplicar e dividir, e também era capaz de armazenar dados em uma memória e imprimir os resultados. Contudo, a conclusão da máquina só ocorreu alguns anos após sua morte. Ela foi a base utilizada para a estrutura dos computadores utilizados atualmente, isso fez com que Charles Babbage fosse considerado como o “Pai do Computador”.

Fonte: VIALI (2020).

2- Organização das Tecnologias da Informação e Comunicação – TiCs

Do ponto de vista **sistêmico**, ==a implantação de sistemas de informação (SI) irá requerer um entendimento total dos demais sistemas existentes na organização, afinal, o SI coleta dados e entrega como produto uma informação, para um ou vários outros sistemas.== Lembremos, também, que ==uma organização é um sistema aberto, que possui inúmeras interações com seu meio externo==. Assim, não há dúvidas da necessidade de integração do SI com os demais sistemas organizacionais. Nesse sentido, entende Prado (2014, p. 6) que:

> “O gestor, em uma organização, deve analisar o impacto do investimento tecnológico na cultura e na dinâmica dela, além dos benefícios e retorno sobre o investimento, quando da adoção da tecnologia. A compreensão do significado da TI em uma maneira holística se faz premente para o alcance dos objetivos de longo prazo. ==O conceito holístico da TI é compreendido quando diferentes tecnologias e sistemas de informação usados em uma organização serão convergentes e resultarão em um processo coerente de tomada de decisão.== Este conceito significará hardware, software, design do sistema de informação que capturará dados transacionais, táticos e estratégicos, processando-os e que auxiliarão os gestores no processo de tomada de decisão. ==A TI também ajudará a automatizar processos de negócios que melhorarão na consistência e na previsibilidade das entradas e saídas, facilitando na construção do protocolo de comunicação”==.

Ao visualizar um ==SI como integrante de um sistema holístico (conjunto de sistemas), teremos condições de entender as necessidades de integração, permitindo, na decisão de um novo projeto de implantação desse novo SI, um barateamento nos custos de coleta, de armazenamento e da manipulação dos dados e um ganho na velocidade de transmissão da informação consolidada e distribuída para diferentes pontos locais geográficos.== Isso vale ==tanto para os sistemas internos à organização quanto para os sistemas externos==. Por exemplo: um dos atores externos envolvidos na implantação de um SI dentro da organização é o Governo, quando, no caso de um comércio, são geradas notas fiscais eletrônicas que devem ser validadas pelo órgão gestor fiscal do estado. A figura a seguir ilustra, de forma resumida, a necessidade de alinhamento das soluções de Tecnologia da Informação (e ai se incluem os Sistemas de Informação) com as estratégias de negócio, regidas pelos demais sistemas da organização e seus processos.

![](https://ceadconteudo.uvv.br/wp-content/uploads/2023/11/20231110-aula_funinf_top02_img01-680x251.jpg)

				Integração das soluções de SI com o negócio.

Do ==lado direito, temos as estratégias de desenvolvimento de soluções em TI, que servirão como suporte às estratégias de negócio (lado direito) e, por elas, serão guiadas.== O foco dessas ==duas estratégias, integradas, é servir às demandas do mercado externo: clientes, governo, fornecedores, etc==. Evidentemente que oferecer um suporte às estratégias de negócio é forçar uma integração (em algum nível) com os demais sistemas organizacionais, como Recursos Humanos, Produção, Financeiro, Vendas, etc.

Quanto ao papel da dimensão **==Tecnologia**, vamos detalhar melhor seus elementos como suporte ao desenvolvimento dos Sistemas de Informação==.  De início, podemos detalhar o ==**Hardware** como infraestrutura física para suporte aos SIs. Falamos que o hardware envolvido em um sistema de computação possui uma “arquitetura” e também uma organização. Arquitetura se relaciona aos atributos de um sistema que são visíveis para o programador ou, em outras palavras, aos que têm impacto direto sobre a execução lógica de um programa.== O termo organização diz respeito à maneira com que as unidades operacionais e seus sistemas de interconexões implementam a arquitetura

> “Os componentes dessa arquitetura eram: uma memória principal, que armazenava dados e instruções; uma unidade lógica e aritmética (ULA), capaz de realizar operações com dados binários; uma unidade de controle, que interpretava e executava instruções armazenadas na memória; dispositivos de entrada e saída (E/S), operados pela unidade de controle” (PRADO, 2014, p. 78).

A próxima figura descreve como cada elemento dessa arquitetura está organizada, cada um com sua função no sistema de computação, que, por ora, vamos nos limitar ao entendimento de um computador comum.

![](https://ceadconteudo.uvv.br/wp-content/uploads/2023/11/20231110-aula_funinf_top02_img02.jpg)

Visão funcional de um computador.

Nessa organização, os **==Dispositivos de Entrada e Saída (E/S) (**Mecanismo de transferência de dados) são o hardware pelo qual os dados do ambiente externo serão coletados e transferidos para o mecanismo de controle (Unidade de Controle), responsável para ora armazenar os dados coletados em um Recurso de armazenamento de dados (Memória), ora gerenciar seu processamento em um recurso de processamento de dados (**Unidade Central de Processamento – CPU**, que contém a unidade lógica e aritmética (ULA)==). No contexto de um SI, temos vários dispositivos de hardware que operam como Dispositivos de E/S, como teclado, leitoras de código de barras, leitoras biométricas, câmeras, sensores de leitura de temperatura ou movimento, microfones, telas sensíveis ao toque – _touchscreen_ (muito utilizadas em bancos) etc. ==Como saída, podemos citar as impressoras, caixas de som, monitores, etc. São esses dispositivos que farão a interface do computador com o meio externo.==

==Uma vez coletados os dados via dispositivos de E/S, esses dados serão armazenados pelo controlador em um hardware, chamado de memória.== As ==memórias podem ser classificadas como **internas** (chamas de principal), voláteis (os dados são perdidos ao se desligar o computador), possuindo vários tipos que estão associados ao espaço de armazenamento e velocidade de acesso aos dados pela Unidade de Controle, e a memória **externa**, utilizada para armazenar dados que possuem maior durabilidade e que não são voláteis (não se perdem quando um computador é desligado).== Essas memórias possuem espaço de armazenamento muito maior que as memórias internas.

![](https://ceadconteudo.uvv.br/wp-content/uploads/2023/11/20231110-aula_funinf_top02_img03.jpg)

				Hierarquia de memórias em um computador.

A figura anterior apresenta uma “hierarquia” de memórias. Quanto mais alta a posição na figura, menor é o espaço de armazenamento da memória, porém, maior é a velocidade de acesso aos dados por ela armazenados. ==Observe que as memórias internas (dentro da própria CPU) são aquelas que, primeiramente, serão acessadas para processamento de uma CPU, sendo as memórias externas (não voláteis) acessadas secundariamente.==

Podemos visualizar o ==**Software** como os recursos que incluem todos os conjuntos de instruções de processamento aplicados a dados e/ou informações==.  Para isso, a construção de Software requer a ==construção de **Programas de computador**, que são um conjunto de instruções que fazem com que um computador execute uma tarefa específica==. De acordo com Laudon (2011, p. 105), um ==software pode ser “**de sistema”** ou “**aplicativo”**.== ==Softwares de sistema administram os recursos e atividades do computador==. ==Softwares aplicativos ‘aplicam’ o computador a uma tarefa específica solicitada pelo usuário final, como o processamento de um pedido ou a geração de listas de mala direta.==

Assim, inúmeros são os softwares existentes dentro de um sistema de informação, podendo atuar como suporte a outros softwares (**softwares de sistema**) e que não estão em uso direto pelo usuário final. Podemos citar os Sistemas Operacionais (Windows, Linux, Android, etc), sistemas embarcados (por exemplo, sensores que controlam a estabilidade em um veículo), sistemas de inteligência artificial, dentre outros.  ==Ainda há os **softwares aplicativos** que realizam tarefas bem especificas de suporte ao usuário final, como um editor de textos, planilhas, navegadores de Internet, etc.== Evidentemente que, ao se construir programas de computador, eles deverão “operar” sobre um hardware específico, isto é, um software precisa de recursos computacionais como processamento e memória para que possam ser executados.

==Quanto ao volume cada vez maior de dados coletados e que devem ser armazenados nos sistemas de informação, são utilizadas as tecnologias dos **sistemas de gerenciamento de bancos de dados**.== De acordo com Laudon (2011, p. 144), “Um ==banco de dados** é um conjunto de arquivos relacionados entre si com registros sobre pessoas, lugares ou coisas”==. Já em Takai (2020, p.15), encontramos um conceito mais amplo associado às tecnologias de armazenamento de dados, definido como um **Sistema Gerenciador de Base de Dados (SGBD):**

> “Um ==**Sistema Gerenciador de Base de Dados** (SGBD) é uma coleção de programas que permitem aos usuários criarem e manipularem uma base de dados. ==Um SGBD é, assim, um sistema de software de propósito geral que facilita o processo de definir, construir e manipular bases de dados de diversas aplicações. ==Definir uma base de dados envolve a especificação de tipos de dados a serem armazenados na base de dados.== Construir uma base de dados é o processo de armazenar os dados em algum meio que seja controlado pelo SGBD. Manipular uma base de dados indica a utilização de funções como a de consulta, para recuperar dados específicos, modificação da base de dados para refletir mudanças no mini-mundo (inserções, atualizações e remoções) e geração de relatórios”.

De acordo com Takai (2020, p.15), então, descrevemos um ==“sistema” (um software) para gerenciar dados, envolvendo uma especificação de tipos de dados, sua construção e implementação.== Após isso, os ==dados serão gerenciados, podendo ser atualizados, excluídos ou simplesmente acessados==. Conforme ressaltado pelo autor, é fundamental que esses dados reproduzam um conceito de negócio, o contexto que os dados deverão representar.

Ainda conforme Takai (2020, p.16), um ==SGBD possui várias funções,== assim, podemos destacar: ==a) **fornecer restrições de Acesso Multiusuário**==, permitindo que os acessos aos dados sejam autorizados devidamente, de acordo com o perfil de cada usuário (alguns podem ler um dado, mas não podem exclui-lo, por exemplo); ==b) **implementar rotinas para permitir Backup e restauração** do Banco de dados, caso ocorram falhas de hardware ou software==; ==c) **Reforçar Restrições de Integridade**, já que muitas aplicações de base de dados terão certas restrições de integridade de dados==. Por exemplo: não é possível excluir dados de um cliente que possui vários pedidos associados e; ==d) **gerenciar o compartilhamento de Dados**, já que, quando multiusuários acessam os dados simultaneamente, é preciso assegurar que tais atualizações resultem em modificações corretas (por exemplo, consultar saldo bancário e retirar dinheiro em um caixa automático num mesmo momento).==

É importante ressaltar que um ==SGBD possui diversos tipos de usuários==. Temos os ==usuários finais, que são aqueles que utilizam de alguma interface de programas de computador para realizar operações básicas sobre as bases de dados existentes==. ==Outros tipos de usuário são aqueles que **desenvolvem softwares** para acesso aos dados==. Eles precisam dominar as regras de acesso e suas linguagens, mas também estão associados às questões de negócio da organização. Por fim, destacamos a atividade do ==**Data Base Administrator** – **DBA**, profissional esse responsável pelas ações de gerenciamento do SGBD, realizando sua construção e gerenciamento, como permissões de acesso e regras de integridade dos dados.==

==A figura a seguir ilustra a estrutura de um SGBD.== Na parte inferior da figura, observamos os locais físicos (hardware) onde os dados (e suas informações conhecidas como metadados) serão armazenados.

![](https://ceadconteudo.uvv.br/wp-content/uploads/2023/11/20231110-aula_funinf_top02_img04.jpg)

Componentes de um sistema gerenciador de banco de dados.

https://www.youtube.com/watch?v=XZmGGAbHqa0&t=68s

Este vídeo apresenta a infraestrutura de um Data Center, um importante local associado a grandes armazenamentos de dados em grandes corporações. O vídeo descreve um Data Center do Google, mostrando sua estrutura física, funcionamento e itens de segurança. É muito interessante e o vídeo tem tradução automática!

Já uma ==infraestrutura de **redes de computadores**, de acordo com Laudon (2011, p.105), proporciona conectividade de dados, voz e vídeo a funcionários, clientes e fornecedores==. Isso inclui tecnologia para operar as redes internas da empresa, serviços prestados por companhias telefônicas ou de telecomunicações, e tecnologia para operar sites e conectar-se com outros sistemas computacionais por meio da Internet.

Presente na vida de milhões de pessoas em todo o mundo, a internet agora estende o seu controle ao mundo dos objetos. É o início de uma revolução tecnológica chamada internet das coisas ou _internet of things_ (IoT), que promete interligar objetos físicos ao mundo virtual de modo que eles possam interagir com as pessoas e se comunicar entre si. A hipótese é que a IoT irá mudar a oferta de alguns produtos e serviços. Este texto apresenta conceitos de IoT e impactos já gerados nos negócios. É um importante guia para este novo conceito.

[Clique aqui](https://revistafae.fae.edu/revistafae/article/view/402/286)

==Assim, uma Rede de Computadores conecta recursos computacionais a seus usuários.== Um melhor exemplo disso é a Internet, a rede mundial de computadores. Ela dispõe de um gigante conjunto de recursos de dados, como imagens, vídeos e áudios, textos e hypertextos, alocados em determinados computadores. Para que possam ser acessados, é necessário interligar computadores separados por milhares de quilômetros, usufruindo, para isso, das outras redes disponíveis pelos patrocinadores no mundo, como governos, empresas privas e organismos de segurança. A figura a seguir apresenta esse conceito de forma mais resumida.

![](https://ceadconteudo.uvv.br/wp-content/uploads/2023/11/20231110-aula_funinf_top02_img05.jpg)

Componentes cliente e servidor de uma rede de computadores.

Na figura, podemos visualizar uma estrutura de “rede” composta por inúmeros dispositivos que irão transportar as solicitações de um computador “cliente” até um computador “servidor”, o qual proverá serviços e dados, que serão transportados de volta a seu cliente. De acordo com Tanenbaum (2011, p. 2), ==as redes de computadores têm como objetivo “deixar todos os programas, equipamentos e, especialmente, dados ao alcance de toda as pessoas da rede, independentemente de localização física do recurso ou usuário”==. Uma rede de computadores pode interligar computadores em um pequeno espaço físico, em uma Rede Local (LAN – _Local Area Network_), ou por uma Rede Metropolitana (MAN – _Metropolitan Area Network_) para conectar diversas Redes Locais dentro de algumas dezenas de quilômetros ou, ainda, computadores dispostos a uma distância de milhares de quilômetros utilizando uma WAN (_Wide Area Network_). A **Internet** é o caso mais clássico de uma grande rede de computadores WAN.

![](https://ceadconteudo.uvv.br/wp-content/uploads/2023/11/20231110-aula_funinf_top02_img06-680x398.jpg)

Estrutura de uma rede WAN – Internet.

https://www.youtube.com/watch?time_continue=9&v=ec3l_11dpWA&embeds_referring_euri=https%3A%2F%2Fceadgraduacao.uvv.br%2F&source_ve_path=MjM4NTE&feature=emb_title

Este vídeo descreve o contexto de um mundo cada vez mais conectado à internet, onde empresas e usuários de tecnologia investem diariamente em soluções de segurança. Esse é um tema muito atual quanto à Governança em TI. Os dados obtidos e processados merecem atenção de todos os profissionais em TI!

3 -  Governança em Ti

Diante de todos os recursos de TI que foram vistos nas seções anteriores e também da necessidade de alinhar esses recursos aos objetivos da organização (nas empresas que não são do setor de TI, esse recurso não é um fim, mas um meio), a questão que se apresenta é: como melhor gerenciar tais recursos? De acordo com Prado (2014, p.82), ==é necessário gerenciar uma infraestrutura de TI que **gere valor e agilidade aos negócios, sendo** necessário compreender os seus diferentes níveis. Esses níveis devem ser de conhecimento dos gestores para que possam tomar as melhores decisões de investimento em TI.==  Esse ==gerenciamento faz parte do que chamamos de **Governança de TI**==, que iremos abordar de forma introdutória nesta seção. Em Prado (2014, p. 20), o ==**conceito de Governança de TI** é dito como liderança, estruturas organizacionais e processos que buscam garantir que a TI sustente e aprimore os objetivos e a estratégia da organização, sendo de responsabilidade dos executivos e da alta direção.== Ainda conforme o autor:

> “Governança de TI é o sistema pelo qual uma organização de TI é dirigida, tratando de direitos decisórios, responsabilidades e mecanismos de monitoramento, visando o **alinhamento estratégico da TI com o negócio**, a avaliação e o gerenciamento de riscos da TI e a melhoria contínua, equilibrando adequadamente os investimentos em pessoas, processos e tecnologias”(PRADO, 2014, p. 22, ).

Por exemplo: quando há a terceirização de serviços, é preciso saber gerenciar os contratos, fornecedores e estabelecer relações baseadas em acordos de níveis de serviço, em que as responsabilidades estão definidas com clareza e a entrega pode ser avaliada com objetividade. Isso é uma ação de “governar” os recursos de TI. Outro importante exemplo apresentado por PRADO (2014, p. 18) é o caso de websites de comércio, que podem ser somente uma forma de vendas de um meio a outro, sem que o embarque de inovações seja obrigatório, mas podem, por seu lado, gerar novas formas de experiência com os clientes, propiciando, assim, verdadeiras vantagens competitivas.  ==No caso de Websites para bancos eletrônicos, eles focam na interface com o usuário final, possibilitando a execução direta de processos que seriam realizados pelos caixas nas agências, trazendo melhoria operacional para o banco.==

Além dessas questões pertinentes ao negócio propriamente dito, ==a governança em TI busca atender a normas e procedimentos regulatórios quanto à transparência das informações.== As ==empresas dependem de TI para mostrar seus resultados operacionais com transparência e atingir seus resultados estratégicos e financeiros,== devendo esses serem informados a outros atores, como Governo, acionistas, clientes, etc. Conforme descrito por Prado (2014, p. 21), a Governança de TI se apoia num tripé:

- ==**Processos**: formalização das atividades a serem realizadas, seja operacionalmente ou para controles estratégicos e gerenciais;==
- ==**Recursos tecnológicos**: componentes de hardware, software, sistemas de telecomunicações e de gestão de dados e informações, utilizados para guarda, geração e uso da informação e do conhecimento;==
- **==Pessoas**: são as responsáveis pelo planejamento, operação, manutenção e utilização da tecnologia da informação. São aqueles que recebem e geram seus resultados, divididos em papéis que, por sua vez, são mapeados nos processos.==

A notícia boa para os profissionais responsáveis por essa governança é que há modelos, normas e padrões que podem ser seguidos (ou mesmo uma combinação deles é possível). Chamamos isso de **_frameworks_** (estruturas) de governança. No decorrer de seu curso, você verá vários deles como, por exemplo, a **norma ISO/IEC 38500**, que tem como objetivo fornecer uma estrutura de princípios para os dirigentes utilizarem na avaliação, no gerenciamento e no monitoramento do uso da tecnologia da informação nas suas organizações, o **CobiT** (_Control Objectives for Information and related Technology),_ que estabelece relacionamentos com os requisitos do negócio, organiza as atividades de TI em um modelo de processos genéricos, identifica os principais recursos de TI que devem possuir mais investimentos e define os objetivos de controle que devem ser considerados para a gestão e, a biblioteca  **ITIL** (_Information Technology Infrastructure Library_) que é um modelo de gerenciamento de serviços de TI.

Na adoção de frameworks de Governanças em TI, é fundamental a participação de alta gestão, pois ninguém melhor do que ela para entender o negócio e comunicar à TI suas demandas e necessidades de negócio. Assim, as decisões a serem tomadas podem ser coerentes e trazer benefícios para o negócio, fazendo com que os investimentos de TI deixem de ser vistos somente como custos e ofereçam verdadeiros diferenciais competitivos para a organização.

Mesmo empresas de pequeno ou médio porte podem implementar a Governança em TI. Conforme Prado (2014, p. 30):

> “Uma alternativa é a contratação de serviços de TI de empresas especializadas ou das operadoras de telefonia. Ainda assim, isto demanda processos internos de gerenciamento dos fornecedores e dos níveis de serviço, para garantir o adequado funcionamento da TI, dos processos de negócio e que a empresa esteja pagando um valor justo pelos serviços que contrata: devem ser proporcionais às necessidades e ao faturamento” 

Diante de tudo que foi discutido, então, a implementação dos recursos tecnológicos (que envolvem os sistemas de informação e as tecnologias da informação e comunicação) necessários ao apoio à gestão da empresa merece atenção especial dos gestores quanto a seus processos, recursos e pessoas envolvidas. Esse é o papel fundamental do profissional de Sistemas de Informação: prover esse conhecimento, essa ligação entre as tecnologias e os objetivos da empresa, sempre de forma eficiente e eficaz.

O link abaixo apresenta uma importante leitura sobre os impactos da quarta Revolução Industrial, fundada no uso intenso das tecnologias da informação. O texto apresenta uma interessante análise das principais tecnologias no Brasil, levantando a discussão se ele será uma potência sustentável com condições de capturar as oportunidades que surgem com as mudanças econômicas, ambientais, sociais e éticas provocadas pelas novas tecnologias. O texto, muito atual, é um ótimo direcionador para todos os profissionais e empresas.

[Clique aqui](https://periodicos.fgv.br/gvexecutivo/article/view/74093/71080)

4 - **Conclusão**

Enfim, chegamos ao final da unidade. Nela, percebemos como as Tecnologias da Informação e Comunicação (TICs) são elemento fundamental para as operações de um SI. Estudamos conceitos importantes como Hardware, Software, Bancos de Dados e Redes de Computadores, bem como tecnologias de ponta inovadoras, que, de fato, estão revolucionando o modo como os negócios são feitos. Percebemos também a importância do alinhamento dos recursos de TI e a gestão da empresa, o que chamamos de Governança de TI. Nas próximas unidades, entenderemos como diferentes tipos de Sistemas de Informação se aplicam às diferentes organizações e o que as empresas de ponta têm utilizado desses recursos.

--- 
Texto - Novos Negócios baseados em internet das coisas 


E:\Documentos\UVV\Fundamentos do sistema de informacao

---
Texto - Os impactos da Quarta Revolução Industrial

E:\Documentos\UVV\Fundamentos do sistema de informacao

---
Aula - vídeo 01

Quais são os principais elementos do sistema de informação.

![[Pasted image 20240215091416.png]]
Os recursos iram automatizar atividades que eram feitas manualmente. 

- O papel (dentro de um sistema maior) das tecnologias da Informação busca atingir os objetivos da organização. Novamente, percebemos que a TI é um meio, e não um fim;
- LAUDON (2011, p. 73) nos fornece um guia para melhor utilizar os recursos de TI:
		1) Identifique a estratégia e metas de seu negócio;
		2) Transforme essas metas estratégicas em atividades e processos concretos;
		3) Defina de que maneira irá avaliar o progresso em direção às metas do negócio (ou seja, as métricas);
			Pergunte-se: "Como a tecnologia da informação pode me ajudar a progredir rumo às metas empresariais e de que maneira ela vai aprimorar os processos e as atividades de negócio?"
		4) avalie o desempenho atual. Deixe que os números falem.

![[Pasted image 20240215210515.png]]
![[Pasted image 20240215210553.png]]

Hardware: é um elemento físico.

![[Pasted image 20240215210939.png]]![[Pasted image 20240215211121.png]]
![[Pasted image 20240215211351.png]]
![[Pasted image 20240215211500.png]]
![[Pasted image 20240215211532.png]]
![[Pasted image 20240215211617.png]]![[Pasted image 20240215211651.png]]

---
Aula - vídeo 02

![[Pasted image 20240215212000.png]]
![[Pasted image 20240215212503.png]]

O mais importante são as pessoas

![[Pasted image 20240215212524.png]]![[Pasted image 20240215212603.png]]
![[Pasted image 20240215212636.png]]

---
BI em 5 minutos 
Quais as perguntas de negócio o Business Intelligence responde?

analisa o passado para os gestores tomem decisões melhores.


- O que acontece
- quantos vezes isso aconteceu 
- quando isso ocorreu
- onde isso ocorreu 
- quem fez isso

---

Aula ao vivo 21/02/2024

Conceitos e elementos de um sistema de informação 

`O que vamos aprender?`

- Termos báscios em hardware
- termos básicos em software
- termos básicos em rede

	TI É UM RECURSO ALINHADO AOS OBJETIVOS DA ORGANIZAÇÃO. GOVERNANÇA


`Termos báscios em hardware`

#CPU 

pesa central do computador, trabalha com todos os cálculos de decisão lógica;

Letra K: CPU desbloqueada, é uma CPU que é possivel fazer um overclock

![[Pasted image 20240221193730.png]]
*Tirar print da gravaçaõ da aula*



- Armazenamento
Unidade de armazenamento volátil: armazenada dados enquanto são utilizadas (memória RAM), quando vc desliga o computador esse memória é deletada.

Unidade de armazenamento permanente: 

## VER ATÉ OS 52 MIN DA AULA

Processamento sequencial: quando a CPU consegue realiza uma tarefa por vez. Nenhum processador atual é sequencial mais.

Processamento Paralelo : quando a CPU consegue realizar mais de 1 tarefa ao mesmo tempo. Também chamado de processador multicore


- THREAD: com a evolução das CPUs, os fabricantes conseguiram fazer com que cada núcleo da CPU seja dividida, a thread é uma divisão dentro dos cores das CPUs, melhorando os seus desempenhos.



- Cooler
Feito para dissipar o calor dentro do computador 

- Placa mãe
O chipset é o que determina quais as funcionalidades que a placa-mãe vai ter 

---
Aula ao vivo dia 22/02

- Memória Ram
Área de armazenamento volátil, os dados ficam na memória RAM enquanto há circuito elétrico pelo computador.

Existem em diversos modelos e especificações 

*DDR* = formato da memória ("Double data ratio");

As memórias podem ser encontradas em diversas taxas de transferências.

A placa mãe especifica o tipo de memória que ela comporta. Também é necessário saber se o processador é compatível.

As memórias podem ser de PC ou de servidor. As memórias de PC são de não ECC, as de servidores são ECC, elas possuem um mecanismo de detecção e correção de erro, elas são bem mais caras, e não é qualquer placa-mãe que suporta essas memórias.

A latência de memoria é o tempo que ela demora para receber a requisição do dado, achar o dado e enviar para o CPU.

A memória RAM é o local aonde os programas vão rodar.

`memória principal` - realmente existe no computador

`memória virtual` -  espaço de de endereços de memória muito mair do que a memória principal, e os programas rodam nesse espaço virtual.

há diversos tipos de memórias
-Registradores
mais rápida. 
Fica dentro da CPU
É extremamente cara.


-CPU cache
são rápidas
ou ficam dentro da CPU (chamadas chace l1) ou fora da cpu (l2 ou l3) e ficam na placa mãe

-RAM

-Dispositivos de Armazenamento em Massa

O registrador é o padrão pelo qual se mede a velocidade de registros da memória.


- PLACA DE VÍDEO
na placa de vídeo não há CPUs e sim GPUs
As GPUs são mais rápidas que as CPUs.
São feitos os cálculos para processar os programas mais pesados

- HD/SSD
no HD (Hard disc Drive) há um disco físico aonde é feito os armazenamentos de dados.
Os HD são mais lentos, porém são mais baratos. é completamente mecânico.

O SSD (Solid State Drive)não possui partes mecânicas, possui vários chips de memórias que não perdem o armazenamento após o fim de carga elétrica. 

Também surgiram o SSHD, que são as misturas desses dois.

*Tecnologia M2* - é parecida com SSD, é encaixado na placa-mãe.

- Gabinete
a gosto do freguês

- Fonte
passa energia para a placa-mão 
As fontes que possuem certificações de segurança "80 plus"
É necessário olhar a potencia da fonte.

fonte modular é uma fonte que não vem com os cabos fixos nela.

Utilizar protetor de surto

- Periféricos
a vontade do fregues 

- Sistema Operacional 
Faz o meio de campo entre o hardware e o usuário.
Os mais comuns são o: Windows, MacOS e Linux.
Os sis. operacional para celular mais famosos são o: android e iOS



`Termos básicos em software: servidor x cliente`

- Servidor
uma maquina que fica disposição e aguarda requisições de dados e/ou serviços.
Geralmente não possuem interface gráfica

- Cliente
Maquina que solicita dados


`Bancos de dados`
- BD x SGBD

`IP, Máscara,GW`

![[Pasted image 20240222151705.png]]

- IP (Internet Protocal): endereço do computador
o formato é de 4 grupos de números de 0 a 255 

Quando o computador A quer mandar mensagem para o computador B ele bota a mensagem dentro de um envelope que navega pela rede até chegar no computador B.

Além do saber o endereço do computador, é necessário saber o endereço do Gateway

- DHCP
é o protocolo de configuração dinamica de host
Distribui os endereços IPs para quem está conectado daquela rede.