# Questões de prova

## Questão 1

*Ano: 2021 Banca: CESPE / CEBRASPE Órgão: PG-DF Prova: CESPE / CEBRASPE - 2021 - PG-DF - Analista Jurídico - Analista de Sistema - Suporte e Infraestrutura*

Acerca de fitotecas, armazenamento de discos e replicação, julgue o item seguinte.

Embora combine vários discos rígidos, formando uma única unidade lógica, a tecnologia RAID não reduz o tempo de transferência de grandes volumes de dados.

Alternativas:

C. Certo

E. Errado

### Comentário

De modo geral, o RAID oferece maior desempenho de leitura e escrita, em graus variados de acordo com o nível do RAID e a disposição dos dados, e segurança, em razão da redundância (exceto RAID 0). **Gabarito: Errado**

## Questão 2

*Ano: 2021 Banca: CESPE / CEBRASPE Órgão: TCE-RJ Prova: CESPE / CEBRASPE - 2021 - TCE-RJ - Analista de Controle Externo - Especialidade: Tecnologia da Informação*

Os sistemas de RAID nível 4 gravam os dados e as informações de paridade distribuídas em todos os discos do volume, o que aumenta a tolerância a falhas e permite a rápida substituição e recuperação do conteúdo de um disco danificado.

Alternativas:

C. Certo

E. Errado

### Comentário

Ambos os níveis 4 e 5 reservam espaço para dados de paridade. Porém, esse espaço se distribui de formas diferentes nos dois níveis: **concentra-se em apenas um disco no nível 4** e divide-se entre todos os discos no nível 5. *Referência: Tanenbaum e Austin. Organização estruturada de computadores, 6ª edição, 2013, p. 76.* **Gabarito: Errado**

## Questão 3

*Ano: 2021 Banca: CESPE / CEBRASPE Órgão: TCE-RJ Prova: CESPE / CEBRASPE - 2021 - TCE-RJ - Analista de Controle Externo - Especialidade: Tecnologia da Informação*

Julgue o item subsecutivo, a respeito de balanceamento de carga e conceitos de falhas e recuperação.

O striping de dados distribui os dados de maneira transparente por múltiplos discos para fazê-los parecer um único disco grande e de rápido desempenho.

Alternativas:

C. Certo

E. Errado

### Comentário

A segmentação ou *striping* é a divisão dos discos em tiras de k setores (k pode ser qualquer número, por exemplo: 1): tira 0 corresponde ao setor 0 a k - 1 (por exemplo, tira 0 = setor 0), tira 1 ao setor k e 2k - 1 (por exemplo, tira 1 = setor 1) etc. É o conceito que fundamenta o RAID 0, mas também está presente em outros níveis, como o 4 e o 5. O ganho de **desempenho** é maior na **leitura** de um **volume grande** de dados. **Gabarito: Certo**

## Questão 4

*Ano: 2020 Banca: FCC Órgão: AL-AP Prova: FCC - 2020 - AL-AP - Analista Legislativo - Administrador de Rede e Telecomunicações*

Considere as características abaixo sobre Redundant Array of Inexpensive Disks − RAID.
− A organização desse nível de RAID grava faixas consecutivas nos discos em um estilo de alternância circular (round-robin).
− Essa distribuição de dados por meio de múltiplos discos é chamada de striping. Por exemplo, se o software emitir um comando para ler um bloco de dados consistindo em quatro faixas consecutivas começando no limite de uma faixa, o controlador de RAID dividirá esse comando em quatro comandos separados, um para cada disco, e os fará operarem em paralelo. Desse modo, haverá E/S paralela sem que o software tome conhecimento disso.
− Não usa área para redundância, funciona melhor com grandes solicitações e funciona pior com sistemas operacionais que habitualmente pedem por dados um setor de cada vez.
Trata-se do RAID:

Alternativas:

A. 3

B. 1

C. 0

D. 6

E. 5 

### Comentário

A questão baseia-se quase literalmente na p. 74 do livro Organização estruturada de computadores (6ª edição) de Tanenbaum e Austin. Ao contrário de outros níveis, RAID 0 não admite redundância de dados e opera simplesmente com a divisão dos discos em faixas (segmentação ou *striping*), de modo que a escrita é feita com alternância circular (faixa 0 no disco 0, faixa 1 no disco 1 etc.) e há a possibilidade de ganho de desempenho, especialmente quando a quantidade de dados é grande. Caso o sistema operacional requisite somente um setor por vez, não haverá redução do tempo de leitura, devido à ausência de paralelismo. **Gabarito: C - 0.**



