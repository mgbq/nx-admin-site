# FontAwesomeIcons
# parameter
| parameterName	| introduce	|required	|valueType	|An optional value	|default|
| ------------|------| ----|----- |-------|---------|
|name	| TheNameOfTheIcon|no|	String|	font-awesome| All icon names|	font-awesome|
# method of application
base
```js
// There's nothing wrong with this but it doesn't work
<nx-icon/>

// Specify icon name
<nx-icon name="github"/>

// Set the inline style
<nx-icon name="github" style="font-size: 100px;"/>

// Set class
<nx-icon name="github" class="icon-class-demo"/>
```
This component just simplifies the writing

```js
<nx-icon name="github"/>
// equate
<i class="fa fa-github" aria-hidden="true"></i>
```

# reference
Icon index

[Font Awesome Chinese website](http://www.fontawesome.com.cn/faicons/)

[fontawesome.com](https://fontawesome.com/icons?d=gallery)