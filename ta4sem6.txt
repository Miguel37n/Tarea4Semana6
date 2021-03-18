#!/bin/bash

menu(){
echo "***************************************"
echo "*                Menu                 *"
echo "*      1. Crear archivo               *"
echo "*      2. Eliminar archivo            *"
echo "*      3. Salir                       *"
echo "***************************************"

echo "Escoja la opcion: "
read opcion

return $opcion
}

clear
menu

while ["$opcion" !=3]
do
	case $opcion in
		1)
		clear
		echo"************************"
		echo"*   CREAR DIRECTORIO   *"
		echo"************************"
		echo "Ingrese nombre del directorio:"
		read directorio

		mkdir $HOME/Documents/$directorio
		echo "Directorio creado correctamente"
		;;

		2)
		clear
		echo"************************"
		echo"*   ELIMINAR DIRECTORIO *"
		echo"************************"
		echo "Ingrese nombre del directorio:"
		read directorio

		mkdir $HOME/Documents/$directorio
		echo "Directorio eliminado correctamente"
		;;

		*)
			echo "Opcion no valida"
		;;
	esac

	echo ""
	echo ""

	menu
done
