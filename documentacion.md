# 1. Introduccion

![](img/1.PNG)

# 2. Preparando nuestro ambiente de trabajo

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="js/jquery.min.js"></script>
    <title>Lección 01</title>
    <style>
        .textoVerde {
            color: green;
            font-weight: bold;
        }
    </style>
</head>

<body>
    <ul>
        <li>Hola 1</li>
        <li>Hola 2</li>
        <li>Hola 3</li>
    </ul>

    <ul>
        <li>Negrita</li>
        <li>Negrita</li>
        <li>Negrita</li>
    </ul>

    <script>
        jQuery('ul').addClass('textoVerde');
    </script>

</body>

</html>
```

# 3. Error muy comun del jQuery

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="js/jquery.min.js"></script>
    <title>Lección 01</title>
    <style>
        .textoVerde {
            color: green;
            font-weight: bold;
        }
    </style>
    <script>
        /*$(document).ready(function () {
            //jQuery('ul').addClass('textoVerde');
            $('ul').addClass('textoVerde');
        });*/
        $(function(){
            //$('ul').addClass('textoVerde');
            $('li:first-child').addClass('textoVerde');
            $('li:last-child').addClass('textoVerde');
        });
    </script>
</head>

<body>
    <ul>
        <li>Hola 1</li>
        <li>Hola 2</li>
        <li>Hola 3</li>
    </ul>

    <ul>
        <li>Negrita</li>
        <li>Negrita</li>
        <li>Negrita</li>
    </ul>



</body>

</html>
```

# 4. Alto - Usemos Bootstrap - Introduccion

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lección 01 - Bootstrap</title>
    <!--Importacion del jQuery-->
    <script src="js/jquery.min.js"></script>

    <!--Importacion de Bootstrap-->
    <link rel="stylesheet" href="css/bootstrap.min.css">

    <style>
        .textoVerde {
            color: green;
            font-weight: bold;
        }
    </style>
    <script>

        $(function () {
            $('li:last-child').addClass('textoVerde');
        });
    </script>
</head>

<body>
    <div class="container">
        <h1>Leccion 01</h1>
        <hr>
        <ul>
            <li>
            <li><span class="badge bg-primary">Hola 1</span></li>
            <li>Hola 2</li>
            <li>Hola 3</li>
        </ul>

        <ul>
            <li>Negrita</li>
            <li>Negrita</li>
            <li>Negrita</li>
        </ul>
        <table class="table table-striped-columns">
            <tr>
                <td>Campo</td>
                <td>Campo</td>
                <td>Campo</td>
                <td>Campo</td>
                <td>Campo</td>
            </tr>
        </table>
        <button type="button" class="btn btn-primary">Primary</button>
        <p><a class="link-opacity-50" href="#">Link opacity 50</a></p>
    </div>

</body>

</html>
```

# 5. Selectores y encadenamiento

```html
<!DOCTYPE html>
<html>

<head>
	<meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
	<title>Lección 02 - Selectores y Encadenamiento</title>

	<!-- Importacion del jQuery -->
	<script src="js/lib/jquery-2.1.4.min.js"></script>

	<!-- Importacion del Bootstrap -->
	<link rel="stylesheet" href="css/bootstrap.min.css">


	<!-- Estilo para esta pagina -->
	<style>
		img {
			width: 200px;
			height: 200px;
		}

		hr {
			margin-bottom: 60px;
		}
	</style>

</head>

<body>


	<div class="container">

		<h1>Selectores y Encadenamiento</h1>
		<hr>

		<div class="row">

			<div class="col-sm-4">
				<img src="img/nophoto.jpg" class="img-circle">
			</div>

			<div class="col-sm-5">
				<p>
					Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quibusdam aspernatur ab commodi tenetur,
					quisquam.
				</p>
			</div>

			<div class="col-sm-3">
				<ul>
					<li>Matemática</li>
					<li>Programación</li>
					<li>Análisis</li>
					<li>Física</li>
					<li>Geografía</li>
				</ul>
			</div>

		</div>
	</div>
	<script>
		/*$("img").attr("src","img/profesor.jpg");
		$("img").removeClass('img-circle');
		$("img").addClass('img-thumbnail');*/

		$("img")
			.attr("src", "img/profesor.jpg")
			.removeClass('img-circle')
			.addClass('img-thumbnail');

		/*Tarea
		$("img")
			.attr("src","img/perrito.jpg")
			.addClass('img-thumbnail');
			
		Agregando clases en una misma sentencia
		$("img")
			.attr("src","img/perrito.jpg")
			.addClass('img-circle img-thumbnail');*/
	</script>
</body>

</html>
```

# 6. replaceWith, children y Find

```html
<!DOCTYPE html>
<html>

<head>
	<meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
	<title>Lección 02 - Selectores y Encadenamiento</title>

	<!-- Importacion del jQuery -->
	<script src="js/lib/jquery-2.1.4.min.js"></script>

	<!-- Importacion del Bootstrap -->
	<link rel="stylesheet" href="css/bootstrap.min.css">


	<!-- Estilo para esta pagina -->
	<style>
		img {
			width: 200px;
			height: 200px;
		}

		hr {
			margin-bottom: 60px;
		}
		.morado {
			color: purple;
		}
		.rojo {
			color: red;
		}
		.azul {
			color: blue;
		}
		.verde {
			color: green;
		}
		.naranja {
			color: orange;
		}
	</style>

</head>

<body>


	<div class="container">

		<h1>Selectores y Encadenamiento</h1>
		<hr>

		<div class="row">

			<div class="col-sm-4 text-center">
				<img src="img/nophoto.jpg" class="img-circle">
				<h4>Fernando Herrera</h4>
			</div>

			<div class="col-sm-5">
				<p>
					Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quibusdam aspernatur ab commodi tenetur,
					quisquam.
				</p>
			</div>

			<div class="col-sm-3">
				<ul>
					<li>Matemática</li>
					<li>Programación</li>
					<li>Análisis</li>
					<li>Física</li>
					<li>Geografía</li>
				</ul>
			</div>

		</div>
	</div>
	<script>

		//Manejo de las imagenes
		$("img")
			.attr("src", "img/profesor.jpg")
			.removeClass('img-circle')
			.addClass('img-circle img-thumbnail');

		//Modificaciones al segundo bloque (col-sm-5)
		$(".col-sm-5")
			.find("p")
			//.text("Saludos, soy un catedratico de Udemy");
			.html("Saludos, soy un <u>catedratico</u> de Udemy");

		//Referencia a la lista ordenanda
		$("ul li")
			.eq(0).addClass('morado').end()
			.eq(1).addClass('rojo').end()
			.eq(2).addClass('azul').end()
			.eq(3).addClass('verde').end()
			.eq(4).addClass('naranja').end()
	</script>
</body>
</html>
```

# 7. Eventos

```html
<!DOCTYPE html>
<html>
<head>
	<meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
	<title>Lección 03 - Eventos</title>

	<!-- Importacion del jQuery -->
	<script src="js/lib/jquery-2.1.4.min.js"></script>
	
	<!-- Importacion del Bootstrap -->
	<link rel="stylesheet" href="css/bootstrap.min.css">

	<style>
		.img100 {
			width: 100px;
			height: 100px;
		}
		.divRojo {
			background-color: red;
			width: 100px;
			height: 100px;
		}
	</style>

</head>
<body>
<div class="container">
	
	<h1>Lección 03: Eventos</h1>
	<hr>

	<button class="btn btn-primary" id="bot1">Evento click</button>

	<br><br>
	<img src="img/profesor.jpg" class="img100">
	
	<br><br>
	<div class="divRojo"></div>

	<br><br>
	<a id="linkUdemy" href="http://udemy.com">Ir a Udemy</a>
</div>
<script>
	$("#bot1").on("click",function(){
		console.log("Click!");
	});
	//Evento mouse enter
	$(".img100").on("mouseenter",function(){
		//console.log("Mouse enter");
		$(this).attr("src","img/nophoto.jpg")


	});
	$(".img100").on("mouseleave",function(){
		//console.log("Mouse leave");
		$(this).attr("src","img/profesor.jpg")
	});
	$(".divRojo").on("click",function(){
		console.log("Click en el div rojo");
	});
	//Controles especiales para links
	// Comportamiento por defecto
	$("#linkUdemy").on('click',function(e){
		e.preventDefault();	//Evita que el comportamiento predeterminado del enlace ocurra
		console.log("Click en el link...");
		var link = $(this).attr("href");
		console.log(link);
		window.location = link;
	});
	//Funcion que se ejecuta cuando el documento HTML se ha cargado completamente
	$(document).ready(function(){
		console.log("La pagina esta lista para lo que sea.")
	})
</script>
</body>
</html>
```

# 8. Acordeones

```html
<!DOCTYPE html>
<html>
<head>
	<meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
	<title>Lección 04 - Acordeones</title>

	<!-- Importacion del jQuery -->
	<script src="js/lib/jquery-2.1.4.min.js"></script>
	
	<!-- Importacion del Bootstrap -->
	<link rel="stylesheet" href="css/bootstrap.min.css">

	<link rel="stylesheet" href="css/style.css">

</head>
<body>


<div class="container">
	
	<h1>Lección 04: Acordeones</h1>
	<hr>
	<div align="center">
		<dl>
			<dt>Titulo del acordeon</dt>
			<dd>Este es el detalle del acordeon</dd>
			<dt>Titulo del acordeon</dt>
			<dd>Este es el detalle del acordeon</dd>
			<dt>Titulo del acordeon</dt>
			<dd>Este es el detalle del acordeon</dd>
			<dt>Titulo del acordeon</dt>
			<dd>Este es el detalle del acordeon</dd>
			<dt>Titulo del acordeon</dt>
			<dd>Este es el detalle del acordeon</dd>
			<dt>Titulo del acordeon</dt>
			<dd>Este es el detalle del acordeon</dd>
			<dt>Titulo del acordeon</dt>
			<dd>Este es el detalle del acordeon</dd>
		</dl>
	</div>
</div>

<script>
	//Funcion anonima
	(function(){
		var dds = $('dd');
		dds.hide();	//Oculta elementos seleccionados
		$('dt').on('mouseenter',function(){
			dds.slideUp(200);	//Anima el ocultamiento gradual de los elementos deslizandolos hacia arriba en 200 milisegundos
			$(this)
				.next()
				.slideDown(200);	//Anima la aparicion gradual de elementos ocultos mediante un efecto de deslizamiento hacia abajo
		});		
	})();
</script>
</body>
</html>
```

```css
dl {
    width: 400px;
}
dd {
    margin: 0;
    padding: 10px;
}
dt {
    cursor: pointer;
    font-size: 18px;
    background-color: #e3e3e3;
    border-bottom: 1px solid #c5c5c5;
    border-top: 1px solid white;
}
```

# 9. Elementos dinamicos: On, Bind

```html
<!DOCTYPE html>
<html>

<head>
	<meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
	<title>Lección 05 - On y Bind</title>

	<!-- Importacion del jQuery -->
	<script src="js/lib/jquery-2.1.4.min.js"></script>

	<!-- Importacion del Bootstrap -->
	<link rel="stylesheet" href="css/bootstrap.min.css">

	<link rel="stylesheet" href="css/style.css">

</head>

<body>
	<div class="container">

		<h1>Lección 05: On y Bind</h1>
		<hr>
		<h3>Click me!!!</h3>
	</div>
	<script>
		(function () {
			var contador = 0;
			$("body").on("click", "h3", function () {
				contador++;
				var h3Dinamico = "<h3 id='h3-" + contador + "'>Dinamico: " + contador + "</h3><hr>";
				$(".container").append(h3Dinamico);	//append agrega contenido al final de los elementos seleccionados
				//$("body").prepend(h3Dinamico);	//prepend agrega contenido al principio del elemento seleccionado
				if (contador == 3) {
					$("#h3-2").bind("click", function () {
						console.log("Funcion dinamica");
					});
				}
				console.log(contador);
			})
		})();
	</script>
</body>

</html>
```

```css
h3 {
    cursor: pointer;
}
```

# 10. Tarea: Tabla de multiplicar
# 11. Resolucion de la Tarea y un extra!

```html
<!DOCTYPE html>
<html>

<head>
	<meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
	<title>Tarea 1</title>

	<!-- Importacion del jQuery -->
	<script src="js/lib/jquery-2.1.4.min.js"></script>

	<!-- Importacion del Bootstrap -->
	<link rel="stylesheet" href="css/bootstrap.min.css">

	<link rel="stylesheet" href="css/style.css">

</head>

<body>
	<div class="container">
		<h1>Tarea: <small>tabla del 3</small></h1>
		<hr>
		<select id="cmbBase" class="form-control">
			<option value="3">3</option>
			<option value="4">4</option>
			<option value="5" selected>5</option>
			<option value="6">6</option>
		</select>
		<hr>
		<button class="btn btn-primary">Agregar Linea</button>
		<table class="table table-striped">
			<tr>
				<th>Base</th>
				<th>x</th>
				<th>Numero</th>
				<th>=</th>
				<th>Resultado</th>
			</tr>
		</table>

	</div>
	<script>
		(function () {
			var contador = 0;
			$("button").on("click", function () {
				contador++;
				var base = $("#cmbBase").val();
				var linea = "";
				linea += '<tr>';
				linea += '<td>'+ base+'</td>';
				linea += '<td>x</td>';
				linea += '<td>'+contador+'</td>';
				linea += '<td>=</td>';
				linea += '<td>'+(base*contador)+'</td>';
				linea += '</tr>';
				$("table").append(linea);
			});

			//Funcion que detecta el cambio de la base
			$("#cmbBase").on("change",function(){
				$("tr").not(":eq(0)").remove();	//Selecciona todas las filas tr y luego las elimina todas, excepto la primera fila
				contador = 0;
			});
		})();

		/*var contador = 0;
		$("button").on("click", function () {
			contador++;
			var nuevaFila = "<tr>" +
				"<td>3</td>" +
				"<td>x</td>" +
				"<td>" + (contador) + "</td>" +
				"<td>=</td>" +
				"<td>" + (3 * contador) + "</td>" +
				"</tr>";
			$("table").append(nuevaFila);
		});*/
	</script>
</body>
</html>
```

