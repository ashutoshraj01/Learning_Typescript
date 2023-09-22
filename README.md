# Typescript

- Superset to Javascript.
- Need to be compiled back to javascript.
- Allows us to use strict types(types of variables be modified) --> debugging becomes easier, clean code, less error prone codes.
- Extra features --> Generics, Interfaces, Tuples.
- It allows to typecheck during development & hence helps in writing cleaner code. eg:-
  ```javascript
      const calculateCircumference(radius: number){
            return 2*Math.PI.radius
        }
    // If we try to provide any other type it will throw error
        calculateCircumference('hello'); // err --> Argument of type 'hello' is not assignable to parameter of type 'number'.
        calculateCircumference(5); // works fine.
  ```

##### Converting Typescript file to Javascript

- Typescript must be already installed.
- Now run command
- tsc inputFile.ts outputFile.js
- tsc inputFile.ts outputFile.js -w --> this will watch the changes & tranpile the ts code to js automatically.
