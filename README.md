# Ejercicio 1
En su labor como programador de software ha sido elegido para el desarrollo de una aplicación que necesita un coordinador logístico de una tienda de reparación de computadores, que desea calcular el promedio de ingresos que han tenido en el último periodo. Se requiere para saber cómo tal el promedio de ingresos netos para los reportes fiscales de la empresa. Como información básica de cada cliente se debe registrar el número de identificación, su nombre y la reparación que se le ha realizado. Aclaraciones:

• Se supondrá que la aplicación solo se requiere para calcular el promedio de un único periodo especifico.

• Para efectos de mantener la simplicidad del ejemplo no se contemplan manejar persistencia en el almacenamiento de los datos.

• No se realiza validación, ni se verifica calidad en los datos ingresados


# HU Programa
![WhatsApp Image 2023-05-16 at 9 33 03 AM](https://github.com/FranksGP/frank/assets/133733876/15013d7b-cdc8-49d7-ba6c-8d840db55f43)


# Diagrama caso de uso




# Diagrama de Flujo
![WhatsApp Image 2023-05-16 at 9 37 46 AM](https://github.com/FranksGP/frank/assets/133733876/dd8d7033-c1b0-4f39-80f0-42158a56725f)


# Pseudocodigo

Inicio
   // Inicializar listas y variables
   pedidos = []
   clientes = []
   identificaciones = []
   costoTotal = 0

   Repetir
      // Solicitar datos del zapato, cliente y costo
      mostrar "Ingrese la talla del zapato:"
      leer talla
      mostrar "Ingrese el modelo del zapato:"
      leer modelo
      mostrar "Ingrese el costo del zapato:"
      leer costo
      mostrar "Ingrese el nombre del cliente:"
      leer nombre
      mostrar "Ingrese la identificación del cliente:"
      leer identificacion

      // Agregar datos a las listas y calcular costo total
      pedidos.agregar(talla + ", " + modelo)
      clientes.agregar(nombre)
      identificaciones.agregar(identificacion)
      costoTotal = costoTotal + costo

      // Preguntar si desea ingresar otro pedido
      mostrar "¿Desea ingresar otro pedido? (Sí/No)"
      leer respuesta

      Mientras respuesta sea "Sí"

   // Mostrar datos almacenados
   mostrar "Datos almacenados:"
   Para i = 0 hasta longitud(pedidos) - 1
      mostrar "Pedido " + (i+1) + ":"
      mostrar "Talla y modelo: " + pedidos[i]
      mostrar "Nombre del cliente: " + clientes[i]
      mostrar "Identificación del cliente: " + identificaciones[i]

   mostrar "Costo total de los pedidos: " + costoTotal
   Fin
