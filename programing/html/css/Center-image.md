Center an image
===============
Read here [https://css-tricks.com/snippets/css/absolute-center-vertical-horizontal-an-image/](https://css-tricks.com/snippets/css/absolute-center-vertical-horizontal-an-image/).

CSS background-image Technique
---
```
html { 
   width:100%; 
   height:100%; 
   background:url(logo.png) center center no-repeat;
}
```

CSS + Inline Image Technique
---
```
img {
   position: absolute;
   top: 50%;
   left: 50%;
   width: 500px;
   height: 500px;
   margin-top: -250px; /* Half the height */
   margin-left: -250px; /* Half the width */
}
```
=> this solution runs ok with me! <3

Table technique
---
```
html, body, #wrapper {
   height:100%;
   width: 100%;
   margin: 0;
   padding: 0;
   border: 0;
}
#wrapper td {
   vertical-align: middle;
   text-align: center;
}
```

Sample html
---
```
<html>
<body>
   <table id="wrapper">
      <tr>
         <td><img src="logo.png" alt="" /></td>
      </tr>
   </table>
</body>
</html>
```

Sample js code to create img in one element
---
```
// <img class="my-icon"/>
let loadingElement = document.createElement('img');
loadingElement.setAttribute('class', 'my-icon');
loadingElement.src = 'url/to/my-icon.gif';

// make loading icon centered
let style = ''
    + ' position: absolute;'
    + ' top: 50%;'
    + ' left: 50%;'
    + ' width: 40px;'
    + ' height: 40px;'
    + ' margin-top: -20px;' /* Half the height */
    + ' margin-left: -20px;' /* Half the width */
    + '';
loadingElement.setAttribute('style', style);

parentElement.appendChild(loadingElement);
```


Good job!
