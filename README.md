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
   
   
   # Codigo java
   
   import java.util.Scanner;
import java.util.Scanner;
 public class zapateria {
     String talla;
     String modelo;
     double costo;
     public zapateria{
         this.talla = talla;
         this.modelo = modelo;
         this.costo = costo;
     }
     public String getTalla(){
         return talla;
     }
     public void setTalla(String talla){
         this.talla = talla;
     }
     public String getModelo(){
         return modelo;
     }
     public void setModelo(String modelo){
         this.modelo = modelos;
     }
     public double getCosto(){
        return costo;
        }
     public void setCostos(double costo){
         this.costo = costo;
     }
     public String toString() {
         return "Talla: "+ talla +", modelo: "+ modelo + ", costo: $"+ costos;
     }
 }
   import java.util.Scanner;
import java.util.ArrayList;

public class tienda
{
   public static void main(String[] args){
       ArrayList<zapateria> pedidos = new ArrayList<zapateria>();
        ArrayList<String> clientes = new ArrayList<String>();
        ArrayList<String> identificaciones = new ArrayList<String>();
       Scanner sc = new Scanner(System.in);
       zapateria[] losZapatos = new zapateria[50];
       int opciones = 0;
       double costoTotal = 0;
       do {
          System.out.println("\nIngrese la talla del zapato:");
            String talla = sc.nextLine();
            System.out.println("Ingrese el modelo del zapato:");
            String modelo = sc.nextLine();
            System.out.println("Ingrese el costo del zapato:");
            double costo = Double.parseDouble(sc.nextLine());
            System.out.println("Ingrese el nombre del cliente:");
            String nombre = sc.nextLine();
            System.out.println("Ingrese la identificación del cliente:");
            String identificacion = sc.nextLine();

            pedidos.add(new losZapatos(talla, modelo, costo));
            clientes.add(nombre);
            identificaciones.add(identificacion);
            costoTotal += costo;

            System.out.println("\n¿Desea ingresar otro pedido?\n1. Sí\n2. No");
            opciones = Integer.parseInt(sc.nextLine());
        } while (opciones != 2); 
       System.out.println("\nDatos almacenados:");

        for (int i = 0; i < pedidos.size(); i++) {
            System.out.println("\nPedido " + (i+1) + ":");
            System.out.println(pedidos.get(i));
            System.out.println("Nombre del cliente: " + clientes.get(i));
            System.out.println("Identificación del cliente: " + identificaciones.get(i));
        }

        System.out.println("\nCosto total de los pedidos: $" + costoTotal);

        sc.close();
   }
}
   
