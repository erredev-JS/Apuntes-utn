# Informe de Estudio sobre Clases en Java (Usando la Clase "Perro" como Ejemplo)

## Introducción

En Java, las clases son un concepto fundamental de la programación orientada a objetos. Las clases permiten modelar y organizar objetos del mundo real en el código. Para ilustrar este concepto, utilizaremos la clase "Perro" como un ejemplo práctico.

## Definición de la Clase "Perro"

La clase "Perro" es una representación de un perro en nuestro programa. Un perro tiene características como su nombre, raza y edad, y puede realizar acciones, como ladrar. A continuación, definiremos la clase "Perro" con atributos y métodos.

```java
public class Perro {
    // Atributos
    private String nombre;
    private String raza;
    private int edad;

    // Constructor
    public Perro(String nombre, String raza, int edad) {
        this.nombre = nombre;
        this.raza = raza;
        this.edad = edad;
    }

    // Método para ladrar
    public void ladrar() {
        System.out.println(nombre + " está ladrando: ¡Guau, guau!");
    }

    // Métodos Getter
    public String getNombre() {
        return nombre;
    }

    public String getRaza() {
        return raza;
    }

    public int getEdad() {
        return edad;
    }
}
