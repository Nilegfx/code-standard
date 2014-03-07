# HTML code standard
Work in progress

## Naming convention:
1. Class, ID names: `lowercase-with-dash`, try to describle it clearly without abbreviations.

## Style:
1. Tag and attribute names should be lowercase, prefix your customized properties with "data-"
    
    ```
    <div class="branch-finder" data-dojo-type="hsbccmb/BranchFinder">
    ```

## Follow HTML standard:
1. Doctype declaration, always use
    
    ```
    <!DOCTYPE html>
    ```
2. First couple lines in the HEAD
    
    ```
    <meta charset="UTF-8">
    <meta http-equiv="x-ua-compatible" content="IE=edge">
    ```

    the first line avoids garbled words caused by wrong encoding detection of browsers,
    the second line prevents MSIE works in legacy standard or quirks mode by default.

## Do NOT use ...:
1. \<a\> tag with href filled with JavaScript codes to prevent default behavior, it violents the principle to seperate structure, presentation, and function. Bind an event in JavsScript to prevent default behavior, or better, use a \<button\> tag instead.
    ```javascript
    function (evt) { evt.preventDefault(); }
    ```
    ```
    <button type="button">
    ```
