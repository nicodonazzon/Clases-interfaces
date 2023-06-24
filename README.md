# Clases-interfaces

En TypeScript, las interfaces son una forma de definir la estructura y los contratos que deben seguir las clases. Puedes implementar una interfaz en una clase utilizando la palabra clave `implements`. Al hacerlo, la clase debe proporcionar implementaciones para todos los miembros declarados en la interfaz.

Aquí tienes un ejemplo básico de cómo implementar una interfaz en una clase:

```typescript
interface Animal {
  name: string;
  sound: string;
  eat(food: string): void;
}

class Dog implements Animal {
  name: string;
  sound: string;

  constructor(name: string) {
    this.name = name;
    this.sound = "Woof";
  }

  eat(food: string) {
    console.log(`${this.name} is eating ${food}`);
  }
}
```

En este ejemplo, tenemos una interfaz llamada `Animal` que define las propiedades `name` y `sound`, así como el método `eat`. Luego, creamos una clase `Dog` que implementa la interfaz `Animal`. La clase `Dog` proporciona implementaciones para las propiedades `name` y `sound`, así como para el método `eat`.

También puedes implementar múltiples interfaces en una clase, separándolas por comas:

```typescript
interface CanFly {
  fly(): void;
}

interface CanSwim {
  swim(): void;
}

class Bird implements CanFly, CanSwim {
  fly() {
    console.log("The bird is flying");
  }

  swim() {
    console.log("The bird is swimming");
  }
}
```

En este ejemplo, la clase `Bird` implementa las interfaces `CanFly` y `CanSwim`, proporcionando implementaciones para los métodos `fly` y `swim` respectivamente.

Al implementar una interfaz en una clase, también puedes agregar propiedades y métodos adicionales a la clase. La interfaz solo establece los requisitos mínimos que deben cumplirse.

Es importante destacar que en TypeScript, la implementación de una interfaz no es obligatoria. Sin embargo, proporciona un mecanismo útil para definir contratos y asegurar que las clases cumplan con ciertas estructuras y comportamientos.
