## wrapper API

### contains(selector)
Returns true if wrapper contains selector

**selector** - `String|Object` CSS selector or Vue component

**returns** - `Boolean`

**example**
```js
wrapper.contains('div') // returns boolean
```
### destroy()
Calls $destroy on vms

**comments** - maybe unneeded. Same could be achieved with `wrapper.vm.$destory`

**example**
```js
wrapper.destroy() // calls destory on vm
```
### dispatch()
Dispatches native event or custom event to wrapper elements or vms

**comments** - should this be broken into two methods - dispatch and emit?

**example**
```js
wrapper.dispatch() // dispatches custom/browser event on wrapper vm/element
```
### didEmit()
Asserts wrapper vm emitted event

**returns** - `Boolean`

**example**
```js
wrapper.didEmit('update') // returns boolean
```
### find(selector)
Returns true if wrapper contains selector

**selector** - `String|Object` CSS selector or Vue component

**returns** - `Object` wrapper containing new elements

**example**
```js
wrapper.find() // returns wrappers/ container class
```
### hasAttribute()
```js
wrapper.hasAttribute('attribute') // returns boolean
```
### hasClass()
```js
wrapper.hasClass('class') // returns boolean
```
### hasStyle()
```js
wrapper.hasProp('style') // returns boolean
```
### hasProp()
```js
wrapper.hasProp('prop') // returns boolean
```
### html()
```js
wrapper.html() // returns HTML of wrapper DOM node as a string
```
### is()
```js
wrapper.is('div') // returns boolean
```
### isEmpty()
```js
wrapper.isEmpty() // returns true if no child nodes
```
### isVueComponent()
```js
wrapper.isVueComponent() // returns boolean
```
### name()
```js
wrapper.name() // returns component name if node is a Vue component, or tag name if native DOM node
```
### setData()
```js
wrapper.setData({data: 'value'})
```
### setProps()
```js
wrapper.setProps({prop: 'value'})
```
### text()
```js
wrapper.text() // returns text content of wrapper
```
### update()
```js
wrapper.update() // forces re render
```
