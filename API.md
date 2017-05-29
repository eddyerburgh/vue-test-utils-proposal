## wrapper API

#### contains(selector)
**selector** - CSS selector or Vue component

**returns** - boolean

**example**
```js
wrapper.contains('div') // returns boolean
```
destroy()
```js
wrapper.destroy() // calls destory on vm
```
dispatch()
```js
wrapper.dispatch() // dispatches custom/browser event on wrapper vm/element
```
didEmit()
```js
wrapper.didEmit('update') // returns boolean
```
find()
```js
wrapper.find() // returns wrappers/ container class
```
hasAttribute()
```js
wrapper.hasAttribute('attribute') // returns boolean
```
hasClass()
```js
wrapper.hasClass('class') // returns boolean
```
hasStyle()
```js
wrapper.hasProp('style') // returns boolean
```
hasProp()
```js
wrapper.hasProp('prop') // returns boolean
```
html()
```js
wrapper.html() // returns HTML of wrapper DOM node as a string
```
is()
```js
wrapper.is('div') // returns boolean
```
isEmpty()
```js
wrapper.isEmpty() // returns true if no child nodes
```
isVueComponent()
```js
wrapper.isVueComponent() // returns boolean
```
name()
```js
wrapper.name() // returns component name if node is a Vue component, or tag name if native DOM node
```
setData()
```js
wrapper.setData({data: 'value'})
```
setProps()
```js
wrapper.setProps({prop: 'value'})
```
text()
```js
wrapper.text() // returns text content of wrapper
```
update()
```js
wrapper.update() // forces re render
```
