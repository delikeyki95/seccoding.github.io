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
