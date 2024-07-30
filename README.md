Proceso EmpresaTurismoMagallanes
	Definir nombre, matricula, nombre_capitan, turno Como Cadena
	Definir cantidad_tripulantes, cantidad_pasajeros, pasajeros_mayores, pasajeros_menores, total_manana, total_tarde, total_puerto, total_pasajeros_mayores, total_pasajeros_menores Como Entero
	Definir total_recaudado, sueldo_total_capitanes, sueldo_basico, bono, descuento_imposiciones, descuento_seguro_vida, sueldo_capitan, promedio_mayores, promedio_menores Como Real
	
	total_manana <- 0
	total_tarde <- 0
	total_puerto <- 0
	total_pasajeros_mayores <- 0
	total_pasajeros_menores <- 0
	total_recaudado <- 0
	sueldo_total_capitanes <- 0
	
	Para i <- 1 Hasta 10 Con Paso 1 Hacer
		Escribir "Registro de la embarcación ", i, ":"
		Escribir "Nombre de la embarcación: "
		Leer nombre
		Escribir "Matrícula de la embarcación: "
		Leer matricula
		Escribir "Nombre del capitán: "
		Leer nombre_capitan
		Escribir "Cantidad de tripulantes: "
		Leer cantidad_tripulantes
		Escribir "Cantidad de pasajeros: "
		Leer cantidad_pasajeros
		Escribir "Cantidad de pasajeros mayores de edad: "
		Leer pasajeros_mayores
		pasajeros_menores <- cantidad_pasajeros - pasajeros_mayores
		
		total_pasajeros_mayores <- total_pasajeros_mayores + pasajeros_mayores
		total_pasajeros_menores <- total_pasajeros_menores + pasajeros_menores
		
		Escribir "¿Salió en la mañana (m) o en la tarde (t)? (Si no salió, presione Enter): "
		Leer turno
		
		Si turno = "m" Entonces
			total_manana <- total_manana + 1
		FinSi
		Si turno = "t" Entonces
			total_tarde <- total_tarde + 1
		FinSi
		
		total_recaudado <- total_recaudado + (cantidad_pasajeros * 250000)
		
		sueldo_basico <- 800000
		bono <- 0.15 * sueldo_basico
		descuento_imposiciones <- 0.02 * sueldo_basico
		descuento_seguro_vida <- 0.03 * sueldo_basico
		sueldo_capitan <- sueldo_basico + bono - descuento_imposiciones - descuento_seguro_vida
		sueldo_total_capitanes <- sueldo_total_capitanes + sueldo_capitan
	FinPara
	
	total_puerto <- 10 - total_manana - total_tarde
	
	promedio_mayores <- total_pasajeros_mayores / 10
	promedio_menores <- total_pasajeros_menores / 10
	
	Escribir "Resultados al final del día:"
	Escribir "Embarcaciones que salieron en la mañana: ", total_manana
	Escribir "Embarcaciones que salieron en la tarde: ", total_tarde
	Escribir "Embarcaciones que se quedaron en el puerto: ", total_puerto
	Escribir "Total recaudado por pasajeros: ", total_recaudado, " CLP"
	Escribir "Sueldo total a pagar a los capitanes: ", sueldo_total_capitanes, " CLP"
	Escribir "Promedio de pasajeros mayores de edad: ", promedio_mayores
	Escribir "Promedio de pasajeros menores de edad: ", promedio_menores
FinProceso
