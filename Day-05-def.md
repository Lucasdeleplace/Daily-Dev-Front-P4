- ***[x] Comprendre le fonctionnement des branches dans Git :***

    **- [x] Lister, changer, créer, supprimer des branches**

    **Lister:** 
    ```bash
        git branch
    ```

    **changer:** 
    ```bash
        git checkout
    ```

    **créer:**
    ```bash
        git branch "name"
    ```

    **créer et changer:**
    ```bash
        git checkout -b "name"
    ```

    **supprimer des braches:**

    ```bash
        git branch -d [nom-de-ma-branche]

        git branch -D [nom-de-ma-branche] --> delete force
    ```

    ***- [x] Quelle est la différence entre `Git switch` et `Git checkout`***

        **Objectif** : git checkout est utilisé à la fois pour changer de branche et pour restaurer les états des fichiers, alors que git switch est spécifiquement conçu pour changer de branche.

        **Sécurité** : git switch ne permet pas d'écraser accidentellement les modifications, car il est conçu pour gérer exclusivement les opérations 
        de branche.
        
        **Clarté** : git switch rend les scripts et les commandes plus clairs, car il est évident à partir de la commande elle-même que vous effectuez un changement de branche.
    - [x] Comprendre le merge dans Git
        - [x] Comprendre le "fast forward"
            
            On avance plus vite dans le code pour allez plus vite a la partis qui nous interesse
        
        - [x] Quelle est la différence entre un "commit" et un "merge commit" ?
            
            Un **commit** enregistre les modifications effectuées sur ton code.
            
            Un **merge commit** est créé lorsque tu fusionnes deux branches pour combiner leurs modifications.

- ***[x] Comprendre le principe de "Pull Request"***

    ça permet de faire un demande de merge au autre membre de l'équipe qui pourront commenté accepter ou refusé le requete

- ***[x] Comprendre le rebase dans Git (quelle différence avec le merge ?)***

     ça ecrase les versions avant 

- ***[x] Ajouter ce repo en upstream dans les remotes sur son local après l'avoir forké et cloné***



- ***[x] Découvrir les conventions de nommage de son versionning avec la convention Angular :***
  - [x] https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-format
  - [x] https://www.conventionalcommits.org/fr/v1.0
  - [ ] Renommer son dernier commit en respectant cette convention

- ***[ ] Comprendre l'utilité et le fonctionnement de `git stash`***

- ***[ ] Créer un cheat sheet sur Git (en groupe en respectant les bests practices et Gitflow)***
