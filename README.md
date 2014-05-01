trabajo-de-web-
===============

desarrolle los siguientes ejercicios utilizando java script y html5
<!DOCTYPE html>
<html>
	<head>
		<center>
		<h3>Validacion de cedulas</h3>
	</head>

	<body>
	<input type="text" id="textocedula" ></br>
	<input type="button" value="Validar Cedula" onClick="validarcedula()">
	</body>
		</center>
		

</html>

<script type="text/javascript">
function validarcedula()
{
	var i;
	var cedula;
	var acumulado;
	cedula=document.getElementById('textocedula').value;
	var instancia;
	acumulado=0;
	for (i=1;i<=9;i++)
	{
		if (i%2!=0)
		{
			instancia=cedula.substring(i-1,i)*2;
			if (instancia>9) instancia-=9;
		}
		else instancia=cedula.substring(i-1,i);
		acumulado+=parseInt(instancia);
	}
	while (acumulado>0)
		acumulado-=10;
	if (cedula.substring(9,10)!=(acumulado*-1))
	{
		alert("Cedula no valida!!");
	}
	else
	{
		alert("Cedula Coorecta");
	}
}
</script>


<!DOCTYPE html>
<html>

	<head>
		<center>
	<h3>Invertir la cadena de texto</h3>
	</head>

	<body>
	<input type="text" name="caja" id="caja">
	<br></br>
	<input type="button" value="Invertir Cadena" onClick="invertir()" >

	</body>

</html>


<script type="text/javascript">

function invertir()
{
var x = document.getElementById("caja").value;
var y = " ";


for(i=x.length ; i>=0; i--)
{
   y = y + x.charAt(i);
}

alert("La cadena invertida es: " +y);

}

</Script>




<!DOCTYPE html>
<html>

	<head>
		<center>
	<h3>Numeros Primos</h3>
	</head>

	<body>
	<p>Ingrese un valor y verifique si este es un numero primo</p></br>
	<input type="text" name="valor" id="valor"><br></br>
	<input type="button" value="Calcular" OnClick="primos()">
	</body>
		</center>

</html>

<script type="text/javascript"> 
function primos()
{
	var x = document.getElementById("valor").value;
	x = parseInt(x);
    var div = 0 ;
    for (var i = 0; i <= x; i++) {
    	if (x%i == 0) 
    	{
    		div++;
    	}
    }
    if (div >= 3 ) 
    {
    	alert("El numero no es primo");
    }
    else
    {
    	alert("El numero es Primo");
    }
}

</script>


<!DOCTYPE html>
<html>
	<center> <h3>Validacion y Suma de Números Binarios</h3>
	<p>Este programa validara y sumara los datos en binarios que se ingresen</p>
	
		Valor 1: <input id="valor1" type="text" ="Ingrese valor 1" /><br>
		Valor 2: <input id="valor2" type="text" label="Ingrese valor 2" /><br></br>
		<input type="button" value="Validar y Sumar" onClick="Sumar(valor1.value , valor2.value)">
	</center>
</html>


<script type="text/javascript"> 
var r, re;

function Sumar(a,b){
validar(a);
validar(b);

r = ( parseInt(a) + parseInt(b) );
re = r.toString(2);
alert("Ambos valores son binarios, la suma de los valores es: " + re);

}


function validar(x)
{
	var	Ban = 0;
	var v, w;

	for (var i = 0; i <= x.length; i++) {
		v = x.charAt(i);
		if((v == 0) || (v == 1)) 
		{
			Ban = 1;
		}
		else
		{
			alert("Porfavor solo ingrese numeros binarios");
			location.href="Sumar y Validar Binario.html";
		}
	}
}

</script>
