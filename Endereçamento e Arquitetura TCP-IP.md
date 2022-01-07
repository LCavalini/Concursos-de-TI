# Endereços IPv4 no IPv6

É possível converter endereços IPv4 para IPv6 da seguinte maneira: ::ffff:x.y.z.w, sendo x.y.z.w os quatro octetos de um endereço IPv4. Os :: iniciais indicam que o endereço inicia com uma sequência de 10 octetos zerados.

# Arquitetura do Bluetooth

"O padrão Bluetooth tem muitos protocolos agrupados livremente em camadas, como mostra a Figura 4.32. A primeira observação a fazer é que a estrutura _não segue o modelo OSI, o modelo TCP/IP, o modelo 802 ou qualquer outro modelo conhecido._" (Tanenbaum, A. Redes de computadores, 5 ed., p. 201)

# Camada de Rede - Orientação à conexão

"Um aspecto um tanto surpreendente do IPsec é que, embora esteja na camada IP, ele é orientado a conexões." (Tanenbaum, A. Redes de Computadores, 5 ed., p. 511) É possível a orientação à conexão na camada de interredes da pilha TCP/IP, apesar de não ser tradicionalmente orientada à conexão.

# Questões de prova

## Questão 1

*CESPE / CEBRASPE - 2018 - Polícia Federal - Perito Criminal*

A respeito das características dos protocolos da arquitetura TCP/IP, julgue o item subsequente.

Erros de transmissão no cabeçalho de um pacote podem ser identificados por meio de uma soma de verificação (checksum) ou por meio de algoritmos do tipo CRC (cyclic redundancy check). A primeira abordagem é utilizada no IP, ICMP e UDP; a segunda encontra aplicações no padrão Ethernet, por exemplo.

Alternativas:

C. Certo

E. Errado

### Comentário

Os protocolos IP e UDP apresentam um campo de *checksum*. No caso do IP, o *checksum* refere-se ao cabeçalho (Tanenbaum, A. Redes de Computadores, p. 275-276). Por sua vez, o *checksum* do UDP é opcional e verifica erros do cabeçalho, dos dados e de um pseudocabeçalho conceitual do IP (Tanenbaum, A. Redes de computadores, 5 ed., 340). O padrão Ethernet , assim como o Wi-Fi (802.11), implementa o CRC (Tanenbaum, A. Redes de computadores, p. 134). O único erro da questão diz respeito ao _ICMP, porque não há o uso de nenhuma das técnicas para o protocolo_.