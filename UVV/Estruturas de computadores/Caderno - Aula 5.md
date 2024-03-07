# Cisco

- Introdução

As empresas, grandes e pequenas, estão investindo fortemente na virtualização e na computação em nuvem. Portanto, é importante que os técnicos e profissionais de ti entendam essas duas tecnologias. Embora as duas tecnologias se sobreponham, elas são, na verdade, duas tecnologias diferentes. O software de virtualização permite que um servidor físico execute vários ambientes computacionais individuais. A computação em nuvem é um termo usado para descrever a disponibilidade de recursos de computação compartilhada, software ou dados, como serviço e sob demanda pela Internet.

Neste capítulo, você aprenderá sobre as vantagens que a virtualização tem sobre o uso tradicional de servidores dedicados, como o uso de menos recursos, exigindo menos espaço, reduzindo custos e aumentando o tempo de atividade do servidor. Você também aprenderá os termos que são usados ao discutir a virtualização do lado do cliente, como o computador host, que se refere ao computador físico controlado por um usuário. O sistema operacional do host é o so no computador host, e o SO convidado é o sistema operacional em execução na máquina virtual no computador host.

Você aprenderá sobre os dois tipos de hipervisores: hypervisor de tipo 1 (nativo), também chamado de hypervisor bare-metal e hypervisor tipo 2 (hospedado). Você também aprenderá os requisitos mínimos do sistema para executar o Windows Hyper-V, que é um hypervisor tipo 2, no Windows 7, no WIndows 8 e no Windows 10.

É importante não conhecer apenas a virtualização e a tecnologia em nuvem, mas também criar habilidades práticas. Neste capítulo, você concluirá um laboratório instalando Linux em uma máquina virtual.

- # Explicação em vídeo - O que é a nuvem?

Have you ever had something happen to your computer or mobile device, causing you to lose important information like documents, photos, or music? Perhaps you had a backup, but restoring the lost data and the applications on another computer can be both costly and time consuming. Or have you ever needed access to information on a specific computer, but that computer was somewhere else? Maybe you had the data on a USB drive, but the computer you are using doesn't have the right application software to access it. Traditionally, we store data and software programs on the computer's hard disk drive. This is known as local storage, but the data and the applications needed to access that data may be lost or not available. What if all that information, the data and the applications, were available over the network, in the cloud?

The cloud simply means the information is stored somewhere else, remotely accessible over the network, and typically over the Internet. It is like having a remote hard disk drive that you can access any time anywhere.

Many applications can be accessed using a web browser. These are known as web apps. A web app is an application software that is stored on a remote server and delivered over the Internet through a web browser such as Chrome or Firefox. Common web apps include Google Docs, Google Photos, Office 365. The cloud also allows for remote file storage and file sharing. For example, Google Drive, Dropbox, and Microsoft OneDrive. It is still a good idea to keep backups of your information, either locally or on a different cloud service. What if that cloud service is no longer in operation? How do you get your information back? Or even can you? And you need to be cautious about trusting your information to a third party. Are they taking the necessary security precautions to protect your data? What if the cloud company loses your data, or has a data breach, and someone now has access to all your information? 

The trend in the last several years has seen individuals and companies moving to cloud services more and more. The cloud offers many advantages, including always-on availability, being able to access your data any time, anywhere, independence from a single point of failure, no longer dependent on that data or software only being available on a single device or computer, improved collaboration, allowing people to share information and collaborate more easily, easier software maintenance, the company operating the cloud services handles all the software upgrades and maintenance. The point is that these services exist outside of your environment, and because these services have traditionally been represented as a cloud icon in topology diagrams, we now say that these services are "in the cloud." 

- # Computação e virtualização em nuvem

Os termos “computação em nuvem” e “virtualização” são frequentemente usados de forma intercambiável, embora signifiquem coisas diferentes.

A virtualização permite que um único computador hospede vários computadores virtuais independentes que compartilham o hardware do computador host. O software de virtualização separa o hardware físico real das instâncias da máquina virtual (VM). As VMs têm seus próprios sistemas operacionais e se conectam aos recursos de hardware por meio de software em execução no computador host. Uma imagem de uma VM pode ser salva como um arquivo e, em seguida, reiniciada quando necessário.

É importante lembrar que todas as VMs compartilham os recursos do computador host. Portanto, o fator de limitação no número de VMs que podem ser executadas ao mesmo tempo está diretamente relacionado à quantidade de capacidade de processamento, memória e armazenamento.

A computação em nuvem separa os aplicativos do hardware. Ele oferece às empresas a entrega sob demanda de serviços de computação pela rede. Os provedores de serviços, como Amazon Web Services (AWS), gerenciam a infraestrutura de nuvem que inclui dispositivos de rede, servidores e dispositivos de armazenamento e são normalmente alojados em um Data Center.

A virtualização é a base que suporta a computação em nuvem. Fornecedores como a AWS oferecem serviços em nuvem usando servidores poderosos que podem provisionar dinamicamente servidores virtuais conforme necessário.

Sem virtualização, a computação em nuvem, como é mais amplamente implementada, não seria possível.

- # Implantação tradicional do servidor

Para apreciar totalmente a virtualização, é necessário primeiro entender como os servidores são usados em uma empresa.

Tradicionalmente, as empresas disponibilizaram aplicativos e serviços para seus usuários usando servidores dedicados poderosos, como mostrado na figura. Esses servidores Windows e Linux são computadores high-end com grandes quantidades de RAM, processadores poderosos e vários dispositivos de armazenamento grandes. Novos servidores serão adicionados se mais usuários ou novos serviços forem necessários.

Os problemas com a abordagem de implantação de servidor tradicional incluem:

- **Recursos desperdiçados** – isso ocorre quando servidores dedicados ficam ociosos por longos períodos de espera até que sejam necessários para entregar seu serviço específico. Enquanto isso, esses servidores desperdiçam energia.

- **Ponto único de falha** – isso ocorre quando um servidor dedicado falha ou fica offline. Não há servidores de backup para lidar com a falha.

- **Expansão de servidor** – Isso ocorre quando uma empresa não tem espaço adequado para abrigar servidores subutilizados fisicamente. Os servidores ocupam mais espaço do que é garantido pelos serviços que fornecem.

A virtualização de servidores para usar recursos com mais eficiência resolve esses problemas.

![[Pasted image 20240305213629.png]]

- # Virtualização de servidores

A virtualização de servidores aproveita os recursos inativos para reduzir o número de servidores necessários para fornecer serviços aos usuários.

Um programa especial chamado hypervisor é usado para gerenciar os recursos do computador e várias VMs. Ele fornece acesso às VMs a todo o hardware da máquina física, como CPUs, memória, controladores de disco e NICs. Cada uma dessas VMs executa um sistema operacional completo e separado.

Com a virtualização, as empresas agora podem consolidar o número de servidores. Por exemplo, não é raro 100 servidores físicos serem consolidados como máquinas virtuais em 10 servidores físicos que usam hipervisores. Na figura, os oito servidores dedicados anteriores foram consolidados em dois servidores com hypervisores para comportar as várias instâncias virtuais dos sistemas operacionais.

![[Pasted image 20240305213854.png]]

## - vantagens da virtualização de servidores

![[Pasted image 20240305214004.png]]
![[Pasted image 20240305214011.png]]
![[Pasted image 20240305214020.png]]
![[Pasted image 20240305214034.png]]
![[Pasted image 20240305214047.png]]
![[Pasted image 20240305214058.png]]
![[Pasted image 20240305214116.png]]
![[Pasted image 20240305214125.png]]
![[Pasted image 20240305214239.png]]

- # Virtualização do Lado do Cliente

Muitas empresas usam a virtualização de servidor para otimizar os recursos de rede e reduzir os custos de equipamentos e manutenção. As empresas também usam a virtualização do lado do cliente para permitir que os usuários com necessidades específicas executem VMs no computador local.

A virtualização do lado do cliente é benéfica para a equipe de ti, oferece suporte a pessoas, desenvolvedores e testadores de software e por motivos educacionais. Fornece aos usuários recursos para testar novos sistemas operacionais, software ou para executar software mais antigo. Também pode ser usado para sandbox e criar um ambiente isolado seguro para abrir ou executar um arquivo suspeito.

Alguns termos que são usados ao discutir a virtualização do lado do cliente incluem:

- **Computador host** – Esse é o computador físico controlado por um usuário. As VMs usam os recursos do sistema da máquina host para inicializar e executar um sistema operacional.

- **Sistema operacional de host (SO host)** - Este é o sistema operacional do computador host. Os usuários podem usar um emulador de virtualização, como VirtualBox no sistema operacional do host para criar e gerenciar VMs.

- **Sistema operacional convidado (SO convidado)** - Este é o sistema operacional que está sendo executado na VM. Os drivers são necessários para executar a versão diferente do sistema operacional.

O sistema operacional convidado é independente do sistema operacional do host. Por exemplo, o sistema operacional do host pode ser o Windows 10 e a VM pode ter o Windows 7 instalado. Esse convidado da VM seria o Windows 7. Neste exemplo, o sistema operacional convidado (Windows 7) não interfere no sistema operacional do host (Windows 10) no computador host.

Os sistemas operacionais host e convidado não precisam ser da mesma família. Por exemplo, o sistema operacional do host pode ser o Windows 10, enquanto o SO convidado é Linux. Isso é de benefício para os usuários que precisam aumentar a funcionalidade do computador host, executando vários sistemas operacionais ao mesmo tempo.

A figura exibe um diagrama lógico da máquina virtual. A caixa cinza inferior representa o computador físico com seu sistema operacional host (por exemplo, Windows 10). Hyper-V, Virtual PC e VirtualBox são exemplos de software de virtualização ou emulador que podem ser usados para criar e gerenciar as três VMs mostradas na parte superior da figura.

![[Pasted image 20240305214506.png]]

- # Hipervisores tipo 1 e tipo 2

O hypervisor, também chamado de Virtual Machine Manager (VMM), é o cérebro da virtualização. O hypervisor é o software usado no computador host para criar e gerenciar VMs.

O hypervisor aloca os recursos físicos do sistema, como CPU, RAM e armazenamento, para cada VM, conforme necessário. Isso garante que a operação de uma máquina virtual não interfira na outra.

Há dois tipos de hipervisores, como mostrado na Figura 1.

- **Hypervisor tipo 1 (nativo)** – Também chamado de hypervisor bare-metal e geralmente usado com virtualização de servidor. Ele roda diretamente no hardware de um host e gerencia a alocação de recursos do sistema para sistemas operacionais virtuais.

- **Hypervisor tipo 2 (hospedado)** – isso é hospedado por um sistema operacional e normalmente é usado com virtualização do lado do cliente. O software de virtualização, como Windows Hyper-V e VMware Estação de trabalho, são exemplos de um hypervisor tipo 2.

Os hipervisores tipo 1 são comuns em data centers e na computação em nuvem. Os exemplos de hipervisores tipo 1 incluem ⁪VMware VSphere/ESXi, Xen e Oracle servidor VM.

Os hipervisores tipo 2, como VMware Estação de trabalho, funcionam com o computador host para criar e usar várias VMs. O Windows Hyper-V também está incluído no Windows 10 pro e no Windows Server (2012 e 2016).

![[Pasted image 20240305214621.png]]

A Figura 2 mostra um exemplo de implementação de um hypervisor tipo 1 e tipo 2. Na implementação tipo 1, o ⁪VMware VSphere é executado diretamente no hardware do servidor sem sistema operacional. ⁪VMware VSphere foi usado para criar uma VM do Windows Server e uma VM de servidor Linux. Na implementação tipo 2, o sistema operacional host no computador é o Windows 10. O Windows Hyper-V foi usado para criar e gerenciar a VM do Windows 7 e uma VM de Linux.

Os emuladores do lado do cliente podem executar o software destinado a um sistema operacional convidado diferente ou um sistema operacional destinado a hardwares diferentes. Por exemplo, se o sistema operacional do host foi Linux e criamos uma VM usando o Windows 7 para executar um aplicativo que só é executado no Windows 7. O computador host Linux irá fingir ser um computador com Windows 7.

![[Pasted image 20240305214709.png]]

- # Requisitos da Máquina Virtual

A computação virtual exige configurações de hardware mais poderosas porque cada instalação precisa de seus próprios recursos.

Todas as máquinas virtuais compartilham os seguintes requisitos básicos do sistema:

- **Suporte do processador** – os processadores, como Intel VT e AMD-V, foram projetados especificamente para suportar a virtualização. Talvez seja necessário ativar o recurso de virtualização nesses processadores. Os processadores com vários núcleos também são recomendados como os núcleos adicionais aumentam a velocidade e a capacidade de resposta ao executar várias VMs.

- **Suporte à memória** – considere que você precisa de memória para o sistema operacional host e precisará agora de RAM suficiente para atender aos requisitos de cada VM e ao seu SO convidado.

- **Armazenamento** – cada VM cria arquivos muito grandes para armazenar sistemas operacionais, aplicativos e todos os dados da VM. Você também deve considerar que uma VM ativa precisará de alguns GB de espaço de armazenamento. Portanto, unidades grandes e rápidas são recomendadas.

- **Requisitos de rede** – requisitos de conexão de rede dependem do tipo de VM. Algumas VMs não exigem conexões externas enquanto outras fazem. As VMs podem ser configuradas em uma rede com ponte, NAT, somente host ou especial para se conectarem apenas a outras VMs. Para se conectar à Internet, uma VM usa um adaptador de rede virtual que simula o adaptador de host real. Em seguida, o adaptador de rede virtual se conecta pela NIC física para estabelecer uma conexão com a Internet.

Os requisitos mínimos do sistema para Windows Hyper-V para Windows 10 e Windows 8 e Windows Virtual PC para Windows 7 são exibidos nas Figuras 1, 2 e 3, respectivamente.

![[Pasted image 20240305214909.png]]

![[Pasted image 20240305214917.png]]

![[Pasted image 20240305214926.png]]

Como um computador físico, as VMs são suscetíveis às mesmas ameaças e ataques maliciosos. Embora as VMs sejam isoladas do host, elas podem compartilhar recursos (por exemplo, NIC, pastas e arquivos). Os usuários devem exercer as mesmas considerações de segurança que o host e instalar o software de segurança, ativar recursos de firewall, instalar patches e atualizar o sistema operacional e os programas. Também é importante manter o software de virtualização atualizado.


![[Pasted image 20240305215012.png]]

- # Como usamos a nuvem

A computação em nuvem fornece aos usuários a entrega sob demanda dos serviços de computação pela Internet. Os serviços de computação em nuvem são proprietários e hospedados por provedores de serviços. A maioria de nós já usa serviços em nuvem ao usar aplicativos de mídia social, acessar uma biblioteca de músicas on-line ou usar o armazenamento on-line para salvar fotos. As empresas geralmente pagam os provedores de nuvem uma taxa de uso com base no acesso e uso de serviços do usuário.

![[Pasted image 20240306184323.png]]
![[Pasted image 20240306184335.png]]
![[Pasted image 20240306184640.png]]
![[Pasted image 20240306184656.png]]
![[Pasted image 20240306184708.png]]

- # Serviços em nuvem

Os provedores de serviços em nuvem podem fornecer vários serviços adaptados para atender às necessidades dos clientes. No entanto, a maioria dos serviços de computação em nuvem pode ser categorizada em três serviços principais de computação em nuvem, conforme definido pelo Instituto Nacional de Padrões e Tecnologia (NIST) em sua Publicação Especial (800-145):

- **Software como serviço (SaaS)** -o provedor de nuvem fornece acesso a serviços, como e-mail, calendário, comunicação e ferramentas de escritório pela Internet, com base na assinatura. Os usuários acessam o software usando um navegador. As vantagens incluem custos antecipados mínimos para clientes e disponibilidade imediata de aplicativos. Os provedores de SaaS incluem o software de relacionamento de gerenciamento de cliente do Salesforce (CRM), Microsoft Office 365, MS SharePoint software e Google G Suite.

- **Plataforma como serviço (PaaS)** – o provedor de nuvem fornece acesso a sistemas operacionais, ferramentas de desenvolvimento, linguagens de programação e bibliotecas usadas para desenvolver, testar e entregar aplicativos. Isso é útil para os desenvolvedores de aplicativos. O provedor de nuvem gerencia a rede, os servidores e a infraestrutura de nuvem subjacentes. Os provedores de PaaS incluem o Amazon Web Service, Oracle Cloud, Google plataforma de nuvem e Microsoft Azure.

- **Infraestrutura como serviço (IaaS)** - O provedor de nuvem gerencia a rede e fornece às organizações acesso a equipamentos de rede, serviços de rede virtualizados, armazenamento, software e infraestrutura de rede de suporte. Há muitas vantagens para as empresas adotarem o IaaS. As empresas não precisam investir em equipamentos de capital e somente pagar pelo uso sob demanda. A rede do provedor inclui redundância e elimina um único ponto de falha na infraestrutura de rede do provedor. A rede também pode se expandir perfeitamente com base nos requisitos atuais. Os provedores IaaS incluem o Amazon Web Service, DigitalOcean e Microsoft Azure.

Os provedores de serviços em nuvem estenderam o modelo IaaS para também fornecer TI como serviço (ITaaS). O ITaaS pode estender a capacidade da TI sem exigir investimento em nova infraestrutura, treinamento de novas equipes ou licenciamento de novo software. Esses serviços estão disponíveis sob demanda e de forma economicamente viável para qualquer dispositivo em qualquer lugar do mundo sem comprometer a segurança ou o funcionamento.

![[Pasted image 20240307164408.png]]


- ### Questões

Leia o cenário e selecione o modelo de nuvem usado.

#### Questão 1

![[Pasted image 20240307164606.png]]
#### resposta
Rede Pública 

#### Questão 2 

![[Pasted image 20240307164831.png]]
#### Resposta
Híbrida

#### Questão 3

![[Pasted image 20240307185757.png]]

#### resposta
privado

#### Questão 4

![[Pasted image 20240307185842.png]]

#### resposta
comunitário

![[Pasted image 20240307190111.png]]

- # Características da computação em nuvem

![[Pasted image 20240307190333.png]]
![[Pasted image 20240307190444.png]]
![[Pasted image 20240307190648.png]]
![[Pasted image 20240307191033.png]]
![[Pasted image 20240307191055.png]]


![[Pasted image 20240307191159.png]]


- # Conclusão 

Neste capítulo, você aprendeu que os termos virtualização e computação em nuvem costumam ser usados de forma intercambiável, embora realmente signifiquem coisas diferentes. A virtualização é uma tecnologia que permite que um único computador hospede vários computadores virtuais que compartilham o mesmo hardware de computador host. A computação em nuvem é uma tecnologia que permite a separação de aplicativos do hardware. A virtualização é a base que suporta a computação em nuvem.

Você aprendeu que a forma tradicional de fornecer aplicativos e serviços aos usuários usando servidores dedicados é ineficiente, não confiável e não escalável. Os servidores dedicados podem ficar inativos por longos períodos, eles são um ponto único de falha e ocupam muito espaço físico. A virtualização resolve esses problemas consolidando muitos servidores virtuais em um único servidor físico, tirando proveito dos recursos ociosos e reduzindo o número de servidores necessários para fornecer serviços aos usuários. Você aprendeu as muitas vantagens que a virtualização tem sobre o uso tradicional de servidores dedicados, como o melhor uso de recursos, menos espaço necessário, custo reduzido e aumento do tempo de atividade do servidor.

A computação em nuvem fornece aos usuários a entrega sob demanda dos serviços de computador pela Internet. A maioria de nós já usa esses serviços quando acessamos serviços de música on-line ou armazenamento de dados on-line. Você aprendeu sobre os tipos de serviços em nuvem oferecidos por provedores de serviços em nuvem. SaaS que fornece acesso a serviços, como e-mail, calendário, comunicação e ferramentas de escritório pela Internet, com base na assinatura. PaaS que fornece acesso a sistemas operacionais, ferramentas de desenvolvimento, linguagens de programação e bibliotecas usadas para desenvolver, testar e disponibilizar aplicativos. E o IaaS, que fornece às organizações acesso a equipamentos de rede, serviços de rede virtualizados, armazenamento, software e infraestrutura de rede de suporte.

O capítulo concluiu vários exercícios para testar sua compreensão da terminologia e das características da computação em nuvem.


---


# Aula gravada