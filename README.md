<?php
 if($_POST) {
# Aqui definimos el usuario y password
# Puedes cambiar el usuario y clave x lo q sea
$usuario = 'lauri';
$clave = 'lauri';
# Aqui compruebo q los datos(usuario y contraseña) ingresados sean igual a lo que eh definido
# Y si son correcto los datos redireciona al enlace de tu sitio Autorizado
# En que caso que no sean correcto los datos  recirecciona al enlace de Error de  Datos Ingresados
if(trim($_POST['user'])==$usuario && trim($_POST['pass'])==$clave) {
header('Location: si_no.html');
 }else{
header('Location: Error.html');
 }
   }

?>
<html>
<head>
<title>Acceso</title>
</head>
<body>
<form action="" method="post">
<table border="1" cellpadding="5" cellspacing="0" align="center">
<tr><td colspan="2" align="center">ACCESO</td></tr>
<tr><td>Usuario:</td> <td><input type="text" name="user" /></td></tr>
<tr><td>Contrasñea:</td> <td><input type="password" name="pass" /></td></tr>
<tr><td align="center" colspan="2"><input type="submit" name="enviar" value="Enviar" /></td></tr>
</table>
</form>
</body>
</html>
