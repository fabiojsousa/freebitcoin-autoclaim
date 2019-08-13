## freebitcoin-autoclaim
Este script tem como finalidade executar a cada hora o freeroll da faucet [freebitco.in](freebitco.in).

Além de executar o roll a cada hora, o script também ativa os rewards points e free btc bonus.

A faucet possui captcha para contas novas e/ou que não possuem um saldo de +/- $100 em Bitcoin. Será necessário ter essa quantia em sua conta para conseguir utilizar o script.

## Colocando o script em ação
1. Vá até o site [freebitco.in](freebitco.in).

2. Faça login na sua conta. Caso ainda não tenha uma conta e queira me apoiar, se cadastre utilizando o meu código de referido: https://freebitco.in/?r=1985913.

3. Instale a extensão [Tampermonkey](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo?hl=pt-BR) no seu Google Chrome. Essa extensão tem como finalidade deixar salvo e executar um código javascript a partir do seu navegador.

4. Acesse o dashboard do Tampermonkey e crie um novo script. Cole o código do arquivo script.js em seu novo script do Tampermonkey.

5. Com o seu script do Tampermonkey pronto, basta atualizar a página do site do freebitcoin para ver no ícone da extensão do Tampermonkey que há 1 script em execução.

## Configurando o script
Logo no início do script você verá essas três variáveis:
```
var ativarRewards = true;
var ativarBonus = true;
var ativarCompraTickets = true;
```
A primeira variável tem como finalidade ativar os rewards points, que basicamente são os pontos de recompensa que você ganha a cada roll para depois trocar por alguma outra coisa que o site oferece.

A segunda variável ativa os bônus para aumentar a quantidade de Bitcoin que você recebe a cada roll.

A terceira variável faz a compra automaticamente dos tickets de loteria, isso as vezes se faz necessário pois se você tiver em sua conta um saldo muito abaixo de $100 em Bitcoin, o site irá requerer o captcha, e desta forma o script não irá funcionar para executar o roll. A compra dos tickets de loteria só acontece se a quantidade que o site requerer não for maior que 350 tickets, pois sendo maior que isso a compra de tickets não é rentável.

Para desativar qualquer um destes comportamentos, basta trocar o valor de `true` para `false`.


