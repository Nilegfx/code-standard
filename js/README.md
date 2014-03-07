# JavaScript code standard
Work in progress

## Naming convention:

Constructors: ```CapitalCase```

Constants: ```UPPER_CASE_WITH_UNDERSCORE```

Everything else: ```camelCase```

## Style

1. Indentation:
Configure your editor to insert 4 spaces when TAB key is pressed.

2. Curly brackets:
Required after statements such as ... ```if, switch, try, catch``` ... etc.
> For ```{```, place it at the end of the previous line, not the begining of the next line, to avoid wrong semicolon insertion causes misinterpretation of the program.

3. Simecolons:Required.

4. Var: required, declare all variables at the top of each function.
> Always remember that JavaScript does NOT have block scope, only functions have scope.


## Do NOT use ...

No language is perfect, there are something you should avoid ...

1. ```eval()```
2. ```with```
3. ```==```: too many unexpected results, use```===```instead.

    ```javascript
    '' == '0' // false
    0 == '' // true
    0 == '0' // true
    false == 'false' // false
    false == '0' // true
    false == undefined // false
    false == null // false
    null == undefined // true
    ' \t\r\n ' == 0 // true
    ```

4. Constructors without protection, which when called without "new", will contaminate other context wherever "this" points to (like "window").

    ```javascript
    function Person(name) {
        // return a new instance when
        // "this" is not pointed to the right place
        if(!(this instanceof Person)) {
            return new Person();
        }
        this.name = name;
    }
    ```

5. Reserved words, a common error like this ...

    ```javascript
    { class: 'my-class-name' }
    ```

    "class" is a reserved word, the browsers with ECMAScript 3 standard will throw an error, but not the ones with ECMAScript 5 standard.
