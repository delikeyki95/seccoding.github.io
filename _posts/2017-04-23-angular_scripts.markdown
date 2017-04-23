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
