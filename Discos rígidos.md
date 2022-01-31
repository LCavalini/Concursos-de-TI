# Organização física do disco rígido

O disco rígido constitui-se, basicamente, de um conjunto de pratos com capacidade de rotação anti-horária, com duas superfícies (superior e inferior) que podem armazenar dados, e de cabeças de leitura (uma para cada superfície de cada prato), que se movem perpendicularmente, ou seja, para as partes internas e externas dos pratos. As cabeças de leitura deslocam-se de maneira idêntica por todas as superfícies dos pratos. 

Cada superfície de cada prato contém várias trilhas, que são círculos concêntricos. A numeração parte da mais externa (0) para a mais interna (n). As trilhas se subdividem em setores.

A projeção vertical de trilhas é denominada cilindro: conjunto de trilhas com mesmo número pertencentes a diferentes superfícies de pratos.

# Organização lógica do disco rígido

## Quantidade de bits por trilha

1. Constante: as trilhas internas têm maior densidade de bits/polegada (porque a área é menor e há a mesma quantidade de dados). Tecnologia CAV (Constant Angular Velocity).
2. Variável: todas as trilhas têm a mesma densidade de bits (quanto mais interna a trilha, menos dados). Tecnologia CLV (Constant Linear Velocity). 

As trilhas são separadas por vãos (gaps), para não haver problemas de alinhamento.

## Setores

Os setores dos discos rígidos armazenam 512 bytes ou 4096 bytes (discos mais novos). Eles compreender também informações de controle (preâmbulo) e de verificação de erro (ECC).

## Métodos de acesso a dados

* CHS (Cylinder, Head, Sector): localiza, na ordem, o cilindro, a cabeça de leitura (determina qual é a superfície do prato) e o setor. **Não é mais usado**.
* LBA (Linear Block Adressage): enumera todos os setores do disco, de 0 a n. Não se consideram os números de cilindro e cabeça.

# Formatação

## Formatação física (baixo nível)

Feita por meio de software pelos fabricantes dos discos rígidos. Divide os discos em cilindros, cabeças e setores.

## Formatação lógica (alto nível)

Feita pelo usuário. Escreve no disco rígido a estrutura do sistema de arquivos do sistema operacional. A menor unidade é o bloco lógico, que compreende um ou mais setores físicos.

# Particionamento

Divisão do disco rígido em partes lógicas.

## MBR (Master Boot Record)

Até 4 partições primárias e ativas, com capacidade de inicialização (boot).

# Tempo de acesso

O tempo de acesso dos discos rígidos depende do tempo das seguintes operações:
1. Tempo de busca (Seek time): o tempo necessário para a cabeça de leitura se posicionar no cilindro. É o maior responsável pelo tempo de acesso. 
2. Tempo de latência ou rotação (Rotation time): o tempo necessário para os pratos girarem até o local do setor.
3. Tempo de transferência (Transfer time): o tempo necessário para a leitura e gravação dos dados no disco.

## Maneiras de reduzir o tempo de acesso

* Cache
* Leitura antecipada de blocos (apenas para arquivos sequenciais)
* Desfragmentação do disco
* Uso de logs estruturados

Referências: anotações das aulas do curso [Sistemas de Arquivos do Prof. Gustavo Vilar do Provas de TI](https://www.provasdeti.com.br/courses-detail.php?curso_info_id=071).

# Questões de prova

## Questão 1

*Quadrix - 2021 Arquitetura de Computadores Armazenamento de Dados em Arquitetura de Computadores CORE-PR Analista (Superior)*

Julgue o item, relativo aos processadores, ao armazenamento de dados e ao processo de formatação.

O processo de formatação apaga todas as informações contidas em um disco. No entanto, ele não altera a localização das trilhas e dos setores, tendo em vista que essa localização é uma parte permanente da estrutura física do disco.

Alternativas:

C. Certo

E. Errado

## Comentário

Existem dois tipos de formatação: física e lógica. A formatação física, geralmente realizada pelo fabricante do disco rígido, compreende a organização dos cilindros (projeção vertical das trilhas), cabeças e setores. É importante ressaltar que, apesar do nome dizer "física", trata-se de um procedimento realizado por software. Por outro lado, a formação lógica, feita por usuários com o auxílio de programas como fdisk, define o sistema de arquivos e os blocos lógicos. Assim, se considerarmos a formação física, veremos que o enunciado está incorreto.

**Gabarito: Errado**

## Questão 2

*Quadrix - 2021 - Arquitetura de Computadores Armazenamento de Dados em Arquitetura de Computadores CORE-PR Analista (Superior)*

Julgue o item, relativo aos processadores, ao armazenamento de dados e ao processo de formatação.

A  capacidade  de  um  sistema  de  armazenamento  em  disco  depende  tanto  da  quantidade  de  discos  usados  quanto da densidade na qual as trilhas e os setores são  colocados. 

Alternativas:

C. Certo

E. Errado

### Comentário

A densidade das trilhas define a quantidade de bits por polegada nas superfícies dos pratos. Assim, quanto maior for a densidade, maior a capacidade armazenamento da trilha.

É importante lembrar que as trilhas são círculos concêntricos definidos na superfície dos pratos e que as trilhas internas são menores que as externas. Existem duas maneiras de distribuir os dados pelo disco: constante - o aumento da densidade das trilhas internas compensa a sua dimensão reduzida - e variável - a densidade das trilhas é sempre igual, de modo que as trilhas internas armazenam menos dados do que as externas.

**Gabarito: Certo**