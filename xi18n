/**
 *  Module dependencies.
 */

var xml = require("node-xml-lite");

/**
 *  Global variables.
 */

var options = {
  root: './'  
};
var source = '';
var locale = '';
var templates = [];

/**
 *  Private functions.
 */

function getTemplateByLabel( name ) {
	for (var t=0; t<templates.length; t++) {
		var template = templates[t];
		if (template.name == name) {
			return template;
		}
	}
	return null;	
}

/**
 *  Public functions.
 */

function init( opt ) {
	options = opt || options;
}

function setSource( src ) {
	source = src;
}

function setLocale( loc ) {
	locale = loc;
}

function build() {	
	var xmlFile = options.root + '/' + source + '_' + locale + '.xml';
	var template = xml.parseFileSync(xmlFile);
	if (!template) {
		return;
	}
	templates = [];
	template.childs.forEach(function(child) {
		templates.push({
			name: child.attrib.name ? child.attrib.name.toLowerCase() : '',
			value: child.childs ? child.childs[0] : ''
		});
	});
}

function replace( name, value ) {	
	for (var t=0; t<templates.length; t++) {
		var template = templates[t];
		template.value = template.value.replace( '{' + name + '}', value );
	}
}

function get( name ) {	
	var template = getTemplateByLabel( name.toLowerCase() );	
	return template ? template.value : 'NOTFOUND';
}

/**
 * Expose functions.
 */

module.exports.init = init;
module.exports.setSource = setSource;
module.exports.setLocale = setLocale;
module.exports.build = build;
module.exports.replace = replace;
module.exports.get = get;
