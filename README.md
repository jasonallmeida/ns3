# Simulador de redes ns-3
O ns-3 me foi apresentado no meu curso de Tecnologia em Redes de Computadores da minha faculdade.
Resolvi usar o Lubuntu 26.04 e o ns-3.48 em uma VM do VirtualBox. Visto que o material do meu curso usou versões bem mais antigas tanto do Linux quanto do ns-3, e ainda abordou sobre ferramenta Bake que já não é mais usada para isso.

# Atualização do sistema
Antes de começar a fazer a instalação do NS-3, atualizei o sistema como um todo.

``` bash
sudo apt updade
sudo apt upgrade
```
<img width="1920" height="970" alt="Update e Upgrade" src="https://github.com/user-attachments/assets/9be1ccc8-a825-4029-b4ec-2a417a8bf06f" />

# Requisitos
Para as versões do ns-3.36 e posteriores, precisei instalar os seguintes pacotes:\
`sudo apt install g++ python3 cmake ninja-build git`\
`sudo apt install ccache`\
`sudo apt install clang-format clang-tidy`\
`gdb valgrind`

Site de referência: https://www.nsnam.org/docs/release/3.48/installation/html/linux.html#requirements

# Download via tarball
Agora vou baixar o arquivo compactado do ns-3 que contém todos os arquivos necessários.
```
cd 
mkdir tarballs
cd tarballs
wget http://www.nsnam.org/release/ns-allinone-3.48.tar.bz2
tar xjf ns-allinone-3.48.tar.bz2
```

Além disso para execução dos script segui o pdf  `ns-3-tutorial`

# Construindo e testando o NS-3
Dentro da pasta descompactada do ns-3 rodar os seguintes comandos:\
`./ns3 configure --enable-examples --enable-tests`\
`./ns3 build`\
<img width="1918" height="946" alt="build" src="https://github.com/user-attachments/assets/d8481c32-e983-47ea-85c4-a77e65ba3fa7" />
`./test.py`\
Teste de instalação das unidades do NS-3\
<img width="1874" height="952" alt="test" src="https://github.com/user-attachments/assets/10d86a8b-3477-4017-9ff1-20ba668a85b5" />
 


# Testando o script hello-simulator.cc e first.cc
<img width="1912" height="974" alt="Hello simulator" src="https://github.com/user-attachments/assets/755defeb-3aee-43f5-a4b0-705aff4c3a3d" />
<img width="1918" height="975" alt="first cc" src="https://github.com/user-attachments/assets/b6e99b95-b311-408e-84da-d59c98831d0d" />


# Instalação dos pacotes para rodar o NetAnim
`sudo apt install qtbase5-dev qtchooser qt5-qmake qtbase5-dev-tools`

# Downloading NetAnim
Primeiro instalar o mercurial: `sudo apt install mercurial`
Depois 
`hg clone http://code.nsnam.org/netanim`

# Building and Starting NetAnim
`cd netanim`
`make clean`
`qmake NetAnim.pro`
 make`

# Configuração NetAnim
O procedimento 
No meu caso copiei o first.cc da pasta examples e joguei para pasta scratch e nomeei ele para myfirst.cc.
Após isso editei o myfirst.cc colocando a linha no cabeçalho do código #include "ns3/netanim-module.h", e AnimationInterface anim ("animation.xml") antes de Simulator::Run();
O procedimento de edição feito no arquivo myfisrt.cc está no site https://www.nsnam.org/wiki/NetAnim_3.108#Prerequisites

depois editado executei o comando `./ns3 run myfirst.cc`

Vai ser criado um arquivo .xml da animação, no meu caso nomeei como animation.xml

# Executando o .xml
Acessar a pasta de instalação do Netanim pelo Terminal e excutar ./NetAnim para abrir o programa
depois só procurar pelo .xml e importar para visualizar a animação

Abrindo o .xml no NetAnim
<img width="1920" height="971" alt="xml myfirst cc" src="https://github.com/user-attachments/assets/ef5add71-b9fd-4c36-b561-da6cacb71b32" />

# Sites
https://www.nsnam.org/docs/release/3.48/installation/html/index.html \
https://www.nsnam.org/wiki/NetAnim_3.108#Prerequisites
