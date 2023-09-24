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
  ```javascript
      - tsc inputFile.ts outputFile.js
      - tsc inputFile.ts outputFile.js -w  // --> this will watch the changes & tranpile the ts code to js automatically.
  ```

##### Arrays

```javascript
1;
let names = ["Mario", "Marian", "David"];
names.push("Heath");
names.push(22); // Not allowed

2;
let names = ["Mario", 33, "David", 91];
names.push("Heath");
names.push(22); // Allowed
names.push(true); // Allowed
names[1] = 123; // Allowed

names = "String"; // names is an array. Its type can't be changed.
```

- Here variables types and values types both are fixed can't be modifed further.

##### Objects

```javascript
   1.
   let ninja = {
     name: 'mario',
     belt: 'black',
     age: 22
   }

   ninja.age = 33;
   ninja.name = "David"
   ninja.age = "24" // Not allowed - change property type not possible.
   ninja.skills:['Fighting'] // Not allowed - adding addtional property not allowed
```

## Explicit Types

```javascript
let name: string;
let age: number;
let isLoggedIn: boolean;
```

##### Arrays

```javascript
let ninjas: string[] = []; // we need to initalize ninjas with value of empty array otherwise it won't work.
ninjas.push("David"); // It will work perfectly fine.

let ninjas2: sting[];
ninjas.push("David"); // It will throw err - Cannot read property 'push' of undefined.
```

#### Union Types

- Creating array of different data types.
- pipe symbol is used for union.

```javascript
let mixedArray: (string | numbers)[] = [];
mixedArray.push(22);
mixedArray.push("David");

let uID: string | number;
```

#### Objects

```javascript
let ninjaObject: object;
ninjaObject = { name: "Test", age: 22 };
ninjaObject = []; // it can hold value of array as Array is a kind object.

let ninjaObject2: {
  name: string,
  age: number,
};
// ninjaObject2 will only take two above defined property.
```
