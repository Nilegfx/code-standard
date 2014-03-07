# CSS code standard
Work in progress

## Units, numbers
1. No units for ```line-height```

    ```css
    p {
        font-size: 12px;
        line-height: 1.5; /* correct */
        line-height: 1.5em; /* wrong */
        line-height: 150%; /* wrong */
    }
    ```

2. Numbers should be divisible by 2, otherwise there will be pixel offset under different browsers.
3. If the number is 0, no units should be provided, it's not neccessary.
