# Laboratório de Redes de Comunicação (ST568) - WIRESHARK - guia professor

Iremos verificar qual a possível falta de segurança gerada caso a conexão com o servidor web não seja criptografada, sendo que a senha é enviada ao servidor via requisição POST em texto simples.

1. Descubra quais os possíveis endereços IP do servidor - devido ao uso de uma rede de CDN, não é possível obter com antecedência à aula qual é o endereço IP do servidor web
	1. **Windows**
		No CMD digitar:
		~~~
		nslookup -type=a st568.l4ti.net.br
		~~~
	2. **Linux**
		No terminal digitar:
		~~~
		dig A st568.l4ti.net.br
		~~~
2. Abra o Wireshark e inicie a captura;
3. Abra o navegador e digite a URL **http://st568.l4ti.net.br**;
4. Na página de login, utilize as credenciais:
	- Usuário: leon
	- Senha: Senhaforte
5. Clique em *Entrar*;
7. Pare a captura do Wireshark;
8. Adcione o seguinte filtro:
~~~
(ip.addr==Endereço1 or ip.addr==Endereço2) and http.request.method==POST
~~~
8. Procure pelo pacote com URI */login;
9. No painel de detalhes do pacote, clique na linha *HTML Transfer Protocol* e evidencie o usuário digitado no campo *user* e a senha, no campo *password*;
10. Inicie uma nova captura;
11. Abra o navegador e digite a URL **https://st568.l4ti.net.br**;
12.  Na página de login, utilize as credenciais:
	- Usuário: leon
	- Senha: Senhaforte
13. Clique em *Entrar*;
14. Pare a captura do Wireshark;
15. Adcione o seguinte filtro:
~~~
(ip.addr==Endereço1 or ip.addr==Endereço2)
~~~
16. Mostre que o máximo que é possível visualizar em um pacote é o TLS.