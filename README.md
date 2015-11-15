# Ti.x2js
This is adapted version of x2js library for Titanium SDK.


## How to use
Original sources and docs available at http://code.google.com/p/x2js

* API functions

    * new X2JS() - to create your own instance to access all library functionality
        * new X2JS(config) - to create your own instance with additional config:        
            * escapeMode : true|false - Escaping XML characters. Default is true from v1.1.0+

            * attributePrefix : "<string>" - Prefix for XML attributes in JSon model. Default is "_"

            * arrayAccessForm : "none"|"property" - The array access form (none|property). Use this property if you want X2JS generates an additional property <element>_asArray to access in array form for any XML element. Default is none from v1.1.0+

            * emptyNodeForm : "text"|"object" - Handling empty nodes (text|object) mode. When X2JS found empty node like <test></test> it will be transformed to test : '' for 'text' mode, or to Object for 'object' mode. Default is 'text'

            * enableToStringFunc : true|false - Enable/disable an auxiliary function in generated JSON objects to print text nodes with text/cdata. Default is true

            * arrayAccessFormPaths : [] - Array access paths. Use this option to configure paths to XML elements always in "array form". You can configure beforehand paths to all your array elements based on XSD or your knowledge. Every path could be a simple string (like 'parent.child1.child2'), a regex (like /.*\.child2/), or a custom function. Default is empty

            * skipEmptyTextNodesForObj : true|false - Skip empty text tags for nodes with children. Default is true.

            * stripWhitespaces : true|false - Strip whitespaces (trimming text nodes). Default is true.

            * datetimeAccessFormPaths : [] - Datetime access paths. Use this option to configure paths to XML
             elements for "datetime form". You can configure beforehand paths to all your array elements based on XSD or your knowledge. Every path could be a simple string (like 'parent.child1.child2'), a regex (like /.*\.child2/), or a custom function. Default is empty

    * instance.xml2json - Convert XML specified as DOM Object to JSON
    * instance.json2xml - Convert JSON to XML DOM Object
    * instance.xml_str2json - Convert XML specified as string to JSON
    * instance.json2xml_str - Convert JSON to XML string
    * instance.asArray - Utility function for working with JSON field always in array form
    * instance.asDateTime - Utility function for convert the specified parameter from XML DateTime to JS Date
    * instance.asXmlDateTime - Utility function for convert the specified parameter to XML DateTime from JS Date or timestamp
