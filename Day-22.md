### Jeudi 14/11/2024

#### Brief

---

### React :

  - **Comprendre ce qu'est un `template` dans React :**  
    [Ici](https://react.dev/learn/rendering-a-component) pour une introduction aux templates et à la façon dont React rend les composants.

    Un template dans React est une manière de définir la structure et le contenu d'un composant en utilisant JSX (JavaScript XML). JSX permet d'écrire du HTML dans du JavaScript.

    ```JSX
    function Welcome(props) {
    return <h1>Hello, {props.name}</h1>;
    }
    ```

  - **Comprendre l'interpolation de texte :**  
    Apprendre à afficher des variables et des expressions dans le JSX.

    L'interpolation de texte permet d'afficher des variables et des expressions dans le JSX en utilisant des accolades {}.

    ```JSX
    const name = 'John';
    const element = <h1>Hello, {name}</h1>;
    ```

  - **Comprendre les composants fonctionnels et les composants de classe :**  
     Différences et usages appropriés pour chaque type de composant.

    Les composants fonctionnels sont des fonctions JavaScript qui acceptent des props et retournent du JSX. Les composants de classe sont des classes ES6 qui étendent React.Component.

    ```JSX
        //Exemple de composant fonctionnel
        function Welcome(props) {

        return <h1>Hello, {props.name}</h1>;
        }

        //Exemple de composant de classe
        class Welcome extends React.Component {
          render() {
            return <h1>Hello, {this.props.name}</h1>;
          }
        }
    ```

  - **Comprendre le binding de propriétés (props) :**

    - [ ] **Connaître les meilleures pratiques pour le binding de propriétés :**  
          Utiliser les props de manière efficace et éviter les pièges courants.

      Les props sont des arguments passés aux composants React. Ils permettent de transmettre des données d'un composant parent à un composant enfant.

      ```JSX
       function Welcome(props) {
           return <h1>Hello, {props.name}</h1>;
         }

         const element = <Welcome name="Sara" />;
      ```

  - **Comprendre le binding d'attributs :**
    Le binding d'attributs en React permet de lier des valeurs aux attributs HTML dans le JSX.

      ```JSX
      const element = <img src={user.avatarUrl} alt={user.name} />;
      ```

  - [ ] **Différence entre le binding d'attribut et le binding de propriété :**
        Savoir comment React gère les attributs HTML dans le JSX.

    Les attributs HTML sont définis dans le balisage HTML et sont utilisés pour initialiser les propriétés DOM. Une fois que l'élément est créé, les attributs HTML ne changent pas.

    Exemple :

      ```JSX
            const element = <img src="image.jpg" alt="Description" />;
      ```

    Dans cet exemple, src et alt sont des attributs HTML.

    Binding de propriété :

    Les propriétés DOM sont des valeurs qui peuvent être modifiées après la création de l'élément. En React, les propriétés sont utilisées pour refléter l'état actuel de l'élément.

    Exemple :

      ```JSX
        const element = <input type="text" value={this.state.inputValue} onChange={this.handleChange} />;
      ```

    - [ ] **Pourquoi utiliser le binding d'attribut :**
          Avantages et scénarios d'utilisation.

      Avantages :

      1. **Initialisation des propriétés DOM** : Les attributs HTML sont utilisés pour initialiser les propriétés DOM lors de la création de l'élément. Cela permet de définir des valeurs par défaut pour les éléments.

      2. Compatibilité avec le HTML standard : Utiliser des attributs HTML permet de maintenir la compatibilité avec le HTML standard, ce qui peut être utile pour le rendu côté serveur ou pour des outils qui analysent le HTML.

      3. Simplicité : Pour des valeurs statiques qui ne changent pas après le rendu initial, les attributs HTML sont simples et faciles à utiliser.

         Scénarios d'utilisation :

         Images : Définir la source (src) et le texte alternatif (alt) pour une image.

          ```JSX
          const element = <img src="image.jpg" alt="Description" />;
          ```

         Liens : Définir l'URL de destination (href) pour un lien.

          ```JSX
          const element = <a href="https://example.com">Visit Example</a>;
          ```

         Formulaires : Définir les attributs statiques des éléments de formulaire, comme le type (type) d'un champ de saisie.

          ```JSX
          const element = <input type="text" placeholder="Enter your name" />;
          ```

         En résumé, le binding d'attribut est utile pour définir des valeurs statiques et initiales des éléments HTML, assurant ainsi une compatibilité avec le HTML standard et une simplicité d'utilisation pour des scénarios où les valeurs ne changent pas dynamiquement.

  - **Comprendre le style en ligne et le CSS :**

  Les styles en ligne peuvent être appliqués directement dans le JSX en utilisant un objet JavaScript. Les fichiers CSS peuvent également être utilisés pour styliser les composants.

  Exemple de style en ligne :

  ```JSX
    const divStyle = {
    color: 'blue',
    backgroundColor: 'lightgray',
    };

    function StyledComponent() {
    return <div style={divStyle}>Hello World!</div>;
    }
  ```

  Exemple de style avec CSS :

  ```CSS
    /* styles.css */
    .myClass {
      color: blue;
      background-color: lightgray;
    }
  ```

  ```JSX
    import './styles.css';

    function StyledComponent() {
      return <div className="myClass">Hello World!</div>;
    }
  ```

  - [ ] **Appliquer du style aux composants :**
        Utiliser les styles en ligne ou des fichiers CSS pour styliser les composants.

    En React, il existe plusieurs façons de styliser les composants. Les deux méthodes les plus courantes sont l'utilisation de styles en ligne et de fichiers CSS.

    Styles en ligne :

    Les styles en ligne sont définis directement dans le JSX en utilisant un objet JavaScript. Chaque propriété CSS est définie en camelCase.

    Exemple :

    ```JSX
          const divStyle = {
            color: 'blue',
            backgroundColor: 'lightgray',
            padding: '10px',
            borderRadius: '5px'
          };

          function StyledComponent() {
            return <div style={divStyle}>Hello World!</div>;
          }
    ```

    Fichiers CSS :
    Les fichiers CSS externes peuvent être utilisés pour styliser les composants. Les classes CSS sont définies dans un fichier .css et appliquées aux éléments en utilisant l'attribut className.

    Exemple :

    ```CSS
          /* styles.css */
          .myClass {
            color: blue;
            background-color: lightgray;
          }
    ```

    ```JSX
          import './styles.css';

          function StyledComponent() {
            return <div className="myClass">Hello World!</div>;
          }
    ```

    Avantages et inconvénients :

    - Styles en ligne :

      - Avantages : Facile à utiliser pour des styles spécifiques et dynamiques, encapsulation des styles au niveau du composant.
      - Inconvénients : Moins réutilisable, peut devenir verbeux pour des styles complexes.

    - Fichiers CSS :

      - Avantages : Réutilisabilité des styles, séparation des préoccupations, plus facile à maintenir pour des styles complexes.
      - Inconvénients : Risque de conflits de noms de classes, nécessite une gestion des dépendances CSS.

    En fonction des besoins de votre projet, vous pouvez choisir l'une ou l'autre méthode, ou même les combiner pour tirer parti des avantages de chacune.

- **Comprendre le binding d'événements :**

  Le binding d'événements permet de gérer les événements utilisateur comme les clics, les changements de valeur, etc.

  - [ ] **Gérer les événements avec React :**
        Utiliser les gestionnaires d'événements comme `onClick`, `onChange`, etc.

    En React, les événements sont gérés de manière similaire aux événements DOM natifs, mais avec quelques différences notables. Les gestionnaires d'événements sont passés en tant que props aux éléments JSX en utilisant la camelCase.

    Utiliser les gestionnaires d'événements :
    onClick : Gérer les clics de souris.

          onChange : Gérer les changements de valeur des champs de formulaire.

          onSubmit : Gérer la soumission de formulaires.

          onMouseOver : Gérer le survol de la souris.

          Avantages des gestionnaires d'événements en React :

    - Encapsulation : Les gestionnaires d'événements sont définis au niveau du composant, ce qui permet une meilleure encapsulation et réutilisabilité.

    - Gestion de l'état : Les gestionnaires d'événements peuvent facilement interagir avec l'état (state) du composant pour mettre à jour l'interface utilisateur de manière réactive.

    - Prévention des comportements par défaut : Les événements peuvent être facilement interceptés et leurs comportements par défaut peuvent être empêchés en utilisant event.preventDefault().

    En utilisant les gestionnaires d'événements comme onClick, onChange, etc., vous pouvez créer des interfaces utilisateur interactives et réactives en React.

- **Comprendre le binding à double sens :**
  Le binding à double sens permet de synchroniser l'état d'un composant avec les entrées utilisateur.

  - [ ] **Utiliser `useState` pour gérer l'état des entrées :**
        Mettre en place le binding à double sens à l'aide des hooks.

    ```JSX
      import { useState } from 'react';

      function NameForm() {
        const [name, setName] = useState('');

        return (
          <input
            type="text"
            value={name}
            onChange={(e) => setName(e.target.value)}
          />
        );
      }
    ```

- **Comprendre le flux de contrôle dans les composants :**

  Le flux de contrôle dans les composants React est influencé par l'état (state) et les props.

  - [ ] **Gérer le flux d'exécution dans un composant :**
        Comprendre comment le state et les props influencent le comportement des composants.

    **State :**
    Le state est un objet qui contient des données spécifiques à un composant et qui peuvent changer au fil du temps. Les changements d'état entraînent un nouveau rendu du composant.

    **Exemple :**

    ```JSX
          import { useState } from 'react';

          function Counter() {
            const [count, setCount] = useState(0);

            function increment() {
              setCount(count + 1);
            }

            return (
              <div>
                <p>Count: {count}</p>
                <button onClick={increment}>Increment</button>
              </div>
            );
          }
    ```

    Dans cet exemple, le state (count) est initialisé à 0 et est mis à jour chaque fois que le bouton est cliqué, ce qui entraîne un nouveau rendu du composant avec la valeur mise à jour.

    **Props :**
    Les props (propriétés) sont des arguments passés aux composants depuis leur parent. Les props sont immuables et ne peuvent pas être modifiés par le composant qui les reçoit.

    **Exemple :**

    ```JSX
          function Welcome(props) {
            return <h1>Hello, {props.name}</h1>;
          }

          function App() {
            return <Welcome name="Sara" />;
          }
    ```

    Dans cet exemple, le composant Welcome reçoit une prop name avec la valeur "Sara" depuis le composant parent App.

    **Interaction entre state et props :**

    - State : Utilisé pour gérer les données internes d'un composant qui peuvent changer au fil du temps.

    - Props : Utilisées pour passer des données et des fonctions d'un composant parent à un composant enfant.

- **Comprendre ce que sont les `hooks` dans React :**
  [Ici](https://react.dev/learn/what-is-a-hook) pour une introduction aux hooks de React.

  Les hooks sont des fonctions qui permettent d'utiliser l'état et d'autres fonctionnalités de React dans les composants fonctionnels.

  ```JSX
    import { useState } from 'react';

    function Counter() {
      const [count, setCount] = useState(0);

      return (
        <div>
          <p>You clicked {count} times</p>
          <button onClick={() => setCount(count + 1)}>Click me</button>
        </div>
      );
    }
  ```

- [ ] **Connaître les différents hooks intégrés à React :**

  - `useState`, `useEffect`, `useContext`, etc., et leurs usages respectifs.

    `useState` :

    Le hook useState permet d'ajouter un état local à un composant fonctionnel. Il retourne une paire de valeurs : l'état actuel et une fonction pour le mettre à jour.

    **Exemple** :

    ```JSX
      import { useState } from 'react';

      function Counter() {
        const [count, setCount] = useState(0);

        return (
          <div>
            <p>Count: {count}</p>
            <button onClick={() => setCount(count + 1)}>Increment</button>
          </div>
        );
      }
    ```

    `useEffect` :

    Le hook useEffect permet d'exécuter des effets secondaires dans les composants fonctionnels, comme les requêtes réseau, les abonnements ou les mises à jour manuelles du DOM. Il s'exécute après chaque rendu.

    **Exemple** :

    ```JSX
      import { useState, useEffect } from 'react';

      function Timer() {
        const [count, setCount] = useState(0);

        useEffect(() => {
          const timer = setInterval(() => {
            setCount((prevCount) => prevCount + 1);
          }, 1000);

          return () => clearInterval(timer); // Cleanup
        }, []);

        return <div>Count: {count}</div>;
      }
    ```

    `useContext` :

    Le hook useContext permet d'accéder au contexte React dans un composant fonctionnel. Il simplifie le partage de valeurs entre les composants sans avoir à passer explicitement des props.

    **Exemple** :

    ```JSX
      import { useContext } from 'react';

      const ThemeContext = React.createContext('light');

      function ThemedComponent() {
        const theme = useContext(ThemeContext);

        return <div className={theme}>Themed Component</div>;
      }
    ```

    `useReducer` :

    Le hook useReducer est une alternative à useState pour gérer des états complexes. Il est similaire à un réducteur Redux.

    **Exemple** :

    ```JSX
      import { useReducer } from 'react';

      const initialState = { count: 0 };

      function reducer(state, action) {
        switch (action.type) {
          case 'increment':
            return { count: state.count + 1 };
          case 'decrement':
            return { count: state.count - 1 };
          default:
            throw new Error();
        }
      }

      function Counter() {
        const [state, dispatch] = useReducer(reducer, initialState);

        return (
          <div>
            <p>Count: {state.count}</p>
            <button onClick={() => dispatch({ type: 'increment' })}>Increment</button>
            <button onClick={() => dispatch({ type: 'decrement' })}>Decrement</button>
          </div>
        );
      }
    ```

    `useRef` :

    Le hook useRef permet de créer une référence mutable qui persiste pendant tout le cycle de vie du composant. Il est souvent utilisé pour accéder directement aux éléments DOM.

    **Exemple** :

    ```JSX
      import { useRef } from 'react';

      function TextInputWithFocusButton() {
        const inputEl = useRef(null);

        const onButtonClick = () => {
          inputEl.current.focus();
        };

        return (
          <div>
            <input ref={inputEl} type="text" />
            <button onClick={onButtonClick}>Focus the input</button>
          </div>
        );
      }
    ```

    `useMemo` :

    Le hook useMemo permet de mémoriser une valeur calculée, ce qui peut améliorer les performances en évitant des calculs coûteux à chaque rendu.

    **Exemple** :

    ```JSX
      import { useMemo } from 'react';

      function ExpensiveCalculationComponent({ num }) {
        const result = useMemo(() => {
          // Expensive calculation
          return num * 2;
        }, [num]);

        return <div>Result: {result}</div>;
      }
    ```

    `useCallback` :

    Le hook useCallback permet de mémoriser une fonction, ce qui peut améliorer les performances en évitant de recréer des fonctions à chaque rendu.

    **Exemple** :

    ```JS
      import { useCallback } from 'react';

      function ParentComponent() {
        const handleClick = useCallback(() => {
          console.log('Button clicked');
        }, []);

        return <ChildComponent onClick={handleClick} />;
      }

      function ChildComponent({ onClick }) {
        return <button onClick={onClick}>Click me</button>;
      }
    ```

    Ces hooks intégrés à React permettent de gérer efficacement l'état, les effets secondaires, le contexte, et bien plus encore dans les composants fonctionnels.

- [ ] **Savoir utiliser le hook `useEffect` :**
      Gestion des effets secondaires dans les composants.

  ```JS
    import { useState, useEffect } from 'react';

    function Timer() {
      const [count, setCount] = useState(0);

      useEffect(() => {
        const timer = setInterval(() => {
          setCount((prevCount) => prevCount + 1);
        }, 1000);

        return () => clearInterval(timer);
      }, []);

      return <div>Count: {count}</div>;
    }
  ```

- [ ] **Comprendre la portée des hooks :**
      Savoir comment et quand utiliser les hooks dans les composants.

  Les hooks ne peuvent être utilisés qu'à l'intérieur des composants fonctionnels ou d'autres hooks personnalisés.
