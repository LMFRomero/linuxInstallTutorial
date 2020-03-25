# Tutorial de Instalação do Ubuntu (dual boot e máquina virtual)

Para começar, você vai precisar ter o [.iso](https://fileinfo.com/extension/iso "O que é uma iso?") do [Ubuntu](https://ubuntu.com/download/desktop "Site do Ubuntu para download") baixada no seu computador.

Recomendo a versão _18.04 LTS_ (Long Term Support) em vez da versão _19.10_  porque a versão 19.10 vai perder suporte em breve. Isso significa que os desenvolvedores não mais farão updates para essa versão.

Em breve, a versão _20.04 LTS_ será lançada e o Ubuntu possui [um recurso](https://ubuntu.com/tutorials/tutorial-upgrading-ubuntu-desktop#1-before-you-start "Como atualizar o Ubuntu de uma versão para outra") para atualizar suas versões de maneira simples. Fica a dica para quem quiser fazer o upgrade de maneira fácil.
Tendo feito o download da iso do Ubuntu, vamos começar a instalação.

Você pode fazer a instalação tanto em uma [máquina virtual](https://github.com/LMFRomero/linuxTutorial/blob/master/README.md#m%C3%A1quina-virtual), quanto em sua própria máquina por meio de um [dual boot](https://github.com/LMFRomero/linuxTutorial/blob/master/README.md#dual-boot)
<br>

### Dual boot:
Para instalar com dual boot, você precisa ter baixado o [Rufus](https://github.com/pbatard/rufus/releases/download/v3.9/rufus-3.9.exe "Baixe o Rufus aqui") no Windows, que é um programa pra criação de pendrives bootáveis. Antes de iniciar, lembre-se: os arquivos do pendrive serão **apagados**, por isso faça backup antes de iniciar.
Agora, abra o programa pra ver a seguinte tela:

<div style="text-align:center"><img src="https://rufus.ie/pics/rufus_pt_BR.png" title="Rufus"/></div><br>

Para tal, escolha o pendrive onde você irá criar o instalador em Dispositivos procure o arquivo .iso com o botão SELECIONAR, clique em INICIAR, depois em OK, na janela que abrirá.

Antes do próximo passo, veja quanta memória o seu Windows ocupa. Você pode fazer isso vendo nas propriedades do drive (C:):

<div style="text-align:center"><img src="https://raw.githubusercontent.com/LMFRomero/linuxTutorial/master/dbDiskSpace.png"/></div><br>


Agora que você tem um pendrive bootável, vamos em *Settings > Update & Security > Recovery* nas configurações do Windows, e, embaixo de *Advanced Startup*, clique em *Restart Now*.

Selecione a opção de iniciar com um dispositivo, e procure por USB HDD, ou algo próximo disso.

O GRUB será iniciado, e você escolhe a opção de instalar o Ubuntu.
<br>

Configure seu teclado, e avance para o próximo passo.

Também aparecerá uma tela para se conectar ao wifi.

Agora, você irá escolher como será a instalação.

<div style="text-align:center"><img src="https://raw.githubusercontent.com/LMFRomero/linuxTutorial/master/vmTipoDeInstall.png" /></div><br>

Prossiga com a *Instalação normal* e a opção de *Baixar atualizações enquanto instala o Ubuntu*

Agora é a parte do particionamento:
<br>
Você irá escolher a opção "*Instalar o Ubuntu ao lado do Windows*". Com isso, abrirá uma tela onde você pode arrastar um divisor para particionar o disco. **Tome cuidado para não deixar o Windows com menos memória do que o que está sendo usado para não apagar os arquivos e/ou corromper o sistema**.

Após escolher a memória destinada aos SOs, clique em *Instalar agora* e prossiga com a instalação até o final e você terá seu Ubuntu pronto pra ser usado.
<br>

### Máquina virtual:
Para instalar em uma máquina virtual, você irá precisar de um software de virtualização, como o [VirtualBox](https://download.virtualbox.org/virtualbox/6.1.4/VirtualBox-6.1.4-136177-Win.exe "Baixe o virtualbox aqui"). Instale caso você ainda não tenha.

<div style="text-align:center"><img src="https://raw.githubusercontent.com/LMFRomero/linuxTutorial/master/vmInicial.png" title="Rufus"/></div><br>

Clique em **New**, para criar uma nova máquina virtual, escolha um nome e coloque as configurações abaixo e depois clique em **Next**.

<div style="text-align:center"><img src="https://raw.githubusercontent.com/LMFRomero/linuxTutorial/master/vmNome%26SO.png"/></div><br>

Escolha um tamanho da memória que será alocada para a VM. Busque manter na faixa verde, pois, mesmo alocando mais RAM para a VM, o seu computador pode perder performance, fazendo a VM também perder. Pessoalmente, mantendo no limite da parte verde (~4096 MB, no meu caso), nunca deu muitos problemas.

<div style="text-align:center"><img src="https://raw.githubusercontent.com/LMFRomero/linuxTutorial/master/vmRAM.png"/></div><br>

Na próxima tela, você irá criar um novo disco virtual.

<div style="text-align:center"><img src="https://raw.githubusercontent.com/LMFRomero/linuxTutorial/master/vmHD.png"/></div><br>

Clique em **Create** e depois em **Next** até chegar nesta imagem:

<div style="text-align:center"><img src="https://raw.githubusercontent.com/LMFRomero/linuxTutorial/master/vmStorageSize.png"/></div><br>

Dê o tamanho de memória para o HD virtual que julgar necessário (a título de comparação, se você usar bastante Linux mas não como SO principal, 30 GBs é mais que suficiente) e clique em **Create**.

Agora, clique com o botão direito na VM e vá em **Settings**.

<div style="text-align:center"><img src="https://raw.githubusercontent.com/LMFRomero/linuxTutorial/master/vmSettings.png"/></div><br>

Lá você irá carregar a ISO com os seguintes passos:

<div style="text-align:center"><img src="https://raw.githubusercontent.com/LMFRomero/linuxTutorial/master/vmChooseISO.png"/></div><br>

Em *4*, você procura a ISO pelos seus diretórios.

Ainda em **Settings**, vá em Display (acima de *1*), procure por Graphics Controller e troque pra VBoxVGA (iremos desfazer isso depois). Isso nos ajudará a mudar a resolução na hora da instalação, para melhor entendimento, pois o VirtualBox pode colocar uma resolução automaticamente que ficará truncando a tela.

Após isso, clique em **OK** e depois em **Start**.

Em **View**, vá em *Virtual Screen 1* e use *Resize* para trocar a resolução para uma que mais te agrade. Depois, ainda em **View**, clique em *Adjust Windows Size*.

<div style="text-align:center"><img src="https://raw.githubusercontent.com/LMFRomero/linuxTutorial/master/vmInstalar.png" /></div><br>

Depois, clique em *Instalar Ubuntu*. 

Configure seu teclado, e avance para o próximo passo.

Agora, você irá escolher como será a instalação.

<div style="text-align:center"><img src="https://raw.githubusercontent.com/LMFRomero/linuxTutorial/master/vmTipoDeInstall.png" /></div><br>

Prossiga com a *Instalação normal* e a opção de *Baixar atualizações enquanto instala o Ubuntu*

Agora é a parte do particionamento. Nesse caso, como estamos usando o disco virtual, então iremos usar todo o disco:

<div style="text-align:center"><img src="https://raw.githubusercontent.com/LMFRomero/linuxTutorial/master/vmApagarDisco.png" /></div><br>

Clique em *Instalar agora*, e continue com a instalação até finalizar.

Quando o SO estiver inicializado, feche a máquina virtual (use a opção de "*Power off the machine*"). Clique com o botão direito na VM, vá em *Settings > Display > Graphics Controller* e selecione VMSVGA novamente. Inicie de novo a VM, vá em *Configurações > Dispositivos > Monitores* e ajuste a resolução. Após isso, seu Ubuntu estará pronto para uso. 
