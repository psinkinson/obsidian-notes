Going to version 12.2.3, on `ng serve` got error:

[styles.css - Error: (0 , _identifier.getUndoPath) is not a function](https://stackoverflow.com/questions/68718162/error-upgrading-from-angular-11-2-to-12-2-styles-css-error-0-identifier)

fix was to downgrade "@angular-devkit/build-angular": "~12.1.4"


Error: 
crypto_js_hmac_sha256__WEBPACK_IMPORTED_MODULE_4___default(...) is not a function

webpack 5 no longer includes some polyfils.

https://stackoverflow.com/questions/67572355/webpack-5-angular-polyfill-for-node-js-crypto-js

In **tsconfig.json** I added:

json
    {
      "compilerOptions": {
        "paths":{
          "crypto":["node_modules/crypto-js"]
        }
     }
    }


And in **angular.json** I added:

json
     {
    "architect": {
            "build": {
              "options": {
                "allowedCommonJsDependencies": ["crypto"],
              }
            }
        }
    }


# CommonJS warnings
**angular.json**:

json
     {
    "architect": {
            "build": {
              "options": {
                "allowedCommonJsDependencies": [
					"crypto-js",
					"@aws-crypto/sha256-js",
					"uuid",
					"@aws-crypto/sha256-browser",
					"fast-xml-parser",
					"@aws-crypto/crc32",
					"buffer",
					"isomorphic-unfetch"
				],
              }
            }
        }
    }
