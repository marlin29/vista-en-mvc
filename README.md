Recibe datos por parte del modelo y esta los muestra
Pueden proporcionar un servicio de "Actualización ()" al que llama el controlador o el modelo.

EJEMPLO DE UN INSERT en el cual manda los datos al controlador
<form id="frmInsert" name="frmInsert" action="controlador.php" method="post" onsubmit="return validar();">
		<input id="idProd" name="idProd" type="text" placeholder="id Producto" value="<?php echo @$cat_mod[0][0]; ?>" hidden/>
		<div class="row">
			<h1>Registrar Producto</h1>
		  <span>
		    <input class="balloon" id="nombre" name="nombre" type="text" placeholder="Nombre" value="<?php echo @$cat_mod[0][1]; ?>" onkeypress="return Vname();" required/><label for="Nombre">Nombre</label>
		  </span>
		  <span>
		    <input class="balloon" id="cant" name="cant" type="text" placeholder="Cantidad" value="<?php echo @$cat_mod[0][2]; ?>" onkeypress="return Vcant();" required/><label for="Cantidad">Cantidad</label>
		  </span>
		  <span>
		    <input class="balloon" id="precio" name="precio" type="text" placeholder="Precio" value="<?php echo @$cat_mod[0][3]; ?>" onkeypress="return Vprecio();"  required/><label for="Precio">Precio</label>
		  </span>
		<input type="submit" name="btnEnviar" id="btnEnviar" value="<?php if(isset($_GET['id_mod'])) {
			echo 'Modificar';
		}
		else
		{
			echo 'Registrar';
		}
		 ?>">
		
		</div>	
	</form>
