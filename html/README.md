# HTML code standard
Work in progress

## 1. Style
1. Tag and attribute names should be lowercase, prefix your customized properties with "data-"
    
    ```
    <div class="branch-finder" data-dojo-type="hsbccmb/BranchFinder">
    ```

## 2. Follow HTML standard
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
