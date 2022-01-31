# Questões de prova

## Questão 1

*Ano: 2021 Banca: CESPE / CEBRASPE Órgão: PG-DF Prova: CESPE / CEBRASPE - 2021 - PG-DF - Analista Jurídico - Analista de Sistema - Suporte e Infraestrutura*

Acerca de fitotecas, armazenamento de discos e replicação, julgue o item seguinte.

A replicação de dados oferece melhor desempenho e disponibilidade a sistemas porque permite que esses sistemas operem sobre cópias sem precisar se comunicar com sites remotos.

Alternativas:

C. Certo

E. Errado

### Comentário

A replicação (cópias locais de dados) permite acessar os dados de mais de um lugar com alto tempo de resposta, o que aumenta o desempenho, porque é possível trabalhar em paralelo ou recorrer ao ponto mais rápido, e a disponibilidade, porque, se houver falha em um local de acesso, busca-se outro.

"A primeira é a replicação de dados. Se for possível manter cópias de um bloco de dados em vários locais, a velocidade dos acessos a partir desses locais pode ser aumentada. Uma dessas técnicas de replicação é fazer cache, na qual uma ou mais cópias de blocos de dados são mantidas próximas de onde estão sendo usadas, bem como no lugar a que elas “pertencem”.Tanenbaum e Austin. Organização estruturada de computadores, 6ª edição, 2013, p. 513.

**Gabarito: Certo.**

## Questão 2

*FGV - 2021 - Redes de Computadores NAS (Network Attached Storage) TCE-AM Auditor*

Sobre as tecnologias de armazenamento SAN e NAS, analise as afirmativas a seguir.

I. A tecnologia NAS opera não em nível de arquivo, mas em nível de bloco.

II. A tecnologia SAN fornece funcionalidade de armazenamento e sistemas de arquivos, como NFS e CIFS.

III. O iSCSI é exemplo de protocolo utilizado em redes SAN.

Está correto somente o que se afirma em:

A. I;

B. II;

C. III;

D. I e II;

E. II e III.

### Comentário

I. A tecnologia NAS opera não em nível de arquivo, mas em nível de bloco.

ERRADO. A tecnologia NAS, que consiste em manter um servidor de arquivos dedicado na rede, disponibiliza arquivos para as máquinas clientes.

II. A tecnologia SAN fornece funcionalidade de armazenamento e sistemas de arquivos, como NFS e CIFS.

ERRADO. A tecnologia SAN, que se define por uma rede segregada para armazenamento, apenas fornece dados no nível de bloco, de modo que o acesso em alto nível depende da existência do sistema operacional do cliente (geralmente, um servidor de arquivos que atua como intermediário).

III. O iSCSI é exemplo de protocolo utilizado em redes SAN.

CERTO. iSCSI é um protocolo de redes SAN que permite trabalhar com comandos SCSI em redes TCP/IP.

**Gabarito: C**