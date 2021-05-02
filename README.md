# Side-by-side `div`s with `inline-block`

**Warning: your browser will consider any space between a closing tag and an opening tag as white space, and place a single "space" character between your images. To prevent this from happening, place the final `>` of the closing `</div>` tag right next to the initial `<` of the following `<div>` opening tag.**

[See on Stack Overflow](https://stackoverflow.com/questions/9555240/delete-white-space-between-divs)

```html
      ...
       <p>Dog's paw</p>
     </div
    ><div>
      <img src="img/nails.jpg" alt="hand" />
      ...
```

If you do not do this, the 50% width of the two images *plus* the unwanted space character will result in a total width of more than 100%, and the second image will wrap to the next line.

If you use Prettier to format your HTML, it will, opinionatedly, "correct" your HTML and reinsert a new line between the two divs, which will break your layout, like this:

```html
    </div>
    <div>
  ```


Click [here](https://dciforks.github.io/inline-block/) for preview
