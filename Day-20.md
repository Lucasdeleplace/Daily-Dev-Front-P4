### Mardi 12/11/2024

#### Brief

---

### Node.js

#### Installation et introduction

- [ ] **Installation de Node.js**  
       Guide d'installation pour différents systèmes d'exploitation (Windows, macOS, Linux).

- [ ] **Différence entre Node et NPM :**  
       Explication de la différence entre Node.js (environnement d'exécution) et NPM (gestionnaire de paquets).

---

#### Découverte des gestionnaires de paquets

- [ ] **Découverte de NPM, Yarn et PNPM :**

  - [ ] Comprendre les différences entre ces gestionnaires de paquets.
  - [ ] Choisir un gestionnaire en fonction des besoins du projet.

- [ ] **Les commandes de base avec un gestionnaire de paquets :**
  - [ ] **Initialiser un projet Node** (`npm init`)
    - [ ] Comprendre la structure du fichier `package.json` ([Référence](https://docs.npmjs.com/cli/v10/configuring-npm/package-json)).
  - [ ] **Installer un package** (localement et globalement).
  - [ ] **Désinstaller un package** (localement et globalement).
  - [ ] **Mettre à jour les packages** (localement et globalement) ainsi que le gestionnaire de paquets.

---

#### Linters et formatters

- [ ] **Découvrir les linters et formatters :**
  - [ ] **Quelle est la différence entre un linter et un formatter ?**  
         Le linter vérifie le code pour s'assurer qu'il suit certaines conventions, tandis que le formatter ajuste le format du code automatiquement.
  - [ ] **Quels sont les principaux outils les plus utilisés ?**  
         Exemples : ESLint, Prettier.
  - [ ] **Installation globale vs installation par projet :**  
         Avantages et inconvénients d'installer les outils globalement ou localement.

---

#### Nodemon

- [ ] **Qu'est-ce que Nodemon ?**
  - [ ] **À quoi sert-il ?**  
         Nodemon redémarre automatiquement le serveur lorsque des modifications sont apportées au code.

---

#### Premier projet avec Node.js

- [ ] **Créer un projet "Hello World!" avec Node.js**  
       Écrire et exécuter un simple serveur qui affiche "Hello World!".

---

### TypeScript

- [ ] **Qu'est-ce que TypeScript ?**  
       Introduction à TypeScript, ses avantages par rapport à JavaScript, et comment il améliore la robustesse du code avec le typage statique.

  TypeScript est un sur-ensemble typé de JavaScript qui compile en JavaScript simple. Il ajoute des types statiques optionnels au langage, ce qui permet de détecter les erreurs à la compilation plutôt qu'à l'exécution.

Exemple :
```js
let message: string = "Hello, TypeScript!";
console.log(message);
```
- [ ] **Installation de TypeScript :**  
       Guide sur l'installation et la configuration de TypeScript dans un projet Node.js.

  Pour installer TypeScript, vous devez avoir Node.js installé. Ensuite, vous pouvez utiliser npm pour installer TypeScript globalement.

Commandes :

```bash
npm install -g typescript
```

Pour initialiser un projet TypeScript, créez un fichier tsconfig.json :

```bash
tsc --init
```

- [ ] **Syntaxe de base de TypeScript :**

  - [ ] Comprendre les types primitifs (string, number, boolean, etc.).

  Comprendre les types primitifs
  TypeScript utilise des annotations de type pour définir les types de variables.

Exemple :

```js
let isDone: boolean = false;
let decimal: number = 6;
let color: string = "blue";

function addNumbers(num1: number, num2: number): number {
  return num1 + num2;
}
console.log(addNumbers("2", "3")); // Erreur de compilation : "Argument of type 'string' is not assignable to parameter of type 'number'"
```

- [ ] Utilisation des interfaces et des types personnalisés.  
       Les interfaces permettent de définir des structures de données complexes.

Exemple :

```js
interface Person {
  firstName: string;
  lastName: string;
  age: number;
}

let user: Person = {
  firstName: "John",
  lastName: "Doe",
  age: 30,
};
```

- [ ] Introduction aux classes et aux modules en TypeScript.

      Les classes en TypeScript sont similaires à celles de JavaScript avec des fonctionnalités supplémentaires comme les modificateurs d'accès.

Exemple :

```js
class Greeter {
  greeting: string;

  constructor(message: string) {
    this.greeting = message;
  }

  greet() {
    return "Hello, " + this.greeting;
  }
}

let greeter = new Greeter("world");
console.log(greeter.greet());
```

Les modules permettent de structurer le code en plusieurs fichiers.

Exemple :

```js
// file: greeter.ts
export class Greeter {
  greeting: string;

  constructor(message: string) {
    this.greeting = message;
  }

  greet() {
    return "Hello, " + this.greeting;
  }
}

// file: main.ts
import { Greeter } from "./greeter";

let greeter = new Greeter("world");
console.log(greeter.greet());
```

- [ ] Pourquoi utiliser TypeScript ?

Eviter les erreurs, Langage Typé, Code plus facile a comprendre/modifier/reutilisable. TypeScript offre une meilleure autocomplétion, erreurs detecter a la compilation avant l'execution du code, le typage ce fais directement a la donnée

### Compétences à Mobiliser

#### Compétences spécifiques Développeur Front-End

- **C1**. Concevoir et déployer des applications en utilisant Node.js.
- **C2**. Utiliser TypeScript pour améliorer la robustesse du code.

#### Compétences transversales

- **C3**. Analyser et résoudre des problèmes liés à la gestion des paquets et aux outils de développement.
- **C4**. Documenter le processus de développement et partager les meilleures pratiques.

---
