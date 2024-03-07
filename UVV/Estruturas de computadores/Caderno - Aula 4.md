# CISCO

Capítulo 6: Rede Aplicada

Hoje praticamente todos os computadores e dispositivos móveis estão conectados a algum tipo de rede e à Internet. Isso significa que configurar e solucionar problemas de redes de computadores agora é uma habilidade essencial para profissionais de TI. Este capítulo se concentra na rede aplicada com uma discussão aprofundada sobre o formato e a arquitetura dos endereços MAC (controle de acesso à mídia) e dos endereços IP (Internet Protocol), IPv4 e IPv6, usados para conectar computadores a uma rede. Exemplos de como configurar o endereçamento estático e dinâmico em computadores estão incluídos. Também é abordada neste capítulo a configuração de redes com e sem fio, firewalls e dispositivos de IoT.

Você aprenderá como configurar placas de interface de rede (NICs), conectar dispositivos a um roteador sem fio e configurar um roteador sem fio para conectividade de rede. Você aprenderá como definir configurações básicas de rede sem fio, conversão de endereços de rede (NAT), configurações de firewall e qualidade de serviço (QoS). Você também aprenderá sobre firewalls, dispositivos da Internet das Coisas (IoT) e solução de problemas de rede. No final do capítulo, você aprenderá o processo de solução de problemas de seis etapas e os problemas e soluções comuns para redes de computadores.

Suas habilidades de rede devem incluir a capacidade de configurar redes sem fio para que os hosts possam se comunicar, configurar firewalls para filtrar o tráfego, verificar a conectividade de rede e resolver problemas de conectividade de rede. Existem três laboratórios incluídos neste capítulo, nos quais você desenvolverá essas habilidades. Nesses laboratórios, você definirá configurações básicas em um roteador sem fio e conectará um PC à rede sem fio, configurações de firewall para implementar a filtragem de endereços MAC, uma DMZ e encaminhamento de porta única e, finalmente, diagnosticar e resolver problemas de rede.


Ethernet LANs use MAC addresses, media access control addresses to accomplish the same thing. Every NIC, network interface card has a unique 48 bit MAC address embedded into the card represented in hexadecimal notation. Also known as a physical address, the MAC address never changes and will be the same wherever the device is located. 
![[Pasted image 20240225164545.png]]

An Ethernet MAC address has two parts. The first 24 bits represent the organizationally unique identifier or OUI. This is the vendor or manufacturer portion of the address. For example, one of several OUI codes associated to Cisco Systems is 00-60-2F, as shown in the example. The second 24 bits are assigned by the vendor and unique to that particular OUI. For example 3A-07-BC is unique to the vendor code 00-60-2F. MAC addresses are 48 bits with the OUI and vendor assigned portions, each being 24 bits. 

MAC addresses are typically represented in hexadecimal, six hexadecimal digits for each portion. 

![[Pasted image 20240225164714.png]]

Ethernet MAC addresses are used for NIC card to NIC card communications on the same network. On an Ethernet LAN there can be multiple devices. Similar to Telethia speaking to Jeremy, when device on a LAN needs to communicate with another device on the same LAN it is important that that device includes the MAC address of the destination in the message, otherwise the devices won't know who the message is for. 

When PC A sends a message to printer B, it will send it to printer B's MAC address. Routers on an Ethernet LAN will also have an Ethernet NIC, which means it has an Ethernet MAC address. Notice router D has two Ethernet NICs, one for each network it is connected to. 

That is what routers do, they connect to multiple networks. Router D's Ethernet NIC, with the address that ends in all Ds, is only used to communicate with other devices on the same network with PC A, printer B and server C. 

Router D's Ethernet NIC with the address ending in all Es, is used to communicate with devices on a separate network. This NIC cannot be reached by devices on the other LANs such as PC A. When server C sends a message for a device on another network, it will send the message to router D's MAC address ending in all Ds. Router D will forward this message at the appropriate interface towards the destination device. 

![[Pasted image 20240225164809.png]]

- #  Endereçamento IPv4

IP addresses allow devices to communicate with each other that are on the same or different networks. Routers are used to forward messages between IP networks. In this analogy, each room would be a different IP network, and Allan would be the router. 

![[Pasted image 20240225172347.png]]

IPv4 addresses are 32-bit addresses, represented in dotted decimal notation. IPv6 addresses are 128-bit addresses, represented by colon-separated hexadecimal notation. The difference between decimal, hexadecimal, and binary is that the decimal number system is base 10, having 10 digits, zero through nine. The hexadecimal system is base 16, having 16 digits, zero through nine, plus A, B, C, D, E, and F, which equate to decimal base 10, 10 through 15, respectively. The binary number system is base two, having only two digits, zero and one. 

![[Pasted image 20240225172412.png]]

IPv4 addresses are four decimal numbers, separated by a decimal, with each representing eight bits, for a total of 32 bits. IPv4 addresses have a 32-bit subnet mask, also represented in dotted decimal notation. Subnet masks are a continuous string of ones, with the rest of the mask being all zero bits. This means that there are specific values that a subnet mask will have, such as 225.255.255.0. 

![[Pasted image 20240225172704.png]]
![[Pasted image 20240225172800.png]]


Subnet masks can be represented in slash notation, using a slash followed by the number of one bits in the subnet mask. This is also known as the prefix length. Although the binary number system is beyond the scope of this video, the dotted decimal subnet mask of 255.255.255.0 would be the same as a slash 24 prefix length. An IP address has two parts: a network portion and a host portion. 

The 32-bit subnet mask is used to differentiate these two parts. The ones in the subnet mask indicate the network portion of the address, whereas the zeroes in the subnet mask indicate the host portion. In our example, the three decimal 255s, 24 one bits, indicate the network portion of the IPv4 address. And the decimal zero, or zero bits, indicate the host portion. 

![[Pasted image 20240225172843.png]]

Let's look at an example. We have two IPv4 networks. 192.168.1.0, with the 255.255.255.0 mask, and 172.16.0.0 with the 255.255.0.0 mask. Network addresses have all zero bits in the host portion. Notice that all the devices in both networks share the same subnet mask, which means the network portion of their addresses are identical, indicated in blue. Their host portions are unique, indicated in red. PC A has the IPv4 host address 192.168.1.100. If PC A moves to a different network, its IPv4 address will change, and it will share the same subnet mask, along with the same network portion of its address, with all other devices on that network. As you can see, PC A now has the IPv4 address 172.16.3.0, with the subnet mask 255.255.0.0, which means it's part of the 172.16.0.0 network. 

![[Pasted image 20240225172849.png]]
- Endereçamento IPv6

IPv6 addresses are represented in hexadecimal notation. Each hexadecimal digit is four bits, which means each segment of four hexadecimal digits will be 16 bits. There are eight 16 bit segments with each segment separated by a colon. Eight 16 bits segments gives us the 128 bits.  .

![[Pasted image 20240225173922.png]]

IPv6 addresses are typically represented in compressed format. This is done using two rules. The first rule is that leading zeros of any 16 bit segment can be omitted. Notice that only the leading zeros in red are omitted.  
![[Pasted image 20240225173935.png]]

The second rule is that a single string of contiguous all-zero segments can be replaced by a single double colon. Notice that two segments in red with all zeros can be replaced by a single double colon, also in red. An IPv6 address can utilize only one double colon. 

![[Pasted image 20240225173946.png]]

Here we see an example of combining both rules. Rule one omits the leading zeros and rule two allows us to use a double colon to represent two all-zero segments. Together, they give us the IPv6 address in compressed format.

![[Pasted image 20240225174004.png]]

Similar to IPv4, IPv6 uses slash notation. The prefix length to indicate the network portion, the prefix, of the IPv6 address. The /64 in our example indicates that the network portion of the address. This means the rest of the address in red is the host portion. The IPv6 address has all zero bits in the host portion indicated by all zeros in the hexadecimal in red. Or a single double colon also in red. 

![[Pasted image 20240225174025.png]]

Let's look at an IPv6 example. We have two IPv6 networks. 2001:db8:acad:100::/64 and 2001:db8:acad:200::/64. Notice that all the devices in both networks share the same prefix length which means the network portion of their addresses are identical indicated in blue. Their host portions are unique indicated in red. PC A has the IPv6 host address 2001:db8:acad:100::77/64 If PC A moves to a different network, its IPv6 address will change and perhaps its prefix link. As you can see, PC A now has the IPv6 address 2001:db8:acad:200::77/64 which means it is now part of the 2001:db8:acad:200::/64 network. 

![[Pasted image 20240225174032.png]]

![[Pasted image 20240225174133.png]]
- Dois endereços de rede

Sua impressão digital e endereço de correspondência são duas maneiras de identificá-lo e localizá-lo. Sua impressão digital geralmente não muda. Sua impressão digital pode ser usada para identificá-lo exclusivamente, em qualquer local. Seu endereço de correspondência é diferente. É a sua localização. Ao contrário da sua impressão digital, seu endereço de correspondência pode mudar.

Os dispositivos conectados a uma rede têm dois endereços semelhantes à sua impressão digital e endereço de correspondência, conforme mostrado na figura. Esses dois tipos de endereços são o endereço MAC (Media Access Control) e o endereço do Protocolo Internet (IP).

O endereço MAC é codificado na placa de interface de rede Ethernet ou sem fio (NIC) pelo fabricante. O endereço permanece no dispositivo, independentemente da rede à qual o dispositivo está conectado. Um endereço MAC tem 48 bits e pode ser representado em um dos três formatos hexadecimais mostrados na Figura 2.

![[Pasted image 20240225174232.png]]

O endereçamento IP é atribuído por administradores de rede com base na localização dentro da rede. Quando um dispositivo for movido de uma rede para outra, provavelmente seu endereço IP vai mudar. Um endereço IP versão 4 (IPv4) tem 32 bits e é representado em notação decimal pontilhada. Um endereço IP versão 6 (IPv6) tem 128 bits e é representado no formato hexadecimal, como mostra a Figura 3.

![[Pasted image 20240225174240.png]]

A Figura 4 mostra uma topologia com duas redes locais (LANs). Essa topologia demonstra que os endereços MAC não mudam quando um dispositivo é movido. Ao contrário dos endereços IP. O laptop foi movido para a LAN 2. Observe que o endereço MAC do laptop não se modificou, mas seu endereço IP mudou.

![[Pasted image 20240225174249.png]]

**Nota**:A conversão entre os sistemas numéricos binário, decimal e hexadecimal está além do escopo deste curso. Pesquise na Internet para saber mais sobre esses sistemas de numeração.

- Exibindo os endereços

Hoje, seu computador provavelmente possui um endereço IPv4 e um IPv6, conforme mostrado para o laptop na figura. No início dos anos 90, havia uma preocupação em ficar sem endereços de rede IPv4. A IETF (Força-tarefa de Engenharia de Internet) começou a procurar um substituto. Isso levou ao desenvolvimento do IPv6. Atualmente, o IPv6 está operando ao lado do IPv4 e está começando a substituí-lo.

A Figura mostra a saída do comando **ipconfig /all** no laptop. A saída é destacada para mostrar o endereço MAC e dois endereços IP.

**Observação**: o sistema operacional Windows chama a NIC de adaptador Ethernet e chama o endereço MAC de endereço físico.

![[Pasted image 20240225174315.png]]

- Formato do Endereço IPv4

Quando você configura manualmente um dispositivo com um endereço IPv4, insere-o no formato decimal pontilhado, conforme mostrado em um computador com Windows na Figura 1. Cada número separado por um ponto é chamado de octeto porque representa 8 bits. Portanto, o endereço de 32 bits 192.168.200.8 possui quatro octetos.

Um endereço IPv4 é composto por duas partes. A primeira para identifica a rede. A segunda parte identifica este dispositivo na rede. A máscara de sub-rede é usada pelo dispositivo para determinar a rede. Por exemplo, o computador na Figura 1 usa a máscara de sub-rede 255.255.255.0 para determinar que o endereço IPv4 192.168.200.8 pertence à rede 192.168.200.0. A parte .8 é a parte do host exclusivo deste dispositivo na rede 192.168.200. Qualquer outro dispositivo com o mesmo prefixo 192.168.200 estará na mesma rede, mas terá um valor diferente para a parte do host. Os dispositivos com um prefixo diferente estarão em uma rede diferente.

![[Pasted image 20240225174411.png]]

Para ver isso no nível binário, você pode converter o endereço IPv4 de 32 bits e a máscara de sub-rede em seus equivalentes binários, conforme mostrado na Figura 2. Um bit em 1 na máscara de sub-rede significa que o bit faz parte da porção de rede. Portanto, os primeiros 24 bits do endereço 192.168.200.8 são bits de rede. Os últimos 8 bits são bits de host.

![[Pasted image 20240225174417.png]]

Quando o dispositivo prepara dados para enviar na rede, ele deve primeiro determinar se os dados devem ser enviados diretamente para o receptor pretendido ou para um roteador. Eles serão enviados diretamente para o destinatário se o destinatário estiver na mesma rede. Caso contrário, o computador enviará os dados para um roteador. Um roteador usa a porção de rede do endereço IP para rotear tráfego entre redes diferentes.

Por exemplo, se o computador Windows na Figura 1 tiver dados para enviar a um host em 192.168.200.25, ele enviará os dados diretamente para esse host, pois possui o mesmo prefixo de 192.168.200. Se o endereço IPv4 do destino for 192.168.201.25, o computador do Windows enviará os dados para um roteador.

- Formatos de Endereço IPv6

O IPv6 supera as limitações de espaço de endereço do IPv4. O espaço de 32 bits de um endereço IPv4 fornece aproximadamente 4.294.967.296 endereços exclusivos. O espaço de endereço IPv6 de 128 bits fornece 340.282.366.920.938.463.463.374.607.431.768.211.456 endereços ou 340 undecilhões de endereços.

Os 128 bits de um endereço IPv6 são gravados como uma sequência de valores hexadecimais, com letras expressas em minúsculas. Cada 4 bits são representados por um único dígito hexadecimal, totalizando 32 valores hexadecimais. Os exemplos mostrados na Figura 1 são endereços IPv6 totalmente expandidos. Duas regras ajudam a reduzir o número de dígitos necessários para representar um endereço IPv6.

**Regra 1 – Omitir 0s à esquerda**

A primeira regra para ajudar a reduzir a notação de endereços IPv6 é omitir os 0s (zeros) à esquerda de qualquer seção de 16 bits. Por exemplo, na Figura 1:

- **0db8** pode ser representado como **db8**, no primeiro endereço IPv6

- **0123** pode ser representado como**123**, no segundo endereço IPv6

- **0001** pode ser representado como **1**, no terceiro endereço IPv6

**Nota**: Os endereços IPv6 devem ser representados em letras minúsculas, mas é comum vê-los em maiúsculas.

![[Pasted image 20240225174512.png]]

**Regra 2: Ocultar todos os segmentos com 0**

A segunda regra para ajudar a reduzir a notação de endereços IPv6 é que dois-pontos em dobro (::) podem substituir qualquer grupo de zeros consecutivos. Os dois-pontos em dobro (::) só podem ser usados uma vez em um endereço; caso contrário, haveria mais de um endereço resultante possível.

As Figuras 2 a 4 mostram exemplos de como usar as duas regras para compactar os endereços IPv6 mostrados na Figura 1.

![[Pasted image 20240225174519.png]]![[Pasted image 20240225174528.png]]
![[Pasted image 20240225174540.png]]

- Endereçamento Estático

Em uma rede pequena, você pode configurar manualmente cada dispositivo com o endereçamento IP adequado. Você atribuiria um endereço IP exclusivo a cada host na mesma rede. Isso é conhecido como endereçamento IP estático.

Em um computador Windows, como mostrado na Figura 1, você pode atribuir as seguintes informações de configuração de endereço IPv4 a um host:

- **Endereço IP** – Identifica este dispositivo na rede.

- **Máscara de sub-rede** - é usada para identificar a rede na qual este dispositivo está conectado

- **Gateway padrão** – identifica o roteador que este dispositivo usa para acessar a Internet ou outra rede

- **Valores opcionais** – Como o endereço do servidor DNS (Domain Name System - Sistema de Nome de Dominio) preferencial e o endereço do servidor DNS alternativo
![[Pasted image 20240225174624.png]]

Informações de configuração semelhantes para o endereçamento IPv6 são mostradas na Figura 2.

![[Pasted image 20240225174628.png]]
- Endereçamento Dinâmico

Em vez de configurar manualmente todos os dispositivos, você pode aproveitar a implementação de um servidor DHCP (Protocolo de Configuração Dinâmica de Host). Um servidor DHCP (Protocolo de Configuração Dinâmica de Host) atribui automaticamente endereços IP, o que simplifica o processo de endereçamento. A configuração automática de alguns dos parâmetros de endereçamento IP também reduz a possibilidade de atribuir endereços IP duplicados ou inválidos.

Por padrão, a maioria dos dispositivos host está configurada para solicitar endereçamento IP de um servidor DHCP. A configuração padrão para um computador Windows é mostrada na figura. Quando um computador é configurado para obter endereço IP automaticamente, todas as outras caixas de configuração de endereçamento IP ficam indisponíveis. Esse processo é o mesmo para uma NIC com ou sem fio.

Um servidor DHCP pode atribuir automaticamente as seguintes informações de configuração de endereço IP a um host:

- Endereço IPv4

- Máscara de sub-rede

- Gateway padrão

- Valores opcionais, como um endereço de servidor DNS

O DHCP também está disponível para atribuir automaticamente informações de endereçamento IPv6.

**Nota**: As etapas para configurar um computador Windows estão além do escopo deste tópico.

![[Pasted image 20240225174659.png]]
- Endereços IPv4 e IPv6 locais de link

Os endereços locais de link para IPv4 e IPv6 são usados por um dispositivo para se comunicar com outros computadores conectados à mesma rede no mesmo intervalo de endereços IP. A principal diferença entre IPv4 e IPv6 é a seguinte:

- Um dispositivo IPv4 usa o endereço local do link se o dispositivo não puder obter um endereço IPv4.

- Um dispositivo IPv6 deve sempre ser configurado de forma dinâmica ou manual com um endereço IPv6 local do link.

**Endereço local do link IPv4**

Se o seu computador Windows não puder se comunicar com um servidor DHCP para obter um endereço IPv4, o Windows atribuirá automaticamente um endereço APIPA (Endereçamento Automático de IP Privado). Esse endereço de link local está no intervalo de 169.254.0.0 a 169.254.255.255.

**Endereço IPv6 de Link Local**

Assim como o IPv4, o endereço local do link IPv6 permite que o dispositivo se comunique com outros dispositivos habilitados para IPv6 na mesma rede e somente nessa rede. Diferentemente do IPv4, todos os dispositivos habilitados para IPv6 precisam ter um endereço local de link. Os endereços locais de link IPv6 estão no intervalo de fe80:: a febf::. Por exemplo, na figura, os links para outras redes estão inativos (não conectados) como notados pelos Xs vermelhos. No entanto, todos os dispositivos na LAN ainda podem usar endereços IPv6 locais de link para se comunicarem.

**Nota**: Diferentemente dos endereços locais de link IPv4, os endereços locais de link IPv6 são usados em uma variedade de processos, incluindo protocolos de descoberta de rede e protocolos de roteamento. Isso está além do escopo deste curso.

![[Pasted image 20240225174733.png]]

- # Adicionando Computadores a uma Rede Existente

Nesta atividade do Packet Tracer, você configurará os computadores para usar DHCP, configurar endereçamento estático, usar **ipconfig** para recuperar informações do IPv4 do host e usar **ping** para verificar a conectividade.

[Packet Tracer – Adicionando Computadores a uma Rede Existente Instruções](https://contenthub.netacad.com/legacy/ITE/7.01/pt/course/files/6.1.2.1%20Packet%20Tracer%20-%20Add%20Computers%20to%20an%20Existing%20Network.pdf)

[Packet Tracer – Adicionando Computadores a uma Rede Existente PKA](https://contenthub.netacad.com/legacy/ITE/7.01/pt/course/files/6.1.2.1%20Packet%20Tracer%20-%20Add%20Computers%20to%20an%20Existing%20Network.pka)

- # Projeto de rede

Como técnico em informática, você deve ser capaz de dar suporte às necessidades de rede de seus clientes. Portanto, você deve estar familiarizado com:

- **Componentes de rede** – Incluem placas de interface de rede (NICs) com e sem fio e dispositivos de rede como switches, pontos de acesso (APs) sem fio, roteadores, dispositivos multiuso, etc.

- **Projeto de rede** – Envolve saber como as redes estão interconectadas para atender às necessidades de uma empresa. Por exemplo, as necessidades de pequenas empresas são muito diferentes das necessidades de empresas de grande porte.

Considere uma pequena empresa com 10 funcionários. Ela contratou você para conectar seus usuários. Como mostrado na figura, um roteador sem fio doméstico ou de pequeno escritório pode ser usado para um número tão pequeno de usuários. Esses roteadores são de múltiplos propósitos e normalmente fornecem recursos de roteador, comutador, firewall e ponto de acesso. Além disso, esses roteadores sem fio geralmente oferecem uma variedade de outros serviços, incluindo DHCP.

Se o negócio fosse muito maior, você não usaria um roteador sem fio. Em vez disso, você consultaria um arquiteto de rede para projetar uma rede de comutadores dedicados, pontos de acesso (AP), dispositivos de firewall e roteadores.

Independentemente do projeto de rede, você deve saber instalar placas de rede, conectar dispositivos com e sem fio e configurar equipamento básico de rede.

**Nota**: Este capítulo se concentrará na conexão e configuração de um pequeno escritório ou roteador sem fio doméstico. O Packet Tracer será usado para demonstrar as configurações. Entretanto, a mesma funcionalidade e elementos gráficos semelhantes da GUI (Graphical User Interface, Interface Gráfica de Usuário) existem em todos os roteadores sem fio. Você pode comprar online vários roteadores sem fio de baixo custo e em lojas de eletrônicos. Pesquise na Internet por “análises de roteadores sem fio” para pesquisar as recomendações atuais.

![[Pasted image 20240225175202.png]]
- # Selecionando uma NIC

É necessário ter uma placa de interface de rede (NIC) para se conectar à rede. Como mostra a Figura 1, existem diferentes tipos de NIC. As NICs Ethernet são usadas para conexão a redes Ethernet, e as placas de rede sem fio são usadas para conexão a redes sem fio 802.11. A maioria das NICs em desktops é integrada à placa-mãe ou está conectada a um slot de expansão. As placas de rede também estão disponíveis no formato USB.

Muitos computadores adquiridos hoje vêm com uma interface de rede com e sem fio integrada na placa-mãe.

![[Pasted image 20240225175221.png]]
- # Instalando e Atualizando uma NIC

Siga as etapas para instalar placas adaptadoras, se você estiver instalando uma NIC dentro do computador. Uma NIC sem fio para um dispositivo de mesa possui uma antena externa conectada à parte traseira da placa ou conectada com um cabo para que possa ser posicionada para a melhor recepção de sinal. Você deve conectar e posicionar a antena.

Às vezes, um fabricante publica um novo software de driver para uma NIC. Um novo driver pode aprimorar a funcionalidade da NIC ou pode ser necessário para compatibilidade do sistema operacional. Os drivers mais recentes de todos os sistemas operacionais suportados estão disponíveis para download no site do fabricante.

Ao instalar um novo driver, desative o software de proteção contra vírus para garantir que o driver seja instalado corretamente. Alguns scanners de vírus reconhecem uma atualização de driver como um possível ataque de vírus. Instale apenas um driver de cada vez; caso contrário, alguns processos de atualização poderão entrar em conflito. Uma prática recomendada é fechar todos os aplicativos em execução para que eles não utilizem nenhum arquivo associado à atualização do driver.

**Nota**: Um exemplo do Gerenciador de dispositivos do Windows e o local para atualizar o driver de uma NIC é mostrado na figura. No entanto, os detalhes de como atualizar drivers para dispositivos e sistemas operacionais específicos estão além do escopo deste tópico.

![[Pasted image 20240225175251.png]]
- # Configurar uma NIC

As configurações de endereço IP devem ser definidas depois que o driver NIC estiver instalado. Para computadores Windows, o endereçamento IP é dinâmico por padrão. Depois de conectar fisicamente um computador Windows à rede, ele enviará automaticamente uma solicitação de endereçamento IPv4 ao servidor DHCP. Se um servidor DHCP estiver disponível, o computador receberá uma mensagem com todas as suas informações de endereçamento IPv4.

**Nota**: O endereçamento dinâmico para IPv6 também pode usar DHCP, mas está além do escopo deste curso.

Esse comportamento padrão dinâmico também é tipicamente para smartphones, tablets, consoles de jogos e outros dispositivos de usuário final. A configuração estática é normalmente o trabalho de um administrador de rede. No entanto, você deve estar familiarizado sobre como acessar configuração de endereçamento IP para qualquer dispositivo que você precise gerenciar.

Para encontrar informações de configuração de endereçamento IP, pesquise na Internet "Configuração do endereço IP do dispositivo", onde o "dispositivo" em sua pesquisa é substituído pelo nome do seu dispositivo, como "iPhone". Por exemplo, a Figura 1 mostra a caixa de diálogo para visualizar e alterar a configuração IPv6 de um computador Windows. A Figura 2 mostra as telas de configuração da configuração automática e manual do IPv4 em um iPhone.
![[Pasted image 20240225175317.png]]![[Pasted image 20240225175322.png]]

- # ICMP

O ICMP (Internet Control Message Protocol) é usado pelos dispositivos em uma rede para enviar mensagens de controle e erro. Existem vários usos diferentes para o ICMP, como apresentar erros de rede, anunciar congestionamento da rede e solucionar problemas.

O ping é usado com frequência para testar conexões entre computadores. Para ver uma lista de opções que podem ser utilizadas com o comando ping, digite **ping /?** na janela Prompt de Comando, como mostrado na Figura 1.

![[Pasted image 20240225175420.png]]

O ping funciona enviando uma solicitação de eco ICMP para o endereço IP digitado. Se o endereço IP estiver acessível, o dispositivo receptor retornará uma mensagem de resposta de eco ICMP para confirmar a conectividade.

Você também pode usar o **ping** comando para testar a conectividade com um site digitando o nome de domínio do site. Por exemplo, se você digitar **ping cisco.com** seu computador primeiro usará o DNS para encontrar o endereço IP e depois enviar a solicitação de eco ICMP para esse endereço IP, como mostra a Figura 2.

![[Pasted image 20240225175424.png]]

- # Configurar uma rede com e sem fio

https://contenthub.netacad.com/legacy/ITE/7.01/pt/index.html#6.1.3.1
- # Conexão de dispositivos com fio à Internet

As etapas para conectar um dispositivo com fio à Internet em uma casa ou pequeno escritório são as seguintes:

**Etapa 1: Conecte um cabo de rede ao dispositivo.**

Para conectar-se a uma rede com fio, conecte um cabo Ethernet à porta NIC, conforme mostrado na Figura 1.

**Etapa 2: Conecte o dispositivo a uma porta do switch.**

Conecte a outra extremidade do cabo a uma porta Ethernet no roteador sem fio, como uma das quatro portas de switch amarelas mostradas na Figura 2. Em uma rede SOHO, o laptop provavelmente se conectaria a uma tomada na parede que, por sua vez, se conectaria a um switch de rede.

**Etapa 3: Conecte um cabo de rede à porta da Internet do roteador sem fio.**

No roteador sem fio, conecte um cabo Ethernet à porta Internet (porta azul na Figura 2). Essa porta também pode ser denominada WAN.

**Etapa 4: Conecte o roteador sem fio ao modem.**

A porta azul na Figura 2 é uma porta Ethernet usada para conectar o roteador a um dispositivo provedor de serviços, como um DSL ou modem a cabo na Figura 3.

**Etapa 5: conectar-se à rede do provedor de serviços.**

O modem é então conectado à rede do provedor de serviços, como mostra a Figura 3.

**Nota**: Um modem separado não é necessário se o roteador sem fio for uma combinação de roteador/modem.

**Etapa 6: Ligue todos os dispositivos e verifique as conexões físicas.**

Ligue o modem de banda larga e conecte o cabo de energia ao roteador. Depois que o modem estabelecer uma conexão com o provedor de serviços de Internet (ISP), ele começará a se comunicar com o roteador. Os LEDs do laptop, roteador e modem acenderão, indicando comunicação. O modem permite que o roteador receba as informações de rede necessárias para obter acesso à Internet do ISP. Essas informações incluem endereços IPv4 públicos, máscara de sub-rede e endereços de servidor DNS. Com o esgotamento dos endereços IPv4 públicos, muitos ISPs também estão fornecendo informações de endereçamento IPv6.

A Figura 4 mostra uma topologia representando a conexão física de um laptop com fio no pequeno escritório ou rede doméstica.

Nota: A configuração do modem a cabo ou DSL geralmente é feita pelo representante do provedor de serviços no local ou remotamente através de uma explicação passo a passo com você no telefone. Se você comprar o modem, ele virá com a documentação de como conectá-lo ao provedor de serviços, o que provavelmente incluirá o contato com o provedor para obter mais informações.

- # Fazendo Logon no Roteador

A maioria dos roteadores sem fio para escritórios residenciais/pequenos escritórios está pronta para serviço de imediato. Eles são pré-configurados para serem conectados à rede e prestarem serviços. Por exemplo, o roteador sem fio usa o DHCP para fornecer automaticamente informações de endereçamento aos dispositivos conectados. Entretanto, nomes de usuário, senhas e endereços IP padrão do roteador sem fio podem ser facilmente encontrados na Internet. Basta inserir a frase de pesquisa "endereço IP padrão de roteador sem fio" ou "senhas padrão de roteador sem fio" para ver uma lista de vários sites que disponibilizam essas informações. Portanto, a prioridade nº 1 deve ser alterar esses padrões por motivo de segurança.

Para acessar a GUI (Graphical User Interface, Interface Gráfica de Usuário) de configuração do roteador sem fio, abra um navegador web. No campo Endereço, digite o endereço IP padrão do roteador sem fio. O endereço IP padrão pode ser encontrado na documentação que acompanha o roteador sem fio ou voce pode pesquisar na Internet. A figura mostra o endereço IPv4 192.168.0.1, que é um padrão comum de muitos fabricantes. Uma janela de segurança solicitará autorização para acessar a GUI (Graphical User Interface, Interface Gráfica de Usuário) do roteador. A palavra admin costuma ser usada para nome de usuário e senha, por padrão. Mais uma vez, consulte a documentação do roteador sem fio ou pesquise na Internet.

![[Pasted image 20240225191735.png]]![[Pasted image 20240225191747.png]]
![[Pasted image 20240225191755.png]]![[Pasted image 20240225191817.png]]
![[Pasted image 20240225191826.png]]![[Pasted image 20240225191833.png]]


## Configurações básicas da rede sem fio
![[Pasted image 20240225192016.png]]
![[Pasted image 20240225192035.png]]
![[Pasted image 20240225192049.png]]![[Pasted image 20240225192101.png]]
![[Pasted image 20240225192111.png]]![[Pasted image 20240225192116.png]]

- # Configurar uma rede sem fio Mesh

Em um pequeno escritório ou rede doméstica, um roteador sem fio pode ser suficiente para fornecer acesso sem fio a todos os clientes. No entanto, se você quiser estender o alcance além de aproximadamente 45 metros em ambientes internos e 90 metros em ambientes externos, poderá adicionar pontos de acesso sem fio. Conforme mostrado na rede mesh sem fio na figura, dois pontos de acesso são configurados com as mesmas configurações da WLAN do nosso exemplo anterior. Observe que os canais selecionados são 1 e 11, para que os pontos de acesso não interfiram no canal 6 configurado anteriormente no roteador sem fio.

Estender uma WLAN em um pequeno escritório ou em casa tornou-se cada vez mais fácil. Os fabricantes simplificaram a criação de um mesh de rede sem fio (WMN) através de aplicativos para smartphone. Você compra o sistema, dispersa os pontos de acesso, conecta-os, baixa o aplicativo e configura seu WMN em algumas etapas. Pesquise na Internet o “melhores sistemas de rede de malha wi-fi” para encontrar análises das ofertas atuais.
![[Pasted image 20240225192145.png]]
- # NAT para IPv4

Em um roteador sem fio, se você procurar uma página como a página Status mostrada na figura, encontrará as informações de endereçamento IPv4 que o roteador usa para enviar dados para a internet. Observe que o endereço IPv4 é 209.165.201.11 é uma rede diferente do endereço 10.10.10.1 atribuído à interface LAN do roteador. Todos os dispositivos na LAN do roteador receberão endereços atribuídos com o prefixo '10.10.10'.

O endereço IPv4 209.165.201.11 é publicamente roteável na Internet. Qualquer endereço com o 10 no primeiro octeto é um endereço IPv4 privado e não pode ser roteado na Internet. Portanto, o roteador usará um processo chamado Network Address Translation (NAT) para converter endereços IPv4 privados em endereços IPv4 roteáveis pela Internet. Com o NAT, um endereço IPv4 de origem privado (local) é convertido em um endereço público (global). O processo é o inverso para pacotes que entram na rede. Usando NAT, o roteador pode converter vários endereços IPv4 internos em endereços públicos.

Alguns provedores (ISPs) usam endereçamento privado para se conectar aos dispositivos do cliente. No entanto, eventualmente, seu tráfego sairá da rede do provedor e será roteado na Internet. Para ver os endereços IP dos seus dispositivos, pesquise na Internet "qual é o meu endereço IP". Faça isso para outros dispositivos na mesma rede e você verá que todos compartilham o mesmo endereço IPv4 público. O NAT torna isso possível rastreando os números de porta de origem para cada sessão estabelecida por um dispositivo. Se o seu provedor de serviços de Internet tiver o IPv6 ativado, você verá um endereço IPv6 exclusivo para cada dispositivo.

- # NAT para IPv4

Em um roteador sem fio, se você procurar uma página como a página Status mostrada na figura, encontrará as informações de endereçamento IPv4 que o roteador usa para enviar dados para a internet. Observe que o endereço IPv4 é 209.165.201.11 é uma rede diferente do endereço 10.10.10.1 atribuído à interface LAN do roteador. Todos os dispositivos na LAN do roteador receberão endereços atribuídos com o prefixo '10.10.10'.

O endereço IPv4 209.165.201.11 é publicamente roteável na Internet. Qualquer endereço com o 10 no primeiro octeto é um endereço IPv4 privado e não pode ser roteado na Internet. Portanto, o roteador usará um processo chamado Network Address Translation (NAT) para converter endereços IPv4 privados em endereços IPv4 roteáveis pela Internet. Com o NAT, um endereço IPv4 de origem privado (local) é convertido em um endereço público (global). O processo é o inverso para pacotes que entram na rede. Usando NAT, o roteador pode converter vários endereços IPv4 internos em endereços públicos.

Alguns provedores (ISPs) usam endereçamento privado para se conectar aos dispositivos do cliente. No entanto, eventualmente, seu tráfego sairá da rede do provedor e será roteado na Internet. Para ver os endereços IP dos seus dispositivos, pesquise na Internet "qual é o meu endereço IP". Faça isso para outros dispositivos na mesma rede e você verá que todos compartilham o mesmo endereço IPv4 público. O NAT torna isso possível rastreando os números de porta de origem para cada sessão estabelecida por um dispositivo. Se o seu provedor de serviços de Internet tiver o IPv6 ativado, você verá um endereço IPv6 exclusivo para cada dispositivo.

- # Qualidade do Serviço

Muitos roteadores domésticos e de pequenos escritórios têm uma opção para configurar a Qualidade de Serviço (QoS). Ao configurar a QoS, você pode garantir que determinados tipos de tráfego, como voz e vídeo, sejam priorizados em relação ao tráfego que não é tão sensível ao tempo, como email e navegação na web. Em alguns roteadores sem fio, o tráfego também pode ser priorizado em portas específicas.

A figura é um exemplo simplificado de uma interface de QoS baseada no GUI do Netgear. Você normalmente encontrará as configurações de QoS nos menus avançados. Se você tiver um roteador sem fio disponível, investigue as configurações de QoS. Às vezes, eles podem estar listados em "controle de banda" ou algo semelhante. Consulte a documentação do roteador sem fio ou pesquise na Internet "configurações de qos" para a marca e o modelo do seu roteador.

![[Pasted image 20240225192325.png]]

- # Packet Tracer - Conecte-se a uma rede sem fio
https://contenthub.netacad.com/legacy/ITE/7.01/pt/index.html#6.1.3.9

- #  Configurações do firewall
https://contenthub.netacad.com/legacy/ITE/7.01/pt/index.html#6.1.4.1


- # UPnP

UPnP (Universal Plug and Play, Plug and Play Universal) é um protocolo que permite que dispositivos se adicionem dinamicamente a uma rede, sem a necessidade de intervenção ou configuração do usuário. Embora conveniente, o UPnP não é seguro. O protocolo UPnP não tem nenhum método para autenticar dispositivos. Portanto, ele considera cada dispositivo como confiável. Além disso, o protocolo UPnP tem várias vulnerabilidades de segurança. Por exemplo, um malware pode usar o protocolo UPnP para redirecionar o tráfego para endereços IP diferentes fora da rede, enviando potencialmente, informações confidenciais para um hacker.

Muitos roteadores sem fio domésticos e de pequenos escritórios têm o UPnP ativado por padrão. Verifique, portanto essa configuração e desative-a, como mostra a figura.

Pesquise na Internet "ferramentas de perfil de vulnerabilidade" para determinar se o seu roteador sem fio está exposto a vulnerabilidades UPnP.

![[Pasted image 20240225195331.png]]
- # DMZ

Uma zona desmilitarizada (DMZ) é uma rede que fornece serviços a uma rede não confiável. Um servidor de e-mail, web, ou um servidor FTP são colocados geralmente na DMZ, para que o tráfego que usa o servidor não venha para dentro da rede local. Isso protege a rede interna contra ataques desse tráfego, mas não protege os servidores na DMZ de forma alguma. É comum que um firewall gerencie o tráfego de e para a DMZ.

Em um roteador sem fio, você pode criar uma DMZ para um dispositivo encaminhando todas as portas de tráfego da Internet para um endereço IP ou endereço MAC específico. Um servidor, uma máquina de jogo, ou uma câmera web podem estar na DMZ, para que o dispositivo possa ser acessado por qualquer pessoa. Por exemplo, o servidor Web na Figura 1 está na DMZ e recebe estaticamente o endereço IPv4 10.10.10.50. A Figura 2 mostra uma configuração típica em que qualquer fonte de tráfego da Internet será redirecionada para o endereço IPv4 10.10.10.50 do servidor Web. No entanto, o servidor da Web está exposto a ataques de hackers na internet e deve ter um software de firewall instalado.

![[Pasted image 20240225195419.png]]![[Pasted image 20240225195425.png]]

- # Encaminhamento de portas

Os firewalls de hardware podem ser usados para bloquear portas TCP e UDP para impedir o acesso não autorizado dentro e fora de uma LAN. No entanto, há situações em que portas específicas precisam ser abertas, para que determinados programas e aplicativos possam se comunicar com dispositivos em redes diferentes. Port forwarding (encaminhamento de portas) é um método baseado em regras de direcionamento de tráfego entre dispositivos em redes separadas.

Quando o tráfego chega no roteador, o roteador determina se o tráfego deverá ser encaminhado para um determinado dispositivo, com base no número da porta encontrado com o tráfego. Os números de porta são associados aos serviços específicos, como FTP, HTTP, HTTPS e POP3. As regras determinam que tráfego é enviado para a LAN. Por exemplo, um roteador pode ser configurado para encaminhar a porta 80, que é associada ao HTTP. Quando o roteador recebe um pacote com a porta destino 80, o roteador encaminha o tráfego para o servidor na rede que serve páginas web. Na figura, o encaminhamento de porta está ativado para a porta 80 e associado ao servidor web no endereço IPv4 10.10.10.50.

O port triggering permite que o roteador encaminhe, temporariamente, os dados, pelas portas de entrada, para um dispositivo específico. Você pode usar o port triggering para encaminhar dados a um computador, apenas quando um intervalo designado de portas é usado para fazer uma requisição de saída. Por exemplo, um videogame pode usar as portas 27000 a 27100 para se conectar com outros participantes. Essas são as portas para o port triggering. Um cliente de bate-papo pode usar a porta 56 para conectar os mesmos jogadores para que possam interagir uns com os outros. Nesse caso, se houver tráfego de jogos em uma porta de saída no intervalo de porta configurado do port triggering, o tráfego de bate-papo de entrada na porta 56 é encaminhado para o computador que está sendo usado para executar o videogame e o bate-papo com amigos. Quando o jogo acaba e as portas não estão mais sendo usadas, a porta 56 não tem mais permissão para enviar tráfego de nenhum tipo a esse computador.

![[Pasted image 20240225195536.png]]
- # Filtragem de endereços MAC

A filtragem de endereços MAC especifica exatamente quais endereços MAC do dispositivo têm permissão ou são impedidos de enviar dados na sua rede. Muitos roteadores sem fio oferecem apenas a opção de permitir ou bloquear endereços MAC, mas não os dois. Os técnicos normalmente configuram os endereços MAC permitidos. O endereço MAC do seu computador Windows pode ser encontrado com o comando **ipconfig /all** como mostrado na Figura 1.

![[Pasted image 20240225195636.png]]

Pode ser necessário pesquisar na Internet onde encontrar o endereço MAC em um dispositivo específico. Encontrar o endereço MAC nem sempre é simples, porque nem todos os dispositivos o chamam de endereço MAC. O Windows o chama de "Endereço físico", como mostra a Figura 1. Em um iPhone, ele é chamado de "Endereço Wi-Fi" e, no Android, é chamado de "Endereço MAC Wi-Fi", como mostra a Figura 2.

![[Pasted image 20240225195642.png]]

Além disso, seu dispositivo pode ter dois ou mais endereços MAC. Por exemplo, o PlayStation 4 na Figura 3 possui dois endereços MAC: um para redes com fio e outro para redes sem fio. Da mesma forma, um PC com Windows pode ter vários endereços MAC. Como mostra a Figura 4, o PC possui três endereços MAC: com fio, sem fio e virtual.

![[Pasted image 20240225195650.png]]

**Nota**: A última metade dos endereços MAC e outras informações de identificação estão desfocadas nas Figuras 2 e 3. Os últimos seis números hexadecimais são substituídos por um **X** na figura 4.

![[Pasted image 20240225195656.png]]
Por fim, considere o fato de que novos dispositivos podem ser adicionados à rede a qualquer momento. Você pode ver como o técnico responsável pela configuração manual de todos esses endereços MAC pode ficar sobrecarregado. Imagine ter que inserir e manter manualmente dezenas de endereços MAC em uma interface como a mostrada na Figura 5.
![[Pasted image 20240225195702.png]]
No entanto, a filtragem de endereço MAC pode ser sua única opção. Soluções melhores, como segurança de porta, exigem a compra de um roteador mais caro ou um dispositivo de firewall separado, e estão além do escopo deste curso.

- # Lista Branca e Lista Negra

A lista de permissões e a lista negra especificam quais endereços IP são permitidos ou negados na sua rede. Semelhante à filtragem de endereços MAC, você pode configurar manualmente endereços IP específicos para permitir ou negar sua rede. Em um roteador sem fio, isso geralmente é feito usando uma lista de acesso ou política de acesso, conforme mostrado na figura. Consulte a documentação do seu roteador sem fio para obter etapas específicas ou procure um tutorial na Internet.

A lista branca é uma boa ferramenta para permitir que seus usuários, como filhos ou funcionários, acessem os endereços IP que você aprova. Você também pode colocar na lista negra ou bloquear explicitamente sites conhecidos. No entanto, semelhante à filtragem de endereço MAC, isso pode se tornar um fardo. Existem melhores soluções. Pesquise na Internet por "software de controle parental" e "filtros de conteúdo".

- # Packet Tracer - Definir configurações de firewall

https://contenthub.netacad.com/legacy/ITE/7.01/pt/index.html#6.1.4.7

- # Internet das Coisas (IoT)

A internet de hoje é significativamente diferente da internet das últimas décadas. A internet de hoje é mais do que email, páginas da web e transferências de arquivos entre computadores. A Internet em evolução está se tornando uma Internet das Coisas (IoT). Os únicos dispositivos que acessam a Internet não serão mais computadores, tablets e smartphones. Os dispositivos equipados com sensor e prontos para a Internet de amanhã incluirão tudo, desde automóveis e dispositivos biomédicos, até eletrodomésticos e ecossistemas naturais.

Você já pode ter alguns dispositivos IoT em sua casa. Você pode comprar todos os tipos de dispositivos conectados, incluindo termostatos, interruptores de luz, câmeras de segurança, trancas de portas e assistentes digitais ativados por voz (como Amazon Alexis e Google Home). Todos esses dispositivos podem ser conectados à sua rede. Além disso, muitos deles podem ser gerenciados diretamente a partir de um aplicativo para smartphone, conforme mostrado na figura.

- # Dispositivos IoT no Packet Tracer

Neste momento em sua infância, o mercado da IoT ainda não concordou com um conjunto de padrões para instalação e configuração de dispositivos da IoT. A configuração de dispositivos IoT é muito específica do dispositivo. Consulte a documentação ou o site do fabricante para obter guias de configuração.

Neste curso, você usará o Packet Tracer para explorar uma configuração básica do dispositivo IoT. A figura mostra todos os dispositivos IoT no Packet Tracer. O Packet Tracer também inclui vários sensores e atuadores. Na figura, os sensores são mostrados no painel inferior da interface do Packet Tracer.

- # Packet Tracer -Controlar dispositivos IoT
https://contenthub.netacad.com/legacy/ITE/7.01/pt/index.html#6.1.5.3

- # Processo Básico de Solução de Problemas para Redes

![[Pasted image 20240225195836.png]]
- # Identificar o Problema

Os problemas de rede podem ser simples ou complexos e podem resultar de uma combinação de problemas de hardware, software e conectividade. Como técnico, você deve desenvolver um método lógico e coerente para diagnosticar problemas de rede eliminando um problema de cada vez.

Por exemplo, para avaliar o problema, determine quantos dispositivos estão enfrentando o problema. Se houver um problema com um dispositivo, comece com esse dispositivo. Se houver problemas com todos os dispositivos, inicie o processo de solução de problemas na sala de rede em que todos os dispositivos estão conectados.

A primeira etapa no processo de solução de problemas é identificar o problema. Use a lista de perguntas abertas e fechadas na figura como ponto de partida para coletar informações do cliente.

![[Pasted image 20240225195850.png]]
- # Estabelecer uma Teoria de Causas Prováveis

Depois de falar com o cliente, você pode estabelecer uma teoria para as causas prováveis. A lista na figura fornece algumas causas prováveis comuns para problemas de rede.

![[Pasted image 20240225195903.png]]

- # Testar a Teoria para Determinar a Causa

Depois que você tiver desenvolvido algumas teorias sobre o que está errado, teste-as para determinar a causa do problema. Depois que a teoria for confirmada, determine os próximos passos para resolver o problema. A lista acima mostra alguns procedimentos rápidos que você pode usar para determinar a causa exata do problema ou até mesmo corrigi-lo. Se um procedimento rápido corrigir o problema, verifique a funcionalidade total do sistema. Caso um procedimento rápido não corrija o problema, talvez seja necessário pesquisar mais para estabelecer a causa exata dele.

![[Pasted image 20240225195915.png]]

- # Estabelecer Plano de Ação para Resolver o Problema e Implementar a Solução

Depois de determinar a causa exata do problema, estabeleça um plano de ação para resolvê-lo e implementar a solução. A lista na figura mostra algumas fontes que você pode usar para reunir informações adicionais para resolver um problema.

![[Pasted image 20240225195940.png]]

- # Verifique a funcionalidade total e, se aplicável, implemente medidas preventivas

Uma vez corrigido o problema, verifique a funcionalidade total e, se aplicável, implemente medidas preventivas. A lista na figura mostra algumas etapas para verificar a solução.

![[Pasted image 20240225195951.png]]

- # Documentar Descobertas, Ações e Resultados

Na etapa final do processo de solução de problemas, documente suas descobertas, ações e resultados, conforme mostrado na lista na figura.

![[Pasted image 20240225200000.png]]
![[Pasted image 20240225200112.png]]

![[Pasted image 20240225200128.png]]![[Pasted image 20240225200143.png]]
![[Pasted image 20240225200153.png]]![[Pasted image 20240225200200.png]]
![[Pasted image 20240225200206.png]]![[Pasted image 20240225200212.png]]
![[Pasted image 20240225200217.png]]
![[Pasted image 20240225200225.png]]![[Pasted image 20240225200431.png]]
![[Pasted image 20240225200439.png]]
![[Pasted image 20240225200446.png]]![[Pasted image 20240225200454.png]]
![[Pasted image 20240225200501.png]]
![[Pasted image 20240225200512.png]]
![[Pasted image 20240225200518.png]]
![[Pasted image 20240225200523.png]]
![[Pasted image 20240225200545.png]]![[Pasted image 20240225200550.png]]
![[Pasted image 20240225200554.png]]
![[Pasted image 20240225200603.png]]
![[Pasted image 20240225200608.png]]

- # Capítulo 6: Rede Aplicada

Neste capítulo, você aprendeu como configurar NICs, conectar dispositivos a um roteador sem fio e configurar um roteador sem fio para conectividade de rede. Você também aprendeu sobre firewalls, dispositivos IoT e solução de problemas de rede. Você aprendeu sobre os endereços MAC de 48 bits que identificaram dispositivos conectados a uma LAN Ethernet e os dois tipos de endereços IP, IPv4 e IPv6. Os endereços IPv4 têm 32 bits e são gravados em formato decimal pontilhado, enquanto os endereços IPv6 têm 128 bits e gravados em formato hexadecimal.

A configuração de um endereço IP em um dispositivo pode ser feita manualmente ou dinamicamente usando o DHCP. Você aprendeu que o endereçamento manual ou estático é apropriado para redes pequenas, enquanto o DHCP é mais adequado para redes maiores. Além de um endereço IP, o DHCP também pode atribuir automaticamente a máscara de sub-rede, o gateway padrão e o endereço dos servidores DNS. Você configurou uma NIC para usar o DHCP em um computador Windows através de um exercício de laboratório. Você conseguiu verificar a configuração da rede usando o comando ipconfig /all no Windows e testar a conectividade usando o ping.

Você aprendeu como configurar uma rede sem fio, incluindo a configuração de um roteador sem fio com configurações sem fio básicas, NAT, configurações de firewall e QoS. Você concluiu dois laboratórios, um sobre a configuração de uma rede sem fio e, em seguida, um laboratório sobre a configuração de firewall. O laboratório de rede sem fio solicitou que você definisse configurações básicas de conexão sem fio em um host sem fio e um ponto de acesso e depois testasse a conectividade. No laboratório de firewall, você configurou a filtragem MAC, uma DMZ e o encaminhamento de porta.

A internet hoje está se tornando mais do que apenas computadores, tablets e smartphones. Está se tornando uma IoT. São dispositivos equipados com sensores e prontos para a Internet que incluem automóveis, dispositivos biomédicos, eletrodomésticos e ecossistemas naturais. Você usou o Packet Tracer para explorar os dispositivos IoT e sua configuração básica.

No final do capítulo, você aprendeu as seis etapas do processo de solução de problemas no que diz respeito às redes.


---
# AULA GRAVADA

![[Pasted image 20240228222410.png]]
![[Pasted image 20240228222441.png]]

Para conectar um computar em rede o elemento principal é uma placa de rede, seja ela com ou sem fio.

Quando há um serviço que atribua automaticamente essas configuração de endereço IP no dispositivo, que é um serviço DHCP, não é necessário configurar. pq o serviço entrega automaticamente a configuração de IP.

O servidor DNS faz a tradução da URL para o endereço IP do servidor. 

Duplex, envia e recebe dados ao mesmo tempo. Half-duplex, envia ou recebe dados, mas não simultaneamente

![[Pasted image 20240228224252.png]]

A configuração do roteador normalmente é através de uma interface web.

![[Pasted image 20240228224400.png]]

Uma das grandes vantagens de se utilizar uma rede, é utilizar o serviço de redes, sendo o principal o de compartilhamento.

O mapeamento de uma unidade local, é quando um computador A, pode ter acesso a arquivos de um computador B, como se esses arquivos estivessem salvos localmente, utilizando o serviço de compartilhamento.

As permissões  podem ser definidas no momento que definimos o compartilhamento. 

![[Pasted image 20240228224745.png]]

*Tecnologias de banda lagar disponíveis *

![[Pasted image 20240228224938.png]]

O DSL usa linhas telefônicas para fornecer as comunicações de dados digitais entre o usuário e a companhia telefônica.

A tecnologia de celular usa os serviços da operadora de celular.

O satélite é uma tecnologia cara e lenta.

![[Pasted image 20240228225233.png]]


O datacenter é uma infraestrutura, e a nuvem é um serviço.

Em um data-center temos a computação em nuvem, uma rede de alta velocidade, software como serviço, segurança de dados e também oferece opções de virtualização.

A nuvem possui alguns modelos:
- privado (modelo exclusivo para algum cliente)
- público (qualquer cliente pode utilizar )
- comunitário (alguma determinada comunidade pode usar)
- híbrido

![[Pasted image 20240228232214.png]]

![[Pasted image 20240228232226.png]]

O protocolo HTTP/HTTPS é utilizado para se comunicar com o servidor que hospeda as páginas web, para que as páginas sejam visualizadas.

SMTP server para enviar e-mail; POP e IMAP servem para receber e-mail

![[Pasted image 20240228232621.png]]
![[Pasted image 20240228232903.png]]

O cache no servidor proxy armazena uma cópia dessas páginas no dispositivo localmente e devolve a solicitação.

o IPS além de detectar também interveem 

![[Pasted image 20240228232932.png]]![[Pasted image 20240228233008.png]]
![[Pasted image 20240228233136.png]]

Na parte de identificar um problema, você entra em contato com o usuário, e faz uma série de perguntas a ele com o objetivo de obter pistas para identificar a causa do problema.

![[Pasted image 20240228233156.png]]

*Os usuários legítimos tem acesso remoto negado* - problema de configuração.

![[Pasted image 20240228233336.png]]
