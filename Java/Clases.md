
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
```

## Características de una Clase

- **Atributos**: Los atributos son variables que representan características del objeto. En el caso de la clase "Perro", los atributos son `nombre`, `raza` y `edad`. Los atributos se definen en la clase y pueden ser privados para aplicar encapsulamiento.

- **Constructor**: Un constructor es un método especial que se utiliza para inicializar los atributos de un objeto cuando se crea una instancia de la clase. En la clase "Perro", tenemos un constructor que toma argumentos para establecer los atributos.

- **Métodos**: Los métodos son funciones que definen el comportamiento de un objeto. La clase "Perro" tiene un método llamado `ladrar()` que permite que el perro ladre.

- **Encapsulamiento**: Java promueve el encapsulamiento al declarar los atributos como privados y proporcionar métodos públicos (métodos Getter) para acceder a ellos. Esto protege los datos y controla el acceso a ellos.

## Uso de la Clase "Perro"

Ahora, veamos cómo se pueden crear objetos de la clase "Perro" y utilizarlos en una aplicación.

```java
public class Main {
    public static void main(String[] args) {
        // Crear objetos de la clase "Perro"
        Perro perro1 = new Perro("Rex", "Labrador", 3);
        Perro perro2 = new Perro("Luna", "Golden Retriever", 2);

        // Hacer que los perros ladren
        perro1.ladrar();
        perro2.ladrar();

        // Acceder a los atributos
        System.out.println(perro1.getNombre() + " es un " + perro1.getRaza() + " de " + perro1.getEdad() + " años.");
        System.out.println(perro2.getNombre() + " es un " + perro2.getRaza() + " de " + perro2.getEdad() + " años.");
    }
}
```

## Conclusiones

La clase "Perro" es un ejemplo práctico de cómo se pueden utilizar clases en Java para modelar objetos del mundo real. Las clases proporcionan una estructura organizada para definir atributos y métodos que representan las características y el comportamiento de los objetos. Al aplicar conceptos como el encapsulamiento, se garantiza que los datos estén protegidos y el acceso a ellos esté controlado. En resumen, las clases son una parte fundamental de la programación en Java y son esenciales para la programación orientada a objetos.
