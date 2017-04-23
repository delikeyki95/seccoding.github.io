---
layout: post
title:  "Angular Scripts"
---
package.json 에 Script 작성

>"script": {<br/>
>    "start": "tsc && concurrently \"npm run tsc:w\" \"npm run lite\"",<br/>
>    "lite": "lite-server",<br/>
>    "postinstall": "typings install",<br/>
>    "tsc": "tsc",<br/>
>    "tsc:w": "tsc -w",<br/>
>    "typings": "typings"<br/>
>},
