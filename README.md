# Tecnológico de Software

## Materia: Fundamentos de Álgebra

### Alumno: Francisco Emilio Esquivel Torres

### Actividad #20 - Matrices

---

Objetivo: Documentar el Excel 

---

Ejemplo de como documentar codigo

```java
import java.util.Scanner;

public class prueba2 {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        String contrasena;
        boolean valido;

        do {
            System.out.print("Ingresa una contraseña: ");
            contrasena = sc.nextLine();

            valido = true; // se asume válida hasta comprobar lo contrario

            // ----------------------------
            // 1. Validar longitud >= 8
            // ----------------------------

             if (contrasena.length() < 8) {
                 System.out.println("Error: mínimo 8 caracteres.");
                 valido = false;
               }else{valido = true;}

            // ----------------------------
            // 2. Validar al menos una mayúscula
            // ----------------------------
            boolean tieneMayus = false;

            for (int i = 0; i < contrasena.length(); i++){
                if(Character.isUpperCase(contrasena.charAt(i))){
                    tieneMayus = true;
                }
            }
            if (tieneMayus) {
                valido = true;
            }else{
                System.out.println("debe contener una mayuscula por lo menos");
                valido = false;
            }


            // ----------------------------
            // 3. Validar al menos una minúscula
            // ----------------------------

            boolean tieneMinus = false;
           

            for (int i = 0; i < contrasena.length(); i++){
                if(Character.isLowerCase(contrasena.charAt(i))){
                    tieneMinus = true;
                }
            }
            if (tieneMinus) {
                valido = true;
            }else{
                System.out.println("debe contener una minuscula por lo menos");
                valido = false;
            }

            // ----------------------------
            // 4. Validar al menos un dígito
            // ----------------------------

            boolean tieneDigito = false;
            // COMPLETAR

             for(int i = 0; i < contrasena.length(); i++){
                if(Character.isDigit(contrasena.charAt(i))){
                    tieneDigito = true;
                    break;
                }
             }
             if(tieneDigito){
                valido = true;
             } else{
                System.out.println("no contiene numeros");
                valido = false;
            }

            // ----------------------------
            // 5. Validar que NO existan espacios
            // ----------------------------

             if (contrasena.contains(" ")) {
                System.out.println("Error: no debe contener espacios.");
                 valido = false;
             }

            // Mensaje final si no es válida
            if (!valido) {
                System.out.println("La contraseña no cumple los requisitos. Intenta de nuevo.\n");
            }

        } while (!valido);

        System.out.println("Contraseña válida.");
    }
}

```
```Excel
=transponer(Kermit !A1:AD30)
```
ejemplo matriz
| | | |
|---|---|---|
|1|2|3|
|a|b|c|
|x|y|z|

1. como programar la hoja de exel
2. Escribir las 5 matrices (30 x 30)
3. Documentar la formula de la transpuesta
4. Documentar la formula de la suma
5. Documentar la formula de la resta
6. Docume ntar la formula de la multiplocacion a escalar
7. Documentar la composicion  


