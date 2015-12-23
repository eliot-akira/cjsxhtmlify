cjsxhtmlify
====

In .babelrc

~~~json
"plugins": [
  ["transform-react-jsx", { "pragma": "jsxhtml" }]
]
~~~

---

Browserify args in gulpfile

~~~javascript
transform: [ 'cjsxhtmlify', 'babelify' ],
extensions: ['.coffee','.js']
~~~

---

In application

~~~coffee
require('cjsxhtmlify').pragma
~~~

This is only necessary once. It makes *jsxhtml* available as a global function. The transformer takes inline JSX and converts it to *jsxhtml* function calls, which then returns an HTML string.

---

Use

~~~coffee
template =
  <div class="something">
    <b>Yey</b>
  </div>
~~~

---

In retrospect, it may keep things simpler to have the template in a separate HTML file, and require it directly using [stringify](https://github.com/JohnPostlethwait/stringify).
