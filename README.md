node-xi18n 
==========

NodeJS i18n module

Usage
==========

``` js
var xi18n = require('xi18n');

xi18n.init({
  root: 'templates/'
});

xi18n.setSource('home'); 
xi18n.setLocale('en_US');
xi18n.build();
xi18n.replace('name','Tierry Danquin');
xi18n.replace('nickname','oOThkOo');

var title = xi18n.get('title');
var keywords = xi18n.get('keywords');
var subject = xi18n.get('subject');
```
Donations
-----

:heart: Donations are always welcome :heart:.

### Buymeacoffee

[<img height="55px" src="https://raw.githubusercontent.com/oOthkOo/oOthkOo/main/assets/bmac-btn.svg">](https://buymeacoffee.com/oothkoo)

### Crypto

Coins | Symbols | Addresses
--- | --- | ---
<img width="32" src="https://raw.githubusercontent.com/oOthkOo/oOthkOo/main/assets/btc.svg" alt="Bitcoin"/> | BTC | 3B52fbzNFQTaKZxWf5GrCUsASD2UP8na4A
<img width="32" src="https://raw.githubusercontent.com/oOthkOo/oOthkOo/main/assets/eth.svg" alt="Ethereum"/> | ETH | 0x1C389f1f85Cdb3C2996b83fAc87E496A80698B7C
<img width="32" src="https://raw.githubusercontent.com/oOthkOo/oOthkOo/main/assets/sol.svg" alt="Solana"/> | SOL | F14pWhGjGLcCF8RMk4JhbK2kD49iBBwa9KFygRJo54Fm
