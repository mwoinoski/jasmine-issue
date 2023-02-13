## Sample code that reproduces an issue with Jasmine

I'm running Node 18.10.0 with Jasmine 4.5.0 on Windows Server 2019.

Both of the following commands execute successfully:
    
    npx jasmine spec/model/gadget.spec.js
    npx jasmine spec/model/widget.spec.js

But the following generates an error:

    npx jasmine spec
  
    Error [ERR_UNSUPPORTED_DIR_IMPORT]: Directory import 'D:\Associate\Downloads\JasmineIssue\spec' is not supported resolving ES modules imported from C:\Users\Associate\AppData\Roaming\npm\node_modules\jasmine\lib\loader.js
    at new NodeError (node:internal/errors:393:5)
    at finalizeResolution (node:internal/modules/esm/resolve:319:17)
    at moduleResolve (node:internal/modules/esm/resolve:916:10)
    at defaultResolve (node:internal/modules/esm/resolve:1124:11)
    at nextResolve (node:internal/modules/esm/loader:163:28)
    at ESMLoader.resolve (node:internal/modules/esm/loader:837:30)
    at ESMLoader.getModuleJob (node:internal/modules/esm/loader:424:18)
    at ESMLoader.import (node:internal/modules/esm/loader:521:22)
    at importModuleDynamically (node:internal/modules/cjs/loader:1088:29)
    at importModuleDynamicallyWrapper (node:internal/vm/module:438:21) {
    code: 'ERR_UNSUPPORTED_DIR_IMPORT',
    url: 'file:///D:/Associate/Downloads/JasmineIssue/spec'
    }
  
