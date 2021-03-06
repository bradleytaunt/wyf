# WYF - Watch Your Figure

Simple CSS "plugin" for toggle-styled figure elements (Watch Your Figure)

- Pure CSS - zero JavaScript
- Only 2.8 kB
- Fully responsive
- Only one class name

## The HTML
```
<figure class="wyf">
    <img src="/images/pig.svg" alt="Pig">
    <input type="checkbox">
    <figcaption>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Beatae ullam hic, nostrum praesentium repellat molestias culpa nemo placeat, alias facere voluptate quidem saepe quisquam nam quas accusamus adipisci provident architecto?</p>
    </figcaption>
</figure>
```

## The CSS
```
figure.wyf {
    position: relative;
}
figure.wyf figcaption {
    background: rgba(0,0,0,0.05);
    opacity: 0;
    padding: 20px;
    position: absolute;
    right: 0;
    top: 10px;
    transition: .3s ease-in-out all;
    width: 300px;
    z-index: -1;
}

figure.wyf input[type="checkbox"] {
    -moz-appearance: none;
    appearance: none;
    background: white url("data:image/svg+xml;base64,PHN2ZyB4bWxucz0naHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmcnIHdpZHRoPSc1MTInIGhlaWdodD0nNTEyJyB2aWV3Qm94PScwIDAgNTEyIDUxMic+PHRpdGxlPmlvbmljb25zLXY1LWU8L3RpdGxlPjxwYXRoIGQ9J00xNjAsMTY0czEuNDQtMzMsMzMuNTQtNTkuNDZDMjEyLjYsODguODMsMjM1LjQ5LDg0LjI4LDI1Niw4NGMxOC43My0uMjMsMzUuNDcsMi45NCw0NS40OCw3LjgyQzMxOC41OSwxMDAuMiwzNTIsMTIwLjYsMzUyLDE2NGMwLDQ1LjY3LTI5LjE4LDY2LjM3LTYyLjM1LDg5LjE4UzI0OCwyOTguMzYsMjQ4LDMyNCcgc3R5bGU9J2ZpbGw6bm9uZTtzdHJva2U6IzAwMDtzdHJva2UtbGluZWNhcDpyb3VuZDtzdHJva2UtbWl0ZXJsaW1pdDoxMDtzdHJva2Utd2lkdGg6NDBweCcvPjxjaXJjbGUgY3g9JzI0OCcgY3k9JzM5OS45OScgcj0nMzInLz48L3N2Zz4=") no-repeat center;
    background-size: 20px;
    border: 1px solid lightgrey;
    cursor: pointer;
    height: 20px;
    outline: none;
    padding: 15px;
    position: absolute;
    right: 0;
    top: 0;
    width: 20px;
}
figure.wyf input[type="checkbox"]:hover {
    background-color: #f9f9f9;
}
figure.wyf input[type="checkbox"]:checked {
    background-image: url("data:image/svg+xml;base64,PHN2ZyB4bWxucz0naHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmcnIHdpZHRoPSc1MTInIGhlaWdodD0nNTEyJyB2aWV3Qm94PScwIDAgNTEyIDUxMic+PHRpdGxlPmlvbmljb25zLXY1LWw8L3RpdGxlPjxsaW5lIHgxPSczNjgnIHkxPSczNjgnIHgyPScxNDQnIHkyPScxNDQnIHN0eWxlPSdmaWxsOm5vbmU7c3Ryb2tlOiMwMDA7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7c3Ryb2tlLWxpbmVqb2luOnJvdW5kO3N0cm9rZS13aWR0aDozMnB4Jy8+PGxpbmUgeDE9JzM2OCcgeTE9JzE0NCcgeDI9JzE0NCcgeTI9JzM2OCcgc3R5bGU9J2ZpbGw6bm9uZTtzdHJva2U6IzAwMDtzdHJva2UtbGluZWNhcDpyb3VuZDtzdHJva2UtbGluZWpvaW46cm91bmQ7c3Ryb2tlLXdpZHRoOjMycHgnLz48L3N2Zz4=");
}
/* You need to add more items here if you exceed the default amount (5) */
figure.wyf input[type="checkbox"]:nth-of-type(1):checked + figcaption,
figure.wyf input[type="checkbox"]:nth-of-type(2):checked + figcaption,
figure.wyf input[type="checkbox"]:nth-of-type(3):checked + figcaption,
figure.wyf input[type="checkbox"]:nth-of-type(4):checked + figcaption,
figure.wyf input[type="checkbox"]:nth-of-type(5):checked + figcaption {
    right: -300px;
    opacity: 1;
}

/* Mobile styling - this will differ depending on your website layout! */
@media(max-width:1100px) {
    figure.wyf figcaption,
    figure.wyf input[type="checkbox"]:checked + figcaption {
        opacity: 1;
        position: relative;
        right: auto !important;
        top: auto;
        transition: none;
        width: 100%;
    }
    figure.wyf input[type="checkbox"] {
        visibility: hidden;
    }
}
```
