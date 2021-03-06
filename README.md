# Namespaced Bootstrap
This project is designed to bring Bootstrap which doesn't conflict with existing CSS and JS of a website.

You should consider using this project if you need to apply Bootstrap partially. ie to particular div of a page.

## Contribute

Even though the project is in alpha stage, it serves it's initial purpose pretty accurately. If you find any problem, you're more than welcomed to create an issue or pull request.

## How to use

1. Install
```bash
npm install --save bootstrap-sass-namespace
```

2. Define class prefix in SASS.
```sass
$class-prefix: 'my-namespace';
@import "node_modules/bootstrap-sass-namespace/assets/stylesheets/_bootstrap.scss";
```

3. Define class prefix in JS **before** including JS assets.
```html
<script>
    BOOTSTRAP_NAMESPACE = 'my-namespace';
</script>
<script src="assets/javascripts/bootstrap.min.js"></script>
```
4. Use special class notation `*prefix*-html-*tag*` on every tag.
Below you can find an example of drop down menu.
```html
<div class="my-namespace-html-div my-namespace-dropdown">
  <button class="my-namespace-html-button my-namespace-btn my-namespace-btn-default my-namespace-dropdown-toggle" type="button" id="dropdownMenu1" data-toggle="dropdown" aria-haspopup="true" aria-expanded="true">
    Dropdown
    <span class="my-namespace-html-span my-namespace-caret"></span>
  </button>
  <ul class="my-namespace-html-ul my-namespace-dropdown-menu" aria-labelledby="dropdownMenu1">
    <li class="my-namespace-html-li"><a class="my-namespace-html-a" href="#">Action</a></li>
    <li class="my-namespace-html-li"><a class="my-namespace-html-a" href="#">Another action</a></li>
    <li class="my-namespace-html-li"><a class="my-namespace-html-a" href="#">Something else here</a></li>
    <li class="my-namespace-html-li my-namespace-divider" role="separator"></li>
    <li class="my-namespace-html-li"><a class="my-namespace-html-a" href="#">Separated link</a></li>
  </ul>
</div>
```

## License

(MIT License)

Copyright (c) 2016 Dima Snisarenko snisarenkodima@gmail.com

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
