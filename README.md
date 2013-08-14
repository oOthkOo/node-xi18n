node-xi18n
==========

NodeJS i18n module

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
