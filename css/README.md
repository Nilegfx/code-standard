# CSS code standard
Work in progress

## General Guidelines 
* Include a commented link at the top of the stylesheets back to the coding standards document
* When minifing a CSS, include a commented link at the top to view the unminified CSS

## Naming convention
* Use lowercase and dashes for Class, ID names.

```css
 .lowercase-with-dash {...} /*recommended*/ 
 
 .Capital-with-dash {...} /*not recommended*/ 
 #CapitalCaseClassOrId {...} /*not recommended*/ 
 #ID_NAME {...} /*not recommended*/ 
```
* try to describle it clearly without abbreviations. avoid names like `blue-bold-heading`, leave the defination of styles out of names, otherwise you may need to change it afterward when styles changed. Try to describle by "What it is" not "How it looks like"

```css
.main-title-heading {...} /*recommended*/

.blue-bold-heading {...} /*not recommended*/ 
```

* Avoid using IDs for styling. IDs are great for anchor links and JS hooks, but avoid using them as styling hooks.

```css
#title {color: green;} /*not recommended*/ 

/*not recommended*/ 
#title {
  background-image: url("path/to/image.jpg");
  text-decoration: underline;
}
```

* There is also a attribute selector to match the start of dash seperated attribute value. `[attr|=value]`

* Avoid qualifying class names with type selectors. you may want to apply it in a different element

```css
.nav {...}/*recommended*/ 
.important {...} /*recommended*/ 

ul.nav {...} /*not recommended*/
span.important {...} /*not recommended*/
```

* Prefix states classes with `is-` for more meaningful naming

```css
.is-hidden {...}/*recommended*/ 
.is-collapsed {...} /*recommended*/ 

.hidden {...} /*not recommended*/
.collapsed {...} /*not recommended*/
```

## Formatting CSS
* Use soft-tabs with 2 space indent.
* Separate selectors and declarations by new lines for multi-lined properties.

**Multi-lined**
```css
.success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #468847;
}
```
**single line**
```css
.success {color: #468847;}
```

* Add a single space before the opening bracket `{` in rule sets.
* Place opening bracket of declaration block in the same line with the declaration and place the closing bracket of declaration block on its own "separate" line

```css
/*recommended*/
.success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #468847;
}

/*not recommended*/
.success 
{
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #468847;
}
  
.success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #468847;}
```

* Add one blank line bewteen rule sets

```css
/*recommended*/
.success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #468847;
}

.error {
  background-color: #ecc7c7;
  border-color: #db0011;
  color: #468847;
}

/*not recommended*/
.success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #468847;
}
.error {
  background-color: #ecc7c7;
  border-color: #db0011;
  color: #468847;
}

```

* Add a space between properties and values after the colon `:`
```css
.success {color: #468847;} /*recommended*/
.success {color:#468847;} /*not recommended*/
```

* Include a semi-colon after every declaration, including the last declaration

```css
/*recommended*/
.selector {
  color: #468847;
  background: #db0011;
}

/*not recommended*/
.selector {color: #468847}

/*not recommended*/
.selector {
  color: #468847;
  background: #db0011
}
```

* Use quotes when needed in selctors or values, prefer double quotes. `input[type="checkbox"]` 

```css
input[type="checkbox"] {...} /*recommended*/

input[type=checkbox] {...} /*not recommended*/
```

* Use lowercase format for property and value names

```css
a {font-weight: bold;} /*recommended*/

a {FONT-WEIGHT: bold;}/*not recommended*/
a {font-weight: BOLD;}/*not recommended*/
a {font-weight: Bold;}/*not recommended*/

```
* Omit leading `0`s in values.

```css
.selector {font-size: .8em;} /*recommended*/

.selector {font-size: 0.8em;}/*not recommended*/
```

## Comments & Documentation
* 


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
