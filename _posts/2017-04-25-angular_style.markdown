---
layout: post
title:  "Property & CSS class Binding 예제"
---

css/style.css

<pre>
html {
    font-family: "Open Sans", Helvetica, Arial, sans-serif;
    height: 100%;
}

body {
    background: -webkit-linear-gradient(#0d263c,#030714) no-repeat fixed;
    background: linear-gradient(#0d263c,#030714) no-repeat fixed;
    color: #ffffff;
    height: 100%;
    margin: 0;
}
img {
    height: 10em;
    width: 10em;
}

h3 {
    color: #9397d8;
    font-size: 18px;
    font-weight: 400;
    margin-top: 0;
    padding: 20px;
}

header h1 {
    color: #66d9f7;
}
header h2 {
    color: #009900;
    font-weight: 400;
    margin-top: 0;
    margin-bottom: 20;
}


ul {
    list-style: none;
    padding: 0;
}

li {
    margin-bottom: 30px;
}

li:last-child {
    margin-bottom: 0;
}

.container {
    max-width: 900px;
}
</pre>


car-part.component.css

<pre>
button {
    background: #fd79fc;
    border-radius: 3px;
    border: 0;
    color: #ffffff;
}

.decrease, .increase {
    width: 20px;
}

.number {
    width: 30px;
    color: black;
    text-align: center;
}

.card {
    background: #24262c;
}

.select-quantity {
    display: inline;
}

.date, .price {
    color: #9397d8;
}

.description {
    color: #66d9f7;
}

.panel-body {
    display: table;
    padding: 0;
}

.featured {
    background: #57595D;
    -webkit-border-image: -webkit-linear-gradient(right, #818fd8 0%, #cbb4e2 50%, #a6f2f5 100%);
    -o-border-image: linear-gradient(to left, #818fd8 0%, #cbb4e2 50%, #a6f2f5 100%);
    border-image: linear-gradient(to left, #818fd8 0%, #cbb4e2 50%, #a6f2f5 100%);
    border-image-slice: 1;
}

.photo {
    float: left;
    margin-right: 30px;
}

.price {
    margin: 0;
    font-size: 18px;
    text-align: center;
    width: 120px;
}

.price-total {
    background:  #9179b7;
    float: right;
    margin: 30px 0;
    padding: 20px 50px;
    text-transform: uppercase;
}

.price-total h3, .price-total p {
    display: inline-block;
    margin: 0;
}

.price-total p {
    color: #362751;
    font-size: 18px;
    font-weight: bold;
}

.price-total h3 {
    font-size: 18px;
    margin-right: 60px;
}

.product-info {
    display: table-cell;
    vertical-align: middle;
}

.product-info td {
    padding: 0 20px;
}

.product-info tr {
    width: 100%;
    display: inline-block;
}
</pre>


Images
<img src="../images/seats.jpg"/><br/>
<img src="../images/shocks.jpg"/><br/>
<img src="../images/tires.jpg"/>
