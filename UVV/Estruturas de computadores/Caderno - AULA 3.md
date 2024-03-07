# Aula gravada

Neste Tópico, você irá aprender como diferentes dispositivos podem se conectar às redes atuais. Esses dispositivos utilizam vários meios como cobre, fibra ótica e sem fio para se conectarem a uma rede e se comunicarem. Você também conhecerá e aprenderá sobre como os dispositivos intermediários, como switchs e roteadores, asseguram que os dados fluam entre a origem e o destino e conhecerá os tipos de redes às quais esses dispositivos se conectam, como redes LANs, WLANs, PANs, MANs e WANs.

Além disso, você entenderá como os dispositivos concordam com regras para se comunicarem corretamente e entenderá como ocorre o processo de comunicação através do estudo do modelo OSI e da pilha de protocolos TCP/IP. À medida em que estudará os protocolos, você conhecerá também o padrão ethernet, os tipos de endereços e o uso de portas. Todos esses elementos suportam o processo de comunicação entre os dispositivos em uma rede.

As redes são sistemas formados por ligações (links). Por exemplo: estradas que conectam grupos de pessoas criam uma rede física. Conexões com seus amigos criam sua rede pessoal. Sites que permitem que cada um crie sua própria página são chamados de rede social.

Para que se tenha uma rede funcional, uma série de dispositivos e ligações devem existir para suportar o trânsito de mensagens entre os diversos aplicativos utilizados pelos usuários. Equipamentos como switchs e roteadores são comuns desde redes domésticas ou pequenas empresas até as redes de médio e grande porte, como grandes corporações ou provedores de Internet.

- *Aula 1 gravada*

![[Pasted image 20240226185820.png]]

Há uma rede de computadores quando há 2 ou mais computadores interligados.

![[Pasted image 20240226185854.png]]

Oque caracteriza um dispositivo final é que as aplicações que a gente utiliza estão instaladas nesse dispositivos.

Não necessariamente o dispositivo de destino está conectado diretamente ao dispositivo de origem nesse caso, precisamos de dispositivos intermediários que são conectados ao dispositivo final para fornecer um caminho disponível para que uma mensagem saia de uma aplicação em um dispositivo origem e chegue no dispositivo de destino. Para isso utilizamos os dispositivos intermediários.

Para liga-los usamos os meios de rede, carrega a mensagem do dispositivo de origem até o final

*Diferença entre o switch e o roteador*
O Switch é responsável por encaminhar mensagens dentro da mesma rede.
O roteador encaminha mensagens para outras redes.

Esses dispositivos para estarem conectados precisam de meios de rede (Ex: cabo, sem fio)

![[Pasted image 20240226190907.png]]

Nas redes peer-to-peer os proprios computadores dos indivíduos fazem o trabalho de cliente e servidor. Não é defino o papel de cliente e servidor. O servidor nao necessariamente está disponível 

Nas redes cliente-servidor o papel do cliente e servidor é bem definido. o servidor ta sempre disponível.

- *Aula gravada 2*
![[Pasted image 20240226193017.png]]

A padronização do setor de rede é importante para ter a interoperacionalidade.

há organizações especificas da industrias que são responsáveis por determinar esses padrões. 

O modelo OSI apresenta 7 camadas: 
- aplicação (7)
- apresentação (6)
- sessão (5)
- transporte (4)
- rede (3) 
- Enlace de dados (2)
- Fisica (1)

Por outro lado na prática é aplicado o modelo TCP/IP:
- Aplicação
- Transporte
- Internet 
- acesso à rede

As 3 camadas superiores do modelo OSI são a camada de aplicação do TCP, a de rede é a de internet, e as ultimas 2 são de acesso à rede.

A função de cada camada:
- a camada de aplicação cria mensagens de solicitação e respostas
- a camada de transporte usa numero de portas para identificar cada aplicação para mandar as mensagens e encapsula-las, controla o envio dos dados, verifica se houve algum erro, retransmitir os dados e endereça as mensagens.
- a camada de internet oferece caminhos para que um fluxo de mensagens sai do destinatário e chegue no usuário final, e para isso utiliza o endereço IP
- na camada de acesso a rede se utiliza o endereço MAC, e movimenta os dados,
- a camada física é queD gera os sinais elétricos.


![[Pasted image 20240227215848.png]]

As redes sem fio tentam prevenir que ocorram uma colisão, mas se ela acontecer  ela vai continuar transmitindo dados.

![[Pasted image 20240227221122.png]]
![[Pasted image 20240227221159.png]]

![[Pasted image 20240227221351.png]]

O cabo que mais se encontra são os cabos de par trançado

![[Pasted image 20240227221520.png]]

No cabo reto as duas extremidades do cabo possuem o mesmo padrão. No cabo cruzado uma extremidade é um padrão o outro e de outro padrão.

![[Pasted image 20240227224159.png]]

O endereço MAC não muda, vem fabricado no dispositivo.

O endereço MAC movimenta os dados de um dispositivo para o outro, dentro de uma mesma rede, a cada parte da rede que a mensagem viaja, o endereço MAC de cada dispositivo de origem e destino é alterado, porque o dispositivo é alterado. 

Diferente do endereço IP, que tem validade global. O endereço IP é usado para saber aonde encaminhar a mensagem.

Só é possivel omitir uma sequência de 0's do endereço IP.

![[Pasted image 20240227224751.png]]

![[Pasted image 20240227225829.png]]

O endereço de host 255 é o endereço de broadcast, e é utilizado pelo dispositivo que quer enviar uma mensagem para todos os dispositivos de uma mesma rede.

![[Pasted image 20240227230203.png]]

![[Pasted image 20240227230244.png]]

O protocolo TCO gera muito mais mensagens e é muito mais lento que o protocolo UDP. Por outro lado o UDP não é muito confiável.

![[Pasted image 20240227230438.png]]
![[Pasted image 20240227230454.png]]

![[Pasted image 20240227230555.png]]

---
# Cisco

- Conceitos de Redes

As redes de computadores permitem que os usuários compartilhem recursos e se comuniquem. Você pode imaginar um mundo sem e-mails, jornais online, blogs, sites e outros serviços oferecidos pela Internet? As redes também permitem que os usuários compartilhem recursos como impressoras, aplicativos, arquivos, diretórios e unidades de armazenamento. Este capítulo apresenta um resumo dos princípios, padrões e finalidades da rede. Os profissionais de TI devem estar familiarizados com os conceitos de rede para atender às expectativas e necessidades dos clientes e usuários da rede.

Você aprenderá os conceitos básicos de design de rede e como os dispositivos na rede afetam o fluxo de dados. Os exemplos incluem: switches, access points sem fio, roteadores e firewalls. Diferentes tipos de conexão com a Internet, como DSL, cabo, celular e satélite, também são abordados. Você aprenderá sobre as quatro camadas do modelo TCP/IP e as funções e os protocolos associados a cada camada. Você também aprenderá sobre muitas redes e protocolos sem fio. Isso inclui protocolos de LAN sem fio IEEE 802.11, protocolos sem fio para proximidade, como identificação de frequência (RFID), comunicação de campo próximo (NFC) e padrões de protocolo Smart Home, como ZigBee e Z-Wave. Esse conhecimento vai ajudar você a projetar, implementar e solucionar problemas de redes. O capítulo conclui com discussões sobre tipos de cabo de rede; par trançado, fibra óptica e coaxial. Você aprenderá como cada tipo de cabo é construído, como eles transportam sinais de dados e casos de uso apropriados para cada um.

É importante não saber apenas sobre a operação e os componentes da rede de computadores, mas também para criar habilidades práticas. Neste laboratório, você vai criar e testar cabos de rede Ethernet de par trançado sem blindagem (UTP) diretos e cruzados.

- Ícones de rede

Redes são sistemas formados por links. As redes de computadores conectam dispositivos e usuários entre si. Uma variedade de ícones de rede é usada para representar diferentes partes de uma rede de computadores.

**Dispositivos Host**

Os dispositivos de rede com os quais as pessoas estão mais familiarizados são chamados de dispositivos finais ou dispositivos host (Figura 1). Eles são chamados de dispositivos finais, pois estão no fim ou na borda de uma rede. Eles também são chamados de dispositivos de host, pois normalmente hospedam aplicativos de rede, como navegadores da Web e clientes de e-mail, que usam a rede para fornecer serviços ao usuário.

![[Pasted image 20240219192737.png]]

**Dispositivos intermediários**

As redes de computadores contêm muitos dispositivos que existem entre os dispositivos host. Esses dispositivos intermediários asseguram que os dados fluam de um dispositivo host para outro. Os dispositivos intermediários mais comuns são mostrados na Figura 2:

- **Switch** - conecta vários dispositivos à rede.

- **Roteador** - encaminha o tráfego entre redes.

- **Roteador** **Sem fio** - conecta vários dispositivos sem fio à rede e pode incluir um switch para conectar os hosts com fio.

- **Ponto de acesso (AP)** - conecta-se a um roteador sem fio e é usado para estender o acesso de uma rede sem fio.

- **Modem** - conecta uma casa ou pequeno escritório à Internet.

![[Pasted image 20240219193032.png]]

**Meio físico de rede**

A comunicação por uma rede é transmitida por um meio. Ele fornece o canal sobre o qual a mensagem viaja da fonte ao destino. O plural de meio é mídia. Os ícones na Figura 3 representam diferentes tipos de mídia de rede. Redes de área local (LANs), redes de longa distância (WANs) e redes sem fio serão discutidas no próximo tópico. Geralmente, a nuvem é usada em topologias de rede para representar conexões com a Internet. A internet geralmente é o meio de comunicação entre uma rede e outra rede.

![[Pasted image 20240219193050.png]]


- topologias e descrições de rede

I - *PAN*
conecta dispositivos (como mouses, teclados, impressoras, smartphone e tablets) que se encontram dentro do alcance de um indivíduo. Esses dispositivos são, geralmente, conectados com a tecnologia Bluetooth. Bluetooth é uma tecnologia sem fio que permite que os dispositivos se comuniquem em distâncias pequenas.

II - LAN (Local Area Network)
é definida como uma rede que conecta dispositivos cabeados em uma pequena área geográfica. Entretanto, a característica que distingue as LANs hoje em dia é que normalmente elas são usadas por um indivíduo (em casa ou em uma empresa pequena) ou completamente gerenciadas por um departamento de TI, como em uma escola ou uma corporação.

III - VLAN #
permitem que um administrador segmente as portas em um único switch como se fossem vários switches. Isso fornece encaminhamento de dados mais eficiente, isolando o tráfego apenas nas portas em que é necessário. As VLANs também permitem que os dispositivos finais sejam agrupados para fins administrativos. No diagrama, a VLAN 2 cria uma LAN virtual para computadores de TI, mesmo em andares diferentes, e pode ter permissões de rede diferentes definidas que as outras VLANs.

![[Pasted image 20240219193753.png]]

IV - WLAN
é semelhante a uma LAN, mas conecta usuários e dispositivos sem fio em uma pequena área geográfica, em vez de usar uma conexão com fio. A WLAN usa ondas de rádio para transmitir dados entre dispositivos sem fio.

V - WMN
usa vários pontos de acesso para estender a WLAN. A topologia mostra um roteador sem fio. Os dois pontos de acesso sem fio estendem o alcance da WLAN dentro de casa. Da mesma forma, empresas e municípios podem usar WMNs para adicionar rapidamente novas áreas de cobertura.

VI - MAN
é uma rede que abrange uma cidade ou um grande campus. A rede consiste em vários prédios interconectados por backbones de fibra ótica ou sem fio.

VII - WAN (Wide Area Network)
conecta várias redes que estão em locais separados geograficamente. Indivíduos e empresas contratam serviços de WAN. O seu provedor de serviços ou celular conecta você à maior WAN, a Internet. Na figura, as redes de Tóquio e Moscou estão conectadas através da Internet.

VIII - rede virtual privada (VPN)
é usada para conectar-se com segurança a outra rede através de uma rede insegura, como a Internet. O tipo mais comum de VPN é usado pelos trabalhadores remotos para acessar uma rede privada corporativa. Trabalhadores remotos são usuários de rede externos ou remotos. Na figura, os links entre o Trabalhador Remoto 1 e o roteador na sede da empresa representam uma conexão VPN. O Trabalhador Remoto 1 usa o software VPN para fazer login seguro na rede da empresa. O Trabalhador Remoto 2 não está conectado com segurança e não poderá acessar os recursos internos da empresa.

- Breve histórico sobre Tecnologias de Conexão

Na década de 1990, a velocidade da Internet era baixa em comparação com a atual, que agora tem largura de banda para transmitir voz e vídeo, além de dados. Uma conexão dial-up requer um modem interno instalado no computador ou um modem externo conectado por USB. A porta de discagem do modem está conectada a um soquete de telefone usando um conector RJ-11. Quando o modem estiver fisicamente instalado, ele deve estar conectado a uma das portas COM de software do computador. O modem também deve ser configurado com propriedades de discagem local, como o prefixo de uma linha externa e o código de área.

O Assistente para configuração de uma conexão ou rede é usado para configurar um link para o servidor ISP. A conexão à Internet evoluiu do telefone analógico para a banda larga:

**Telefone Analógico**

O acesso à Internet por telefone analógico pode transmitir dados por meio de linhas telefônicas de voz padrão. Esse tipo de serviço usa um modem analógico para fazer uma chamada telefônica para outro modem em um site remoto. Esse método de conexão é conhecido como dialup.

**Rede Digital de Serviços Integrados**

O ISDN (Rede Digital de Serviços Integrado - Integrated Service Digital Network) usa vários canais e pode transportar diferentes tipos de serviços; portanto, ele é considerado um tipo de banda larga. O ISDN é um padrão para enviar voz, vídeo e dados por fios de telefone normais. A largura de banda de ISDN é maior do que a discagem tradicional.

**Banda Larga**

A banda larga usa frequências diferentes para enviar vários sinais na mesma mídia. Por exemplo, os cabos coaxiais usados para levar a televisão a cabo para sua casa podem transmitir transmissões de rede de computadores ao mesmo tempo que centenas de canais de TV. O telefone celular pode receber chamadas de voz e, ao mesmo tempo, usar um navegador da Web.

Algumas conexões de rede de banda larga comuns incluem cabo, linha de assinante digital (DSL), ISDN, satélite e celular. A figura mostra o equipamento usado para se conectar a sinais de banda larga ou transmiti-los.


	*DSL, cabo e fibra*

O DSL e o cabo usam um modem para se conectar à Internet através de um provedor de serviços de Internet (ISP), como mostrado na figura. Um modem DSL conecta a rede de um usuário diretamente à infraestrutura digital da companhia telefônica. Um modem a cabo conecta a rede do usuário a um provedor de serviços de cabo.

**DSL**

A DSL (Digital Subscriber Line - Linha de Assinante Digital) é um serviço sempre conectado, ou seja, não é necessário discar toda vez que quiser se conectar à Internet. Os sinais de voz e de dados são transportados em frequências diferentes nos fios telefônicos de cobre. Um filtro impede que os sinais de DSL interfiram nos sinais de telefone.

**Cabo**

Uma conexão de Internet a cabo não utiliza linhas telefônicas. O cabo usa linhas coaxiais projetadas originalmente para transmitir TV a cabo. Um modem a cabo conecta o seu computador à empresa de TV a cabo. Você pode conectar seu computador diretamente ao modem a cabo. No entanto, conectar um dispositivo de roteamento ao modem permite que vários computadores compartilhem a conexão com a Internet.

**Fibra**

Os cabos de fibra ótica são feitos de vidro ou plástico e usam luz para transmitir dados. Eles têm uma largura de banda muito alta, o que permite que transmitam grandes quantidades de dados. Em algum ponto na conexão com a Internet, seus dados vão atravessar uma rede de fibra. A fibra é utilizada em redes de backbone, grandes data centers e ambientes de empresas de grande porte. As infra-estruturas de cabeamento de cobre mais antigas em casa e nas empresas estão cada vez mais sendo substituídas por fibra. Por exemplo, na figura, a conexão do cabo inclui uma rede HFC (fibra híbrida coaxial) na qual a fibra é usada na última milha até a casa do usuário. Na casa do usuário, a rede volta para o cabo coaxial de cobre.

A escolha da conexão varia dependendo da localização geográfica e da disponibilidade do provedor de serviço.


- Serviço de Internet Sem Fio Com Linha de Visão

A Internet sem fio com linha de Visão é um serviço sempre conectado que usa sinais de rádio para transmitir o acesso à Internet, como mostrado na figura. Os sinais de rádio são enviados de uma torre para o receptor conectado pelo cliente a um computador ou um dispositivo de rede. É necessário que o caminho entre a torre de transmissão e o cliente esteja livre. A torre pode se conectar a outras torres ou diretamente a uma conexão de backbone da Internet. A distância que o sinal de rádio consegue percorrer continuando forte o bastante para fornecer um sinal claro depende da frequência do sinal. Uma frequência mais baixa de 900 MHz pode percorrer até 40 milhas (65 km), enquanto uma frequência mais alta de 5.7 GHz pode percorrer apenas 2 milhas (3 km). Condições climatológicas extremas, árvores e prédios altos podem afetar o desempenho e a intensidade do sinal.

![[Pasted image 20240219202620.png]]

- Satélite

O satélite de banda larga é uma alternativa para clientes que não possam ter conexões DSL ou a cabo. Uma conexão via satélite não exige linha telefônica ou cabo porque usa uma antena parabólica para a comunicação bidirecional. A antena parabólica envia e recebe sinais de/para um satélite que os retransmite para um provedor de serviços, como mostrado na figura. As velocidades de download podem chegar a pelo menos 10 Mb/s, enquanto a velocidade de upload alcança 1/10 desse valor. Leva tempo para o sinal da antena parabólica ser retransmitido para o ISP pelo satélite que orbita a Terra. Por causa dessa latência, fica difícil usar aplicativos sensíveis a tempo, como jogos de vídeo game, VoIP e videoconferência.

- Celular

A tecnologia de telefonia celular depende de torres de celular distribuídas por toda a área de cobertura do usuário para fornecer acesso contínuo aos serviços de telefonia celular e à Internet. Com o advento da terceira geração (3G) da tecnologia celular, os smartphones puderam acessar a internet. As velocidades de download e upload continuam a melhorar com cada iteração da tecnologia de telefone celular.

Em algumas regiões do mundo, os smartphones são a única forma de os usuários acessarem a Internet. Nos Estados Unidos, os usuários estão cada vez mais contando com smartphones para acesso à Internet. De acordo com o Pew Research Center, em 2018 20% dos adultos nos Estados Unidos, não usam banda larga em casa (28% para adultos 18-29). Em vez disso, eles usam um smartphone para acesso pessoal à Internet. Pesquise "Pew Internet Research" para obter estatísticas mais interessantes.

- Hotspot móvel e compartilhamento de Internet

Muitos telefones celulares oferecem a capacidade de conectar outros dispositivos, como mostra a figura. Essa conexão, conhecida como tethering (vínculo), pode ser feita usando Wi-Fi, Bluetooth ou um cabo USB. Depois que o dispositivo estiver conectado, ele pode usar a conexão do celular para acessar a Internet. Quando um celular permite que os dispositivos Wi-Fi se conectem e usem a rede de dados móveis, isso é chamado de hotspot.

![[Pasted image 20240219202756.png]]

- # Protocolos da camada de transporte

![[Pasted image 20240219205955.png]]Network communications involves a suite of protocols known as the Internet Protocol suite or more commonly known as the TCP/IP protocol suite. This protocol suite includes all the protocols used in various aspects of end-to-end network communications, including addressing, routing, and reliability. 

The TCP/IP protocol suite is also a conceptual model that classifies and organizes the various protocols into four different layers: Network Access, Internet, Transport, and Application. The Transport layer includes two protocols: TCP, Transmission Control Protocol, and UDP, User Datagram Protocol. These protocols determine how the data will be delivered, reliably or unreliably. It is up to the network application to choose.

If the application chooses TCP, the data will be delivered reliably with guaranteed delivery and assembled in the proper order. Or it can choose UDP when the data needs to be delivered as quickly as possible, with some tolerance for loss of data. TCP adds some "overhead," which means there will be some additional delay. For example, the Network Application HTTP uses TCP to make sure all the data is delivered reliably. 

Here, the user types in the URL www.MyBank.example. TCP is used to transport the information reliably between the user's computer and the web server. The web server, also using TCP, sends the requested data, the webpage, in separate segments. 

Each segment includes a sequence number so the receiver knows if anything is missing and so it can assemble it in the proper order. UDP is a simpler protocol used to send data as quickly as possible, even if some data doesn't get delivered. Network applications such as those used for sending voice and real-time video can sacrifice some data loss in order for the data to be delivered as quickly as possible. As you can see, UDP does not include any functions for reliability, such as there are no sequence numbers in the UDP segments. 

To summarize, the application such as those that perform file transfers, downloading webpages and email, all use the reliable Transport protocol TCP, whereas UDP is used for applications such as real-time video and voice where speed is more important than reliability. 

![[Pasted image 20240219210511.png]]

![[Pasted image 20240219210650.png]]

- O Modelo TCP/IP

O modelo TCP/IP consiste em camadas que executam as funções necessárias para preparar dados para transmissão por uma rede. O TCP/IP representa dois protocolos importantes: TCP (Transmission Control Protocol - Protocolo de Controle de Transmissão) e IP (Internet Protocol - Protocolo de Internet). O TCP é responsável por rastrear todas as conexões de rede entre o dispositivo de um usuário e vários destinos. O Protocolo da Internet (IP) é responsável por adicionar endereçamento para que os dados possam ser roteados para o destino pretendido.

Os dois protocolos que operam na camada de transporte são TCP (Transport Control Protocol) e UDP (User Datagram Protocol), como mostrado na Figura 1. O TCP é considerado um protocolo de camada de transporte confiável, completo, que garante que todos os dados cheguem ao destino. Ao contrário, o UDP é um protocolo muito simples da camada de transporte que não fornece nenhuma confiabilidade. A Figura 2 realça as propriedades do TCP e do UDP.

![[Pasted image 20240219210741.png]]
![[Pasted image 20240219210749.png]]

- TCP

O transporte TCP é análogo a enviar pacotes que são rastreados da origem ao destino. Se um pedido pelo correio estiver dividido em vários pacotes, um cliente poderá verificar on-line a sequência de recebimento do pedido.

Com o TCP, existem três operações básicas de confiabilidade:

- Numeração e rastreamento de segmentos de dados transmitidos por um dispositivo específico a um host específico

- Confirmar dados recebidos

- A retransmissão de dados não confirmados após um determinado período de tempo

Clique em Reproduzir na figura para ver como segmentos TCP e as confirmações são transmitidos do remetente ao destinatário.

![[Pasted image 20240219210932.png]]
![[Pasted image 20240219210956.png]]
![[Pasted image 20240219211011.png]]
![[Pasted image 20240219211025.png]]
![[Pasted image 20240219211033.png]]
![[Pasted image 20240219211044.png]]
![[Pasted image 20240219211100.png]]

- UDP

O UDP é semelhante a colocar uma carta normal, não registrada, no correio. O remetente da carta não tem conhecimento se o destinatário está disponível para receber a carta. Nem a agência de correio é responsável por rastrear a carta ou informar ao remetente se ela não chegar ao destino final.

O UDP oferece as funções básicas fornecendo segmentos de dados apropriados entre as aplicações, com pouca sobrecarga e verificação de dados. O UDP é conhecido como um protocolo de entrega de melhor esforço. No contexto de redes, a entrega de melhor esforço é referida como não confiável, porque não há confirmação de que o dado é recebido no seu destino.

![[Pasted image 20240219211200.png]]
![[Pasted image 20240219211217.png]]
![[Pasted image 20240219211259.png]]

- Números de porta de aplicativo

TCP and UDP use source and destination port numbers to keep track of application conversations. Every network application is identified by the transport protocol using a well-known port number. The source port number is associated with the application that originated the request, known as the client computer. The destination port number is usually a well-known port number associated with the destination application on the remote device, the server computer. 

In this example, the user has entered the URL, www.netacad, into their web browser. The web browser is sending the information using the network application protocol HTTP, which uses the transport protocol TCP. The user's operating system has selected the TCP source port 1024 to refer to any communications coming from this specific web browser window or process. It is also using the well-known TCP destination port 80 so the www.netacad.com web server knows this data is for its HTTP application. 

After receiving the request from the client, when the www.netacad.com web server sends the server the data it has requested, it will be sent from its TCP source port 80, in other words, from HTTP application. When sending the data to the client, the server will use the client's TCP source port as the TCP destination port, in this case, port 1024. This is so the client knows which specific application this specific web browser window or tab this data is intended for. 

If the client opens up a separate browser window, in this case, entering the URL www.cisco.com, a different TCP source port number will be associated with this specific web browser window. In this case, TCP source port 1555. Although the HTTP request message will be sent to a different server, the same well-known TCP destination port number of 80 is used to indicate this is for the HTTP application. When the www.cisco.com web server sends the specific client the data it has requested, it will be sent from its TCP source port 80, its HTTP application. The server will use the client's TCP source port as the TCP destination port, port 1555. When the client receives this information, it examines the destination port number to know which browser window the data is intended for.

![[Pasted image 20240219211652.png]]

- Classificar números de portas de aplicativo

TCP e o UDP usam números de porta origem e destino para monitorar conversações de aplicações. O número de porta origem está associado à aplicação de origem no dispositivo local. O número de porta destino está associado à aplicação de destino no dispositivo remoto. Essas não são portas físicas. São números usados pelo TCP e UDP para identificar os aplicativos que devem manipular os dados.

O número de porta origem é gerado dinamicamente pelo dispositivo de envio. Esse processo permite que várias conversações ocorram simultaneamente para a mesma aplicação. Por exemplo, quando você usa um navegador web, pode ter mais de uma guia aberta em um determinado momento. O número de porta destino é 80 para o tráfego web normal ou 443 para o tráfego web seguro. Esses são chamados de números de porta conhecidos, porque são consistentemente usados pela maioria dos servidores da Web na Internet. Mas a porta origem será diferente para cada guia aberta. É assim que o computador sabe para qual guia do navegador web entregar o conteúdo web. Da mesma forma, outros aplicações de rede (como e-mail e transferência de arquivos) têm seus próprios números de porta atribuídos.

Há uma série de tipos diferentes de protocolos de camada de aplicação que são identificados por números de porta TCP ou UDP na camada de transporte.

- Protocolos relacionados à World Wide Web (Figura 1)

![[Pasted image 20240219211851.png]]

- Protocolos de gerenciamento de e-mail e identidade. (Figura 2)

![[Pasted image 20240219211924.png]]

- Protocolos de gerenciamento e transporte de arquivos (Figura 3)

![[Pasted image 20240219212012.png]]

$ A CISCO fala que a AFP é TCP no 5.2.2.3

- Protocolos de acesso remoto. (Figura 4)

![[Pasted image 20240219212046.png]]

- Protocolos de operações de rede. (Figura 5)

![[Pasted image 20240219212119.png]]

A Figura 6 mostra uma tabela de Resumo de todos esses protocolos de aplicação listados na ordem do protocolo.

![[Pasted image 20240219212132.png]]

- Protocolos WLAN

Os padrões do Instituto de engenheiros elétricos e eletrônicos (IEEE) para Wi-Fi, conforme especificado no grupo de padrões coletivo 802.11 que especificam as frequências de rádio, velocidades e outros recursos para WLANs. Diversas implementações do padrão IEEE 802.11 foram desenvolvidas ao longo dos anos, como mostrado na figura.

Os padrões 802.11a, 802.11b e 802.11g são considerados antigos. As novas WLANs devem implementar dispositivos 802.11ac. As implementações de WLAN atuais devem fazer a atualização para o 802.11ac ao comprar novos dispositivos.

![[Pasted image 20240220195333.png]]

- Bluetooth, NFC, e RFID

Os protocolos sem fio para a conectividade por proximidade incluem Bluetooth, identificação por radiofrequência (RFID) e comunicação de campo near-line (NFC).

**Bluetooth**

Um dispositivo Bluetooth pode conectar até sete outros dispositivos Bluetooth, como mostra a Figura 1. Descritos no padrão IEEE 802.15.1, os dispositivos Bluetooth operam na faixa de radiofrequência de 2,4 a 2,485 GHz e geralmente são usados para PANs. O padrão Bluetooth incorpora o recurso AFH (Salto de Frequência Adaptável - Adaptive Frequency Hopping). O AFH permite que os sinais "saltem" usando diferentes frequências dentro do alcance do Bluetooth, reduzindo assim a possibilidade de interferência quando houver vários dispositivos Bluetooth presentes.

**RFID**

A RFID usa as frequências no intervalo de 125 MHz a 960 MHz para identificar exclusivamente os itens, como em um departamento de remessa, como mostrado na Figura 2. As Tags RFID ativas que contêm uma bateria podem transmitir sua ID até 100 metros. As tags de RFID passivas dependem do leitor de RFID para usar ondas de rádio para ativar e ler a tag. As etiquetas RFID passivas são normalmente usadas para escaneamento próximo, mas têm um alcance de até 25 metros.

**NFC**

A NFC usa a frequência de 13,56 MHz e é um subconjunto dos padrões RFID. O NFC foi projetado para ser um método seguro para concluir as transações. Por exemplo, um consumidor paga por bens ou serviços acenando com o telefone perto do sistema de pagamento, como mostra a Figura 3. Com base em um ID exclusivo, o pagamento é cobrado diretamente em uma conta pré-paga ou conta bancária. O NFC também é usado em serviços de transporte público, no setor de estacionamento público e em muitas outras áreas de consumo.

![[Pasted image 20240220203245.png]]

- ZigBee e Z-Wave

O ZigBee e o Z-Wave são dois padrões de casa inteligentes que permitem que os usuários conectem vários dispositivos em uma rede de malha sem fio. Normalmente, os dispositivos são gerenciados a partir de um aplicativo para smartphone, conforme mostrado na figura.

**ZigBee**

O Zigbee usa rádios digitais de baixa potência, baseados no padrão sem fio IEEE 802.15.4 para redes de área pessoal sem fio de baixa taxa (LR-WPANs), destinadas a serem usadas por dispositivos de baixo custo e baixa velocidade. O ZigBee opera nas frequências de 868 MHz a 2,4 GHz e é limitado a 10 a 20 metros. O ZigBee tem uma taxa de dados de 40-250 KB/s e pode suportar aproximadamente 65.000 dispositivos.

A especificação de ZigBee depende de um dispositivo principal chamado de coordenador de ZigBee. Com a tarefa de gerenciar todos os dispositivos de cliente ZigBee, o coordenador de ZigBee é responsável pela criação e manutenção da rede ZigBee.

Embora ZigBee seja um padrão aberto, os desenvolvedores de software devem ser um membro pago da Aliança de ZigBee para usar e contribuir com o padrão.

**Z-Wave**

A tecnologia Z-Wave é um padrão proprietário que agora é de Propriedade do Silicon Labs. No entanto, uma versão pública da camada de interoperabilidade de Z-Wave foi aberta em 2016. Esses padrões de código aberto Z-Wave incluem a segurança S2 de Z-Wave, Z/IP para transportar sinais de Z-Wave em redes IP e middleware de Z-Ware.

O Z-Wave opera em uma variedade de frequências com base no país de 865,2 MHz na Índia para 922-926 MHz no Japão. O Z-Wave opera em 908,42 MHz na América do Norte. O Z-Wave pode transmitir dados de até 100 metros, mas tem uma taxa de dados mais lenta do que ZigBee a 9,6-100 KB/s. O Z-Wave pode suportar até 232 dispositivos em uma rede de malha sem fio.

Pesquise "ZigBee e Z-Wave" na Internet para conhecer as informações mais recentes sobre esses dois padrões Smart Home.

**O mercado doméstico inteligente**

O mercado de produtos de casas inteligentes continua crescendo. De acordo com o Statista.com, o número de casas inteligentes foi 34,8 milhões em 2018, que foi um aumento de 28,4% de 2017. O mercado doméstico inteligente continuará a oferecer oportunidades econômicas para indivíduos e empresas.

![[Pasted image 20240220204026.png]]
![[Pasted image 20240220204033.png]]
![[Pasted image 20240220204044.png]]
![[Pasted image 20240220204053.png]]
![[Pasted image 20240220204107.png]]
![[Pasted image 20240220204125.png]]
![[Pasted image 20240220204140.png]]
![[Pasted image 20240220204328.png]]

-  Serviços de rede
A client computer uses client software to request the service of a server. The server computer uses server software to provide services to one or more clients. DHCP or Dynamic Host Configuration Protocol is a network service that allows a DHCP server to provide addressing information to client computers. This DHCP client has been configured to obtain its addressing information automatically from a DHCP server. This is the default on most user computers and devices. 

The DHCP client sends a DHCP request message asking the DHCP server for this information. The DHCP server may be a local router or a server computer. The DHCP server will then respond with the appropriate addressing information. This will include a specific IP address for the client, and can also include an address for the default gateway and a DNS server. 

DNS, or Domain Name System, is a network service that provides an IP address for a known domain name, such as a URL. In this example, the user has entered the URL, www.netacad.com into a web browser. However, to request this information from the web server, the client needs to know the IP address of the web server. The client sends the DNS server a DNS request message, asking for the IP address associated with the domain name, www.netacad.com. The DNS server will determine the answer, and respond to the client's request with the proper IP address. 

The client can now send its HTTP request to the www.netacad.com web server. HTTP, or HyperText Transfer Protocol, is a network service that provides for the delivery of worldwide web messages between a client web browser and a web server. The HTTP client, using a web browser, requests the information associated with a specific URL from a web server. The HTTP server, or web server, responds by sending the client the files associated with this specific website. This may include HTML code, images, audio and video. 

- Funções do servidor

Todos os computadores conectados a uma rede que participam diretamente na comunicação de rede são classificados como hosts. Hosts também são chamados dispositivos finais. Os hosts em redes executam uma determinada função. Alguns desses hosts realizam tarefas de segurança, enquanto outros fornecem serviços web. Existem também muitos sistemas integrados ou legados que executam tarefas específicas, como serviços de arquivo ou de impressão. Os hosts que fornecem serviços são chamados de servidores. Os hosts que usam esses serviços são chamados de clientes.

Cada serviço exige um software de servidor separado. Por exemplo, um servidor exige um software de servidor Web para forneça serviços web à rede. Um computador com software de servidor pode fornecer serviços simultaneamente para um ou vários clientes. Além disso, um único computador pode executar vários tipos de software de servidor. Em casa ou em uma empresa pequena, pode ser necessário que um computador atue como um servidor de arquivos, um servidor Web e um servidor de e-mail.

Os clientes precisam de um software instalado para solicitar e exibir as informações obtidas do servidor. Um exemplo de software cliente é um navegador, como Chrome ou FireFox. Um único computador pode também executar vários tipos de software cliente. Por exemplo, um usuário pode verificar e-mails e exibir uma página Web enquanto envia mensagens instantâneas e ouve rádio pela Internet.

![[Pasted image 20240220204803.png]]
![[Pasted image 20240220204809.png]]
![[Pasted image 20240220204815.png]]

- Servidor DHCP

Um host precisa de informações de endereço IP para poder enviar dados na rede. Dois serviços importantes de endereço IP são o DHCP (Dynamic Host Configuration Protocol) e o DNS (Serviço de Nomes de Domínio).

DHCP é um serviço usado por ISPs, administradores de rede e roteadores sem fio para atribuir automaticamente informações de endereçamento IP a hosts, como mostrado na Figura.

![[Pasted image 20240220204840.png]]

- Servidor DNS

DNS é o método usado pelos computadores para converter nomes de domínio em endereços IP. Na Internet, esses nomes de domínio, como http://www.cisco.com, são muito mais fáceis de serem lembrados pelas pessoas do que 198.133.219.25, que é o verdadeiro endereço IP numérico desse servidor. Se a Cisco decidir alterar o endereço IP numérico do site www.cisco.com, o usuário não tomará conhecimento disso porque o nome de domínio permanecerá o mesmo. O novo endereço é simplesmente vinculado ao nome de domínio atual e a conectividade é mantida.

As figuras de 1 a 5 mostram os passos envolvidos na resolução DNS.

![[Pasted image 20240220204924.png]]
![[Pasted image 20240220204930.png]]
![[Pasted image 20240220204935.png]]
![[Pasted image 20240220204940.png]]
![[Pasted image 20240220204945.png]]

- Servidor de Impressão

Os servidores de impressão permitem que vários usuários de computador acessem uma única impressora. Um servidor de impressão tem três funções:

- Fornecer acesso do cliente a recursos de impressão.

- Gerenciar trabalhos de impressão mantendo-os em uma fila até que o dispositivo de impressão esteja pronto e depois alimentando informações de impressão ou enviando-as para o spool da impressora.

- Oferecer feedback a usuários.


- Servidor de arquivos

O File Transfer Protocol (FTP) oferece a capacidade de transferir arquivos entre um cliente e um servidor. Um cliente FTP é um aplicativo em um computador que serve para enviar e receber arquivos de um servidor que executa FTP como um serviço.

Como a figura ilustra, para transferir dados com sucesso, o FTP precisa de duas conexões entre o cliente e servidor, uma para comandos e respostas, outra para a transferência real de arquivos.

O FTP tem muitas deficiências na segurança. Portanto, devem ser usados serviços de transferência de arquivos mais seguros, como um destes:

- **Protocolo FTPS (Protocolo Seguro de Transferência de Arquivos)** – Um cliente FTP pode requisitar que uma sessão de transferência de arquivos seja criptografada. O servidor de arquivos pode aceitar ou recusar a requisição.

- **SSH File Transfer Protocol (SFTP)** - Como uma extensão do protocolo Secure Shell (SSH), o SFTP pode ser usado para estabelecer uma sessão segura de transferência de arquivos.

- **SCP (Cópia Segura)** – O SCP (Secure Copy Protocol) também usa o SSH para proteger transferências de arquivos.
![[Pasted image 20240220205038.png]]

- Servidor Web

Os recursos web são fornecidos por um servidor web. O host acessa os recursos web através dos protocolos HTTP ou HTTP seguro (HTTPS). HTTP é um conjunto de regras para a troca de texto, imagens gráficas, som e vídeo na Internet. O HTTPS adiciona serviços de criptografia e autenticação usando o protocolo SSL (Secure Sockets Layer) ou o protocolo TLS (Transport Layer Security) mais recente. O HTTP opera na porta 80. O HTTPS opera na porta 443.

Para entender melhor como o navegador web e o cliente web interagem, podemos examinar como uma página web é aberta em um navegador. Neste exemplo, use a URL http://www.cisco.com/index.html.

Primeiro, como mostra a Figura 1, o navegador interpreta as três partes da URL:

**http**(protocolo ou esquema)

**www.cisco.com**(nome do servidor)

**index.html**(nome da arquivo específico requisitado)

O navegador verifica com um servidor de nomes de domínio (DNS) para converter www.cisco.com em um endereço numérico, usado para conectar-se ao servidor. Usando os requisitos de HTTP, o navegador envia uma solicitação GET ao servidor e solicita o arquivo index.html, conforme mostrado na Figura 2. O servidor envia o código HTML dessa página web para o navegador do cliente, como mostrado na Figura 3. Finalmente, como mostra a Figura 4, o navegador interpreta o código HTML e formata a página na janela do navegador.

![[Pasted image 20240223223734.png]]![[Pasted image 20240223223740.png]]
![[Pasted image 20240223223748.png]]
![[Pasted image 20240223223753.png]]

- # Servidor de e-mail

O e-mail precisa de várias aplicações e serviços, como mostrado na figura. O e-mail é um método de armazenar, de enviar e de recuperar mensagens eletrônicas em uma rede. Mensagens de e-mail são armazenadas nos bancos de dados em servidores de e-mail.

Os clientes de e-mail se comunicam com os servidores de e-mail para enviar e receber e-mails. Os servidores de e-mail se comunicam com outros servidores de e-mail para transportar mensagens de um domínio para outro. Um cliente de e-mail não se comunica diretamente com outro para enviar e-mails. Em vez de isso, os clientes confiam nos servidores para transportar mensagens.

O e-mail suporta três protocolos separados para a operação: Simple Mail Transfer Protocol (SMTP - Protocolo de Transferência de Correio Simples), Post Office Protocol (POP - Protocolo dos Correios) e Internet Message Access Protocol (IMAP - Protocolo de Acesso a Mensagem da Internet). O processo da camada de aplicação que envia e-mail usa o SMTP. Um cliente recupera e-mails usando um dos dois protocolos da camada de aplicação: POP ou IMAP.

- # Servidor Proxy

Os servidores proxy têm autoridade para atuar como outro computador. Um uso conhecido dos servidores proxy é agir como armazenamento ou cache para páginas web que são acessadas com frequência por dispositivos na rede interna. Por exemplo, o servidor proxy na figura está armazenando páginas web de www.cisco.com. Quando algum host interno envia uma requisição GET HTTP para www.cisco.com, o servidor proxy faz o seguinte:

1. Intercepta as requisições.

2. Verifica se o conteúdo do site mudou.

3. Caso contrário, o servidor proxy responde ao host com a página web.

Além disso, um servidor proxy pode efetivamente ocultar os endereços IP de hosts internos porque todas as requisições que saem para a Internet são originadas pelo endereço IP do servidor proxy.


 - Servidor de autenticação

O acesso a dispositivos de rede normalmente é controlado através de serviços de autenticação, autorização e contabilização. Conhecidos como AAA (Authentication Authorization Accounting) ou "triplo A", esses serviços fornecem a estrutura primária para configurar o controle do acesso em um dispositivo de rede. O AAA é uma forma de controlar quem acessa uma rede (autenticação), o que pode fazer enquanto permanece nela (autorização) e quais ações realiza ao acessar a rede (contabilização).

Na figura, o cliente remoto passa por um processo de quatro etapas para se autenticar com um servidor AAA e obter acesso à rede.

![[Pasted image 20240223223943.png]]

-  Servidor Syslog

Muitos dispositivos de rede são compatíveis com syslog, incluindo: roteadores, switches, servidores de aplicativos, firewalls e outros dispositivos de rede. O protocolo syslog permite que os dispositivos de rede enviem suas mensagens de sistema por meio da rede para servidores syslog.

O serviço de logging de syslog oferece três funções principais:

- A capacidade de coletar informações de registro para monitorar e solucionar problemas

- A capacidade de selecionar o tipo de informações de registro que são capturadas

- A capacidade de especificar destinos de mensagens syslog capturadas

![[Pasted image 20240223224029.png]]


- `Dispositivos básicos de rede`

https://contenthub.netacad.com/legacy/ITE/7.01/pt/index.html#5.3.1.1

Ethernet Switch conecta dispositivos como computadores, impressouras  e roteadores que estão na mesma ethernet local area network.

Os dispositovs se conectam através do Macaddress.

![[Pasted image 20240223224652.png]]

![[Pasted image 20240223224639.png]]
![[Pasted image 20240223224711.png]]


- Placa de interface de Rede

Uma placa de interface de rede (NIC) fornece a conexão física à rede no PC ou outro dispositivo final. Como mostra a figura, existem diferentes tipos de NICs. As NICs Ethernet são usadas para conexão a redes Ethernet, e as placas de rede sem fio são usadas para conexão a redes sem fio 802.11. A maioria das NICs em desktops é integrada à placa-mãe ou está conectada a um slot de expansão. As placas de rede também estão disponíveis no formato USB.

Uma NIC também desempenha a importante função de endereçar dados com o endereço de controle de acesso à mídia (MAC) da NIC e enviar os dados como bits na rede. As placas de rede encontradas na maioria dos computadores atualmente têm capacidade para gigabit Ethernet (1000 Mbps).

**Observação**: os computadores e as placas-mãe de hoje normalmente têm placas de rede integradas, incluindo o recurso sem fio. Consulte as especificações do fabricante para obter mais informações.

- Repetidores, bridges e hubs

Nos primórdios da rede, as soluções como o uso de repetidores, hubs e pontes foram criadas para adicionar mais dispositivos à rede.

**Repetidor**

Regenerar sinais fracos é a principal finalidade de um repetidor, como mostrado na Figura 1. Os repetidores também são chamados de extensores porque estendem a distância que um sinal pode percorrer. Nas redes atuais, os repetidores são usados com mais frequência para regenerar sinais em cabos de fibra ótica. Além disso, todo dispositivo de rede que recebe e envia dados regenera o sinal.

![[Pasted image 20240223224917.png]]

**Hub**

Os hubs, como mostra a Figura 2, recebem dados em uma porta e os enviam para todas as outras portas. Um hub estende o alcance de uma rede porque regenera o sinal elétrico. Os hubs podem se conectar a outro dispositivo de rede, como um switch ou um roteador, que se conecta a outras seções da rede.

Os hubs são dispositivos legados e não devem ser usados nas redes atuais. Os hubs não segmentam o tráfego de rede. Quando um dispositivo envia tráfego, o hub inunda esse tráfego para todos os outros dispositivos a ele conectados. Os dispositivos compartilham a largura de banda.

![[Pasted image 20240223224925.png]]


**Bridge**

As bridges foram introduzidas para dividir LANs em segmentos. Elas mantêm um registro de todos os dispositivos em cada segmento. Uma bridge pode filtrar o tráfego de rede entre segmentos de uma LAN. Isso ajuda a reduzir a quantidade de tráfego entre dispositivos. Por exemplo, na Figura 2, se o PC-A precisar enviar um trabalho para a impressora, o tráfego não será mais encaminhado para o Segmento 2. Entretanto, o servidor também receberá o tráfego desse trabalho para impressão.

![[Pasted image 20240223224931.png]]

- Switches

Bridges e hubs passaram a ser considerados dispositivos antigos devido aos benefícios e ao baixo custo dos switches. Como mostrado na Figura 3, um switch microssegmenta uma LAN. Microssegmentar significa que os switches filtram e segmentam o tráfego de rede enviando dados apenas para o dispositivo ao qual eles são enviados. Isso fornece largura de banda dedicada mais elevada para cada dispositivo na rede. Quando PC-A enviar um trabalho para a impressora, somente a impressora receberá o tráfego. Os switches e as bridges legado executam a microssegmentação; no entanto, os switches executam essa operação de filtragem e encaminhamento no hardware e também incluem recursos adicionais.

**Operação de Switch**

Cada dispositivo em uma rede tem um endereço de controle de acesso à mídia (MAC) exclusivo. Esse endereço é codificado pelo fabricante da NIC. À medida que os dispositivos enviam dados, os switches inserem o endereço MAC do dispositivo em uma tabela de switching que registra o endereço MAC para cada dispositivo conectado ao switch e registra qual porta do switch pode ser usada para acessar um dispositivo com um determinado endereço MAC. Quando chega tráfego destinado a um endereço MAC específico, o switch usa a tabela de switching para determinar qual porta deve ser usada para acessar o endereço MAC. O tráfego é encaminhado da porta para o destino. Com o envio de tráfego apenas de uma porta para o destino, as outras portas não são afetadas.

**Switches gerenciados e não gerenciados**

Em redes maiores, os administradores de rede geralmente instalam switches gerenciados. Os switches gerenciados são fornecidos com recursos adicionais que o administrador de rede pode configurar para melhorar a funcionalidade e a segurança da rede. Por exemplo, um switch gerenciado pode ser configurado com VLANs e segurança de porta.

Em uma rede doméstica ou de pequena empresa, você provavelmente não precisa da complexidade e despesa adicionais de um switch gerenciado. Em vez disso, você pode considerar a instalação de um switch não gerenciado. Esses switches normalmente não têm interface de gerenciamento. Basta conectá-los à rede e conectar os dispositivos de rede para se beneficiar de recursos de microsegmentação de switch.

- Access points sem fio

Os pontos de acesso sem fio, como mostra a Figura, fornecem acesso à rede para dispositivos sem fio, como laptops e tablets. O ponto de acesso sem fio usa as ondas de rádio para se comunicar com a placa de rede sem fio nos dispositivos e em outros pontos de acesso sem fio. Um ponto de acesso tem um alcance limitado de cobertura. As grandes redes exigem que vários pontos de acesso forneçam cobertura sem fio adequada. Um ponto de acesso sem fio somente proporciona conectividade à rede, enquanto um roteador sem fio proporciona recursos adicionais.

- Roteadores

Switches e APs sem fio encaminham dados dentro de um segmento de rede. Os roteadores podem ter toda a funcionalidade de um switch ou de um AP sem fio. No entanto, os roteadores conectam redes, conforme mostrado na figura. Os switches usam endereços MAC para encaminhar o tráfego dentro de uma única rede. Os roteadores usam endereços IP para encaminhar o tráfego para outras redes. Em redes maiores, os roteadores se conectam a switches, que se conectam a LANs, como o roteador à direita na Figura. O roteador serve como gateway para redes externas.

O roteador à esquerda na Figura também é conhecido como dispositivo multiuso ou roteador integrado. Ele inclui um switch e um ponto de acesso sem fio. Em algumas redes, é mais conveniente comprar e configurar um dispositivo que atenda a todas as suas necessidades do que comprar um dispositivo separado para cada função. Isso acontece principalmente para escritórios residenciais/pequenos escritórios. Os dispositivos multiuso também podem incluir um modem para conectar-se à Internet.

![[Pasted image 20240223225443.png]]

-  Dispositivos de segurança

A firewall is a network security device or software within a device that monitors and controls incoming and outgoing network traffic based on a predetermined set of security rules. 

An integrated router typically contains a switch, a router, and a firewall. 

The firewall acts as a barrier between a trusted internal network and an untrusted external network, such as the internet. Firewalls use various devices to enforce a predetermined set of security rules. This may include one or more access control lists, ACLs, used to determine what type of traffic will be permitted or denied. 

Two other types of security devices are intrusion detection systems, IDSs, and intrusion prevention systems, IPSs. An IDS passively monitors traffic on the network, comparing the captured traffic stream with known malicious signatures. 

An IPS actively monitors traffic before reaching the destination. If the data is acceptable, the traffic is permitted. If the data is unacceptable, then the traffic will be denied. 

-  Dispositivos de segurança

![[Pasted image 20240223225723.png]]

- Firewalls

Um roteador integrado normalmente contém um switch, um roteador e um firewall, como mostrado na figura. Os firewalls protegem dados e equipamentos em uma rede contra acesso não autorizado. Um firewall reside entre duas ou mais redes. Como ele não usa os recursos dos computadores que está protegendo, não há impacto no desempenho do processamento.

Os firewalls usam várias técnicas para determinar o que é permitido ou tem acesso negado em um segmento de rede, como, por exemplo, uma Lista de Controle de Acesso (ACL - Access Control List). Essa lista é um arquivo utilizado pelo roteador que contém regras sobre tráfego de dados entre redes.

**Observação**: em uma rede segura, se o desempenho do computador não for um problema, ative o firewall interno do sistema operacional para obter segurança adicional. Por exemplo, no Windows 10, o firewall é chamado Windows Defender Firewall. Alguns aplicativos podem não funcionar de forma adequada se o firewall não estiver configurado corretamente para eles.

![[Pasted image 20240223230203.png]]

- IDS e IPS

Os Sistemas de Detecção de Intrusão (IDS - Intrusion Detection System) monitoram passivamente o tráfego na rede. Os sistemas IDS independentes deram lugar aos Sistemas de Prevenção de Invasão (IPS - Intrusion Prevention System). Mas o recurso de detecção de um IDS ainda faz parte da implementação de qualquer IPS. A Figura 1 mostra que um dispositivo habilitado para IDS copia o fluxo de tráfego e analisa o tráfego copiado em vez dos pacotes reais encaminhados. Trabalhando off-line, ele compara o fluxo de tráfego capturado com assinaturas reconhecidamente mal-intencionadas, como um software que verifica a existência de vírus.

Um IPS se baseia na tecnologia IDS. Entretanto, um dispositivo IPS é implementado no modo InLine. Isso significa que todo o tráfego de ingresso (entrada) e egresso (saída) deve fluir por ele para processamento. Como mostrado na Figura 2, um IPS não permite que os pacotes ingressem no lado confiável da rede sem primeiro serem analisados.

A maior diferença entre o IDS e o IPS é que um IPS responde imediatamente e não permite que nenhum tráfego malicioso passe, enquanto um IDS permite que tráfego malicioso passe, antes de abordar o problema. No entanto, um IPS mal configurado pode afetar negativamente o fluxo do tráfego na rede.
![[Pasted image 20240223235750.png]]![[Pasted image 20240223235757.png]]

- UTMs

UTM (Gerenciamento Unificado de Ameaças - Unified Threat Management) é um nome genérico para um dispositivo completo de segurança. Os UTMs incluem todas as funcionalidades de um IDS/IPS, além de serviços de firewall stateful. Os firewalls stateful fornecem filtragem de pacotes stateful usando informações de conexão mantidas em uma tabela de estado. Um firewall stateful rastreia cada conexão registrando tanto os endereços de origem e de destino como os números de porta de origem e de destino.

Além de IDS/IPS e serviços de firewall stateful, os UTMs normalmente também fornecem serviços de segurança adicionais, como:

- Proteção de Dia Zero

- Proteção contra Negação de Serviços (DoS - Denial-of-Service) e contra Negação de Serviços Distribuída (DDoS - Distributed Denial-of-Service)

- Filtragem de proxy de aplicações

- Filtragem de e-mail para ataques de spam e de phishing

- Antispyware

- Controle de acesso à rede

- Serviços VPN

Essas funções podem variar consideravelmente, dependendo do fabricante do UTM.

Atualmente, no mercado de firewall, os UTMs agora são chamados de firewalls da próxima geração. Por exemplo, o Cisco Adaptive Security Appliance na figura oferece os recursos mais recentes de firewall de última geração.

![[Pasted image 20240225133535.png]]

- Servidor de gerenciamento de terminal

Um servidor de gerenciamento de Endpoint normalmente é responsável por monitorar todos os dispositivos finais na rede, incluindo desktops, notebooks, servidores, tablets e qualquer dispositivo conectado à rede. Um servidor de gerenciamento de terminal pode restringir a conexão de um dispositivo final à rede se o dispositivo não atender a certos requisitos predeterminados. Por exemplo, é possível verificar se os dispositivos têm o sistema operacional e as atualizações de antivírus mais recentes.

O centro de Digital Network Architecture (DNA) da Cisco é um exemplo de uma solução que oferece gerenciamento de Endpoint. No entanto, o DNA da Cisco é muito mais. É uma solução de gerenciamento abrangente para gerenciar todos os dispositivos conectados à rede, de modo que o administrador de rede possa otimizar o desempenho da rede para oferecer a melhor experiência possível de usuário e aplicativo. As ferramentas para gerenciar a rede estão disponíveis para a interface do Cisco DNA Center, como mostrado na figura.

![[Pasted image 20240225134041.png]]

![[Pasted image 20240225135940.png]]


- Sistemas integrados e legados

Os sistemas legados são aqueles computadores e sistemas de rede que não são mais compatíveis, mas ainda estão em operação nas redes atuais. Os sistemas legados variam de sistemas de controle industrial (ICSs) a sistemas de mainframe de computador e uma ampla variedade de dispositivos de rede, como hubs e pontes. Os sistemas legados são inerentemente vulneráveis a violações de segurança, pois não podem ser atualizados ou corrigidos. Uma solução para aliviar parte do risco à segurança é diminuir o espaço desses sistemas. Air gapping é o processo de isolar fisicamente os sistemas legados de outras redes e particularmente da Internet.

Os sistemas integrados estão relacionados aos sistemas legados, pois muitos sistemas legados têm microchips integrados. Esses microchips incorporados geralmente são programados para fornecer instruções de entrada e saída dedicadas a um dispositivo especializado. Exemplos de sistemas incorporados em casa são coisas como termostato, geladeira, fogão, lava-louças, máquina de lavar, consoles de videogame e TVs inteligentes. Os sistemas integrados estão se tornando cada vez mais conectados à Internet. A segurança deve ser o principal quando o técnico recomenda e instala sistemas incorporados.

- Patch Panel

Um patch panel normalmente é usado como um lugar para coletar cabos de entrada dos diversos dispositivos de rede em uma instalação, como mostrado na Figura. Ele oferece um ponto de conexão entre computadores e os switches ou roteadores. Um patch panel pode ser ou não alimentado por energia. Um patch panel com energia pode regenerar sinais fracos antes de enviá-los para o próximo dispositivo.

Por segurança, assegure-se de que todos os cabos estejam presos usando braçadeiras ou produtos de gerenciamento de cabos e não estejam atravessando passagens ou correndo sob mesas onde possam ser chutados

- Power over Ethernet e Ethernet over Power

A Power over Ethernet (PoE) é um método para alimentar dispositivos que não têm bateria ou acesso a uma tomada elétrica. Um switch PoE transfere pequenas quantidades de corrente CC por um cabo Ethernet, juntamente com os dados, para alimentar dispositivos PoE. Dispositivos de baixa voltagem compatíveis com PoE (como pontos de acesso Wi-Fi, dispositivos de vigilância por vídeo e telefones IP) podem ser alimentados de locais remotos. Os dispositivos com suporte para PoE podem receber alimentação por uma conexão Ethernet em distâncias de até 100m. A energia também pode ser inserida no meio de um cabo que utilize um injetor PoE, como mostrado na Figura 2.

O Ethernet over Power, ou mais comumente chamado de rede powerline, usa a fiação elétrica existente para conectar dispositivos, como mostra a Figura 3. O conceito de “sem novos fios” significa a capacidade de conectar um dispositivo à rede onde quer que haja uma tomada elétrica. Isso reduz o custo de instalar cabos de dados e não há custo adicional à conta de luz. Usando a mesma fiação que fornece a eletricidade, a rede powerline envia informações ao enviar dados em determinadas frequências. A Figura 3 é um adaptador de rede Powerline conectado a uma tomada elétrica.

![[Pasted image 20240225143017.png]]
![[Pasted image 20240225143021.png]]
![[Pasted image 20240225143026.png]]

- Controlador de rede baseado em nuvem

Um controlador de rede baseado em nuvem é um dispositivo na nuvem que permite que os administradores de rede gerenciem dispositivos de rede. Por exemplo, uma empresa de médio porte com vários locais pode ter centenas de pontos de acesso sem fio. Gerenciar esses dispositivos pode ser complicado sem usar algum tipo de controlador.

Por exemplo, Cisco Meraki fornece redes baseadas em nuvem que centralizam o gerenciamento, a visibilidade e o controle de todos os dispositivos Meraki em uma única interface de painel, como mostrado na figura. O administrador de rede pode gerenciar os dispositivos sem fio em vários locais com o clique de um botão do mouse..

![[Pasted image 20240225143231.png]]

-  Ferramentas de cabo de rede

Hello everyone. We know that computers and laptops and mobile devices are great devices to work on and deploy, but all these devices are becoming reliant on network connections. As you journey further on becoming an IT professional, you have to build up your networking skills and start building a networking toolkit. 

I'm here to show you some of the popular items that you may find in a toolkit for network technicians. To start, you want to have a network cable crimper. You want to have wire strippers. You want to have cable connectors. Also it would be nice to have a punch down tool. We'll talk about these extra two items in just a little bit. 

Now, this cable crimper allows you to terminate both network cables and phone cables. We're going to be utilizing connectors with this and these connectors can be bought in bulk and they're used on the eight copper wires of a network cable. We use them in order to terminate the cable and make the network cables usable by devices. 

These wire strippers here, they're used to strip the outer sheath off the network and phone wires and once those wires are exposed, we could then utilize these connectors. A punch down tool is used to terminate the network cable that is eight raw copper wires into a punch down block. 

A punch down block is a common item that you'll find in enterprise network. The punch down block has slots for each of the eight wires to be punched into the slots and the nice thing about this tool, as it punches those eight wires down into the network block itself we can see that it has a cut side. It will cut off any excess network cable wire off of the punch block. 

Now when we were working with current, terminated and deploy network cabling, it's very important to have a basic network cable tester. With this network cable here, we can plug both ends of a network cable into the tester and this allows us to verify that the cable is of good quality and that all eight pins are terminated properly. 

Now there's a variety of different types of testers. I prefer the ones with LCD screens, some also have LED lights instead. The ones with the LCD screen can easily show you exactly which pin is experiencing issues. These tools can be very basic or very advanced. This one for example can use DHCP, ping and even test power over Ethernet. 

Other tools that exist can help you trace a network cable and find the device or panel it's connected to. This is called a toner probe. You use this in order to locate network cables that could be part of a huge bunch or even just a cable that's a very long run. This is called a probe because it's able to pick up the tone that is placed on a cable. Many different types of devices can put a tone on the wire including this cable tester right here. 

When you put all these tools together in a tool bag you're one step closer to becoming an IT professional.

![[Pasted image 20240225145215.png]]![[Pasted image 20240225145221.png]]
![[Pasted image 20240225145227.png]]
![[Pasted image 20240225145232.png]]
![[Pasted image 20240225145238.png]]
![[Pasted image 20240225145245.png]]
![[Pasted image 20240225145255.png]]
![[Pasted image 20240225145303.png]]
![[Pasted image 20240225145318.png]]
![[Pasted image 20240225145326.png]]


![[Pasted image 20240225145557.png]]

- Tipos de cabo

Há uma grande variedade de cabos de rede disponível, como mostrado na Figura. Os cabos coaxiais e de par trançado usam sinais elétricos em cobre para transmitir dados. Os cabos de fibra óptica usam sinais de luz para transmitir dados. Esses cabos são diferentes em termos de largura de banda, tamanho e custo.

- Cabos Coaxiais

O cabo coaxial é feito geralmente de cobre ou alumínio. Ele é usado por empresas de TV a cabo e sistemas de comunicação via satélite. O cabo coaxial é envolto por uma capa ou um revestimento e pode ter uma série de conectores como terminação, como mostrado na Figura.

O cabo coaxial transporta dados na forma de sinais elétricos. Ele fornece blindagem aprimorada em comparação com o UTP (par trançado não blindado), portanto, possui uma relação sinal / ruído mais alta, permitindo o transporte de mais dados. Entretanto, o cabeamento de par trançado substituiu o coaxial em LANs porque, quando comparado ao UTP, o coaxial é fisicamente mais difícil de instalar, mais caro e mais difícil de solucionar problemas.

![[Pasted image 20240225145647.png]]

- Cabos Par Trançado

O par trançado é um tipo de cabeamento de cobre utilizado para comunicações telefônicas e a maioria das redes Ethernet. O par é trançado para fornecer proteção contra diafonia (crosstalk), que é o ruído gerado por pares adjacentes de fios no cabo. O cabeamento de par trançado sem blindagem (UTP) é a variedade mais comum desse tipo de cabo.

Como mostrado na Figura 1, o cabo UTP consiste em quatro pares de cabos codificados por cores que foram trançados e depois colocados em uma capa plástica flexível que protege contra danos físicos menores. Entretanto, o UTP não protege contra Interferência Eletromagnética (EMI - Electromagnetic Interference) ou Interferência de Radiofrequência (RFI - Radio Frequency Interference). EMI e RFI podem ser causadas por várias fontes, incluindo motores elétricos e lâmpadas fluorescentes.

O Par Trançado Blindado (STP - Shielded Twisted Pair) foi projetado para oferecer a melhor proteção contra EMI e RFI. Como mostra a Figura 2, cada par trançado é envolvido em uma blindagem de alumínio. Os quatro pares são então embrulhados em uma trança ou folha metálica.

Os cabos UTP e STP terminam com um conector RJ-45 e são acoplados a soquetes RJ-45, como mostrado na Figura 3. Comparado ao cabo UTP, o cabo STP é significativamente mais caro e difícil de instalar. Para aproveitar totalmente a blindagem, os cabos STP têm como terminação conectores de dados STP RJ-45 blindados especiais (não mostrados). Se o cabo não estiver devidamente aterrado, a blindagem poderá atuar como uma antena e captar sinais indesejados.

![[Pasted image 20240225145728.png]]![[Pasted image 20240225145732.png]]
![[Pasted image 20240225145737.png]]
![[Pasted image 20240225145805.png]]
![[Pasted image 20240225145851.png]]![[Pasted image 20240225145901.png]]

![[Pasted image 20240225145925.png]]
![[Pasted image 20240225145929.png]]![[Pasted image 20240225145944.png]]

-  Construa e teste um cabo de rede

Hello, everyone. All of these tools here are common network termination tools. We have extra network cable that is not terminated. Here is a crimping tool, and some RJ45 connectors that we can use to terminate our network cable. We have a couple of steps in order to successfully build a custom length network cable. 

First step is to commonly measure the length of the cable you're going to need. This is a great reason for making your own cables, because we like to pick a custom length, and not have to buy a pre-made cable with a pre-picked length. 

Now that we have our measured length of cable, we can use the cutting blade on our crimping tool to cut our cable. Got the cutting blade right here. I put the cable in, and I'd be able to cut it, if needed. We can use the cable stripper to strip the outer housing off the network cable. We're going to place the cable in this groove right here on our cable stripper, and we can go rather far on this cable without a problem. Just take that into account when you're talking about length. I can press and hold the cable stripper down on the cable, and I'll just twist it, and this is going to cut through that outer sheath. And this is going to allow us to pull that outer housing off of the network cable. You can see that right here, how it's coming off. 

After removing the outer sheath, you'll find four pairs of wires. We'll have to untwist the four pairs, and organize them into eight individual copper wires. When you're separating those four pairs from each other, what I find in the middle of mine, is this plastic separator. This is common in our Cat 6 wires like this one, which allows it to prevent interference and cross talk between our pairs. What we're going to do right now is cut this plastic separator off, because it's going to be in the way when we try to put our RJ45 connector on. So I can take my cutting tool and just cut that plastic separator off. Does a great job inside of the cable, but it's in the way for the RJ45 connector. Also, what we'll find in my cable is this string. These are meant to be pull, strings that allow you to pull on the sheath and be able to slice through the sheath. That's also going to be in the way for me, so I'm going to cut that off, because we don't need it at this time.  

So, this is where we now want to untwist all the wires, and this is going to take us sometime to do. What we're going to find is that each pair of wires, well, they're going to be having different number of twists per inch, and you'll be able to see that. For example, the ones that will be the hardest to untwist, is going to be blue/white blue. That has more twists per inch for example, than looking at brown/white brown. Those more twists per inch for each pair is going to allow us to have less cross talk, and interference between those pairs. They thought of everything, didn't they. So I'll continue to untwist, and we'll come back. 

Now that my eight individual wires are untwisted, what we want to do is pull them all so they're really straight. The straighter you can make them, the easier it's going to be to organize the wires in the correct color code, as well as the easier it will be to crimp them with the RJ45 connector. Now, I'm not worrying right now, too much about color code organization, I just want to get them as straight as possible. What some people like to do, is if you can gather all of them at the end of the wires with your fingers, you can actually pull it straight and wiggle back and forth, and you get straighter wires.

Now, what I like to do is organize them in the correct color code. There's different standards, 568A or 568B. I'm going to follow the T568B standard and put these wires in the correct order. That order's going to be orange/white orange, green/white blue, blue/white green, brown/white brown. And to do that, I'm just literally going to take the orange/white and put it over to the side, followed by orange. Then I'll follow that one correctly with the green/white and bring that one over, and then follow it with the next color. I'll do that, and we'll come back

Once you have them in the correct color order, such as we see here, we like to take one of our RJ45 connectors and we'd slide it on. The current problem is that connectors not going to fit well, the wires are too long. We want this sheath to be about here in the connector, so when we crimp, this connectors going to hold onto that sheath, not onto the wires. So what I need to do is take my tool, which I can take either a pair of snips, or a cutting tool like this, and I need to cut these shorter. I'll go ahead, and I'm just going to give it a snip. Make sure you use a tool that's sharp. You want a nice even cut as much as possible. 

Now that these wires are cut, we can verify that they're still in the correct order, and we can take an RJ45 connector, and we're going to slide this on just like so. And we'll push those in tight. We can watch those wires go into the RJ45 connector, push far enough and we should see that plastic sheath go in as well, awesome. We can check the front of the RJ45 connector and see all of those color codes coming in beautifully. 

Now we'll take our crimper, and we'll slide our cable into the crimper. It's all the way in, we'll give it a tight squeeze, and now it's crimped on. We can see it holding on to the plastic sheath and our eight copper wires are all the way in. 

Now the connector is attached to the eight wires, and the outer housing, before we deploy this, we should verify the quality of the cable. You take something like this, which is a cable tester, plug it in on both sides, turn it on, and we'll be able to watch it go. Checking the quality of our cable, and we should see all eight wires come up as successful, we'll see eight lines. And we did it, all eight lines came up, letting us know the quality of our cable is perfect. You're able to see that, right here. And it tells us it’s a three foot cable, so hopefully, you have a three foot purpose. Grab some tools and get started crafting your own custom length network cable. 


- Cabos de Fibra Óptica

A fibra óptica é composta por dois tipos de vidro (núcleo e revestimento interno) e uma proteção exterior (capa). Clique em cada componente na figura para obter mais informações.

Como usa luz para transmitir sinais, o cabo de fibra ótica não é afetado por EMI ou RFI. Todos os sinais são convertidos em pulsos de luz quando entram no cabo e são convertidos em sinais elétricos quando saem dele. Isso significa que o cabo de fibra óptica pode fornecer sinais mais nítidos, que alcançam maiores distâncias e tem maior largura de banda que o cabo feito de cobre ou outros metais. Embora a fibra óptica seja muito fina e suscetível a dobras, as propriedades do núcleo e do revestimento interno a tornam muito forte. A fibra óptica é durável e implantada em condições de ambiente hostis nas redes em todo o mundo.

![[Pasted image 20240225150803.png]]![[Pasted image 20240225150810.png]]
![[Pasted image 20240225150820.png]]
![[Pasted image 20240225150826.png]]![[Pasted image 20240225150831.png]]

- Tipos de Fibra

Os cabos de fibra óptica são amplamente classificados em dois tipos:

- **Fibra monomodo (SMF - Single-Mode Fiber)** – Consiste em um núcleo muito pequeno e usa a tecnologia a laser para enviar um único raio de luz, como mostrado na Figura 1. Popular nas situações de longa distância que abrangem centenas de quilômetros, como aquelas necessárias na telefonia de longa distância e em aplicações de TV a cabo.

- **Fibra multimodo (MMF - Multi-Mode Fiber)** – Consiste em um núcleo maior e usa emissores de LED para enviar pulsos de luz. Especificamente, a luz de um LED entra na fibra multimodo em ângulos diferentes, conforme mostrado na Figura 2. Popular nas LANs porque pode ser acionada por LEDs de baixo custo. Ela fornece largura de banda até 10 Gb/s por links de até 550 metros.
![[Pasted image 20240225150851.png]]![[Pasted image 20240225150857.png]]

- Conectores de Fibra Óptica

Um conector de fibra óptica termina a extremidade de uma fibra óptica. Há vários conectores de fibra óptica disponíveis. As principais diferenças entre os tipos de conectores são as dimensões e os métodos de acoplamento. As empresas decidem os tipos de conectores que serão usados, com base no seu equipamento.

Clique em cada conector na figura para saber sobre os tipos mais comuns de conectores de fibra ótica.

Para os padrões de fibra com FX e SX no nome, a luz viaja em uma direção sobre a fibra óptica. Portanto, são necessárias duas fibras para suportar a operação full duplex. Os cabos do patch da fibra óptica juntam dois cabos de fibra óptica e os conectam com um par de conectores de fibra simples padrão. Alguns conectores de fibra aceitam fibras de transmissão e de recepção em um único conector, conhecido como conector duplex, conforme mostrado no Conector LC Duplex Multimodo na Figura.

Para padrões de fibra com BX no nome, a luz viaja em ambas as direções em um único cabo de fibra. Isso é feito através de um processo chamado Wave Division Multiplexing (WDM). WDM é uma tecnologia que separa os sinais de transmissão e recepção dentro da fibra.

Para obter mais informações sobre padrões de fibra, procure "padrões de fibra óptica Gigabit Ethernet".

![[Pasted image 20240225150937.png]]![[Pasted image 20240225150942.png]]![[Pasted image 20240225150945.png]]![[Pasted image 20240225150949.png]]

![[Pasted image 20240225151036.png]]

---

# TESTE
![[Pasted image 20240303214731.png]]![[Pasted image 20240303214737.png]]
![[Pasted image 20240303214743.png]]![[Pasted image 20240303214749.png]]
![[Pasted image 20240303214754.png]]![[Pasted image 20240303214802.png]]
![[Pasted image 20240303214807.png]]![[Pasted image 20240303214813.png]]![[Pasted image 20240303214818.png]]
![[Pasted image 20240303214824.png]]
![[Pasted image 20240303214831.png]]![[Pasted image 20240303214835.png]]
![[Pasted image 20240303214841.png]]![[Pasted image 20240303214846.png]]![[Pasted image 20240303214850.png]]
![[Pasted image 20240303214858.png]]![[Pasted image 20240303214903.png]]
![[Pasted image 20240303214911.png]]
![[Pasted image 20240303214918.png]]
![[Pasted image 20240303214926.png]]
![[Pasted image 20240303214934.png]]![[Pasted image 20240303214941.png]]