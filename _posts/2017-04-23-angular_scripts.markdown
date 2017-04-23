---
layout: post
title:  "Angular Scripts"
---
package.json 에 Script 작성

>"script": {<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;"start": "tsc && concurrently \"npm run tsc:w\" \"npm run lite\"",<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;"lite": "lite-server",<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;"postinstall": "typings install",<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;"tsc": "tsc",<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;"tsc:w": "tsc -w",<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;"typings": "typings"<br/>
>},

tsconfig.json 에 작성

>{<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;"compilerOptions": {<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"module": "commonjs",<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"target": "es5",<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"sourceMap": true,<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"experimentalDecorators": true,<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"emitDecoratorMetadata": true<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;},<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;"exclude": [<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"node_modules"<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;]<br/>
>}

typings.json 에 작성

>{<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;"globalDependencies": {<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"core-js": "registry:dt/core-js#0.0.0+20160725163759",<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"jasmine": "registry:dt/jasmine#2.2.0+20160621224255",<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"node": "registry:dt/node#6.0.0+20160909174046"<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;}<br/>
>}

systemjs.config.js

>/**<br/>
> * System configuration for Angular 2 samples<br/>
> * Adjust as necessary for your application needs.<br/>
> */<br/>
>(function(global) {<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;// map tells the System loader where to look for things<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;var map = {<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'app':                        'app', // 'dist',<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'@angular':                   'node_modules/@angular',<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'angular2-in-memory-web-api': 'node_modules/angular2-in-memory-web-api',<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'rxjs':                       'node_modules/rxjs'<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;};<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;// packages tells the System loader how to load when no filename and/or no extension<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;var packages = {<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'app':                        { main: 'main.js',  defaultExtension: 'js' },<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'rxjs':                       { defaultExtension: 'js' },<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'angular2-in-memory-web-api': { defaultExtension: 'js' }<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;};<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;var ngPackageNames = [<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'common',<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'compiler',<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'core',<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'http',<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'platform-browser',<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'platform-browser-dynamic',<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'router',<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'router-deprecated',<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'upgrade'<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;];<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;// Add package entries for angular packages<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;ngPackageNames.forEach(function(pkgName) {<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;packages['@angular/'+pkgName] = { main: '/bundles/'+pkgName+'.umd.js', defaultExtension: 'js' };<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;});<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;var config = {<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;map: map,<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;packages: packages<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;}<br/>
>&nbsp;&nbsp;&nbsp;&nbsp;System.config(config);<br/>
>})(this);
