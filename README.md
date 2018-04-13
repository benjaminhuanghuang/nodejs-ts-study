## Reference
    - Developing a RESTful API with Node and TypeScript
        - http://mherman.org/blog/2016/11/05/developing-a-restful-api-with-node-and-typescript/
    
    - Building a Node.js App with TypeScript Tutorial
        - https://blog.risingstack.com/building-a-node-js-app-with-typescript-tutorial/
        - https://github.com/RisingStack/node-typescript-starter

    - Node Hero - Node.js Project Structure Tutorial
        - https://blog.risingstack.com/node-hero-node-js-project-structure-tutorial/

        
## Setup
```
    npm install -g typescript

```

## TypeSciprt config
- in compilerOptions we tell TypeScript that we’ll be targeting ES2015 and that we’d like a CommonJS style module as output (the same module style that Node uses)
- the include section tells the compiler to look for .ts files in the “src” directory
- the exclude section tells the compiler to ignore anything in “node_modules”


## Type
    In TypeScript, when you install third-party packages, you should also pull down the package’s type definitions. 
    This tells the compiler about the structure of the module that you’re using, giving it the information needed to properly evaluate the types of structures that you use from the module.

    Before TypeScript 2.0, dealing with .d.ts (type definition) files could be a real nightmare.
    With TypeScript 2.0, TypeScript definitions are managed by npm and installed as scoped packages. To install a type module, prefix its name with @types/
    Install the type definitions for Node, Express, and debug:
    ```
    $ npm install @types/node@6.0.46 @types/express@4.0.33 @types/debug@0.0.29 --save-dev
    ```
## TDD
    Mocha can only interpret JavaScript files, not TypeScript.
    ts-node will interpret and transpile our TypeScript in memory as the tests are run.

## Add ESLint
    To use ESLint with TypeScript, you have to add an extra package: 
    ```
    typescript-eslint-parser
    ```
    Run ESLint
    ```
    eslint src --ext ts
    ```