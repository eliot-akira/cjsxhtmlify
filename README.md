cjsxhtmlify
====

In .babelrc

~~~json
"plugins": [
  ["transform-react-jsx", { "pragma": "jsxhtml" }]
]
~~~

Browserify args in gulpfile

~~~javascript
transform: [ 'cjsxhtmlify', 'babelify' ],
extensions: ['.coffee','.js']
~~~

In application

~~~coffee
require 'jsxhtml'
~~~

Use

~~~coffee
template =
  <div class="something">
    <b>Yey</b>
  </div>
~~~
