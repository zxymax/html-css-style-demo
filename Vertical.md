### div 垂直居中几种实现方法

```html
<div class="wrapper">
  <div class="inner"></div>
</div>
```

#### (1)
```css
.wrapper {
  width: 600px;
  height: 400px;
  border: 2px solid black;
  display: flex;
  justify-content: center;
  align-items: center;
}
.inner {
  width: 150px;
  height: 100px;
  background: red;
}
```


#### (2)
```css
.wrapper {
  width: 600px;
  height: 400px;
  border: 2px solid black;
  position: relative;
}

.inner {
  width: 150px;
  height: 100px;
  background: red;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```

#### (3)
```css
.wrapper {
  width: 600px;
  height: 400px;
  border: 2px solid black;
  position: relative;
}

.inner {
  width: 150px;
  height: 100px;
  background: red;
  position: absolute;
  margin: auto;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
}
```

#### (4)
```css
.wrapper {
  width: 600px;
  height: 400px;
  display: grid;
  place-items: center;
  border: 2px solid blue;
}

.inner {
  width: 150px;
  height: 100px;
  background: red;
}
```
#### (5)
```css
.wrapper {
  display: flex;
  flex-direction: column;
  border: 2px solid black;
  width: 600px;
  height: 400px;
}

.inner {
  width: 150px;
  height: 100px;
  background: red;
  margin: auto;
}
```

#### (6)
```css
.wrapper {
  width: 600px;
  height: 400px;
  border: 2px solid black;
  display: flex;
}

.inner {
  width: 150px;
  height: 100px;
  background: red;
  align-self: center;
  margin: auto;
}
```

#### (7)
```css
.wrapper {
  width: 600px;
  height: 400px;
  border: 2px solid black;
  display: grid;
}

.inner {
  width: 150px;
  height: 100px;
  background: red;
  justify-self: center;
  align-self: center;
}
```

#### (8)
```css
.wrapper {
  width: 600px;
  height: 400px;
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: repeat(3, 1fr);
  border: 2px solid black;
}

.wrapper::before,
.wrapper::after {
  content: '';
}

.inner {
  width: 150px;
  height: 100px;
  background: red;
  margin: 0 auto;
}
```

#### (9)
```css
.wrapper{
  width: 600px;
  height: 400px;
  border: 2px solid black;
  display:grid;
  grid-template-columns:1fr;
  grid-template-rows: repeat(3, 1fr);
}

.inner{
  background: red;
  width: 150px;
  height: 100px;
  margin: 0 auto;
  grid-row: 2 / span 1;
}

```

#### (10)
```css
.wrapper {
  width: 600px;
  height: 400px;
  border: 2px solid black;
  display: table-cell;
  vertical-align: middle;
}

.inner {
  width: 150px;
  height: 100px;
  background: red;
  margin: 0 auto;
}
```

