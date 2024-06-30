# CREAR PDF CON DOMPDF

Usamos la libreria https://github.com/dompdf/dompdf 


## 00-quickstart.php

Ejemplo de la DOMPDF

## 01-curso.php

Leemos un JSON y generamos un pdf de todo el curso.

```php
// Output the generated PDF to Browser
$dompdf->stream();
```	

## 02-curso.php

Guardamos los pdf en el servidor 

```php	
// Guardar el PDF en el servidor
$pdfOutput = $dompdf->output();
$nombrearchivo = 'curso_'.time().'.pdf';
file_put_contents('pdf/'.$nombrearchivo, $pdfOutput);
```

