# Questões de prova

## Questão 1

*IF Sul Rio-Grandense - 2021 Programação JavaScript IF Sul Rio-Grandense Professor*

Na versão draft da especificação Web Storage, são definidas duas propriedades no objeto Window, localStorage e sessionStorage.

Sobre o armazenamento de dados em JavaScript, usando localStorage, afirma-se que

A - dados armazenados por meio do localStorage têm a mesma vida útil que a janela de nível superior ou guia do navegador em que o script que os armazenou está sendo executado.

B - o escopo de armazenamento do localStorage permite que, por exemplo, os dados armazenados em uma visita a um site, usando Firefox, estejam acessíveis quando for realizada uma segunda visita usando o Chrome.

C - dados armazenados por meio de localStorage têm vida útil diferente de dados armazenados por meio de sessionStorage.

D - localStorage tem como escopo a origem do documento, que é definida por seu protocolo, porta e criptografia.

### Comentário

O HTML5 trouxe duas novas formas de armazenar dados (web storage), além dos tradicionais cookies:
* sessionStorage: armazena os dados durante a sessão. Se o navegador for fechado, os dados serão perdidos;
* localStorage: armazena os dados de forma mais permanente, não se extinguindo com a sessão.

Fonte: https://developer.mozilla.org/pt-BR/docs/Web/API/Web_Storage_API

GABARITO: C