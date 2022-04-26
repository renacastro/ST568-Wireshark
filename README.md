# Laboratório de Redes de Comunicação (ST568) - WIRESHARK

## INSTALAÇÃO DO WIRESHARK
### Windows
O Wireshark pode ser baixado diretamente pelo site da Wireshark Foundation.

Acesse [https://www.wireshark.org/download.html](https://www.wireshark.org/download.html) e, dentro de "Stable Release", clique na versão compatível com o seu sistema: "Windows Installer (64-bit)" ou "Windows Installer (32-bit)".

Abra o arquivo baixado **.exe**. 

Antes de iniciar a instalação, o Windows irá perguntar de "Deseja permitir que este aplicativo faça alterações em seu dispositivo?". Caso o nome do aplicativo seja *Wireshark installer* e o fornecedor *Wireshark Foundation, Inc.*, clique em *Sim*.

Ao abrir o inicializador:
1. Uma tela de boas vindas surgirá, clique em "*Next*";

![Alt text](images/windows-install/windows-1.png "Windows Install 1")

2. Em "*License Agreement*", clique em "*Noted*";

![Alt text](images/windows-install/windows-2.png "Windows Install 2")

3.  Em "*Choose Components*", verifique se todos os componentes estão selecionados e clique em "*Next*";

![Alt text](images/windows-install/windows-3.png "Windows Install 3")

4. Em "*Additional Tasks*":
	1. Em "*Create Shortcuts*", selecione os itens de acordo com sua preferência;
	2. Em "*Associate File Extensions*", selecione a opção "*Associate trace file extensions with Wireshark*".

![Alt text](images/windows-install/windows-4.png "Windows Install 4")

5. Em "*Choose Install Location*", clique em "*Next*";

![Alt text](images/windows-install/windows-5.png "Windows Install 5")

6. Em "*Packet Capture*", verifique se "*Install Npcap (versão)*" está selecionado e clique em "*Next*";

![Alt text](images/windows-install/windows-6.png "Windows Install 6")

7. Em "*USB Capture*", verifique se "*USBPcap (versão)*" não está selecionado e clique em "*Next*" (não iremos utilizá-lo nesta aula, mas pode instalá-lo caso tenha a curiosidade de analisar o tráfego das portas USB);

![Alt text](images/windows-install/windows-7.png "Windows Install 7")

8. Aguarde a instalação do programa;
9. Uma janela de instalação no Npcap irá abrir;
10. Em "*License Agreement*", clique em "*I Agree*";

![Alt text](images/windows-install/windows-8.png "Windows Install 8")

11. Em "*Installation Options*" deixe tudo não selecionado (mas pode clicar em "*Support raw 802.11 traffic*" caso tenha a curiosidade de capturar e analisar o cabeçalho Wi-Fi);

![Alt text](images/windows-install/windows-9.png "Windows Install 9")

12. Aguarde a instalação do Npcap, quando "*Installation Complete*" aparecer, clique em "*Next*";

![Alt text](images/windows-install/windows-10.png "Windows Install 10")

13. Em "*Finished*", clique em "*Finish*". A instalação no Npcap irá fechar, e a instalação do Wireshark, continuar;

![Alt text](images/windows-install/windows-11.png "Windows Install 11")

14. Em "*Installation Complete*", clique em "*Next*";

![Alt text](images/windows-install/windows-12.png "Windows Install 12")

15. Em "*Completing Wireshark (...) Setup*, clique em "*Finish*". O instalador irá se fechar;

![Alt text](images/windows-install/windows-13.png "Windows Install 13")

16. Verifique se o programa foi instalado corretamente.




### Linux
Por padrão, a grande maioria dos sistemas Linux contam com o Wireshark em seus repositórios. A instalação é muito simples de ser feita e necessita apenas do uso do terminal como um superusuário.


Para instalá-lo em sistemas baseados em **Debian e Ubuntu**, copie e cole o comando abaixo em seu terminal:
~~~
sudo apt update && sudo apt install wireshark
~~~

Durante a instalação, uma tela chamada "Configuring wireshark-common" poderá aparecer. Dê enter na primeira janela e, na segunda tela, utilize as setas direcionais para selecionar "Yes" e dê enter. Com essa configuração cria-se um grupo no sistema denominado "wireshark" o qual permite que não super-usuários membros possam visualizar as interfaces de rede.


Para instalá-lo em sistemas baseados em **RedHat (como o Fedora)**, copie e cole o comando abaixo em seu terminal:
~~~
sudo dnf install wireshark
~~~


Para instalá-lo em sistemas baseados em **ArchLinux,** copie e cole o comando abaixo em seu terminal:
~~~
sudo pacman -S wireshark-gtk
~~~


**Após a instalação** do Wireshark, é necessário adcionar o seu usuário ao grupo "wireshark" para que não seja necessário utilizar o programa como um superusuário. Abra o terminal e digite o comando:
~~~
sudo usermod -a -G wireshark nome_do_seu_usuário
~~~




## CONHECENDO O SOFTWARE
### Capturando pacotes

#### Iniciando a captura
Ao iniciar o Wireshark, uma tela de boas-vindas lista as conexões de rede disponíveis em seu dispositivo atual. À direita de cada interface de rede, existe um gráfico que indica a qual utilização da interface ao vivo. 

![Alt text](images/wireshark-welcome.png "Wireshark Welcome Screen")

Para capturar o tráfego de uma ou mais interfaces, selecione as interfaces desejadas e pressione **Ctrl + E**.


#### Parando a captura
Para parar a captura, pressione **Ctrl + E**. Ou vá para a barra de ferramentas do Wireshark e selecione o botão quadrado e vermelho que está localizado próximo à barbatana de tubarão azul, no canto superiro direito.

![Alt text](images/stop-capture.png "Wireshark Stop Capturing")


#### Salvando e exportando a captura
Para salvar a captura, no menu superior direito, vá em **File > Save** ou pressione **Ctrl + S**. 
Caso prefira fazer a exportação de elementos específicos da captura, utilize as opções de exportação encontradas em  **File > Export...**.

![Alt text](images/save-as.png "Wireshark Save/Export")


### Analisando os pacotes capturados
#### A interface de captura
![Alt text](images/wireshark-capture-sections.png "Wireshark Sections")

A interface de dados capturados é composto por três seções:
1. O painel da lista de pacotes
2. O painel de detalhes do pacote
3. O painel de bytes do pacote


##### Lista de pacotes
A


##### Detalhes do pacote
A


##### Bytes do pacote
A


#### Filtros
A


#### Regras de cores
A


#### Estatísticas
A



## ENTENDENDO A DIFERENÇA ENTRE HTTP E HTTPS