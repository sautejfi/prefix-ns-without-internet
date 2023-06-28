# prefix-ns

This npm module gives easy access to the prefixes and namespaces of [prefix.cc](prefix.cc).

Warning : The dump is never updated. It uses always the default dump (`data.json`) 
There is no internet download for each installation

## Usage
```$JavaScript
let prefixns = require('prefix-ns');

//The following method returns an array of all prefixes.
let allPrefixes = prefixns.getPrefixes();
console.log(allPrefixes);

// --> ['rdf', 'foaf', ...]

//The following method returns the namespace of a given prefix.
//null is returned when the prefix is not found.
let namespace = prefixns.getNamespaceViaPrefix('foaf');
console.log(namespace);

// --> http://xmlns.com/foaf/0.1/

//The following method returns the prefix of a given namespace.
//null is returned when the namespace is not found.
let prefix = prefixns.getPrefixViaNamespace('http://xmlns.com/foaf/0.1/');
console.log(prefix);

// --> foaf

//The following method returns a map where the prefixes are the keys and the namesapces are the values.
let map = prefixns.asMap();
console.log(map.foaf);

// --> http://xmlns.com/foaf/0.1/
```

## License
MIT