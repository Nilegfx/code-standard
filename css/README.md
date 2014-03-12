# CSS code standard
Work in progress

## Naming convention:
1. Class, ID names: `lowercase-with-dash`, try to describle it clearly without abbreviations. 

    > Also it's better to avoid names like `blue-bold-heading`, leave the defination of styles out of names, otherwise you may need to change it afterward when styles changed. Try to describle by "What it is" not "How it looks like".
    
    > Only assign ID to an element if it's unique, assign same classes to items that share the same stylesheet rules.
    
    > There is also a attribute selector to match the start of dash seperated attribute value. `[attr|=value]`

## Units, numbers
1. No units for `line-height`

    ```css
    p {
        font-size: 12px;
        line-height: 1.5; /* correct */
        line-height: 1.5em; /* wrong */
        line-height: 150%; /* wrong */
    }
    ```

1. Numbers should be divisible by 2, otherwise there will be pixel offset under different browsers.
1. If the number is 0, no units should be provided, it's not neccessary.

## Do not restate certain properties
1. `display: block`:

    ```css
    li {
        float: left;
        display: block; /* unneccessary */
    }
    button {
        position: absolute;
        display: block; /* unneccessary */
    }
    ```

## Best practices
1. The way to clear float
2. The way to center an element
