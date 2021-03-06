
# example.js

``` javascript
var Worker = require("worker-loader?name=hash.worker.js!./worker");
var worker = new Worker;
worker.postMessage("b");
worker.onmessage = function(event) {
	var templateB = event.data; // "This text was generated by template B"
}
```

# worker.js

``` javascript
onmessage = function(event) {
	var template = event.data;
	require(["../require.context/templates/" + event.data], function(tmpl) {
		postMessage(tmpl());
	});
}
```

# dist/output.js

<details><summary><code>/******/ (function(modules) { /* webpackBootstrap */ })</code></summary>

``` javascript
/******/ (function(modules) { // webpackBootstrap
/******/ 	// The module cache
/******/ 	var installedModules = {};
/******/
/******/ 	// The require function
/******/ 	function __webpack_require__(moduleId) {
/******/
/******/ 		// Check if module is in cache
/******/ 		if(installedModules[moduleId]) {
/******/ 			return installedModules[moduleId].exports;
/******/ 		}
/******/ 		// Create a new module (and put it into the cache)
/******/ 		var module = installedModules[moduleId] = {
/******/ 			i: moduleId,
/******/ 			l: false,
/******/ 			exports: {}
/******/ 		};
/******/
/******/ 		// Execute the module function
/******/ 		modules[moduleId].call(module.exports, module, module.exports, __webpack_require__);
/******/
/******/ 		// Flag the module as loaded
/******/ 		module.l = true;
/******/
/******/ 		// Return the exports of the module
/******/ 		return module.exports;
/******/ 	}
/******/
/******/
/******/ 	// expose the modules object (__webpack_modules__)
/******/ 	__webpack_require__.m = modules;
/******/
/******/ 	// expose the module cache
/******/ 	__webpack_require__.c = installedModules;
/******/
/******/ 	// define getter function for harmony exports
/******/ 	__webpack_require__.d = function(exports, name, getter) {
/******/ 		if(!__webpack_require__.o(exports, name)) {
/******/ 			Object.defineProperty(exports, name, { enumerable: true, get: getter });
/******/ 		}
/******/ 	};
/******/
/******/ 	// define __esModule on exports
/******/ 	__webpack_require__.r = function(exports) {
/******/ 		if(typeof Symbol !== 'undefined' && Symbol.toStringTag) {
/******/ 			Object.defineProperty(exports, Symbol.toStringTag, { value: 'Module' });
/******/ 		}
/******/ 		Object.defineProperty(exports, '__esModule', { value: true });
/******/ 	};
/******/
/******/ 	// create a fake namespace object
/******/ 	// mode & 1: value is a module id, require it
/******/ 	// mode & 2: merge all properties of value into the ns
/******/ 	// mode & 4: return value when already ns object
/******/ 	// mode & 8|1: behave like require
/******/ 	__webpack_require__.t = function(value, mode) {
/******/ 		if(mode & 1) value = __webpack_require__(value);
/******/ 		if(mode & 8) return value;
/******/ 		if((mode & 4) && typeof value === 'object' && value && value.__esModule) return value;
/******/ 		var ns = Object.create(null);
/******/ 		__webpack_require__.r(ns);
/******/ 		Object.defineProperty(ns, 'default', { enumerable: true, value: value });
/******/ 		if(mode & 2 && typeof value != 'string') for(var key in value) __webpack_require__.d(ns, key, function(key) { return value[key]; }.bind(null, key));
/******/ 		return ns;
/******/ 	};
/******/
/******/ 	// getDefaultExport function for compatibility with non-harmony modules
/******/ 	__webpack_require__.n = function(module) {
/******/ 		var getter = module && module.__esModule ?
/******/ 			function getDefault() { return module['default']; } :
/******/ 			function getModuleExports() { return module; };
/******/ 		__webpack_require__.d(getter, 'a', getter);
/******/ 		return getter;
/******/ 	};
/******/
/******/ 	// Object.prototype.hasOwnProperty.call
/******/ 	__webpack_require__.o = function(object, property) { return Object.prototype.hasOwnProperty.call(object, property); };
/******/
/******/ 	// __webpack_public_path__
/******/ 	__webpack_require__.p = "dist/";
/******/
/******/
/******/ 	// Load entry module and return exports
/******/ 	return __webpack_require__(__webpack_require__.s = 0);
/******/ })
/************************************************************************/
```

</details>

``` javascript
/******/ ([
/* 0 */
/*!********************!*\
  !*** ./example.js ***!
  \********************/
/*! no static exports found */
/***/ (function(module, exports, __webpack_require__) {

var Worker = __webpack_require__(/*! worker-loader?name=hash.worker.js!./worker */ 1);
var worker = new Worker;
worker.postMessage("b");
worker.onmessage = function(event) {
	var templateB = event.data; // "This text was generated by template B"
}


/***/ }),
/* 1 */
/*!****************************************************************************************!*\
  !*** (webpack)/node_modules/worker-loader/dist/cjs.js?name=hash.worker.js!./worker.js ***!
  \****************************************************************************************/
/*! no static exports found */
/***/ (function(module, exports, __webpack_require__) {

module.exports = function() {
  return new Worker(__webpack_require__.p + "hash.worker.js");
};

/***/ })
/******/ ]);
```

# dist/[hash].worker.js

``` javascript
/******/ (function(modules) { // webpackBootstrap
/******/ 	window["webpackChunk"] = function webpackChunkCallback(chunkIds, moreModules) {
/******/ 		for(var moduleId in moreModules) {
/******/ 			modules[moduleId] = moreModules[moduleId];
/******/ 		}
/******/ 		while(chunkIds.length)
/******/ 			installedChunks[chunkIds.pop()] = 1;
/******/ 	};
/******/
/******/ 	// The module cache
/******/ 	var installedModules = {};
/******/
/******/ 	// object to store loaded chunks
/******/ 	// "1" means "already loaded"
/******/ 	var installedChunks = {
/******/ 		0: 1
/******/ 	};
/******/
/******/ 	// The require function
/******/ 	function __webpack_require__(moduleId) {
/******/
/******/ 		// Check if module is in cache
/******/ 		if(installedModules[moduleId]) {
/******/ 			return installedModules[moduleId].exports;
/******/ 		}
/******/ 		// Create a new module (and put it into the cache)
/******/ 		var module = installedModules[moduleId] = {
/******/ 			i: moduleId,
/******/ 			l: false,
/******/ 			exports: {}
/******/ 		};
/******/
/******/ 		// Execute the module function
/******/ 		modules[moduleId].call(module.exports, module, module.exports, __webpack_require__);
/******/
/******/ 		// Flag the module as loaded
/******/ 		module.l = true;
/******/
/******/ 		// Return the exports of the module
/******/ 		return module.exports;
/******/ 	}
/******/
/******/ 	// This file contains only the entry chunk.
/******/ 	// The chunk loading function for additional chunks
/******/ 	__webpack_require__.e = function requireEnsure(chunkId) {
/******/ 		var promises = [];
/******/ 		promises.push(Promise.resolve().then(function() {
/******/ 			// "1" is the signal for "already loaded"
/******/ 			if(!installedChunks[chunkId]) {
/******/ 				importScripts("" + chunkId + ".hash.worker.js");
/******/ 			}
/******/ 		}));
/******/ 		return Promise.all(promises);
/******/ 	};
/******/
/******/ 	// expose the modules object (__webpack_modules__)
/******/ 	__webpack_require__.m = modules;
/******/
/******/ 	// expose the module cache
/******/ 	__webpack_require__.c = installedModules;
/******/
/******/ 	// define getter function for harmony exports
/******/ 	__webpack_require__.d = function(exports, name, getter) {
/******/ 		if(!__webpack_require__.o(exports, name)) {
/******/ 			Object.defineProperty(exports, name, { enumerable: true, get: getter });
/******/ 		}
/******/ 	};
/******/
/******/ 	// define __esModule on exports
/******/ 	__webpack_require__.r = function(exports) {
/******/ 		if(typeof Symbol !== 'undefined' && Symbol.toStringTag) {
/******/ 			Object.defineProperty(exports, Symbol.toStringTag, { value: 'Module' });
/******/ 		}
/******/ 		Object.defineProperty(exports, '__esModule', { value: true });
/******/ 	};
/******/
/******/ 	// create a fake namespace object
/******/ 	// mode & 1: value is a module id, require it
/******/ 	// mode & 2: merge all properties of value into the ns
/******/ 	// mode & 4: return value when already ns object
/******/ 	// mode & 8|1: behave like require
/******/ 	__webpack_require__.t = function(value, mode) {
/******/ 		if(mode & 1) value = __webpack_require__(value);
/******/ 		if(mode & 8) return value;
/******/ 		if((mode & 4) && typeof value === 'object' && value && value.__esModule) return value;
/******/ 		var ns = Object.create(null);
/******/ 		__webpack_require__.r(ns);
/******/ 		Object.defineProperty(ns, 'default', { enumerable: true, value: value });
/******/ 		if(mode & 2 && typeof value != 'string') for(var key in value) __webpack_require__.d(ns, key, function(key) { return value[key]; }.bind(null, key));
/******/ 		return ns;
/******/ 	};
/******/
/******/ 	// getDefaultExport function for compatibility with non-harmony modules
/******/ 	__webpack_require__.n = function(module) {
/******/ 		var getter = module && module.__esModule ?
/******/ 			function getDefault() { return module['default']; } :
/******/ 			function getModuleExports() { return module; };
/******/ 		__webpack_require__.d(getter, 'a', getter);
/******/ 		return getter;
/******/ 	};
/******/
/******/ 	// Object.prototype.hasOwnProperty.call
/******/ 	__webpack_require__.o = function(object, property) { return Object.prototype.hasOwnProperty.call(object, property); };
/******/
/******/ 	// __webpack_public_path__
/******/ 	__webpack_require__.p = "dist/";
/******/
/******/
/******/ 	// Load entry module and return exports
/******/ 	return __webpack_require__(__webpack_require__.s = 0);
/******/ })
/************************************************************************/
/******/ ([
/* 0 */
/*!*******************!*\
  !*** ./worker.js ***!
  \*******************/
/*! no static exports found */
/***/ (function(module, exports, __webpack_require__) {

onmessage = function(event) {
	var template = event.data;
	__webpack_require__.e(/*! AMD require */ 1).then(function() { var __WEBPACK_AMD_REQUIRE_ARRAY__ = [__webpack_require__(1)("./" + event.data)]; (function(tmpl) {
		postMessage(tmpl());
	}).apply(null, __WEBPACK_AMD_REQUIRE_ARRAY__);}).catch(__webpack_require__.oe);
}


/***/ })
/******/ ]);
```

# dist/1.[hash].worker.js

``` javascript
window["webpackChunk"]([1],[
/* 0 */,
/* 1 */
/*!**************************************************!*\
  !*** ../require.context/templates sync ^\.\/.*$ ***!
  \**************************************************/
/*! no static exports found */
/***/ (function(module, exports, __webpack_require__) {

var map = {
	"./a": 2,
	"./a.js": 2,
	"./b": 3,
	"./b.js": 3,
	"./c": 4,
	"./c.js": 4
};


function webpackContext(req) {
	var id = webpackContextResolve(req);
	return __webpack_require__(id);
}
function webpackContextResolve(req) {
	var id = map[req];
	if(!(id + 1)) { // check for number or string
		var e = new Error("Cannot find module '" + req + "'");
		e.code = 'MODULE_NOT_FOUND';
		throw e;
	}
	return id;
}
webpackContext.keys = function webpackContextKeys() {
	return Object.keys(map);
};
webpackContext.resolve = webpackContextResolve;
module.exports = webpackContext;
webpackContext.id = 1;

/***/ }),
/* 2 */
/*!*****************************************!*\
  !*** ../require.context/templates/a.js ***!
  \*****************************************/
/*! no static exports found */
/***/ (function(module, exports) {

module.exports = function() {
	return "This text was generated by template A";
}

/***/ }),
/* 3 */
/*!*****************************************!*\
  !*** ../require.context/templates/b.js ***!
  \*****************************************/
/*! no static exports found */
/***/ (function(module, exports) {

module.exports = function() {
	return "This text was generated by template B";
}

/***/ }),
/* 4 */
/*!*****************************************!*\
  !*** ../require.context/templates/c.js ***!
  \*****************************************/
/*! no static exports found */
/***/ (function(module, exports) {

module.exports = function() {
	return "This text was generated by template C";
}

/***/ })
]);
```

# Info

## Unoptimized

```
Hash: 0a1b2c3d4e5f6a7b8c9d
Version: webpack 4.29.0
           Asset      Size  Chunks             Chunk Names
1.hash.worker.js  1.79 KiB          [emitted]  
  hash.worker.js  4.98 KiB          [emitted]  
       output.js  4.42 KiB       0  [emitted]  main
Entrypoint main = output.js
chunk    {0} output.js (main) 326 bytes [entry] [rendered]
    > ./example.js main
 [0] ./example.js 229 bytes {0} [built]
     single entry ./example.js  main
 [1] (webpack)/node_modules/worker-loader/dist/cjs.js?name=hash.worker.js!./worker.js 97 bytes {0} [not cacheable] [built]
     cjs require worker-loader?name=hash.worker.js!./worker [0] ./example.js 1:13-66
Child worker:
               Asset      Size  Chunks             Chunk Names
    1.hash.worker.js  1.79 KiB       1  [emitted]  
      hash.worker.js  4.98 KiB       0  [emitted]  main
    Entrypoint main = hash.worker.js
    chunk    {0} hash.worker.js (main) 162 bytes >{1}< [entry] [rendered]
        > !!./worker.js main
     [0] ./worker.js 162 bytes {0} [built]
         single entry !!./worker.js  main
    chunk    {1} 1.hash.worker.js 457 bytes <{0}> [rendered]
        > [0] ./worker.js 3:1-5:3
     [1] ../require.context/templates sync ^\.\/.*$ 217 bytes {1} [built]
         amd require context ../require.context/templates [0] ./worker.js 3:1-5:3
     [2] ../require.context/templates/a.js 80 bytes {1} [optional] [built]
         context element ./a [1] ../require.context/templates sync ^\.\/.*$ ./a
         context element ./a.js [1] ../require.context/templates sync ^\.\/.*$ ./a.js
     [3] ../require.context/templates/b.js 80 bytes {1} [optional] [built]
         context element ./b [1] ../require.context/templates sync ^\.\/.*$ ./b
         context element ./b.js [1] ../require.context/templates sync ^\.\/.*$ ./b.js
     [4] ../require.context/templates/c.js 80 bytes {1} [optional] [built]
         context element ./c [1] ../require.context/templates sync ^\.\/.*$ ./c
         context element ./c.js [1] ../require.context/templates sync ^\.\/.*$ ./c.js
```

## Production mode

```
Hash: 0a1b2c3d4e5f6a7b8c9d
Version: webpack 4.29.0
           Asset       Size  Chunks             Chunk Names
1.hash.worker.js  593 bytes          [emitted]  
  hash.worker.js   1.27 KiB          [emitted]  
       output.js   1.06 KiB       0  [emitted]  main
Entrypoint main = output.js
chunk    {0} output.js (main) 326 bytes [entry] [rendered]
    > ./example.js main
 [0] ./example.js 229 bytes {0} [built]
     single entry ./example.js  main
 [1] (webpack)/node_modules/worker-loader/dist/cjs.js?name=hash.worker.js!./worker.js 97 bytes {0} [not cacheable] [built]
     cjs require worker-loader?name=hash.worker.js!./worker [0] ./example.js 1:13-66
Child worker:
               Asset       Size  Chunks             Chunk Names
    1.hash.worker.js  593 bytes       1  [emitted]  
      hash.worker.js   1.27 KiB       0  [emitted]  main
    Entrypoint main = hash.worker.js
    chunk    {0} hash.worker.js (main) 162 bytes >{1}< [entry] [rendered]
        > !!./worker.js main
     [0] ./worker.js 162 bytes {0} [built]
         single entry !!./worker.js  main
    chunk    {1} 1.hash.worker.js 457 bytes <{0}> [rendered]
        > [0] ./worker.js 3:1-5:3
     [1] ../require.context/templates sync ^\.\/.*$ 217 bytes {1} [built]
         amd require context ../require.context/templates [0] ./worker.js 3:1-5:3
     [2] ../require.context/templates/a.js 80 bytes {1} [optional] [built]
         context element ./a [1] ../require.context/templates sync ^\.\/.*$ ./a
         context element ./a.js [1] ../require.context/templates sync ^\.\/.*$ ./a.js
     [3] ../require.context/templates/b.js 80 bytes {1} [optional] [built]
         context element ./b [1] ../require.context/templates sync ^\.\/.*$ ./b
         context element ./b.js [1] ../require.context/templates sync ^\.\/.*$ ./b.js
     [4] ../require.context/templates/c.js 80 bytes {1} [optional] [built]
         context element ./c [1] ../require.context/templates sync ^\.\/.*$ ./c
         context element ./c.js [1] ../require.context/templates sync ^\.\/.*$ ./c.js
```
