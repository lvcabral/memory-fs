# memory-fs

[![NPM Version](https://img.shields.io/npm/v/%40lvcabral%2Fmemory-fs)](https://www.npmjs.com/package/@lvcabral/memory-fs)
[![GitHub](https://img.shields.io/github/license/lvcabral/terminal)](./LICENSE)

> FORK INFO: Created to support [brs-engine](https://github.com/lvcabral/brs-engine) project.

A simple in-memory filesystem. Holds data in a javascript object.

``` javascript
var MemoryFileSystem = require("memory-fs");
var fs = new MemoryFileSystem(); // Optionally pass a javascript object

fs.mkdirpSync("/a/test/dir");
fs.writeFileSync("/a/test/dir/file.txt", "Hello World");
fs.readFileSync("/a/test/dir/file.txt"); // returns Buffer("Hello World")

// Async variants too
fs.unlink("/a/test/dir/file.txt", function(err) {
	// ...
});

fs.readdirSync("/a/test"); // returns ["dir"]
fs.statSync("/a/test/dir").isDirectory(); // returns true
fs.rmdirSync("/a/test/dir");

fs.mkdirpSync("C:\\use\\windows\\style\\paths");
```

## License

Copyright (c) 2012-2014 Tobias Koppers

MIT (http://www.opensource.org/licenses/mit-license.php)
