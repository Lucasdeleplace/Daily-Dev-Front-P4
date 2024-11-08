### Jeudi 07/11/2024

#### Brief

---

### POO (Programmation Orientée Objet)

#### JavaScript et l'Objet

- [ ] **JavaScript est-il un langage orienté objet ?**  
       Discussion sur les caractéristiques de la POO dans JavaScript.

  JavaScript est un langage orienté objet basé sur des prototypes. Cela signifie qu'au lieu d'utiliser des classes pour créer des objets, JavaScript utilise des prototypes. Cependant, depuis ECMAScript 6 (ES6), JavaScript supporte également les classes, ce qui le rapproche des langages orientés objet traditionnels.

---

poo paradicme facon apprende en consi que code object element object


#### Concepts Fondamentaux

- [ ] **Comprendre l'abstraction :**  
       Principe consistant à masquer les détails complexes pour ne présenter que l'essentiel.

  L'abstraction consiste à masquer les détails complexes d'une fonctionnalité pour ne présenter que l'essentiel. Cela permet de simplifier l'utilisation des objets en cachant les détails d'implémentation.

  ```js
  class Car {
    constructor(make, model) {
      this.make = make;
      this.model = model;
    }

    startEngine() {
      console.log("Engine started");
    }
  }

  const myCar = new Car("Toyota", "Corolla");
  myCar.startEngine();
  ```

- [ ] **Le principe d'instance :**  
       Qu'est-ce qu'une instance d'une classe et comment elle est créée.

  Une instance est un objet créé à partir d'une classe. Chaque instance possède ses propres propriétés et méthodes définies par la classe.

  ```js
  class Dog {
    constructor(name) {
      this.name = name;
    }

    bark() {
      console.log(`${this.name} barks!`);
    }
  }

  const myDog = new Dog("Rex");
  myDog.bark();
  ```

---

#### Les Classes en JavaScript

- [ ] **Qu'est-ce qu'une classe ?**

  Une classe est un modèle pour créer des objets. Elle définit les propriétés et les méthodes que les objets créés à partir de cette classe posséderont.

  - [ ] **Différences entre classes concrètes et abstraites**  
         Comprendre les distinctions entre une classe implémentée directement et une classe abstraite servant de modèle.

    Une classe concrète est une classe qui peut être instanciée directement. Une classe abstraite, en revanche, ne peut pas être instanciée et sert de modèle pour d'autres classes.

    ```js
    //Class abstraites
    class Animal {
      constructor(name) {
        if (new.target === Animal) {
          throw new TypeError("Cannot construct Animal instances directly");
        }
        this.name = name;
      }

      makeSound() {
        throw new Error("Method 'makeSound()' must be implemented.");
      }
    }

    //class concrètes
    class Dog extends Animal {
      makeSound() {
        console.log("Woof!");
      }
    }

    const myDog = new Dog("Rex");
    myDog.makeSound(); // Woof!
    ```

  - [ ] **Le `constructor` :**  
         Utilité et fonctionnement du constructeur pour initialiser les objets.

    Le constructeur est une méthode spéciale utilisée pour initialiser les objets créés à partir d'une classe.

    ```js
    class Book {
      constructor(title, author) {
        this.title = title;
        this.author = author;
      }
    }

    const myBook = new Book("1984", "George Orwell");
    console.log(myBook.title); // 1984
    ```

  - [ ] **Attributs / Propriétés :**  
         Définition et gestion des attributs d'une classe.

          Les attributs ou propriétés sont des variables associées à un objet. Elles définissent les caractéristiques de l'objet.

          ```js
          class User {
              constructor(username, email) {
            this.username = username;
            this.email = email;
            }
          }

          const user1 = new User('john_doe', 'john@example.com');
          console.log(user1.username);
          ```

  - [ ] **Méthodes :**
  Les méthodes sont des fonctions associées à un objet. Elles définissent les comportements de l'objet.
    ```js
      class Calculator {*
      //methode add
        add(a, b) {
          return a + b;
        }
      //methode subtract
        subtract(a, b) {
          return a - b;
        }
      }

      const calc = new Calculator();
      console.log(calc.add(5, 3)); // 8
      console.log(calc.subtract(5, 3)); // 2
    ```
    - [ ] Différences entre méthodes et fonctions.

    Les méthodes sont des fonctions définies à l'intérieur d'une classe et associées à des objets. Les fonctions, en revanche, sont définies indépendamment des classes.

    ```js
    //fonction
      function greet() {
        console.log('Hello!');
      }

      class Greeter {
        //methode
        greet() {
          console.log('Hello from the class!');
        }
      }

      greet(); // Hello!
      const greeter = new Greeter();
      greeter.greet(); // Hello from the class!
    
    ```
    - [ ] Utilité des méthodes dans le cadre de la POO.

      Les méthodes permettent de définir les comportements des objets et d'interagir avec leurs propriétés.

    - [ ] Utilisation des **getters** et **setters** pour contrôler l'accès aux propriétés.

    Les getters et setters sont des méthodes spéciales qui permettent de contrôler l'accès aux propriétés d'un objet.

    ```js
    class Person {
      constructor(name) {
        this._name = name;
      }

      get getName() {
        return this._name;
      }

      set setName(newName) {
        if (newName.length > 0) {
          this._name = newName;
        } else {
          console.log('Name cannot be empty');
        }
      }
    }

    const person = new Person('Alice');
    console.log(person.getName); // Alice
    person.setName = 'Bob';
    console.log(person.name); // Bob
    person.setName = ''; // Name cannot be empty
    
    ```

---

#### Les Objets en JavaScript

- [ ] **Comprendre ce qu'est un objet :**  
       Représentation d'une instance d'une classe avec ses propriétés et méthodes.



---

#### Encapsulation

- [ ] **Qu'est-ce que l'encapsulation ?**

  L'encapsulation est un principe fondamental de la programmation orientée objet (POO) qui consiste à regrouper les données (propriétés) et les méthodes (comportements) qui manipulent ces données au sein d'une même unité, appelée classe. Cela permet de protéger les données internes d'un objet et de contrôler leur accès.

  - [ ] **À quoi sert l'encapsulation ?**  
         Protège les données internes d'un objet et contrôle leur accès.

         L'encapsulation sert à protéger les données internes d'un objet contre les modifications non autorisées et à contrôler leur accès. Cela permet de garantir l'intégrité des données et de définir des interfaces claires pour interagir avec l'objet.

  - [ ] **Mots-clés réservés pour l'encapsulation :**  
         Apprentissage des modificateurs d'accès comme `private`, `protected`, `public`.

      Les modificateurs d'accès comme private, protected, et public sont utilisés pour contrôler la visibilité et l'accessibilité des propriétés et des méthodes d'une classe.

      - private : Les membres privés ne sont accessibles qu'à l'intérieur de la classe où ils sont définis.
      - protected : Les membres protégés sont accessibles dans la classe où ils sont définis et dans les classes dérivées.
      - public : Les membres publics sont accessibles depuis n'importe où.

    ```js 
          class Animal {
            public name;
            protected age;
            private type;

            constructor(name, age, type) {
              this.name = name;
              this.age = age;
              this.type = type;
            }

            getType() {
              return this.type;
            }
          }

          class Dog extends Animal {
            constructor(name, age, type) {
              super(name, age, type);
            }

            getAge() {
              return this.age;
            }
          }

          const dog = new Dog('Rex', 5, 'Mammal');
          console.log(dog.name); // Rex
          console.log(dog.getAge()); // 5
          console.log(dog.getType()); // Mammal
      ```
  - [ ] **Principe de "scope" (portée) :**  
         Comprendre la portée des variables et leur accessibilité dans une classe et un objet.

         La portée (scope) des variables détermine où ces variables peuvent être accessibles. En JavaScript, la portée peut être globale, locale à une fonction, ou locale à un bloc (définie par des accolades {}).


  - [ ] **Pourquoi l'encapsulation est-elle un principe fondamental de la POO ?**  
        L'importance de cette notion dans la gestion sécurisée des données et des comportements des objets.

        L'encapsulation est essentielle pour la gestion sécurisée des données et des comportements des objets. Elle permet de :

          - Protéger les données internes contre les modifications non autorisées.
          - Contrôler l'accès aux données et aux méthodes.
          - Simplifier la maintenance et l'évolution du code en définissant des interfaces claires.
          - Favoriser la réutilisabilité et la modularité du code.

        En résumé, l'encapsulation contribue à la robustesse, à la sécurité et à la clarté du code en POO.

---

### Compétences à Mobiliser

#### Compétences spécifiques Développeur Front-End

- **C1**. Concevoir des applications en utilisant les principes de la POO.
- **C2**. Implémenter des classes et des objets en JavaScript pour structurer le code.

#### Compétences transversales

- **C3**. Analyser et résoudre des problèmes de programmation complexes.
- **C4**. Documenter et partager des connaissances sur les meilleures pratiques en POO.

---
