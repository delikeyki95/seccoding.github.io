---
layout: post
title:  "Angular Scripts"
---
package.json 에 Script 작성

<pre>
"scripts": {
    "start": "tsc && concurrently \"npm run tsc:w\" \"npm run lite\"",
    "lite": "lite-server",
    "postinstall": "typings install",
    "tsc": "tsc",
    "tsc:w": "tsc -w",
    "typings": "typings"
}
</pre>

tsconfig.json 에 작성

<pre>
{
  "compilerOptions": {
    "module": "commonjs",
    "target": "es5",
    "sourceMap": true,
    "experimentalDecorators": true,
    "emitDecoratorMetadata": true
  },
  "exclude": [
    "node_modules"
  ]
}
</pre>

typings.json 에 작성

<pre>
{
  "globalDependencies": {
    "core-js": "registry:dt/core-js#0.0.0+20160725163759",
    "jasmine": "registry:dt/jasmine#2.2.0+20160621224255",
    "node": "registry:dt/node#6.0.0+20160909174046"
  }
}
</pre>

systemjs.config.js

<pre>
/**
 * System configuration for Angular 2 samples
 * Adjust as necessary for your application needs.
 */
(function(global) {
    // map tells the System loader where to look for things
    var map = {
        'app':                        'app', // 'dist',
        '@angular':                   'node_modules/@angular',
        'angular2-in-memory-web-api': 'node_modules/angular2-in-memory-web-api',
        'rxjs':                       'node_modules/rxjs'
    };
    // packages tells the System loader how to load when no filename and/or no extension
    var packages = {
        'app':                        { main: 'main.js',  defaultExtension: 'js' },
        'rxjs':                       { defaultExtension: 'js' },
        'angular2-in-memory-web-api': { defaultExtension: 'js' }
    };
    var ngPackageNames = [
        'common',
        'compiler',
        'core',
        'http',
        'platform-browser',
        'platform-browser-dynamic',
        'router',
        'router-deprecated',
        'upgrade'
    ];
    // Add package entries for angular packages
    ngPackageNames.forEach(function(pkgName) {
        packages['@angular/'+pkgName] = { main: '/bundles/'+pkgName+'.umd.js', defaultExtension: 'js' };
    });
    var config = {
        map: map,
        packages: packages
    }
    System.config(config);
})(this);
</pre>
