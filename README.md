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

var text = xi18n.get('title');
var text = xi18n.get('title');

function get( name ) {	
var template = getTemplateByLabel( name.toLowerCase() );	
return template ? template.value : 'NOTFOUND';
}
