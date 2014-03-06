CifradCesar
===========

<!doctype html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>

  <script src="CCesar.js" ></script>

</head>

<body>
  <table>
  <tr>
    <td>
    <label text="ESCRIBA AQUI SU PALABRA A CIFRAR"> </label>  //LABEL

       <input type="text" size="40" name="tbx1" value=" ">  //CUADRO DE TEXTO DONDE SE MUESTRA EL RESULTADO
    </td>
    <td>
       <textarea name="ta1" cols="60" rows="6" ></textarea>   //AQUI ESCRIBIMOS LA PALABRA A CIFRAR
    </td> 
    <td>
      <tr>
      <input type="button" value="Cifrar" onclick="encode(); return false;">// BOTON PARA CIFRAR
    </td>
    <td>
      <input type="button" value="Borrar" >// BOTON PARA BORRAR
    </td>
    <td>
    <input type="button" value="Descifrar" onclick="decode(); return false;">// BOTON PARA DESENCRIPTAR
    </td>
      </tr>
  </tr>
  </table>

</body>

</html>


////////////////////////////////////////////////////////////////////////////////////////////////////////////////
// CCesar en javascript


<script>
var wt = ""; var all = "";var all2 = "";var alpha2 = "abcdefghijklmnopqrstuvwxyz";

var a = "a"; var b = "b"; var c = "c"; var d = "d"; var e = "e"; var f = "f"; var g = "g"; var h = "h";
var i = "i"; var j = "j"; var k = "k"; var l = "l"; var m = "m"; var n = "n"; var o = "o"; var p = "p"; 
var q = "q"; var r = "r"; var s = "s"; var t = "t"; var u = "u"; var v = "v"; var w = "w"; var x = "x";
var y = "y"; var z = "z";

var alpha = new Array('a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z');

function encode() 
{
   wt = "";
   et = "";
   all = "";
   var theText = document.f1.ta1.value.toLowerCase();
   var num = document.f1.tb1.value;
   i2 = 0;
   for (i = 0; i < num; i++) 
   { 
     i2 = i2 + 1;
     if (i2 == 26) i2 = 0;
   }
       a = alpha[i2]; i2 = next(i2);  b = alpha[i2]; i2 = next(i2);  c = alpha[i2]; i2 = next(i2);  d = alpha[i2]; i2 = next(i2);  e = alpha[i2]; i2 = next(i2);
       f = alpha[i2]; i2 = next(i2);  g = alpha[i2]; i2 = next(i2);  h = alpha[i2]; i2 = next(i2);  i = alpha[i2]; i2 = next(i2);  j = alpha[i2]; i2 = next(i2); 
       k = alpha[i2]; i2 = next(i2);  l = alpha[i2]; i2 = next(i2);  m = alpha[i2]; i2 = next(i2);  n = alpha[i2]; i2 = next(i2);  o = alpha[i2]; i2 = next(i2);
       p = alpha[i2]; i2 = next(i2);  q = alpha[i2]; i2 = next(i2);  r = alpha[i2]; i2 = next(i2);  s = alpha[i2]; i2 = next(i2);  t = alpha[i2]; i2 = next(i2);
       u = alpha[i2]; i2 = next(i2);  v = alpha[i2]; i2 = next(i2);  w = alpha[i2]; i2 = next(i2);  x = alpha[i2]; i2 = next(i2);  y = alpha[i2]; i2 = next(i2);
       z = alpha[i2]; i2 = next(i2);

     var all = a+b+c+d+e+f+g+h+i+j+k+l+m+n+o+p+q+r+s+t+u+v+w+x+y+z;
     all = all.split("");
      encode2(all);
}

function next(x) {
  if (x == 25) 
  x = -1;
  x = x + 1;
 return x;
}

function encode2(all2) 
{
  var temp2 = document.f1.ta1.value.toLowerCase();
  temp2 = temp2.split("");
  var q = 0;
  while (q < temp2.length) { 
  wt = temp2[q];
  var where = alpha2.indexOf(wt);
  if (where == -1) 
  {
  et += wt; 
  }
  if (where != -1) 
  {
  et += all2[where]; 
  }
  
  q = q + 1;
}
   document.f1.ta2.value = et;
}

function decode()

{
  wt = "";
  et = "";
  all = "";
  all3 = "";

   var theText = document.f1.ta2.value.toLowerCase();
   var num = document.f1.tb1.value;
     i2 = 0;
       for (i = 0; i < num; i++) {
       i2 = i2 + 1;
       if (i2 == 26) i2 = 0;
}
  a = alpha[i2]; i2 = next(i2); b = alpha[i2]; i2 = next(i2); c = alpha[i2]; i2 = next(i2); d = alpha[i2]; i2 = next(i2); e = alpha[i2]; i2 = next(i2);
  f = alpha[i2]; i2 = next(i2); g = alpha[i2]; i2 = next(i2); h = alpha[i2]; i2 = next(i2); i = alpha[i2]; i2 = next(i2); j = alpha[i2]; i2 = next(i2);
  k = alpha[i2]; i2 = next(i2); l = alpha[i2]; i2 = next(i2); m = alpha[i2]; i2 = next(i2); n = alpha[i2]; i2 = next(i2); o = alpha[i2]; i2 = next(i2);
  p = alpha[i2]; i2 = next(i2); q = alpha[i2]; i2 = next(i2); r = alpha[i2]; i2 = next(i2); s = alpha[i2]; i2 = next(i2); t = alpha[i2]; i2 = next(i2);
  u = alpha[i2]; i2 = next(i2); v = alpha[i2]; i2 = next(i2); w = alpha[i2]; i2 = next(i2); x = alpha[i2]; i2 = next(i2); y = alpha[i2]; i2 = next(i2);
  z = alpha[i2]; i2 = next(i2);

  var all = a+b+c+d+e+f+g+h+i+j+k+l
           +m+n+o+p+q+r+s+t+u+v+w+x+y+z;
      all3 = all;
      all = all.split("");
      decode2(all3);
}


function decode2(all2) 

{ 
 var alpha2 = "abcdefghijklmnopqrstuvwxyz";
     alpha2 = alpha2.split("");
 var temp2 = document.f1.ta2.value.toLowerCase();
     temp2 = temp2.split("");
     var v = 0;
    while (v < temp2.length) {
      wt = temp2[v];
      var where = all2.indexOf(wt);
       if (where == -1) 
       {
       et += wt; 
       }
       if (where != -1) 
       {
       et += alpha2[where]; 
       }
       v   = v + 1;
}
document.f1.ta1.value = et;
}

</script>
