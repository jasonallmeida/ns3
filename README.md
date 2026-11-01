# ns3
Usei os materiais disponíveis no site oficial do NSNAM para fazer a instalação e configuração do NS3:<https://www.nsnam.org/docs/release/3.48/installation/html/index.html>.
Foi usado a instalação me baseando nosite oficial: https://www.nsnam.org/docs/release/3.48/installation/html/index.html
Foi usado Lubuntu lubuntu-26.04.1 e ns-3.48
O NS3 foi apresentado a mim no meu curso CST de Redes de Computadores.
Resolvi seguir os passos usando uma versão mais recente do lubuntu e do próprio ns3.
Visto que no material da culdade tratava das versões mais antigas do simulador e ainda havia uso da ferramenta bake (já não é mais usada)
Download via tarball
Além disso para execução dos script segui o pdf  ns-3-tutorial

De inicio já inicie o update e upgrade para atualizar o sistema.


<img width="1920" height="970" alt="Update e Upgrade" src="https://github.com/user-attachments/assets/9be1ccc8-a825-4029-b4ec-2a417a8bf06f" />

Construção do NS3
<img width="1918" height="946" alt="build" src="https://github.com/user-attachments/assets/d8481c32-e983-47ea-85c4-a77e65ba3fa7" />

Teste de instalação das unidades do NS-3
<img width="1874" height="952" alt="test" src="https://github.com/user-attachments/assets/03b1a3d7-edeb-4db5-97c6-64fe8e380164" />

Executando scripts hello-simulator.cc
<img width="1912" height="974" alt="Hello simulator" src="https://github.com/user-attachments/assets/755defeb-3aee-43f5-a4b0-705aff4c3a3d" />
 e first.cc

 <img width="1918" height="975" alt="first cc" src="https://github.com/user-attachments/assets/b6e99b95-b311-408e-84da-d59c98831d0d" />


# Instalação dos pacotes para rodar o net anim
`sudo apt install qtbase5-dev qtchooser qt5-qmake qtbase5-dev-tools`

#Downloading NetAnim
Primeiro instalar o mercurial: sudo apt install mercurial
Depois hg clone http://code.nsnam.org/netanim

# Building and Starting NetAnim
cd netanim
make clean
qmake NetAnim.pro
make

# Configuração NetAnim
O procedimento 
No meu caso copiei o first.cc da pasta examples e joguei para pasta scratch e nomeei ele para myfirst.cc
O procedimento de edição feito no arquivo myfisrt.cc está no site https://www.nsnam.org/wiki/NetAnim_3.108#Prerequisites

depois editado executei o comando ./ns3 run myfirst.cc

Vai ser criado um arquivo .xml da animação, no meu caso nomeei como animation.xml

#Executando o .xml
Acessar a pasta de instalação do netanim pelo Terminal e excutar ./NetAnim para abrir o programa
depois só procurar pelo .xml e importar para visualizar a animação
