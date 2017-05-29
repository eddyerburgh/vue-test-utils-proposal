# API

### methods
- [mount](#mountcomponent-options)
- [shallow](#shallowcomponent-options)
- [wrapper](#wrapper)
  * [contains](#containsselector)
  * [destroy](#destroy)
  * [dispatch](#dispatchevent)
  * [didEmit](#didemit)
  * [find](#findselector)
  * [hasAttribute](#hasattributeattribute)
  * [hasClass](#hasclassclass)
  * [hasStyle](#hasstylestyle)
  * [hasProp](#haspropprop)
  * [html](#html)
  * [is](#isselector)
  * [isEmpty](#isEmpty)
  * [isVueInstance](#isVueInstance)
  * [name](#name)
  * [setData](#setdatadata)
  * [setProps](#setpropsprops)
  * [text](#text)
  * [update](#update)

## mount(Component, options)

Mount component.

#### options `Object`

**attachToDocument** `Boolean` attach DOM to document. Default false

**globals** - `Object` methods and properties to be added as globals

**provide** - `Object` properties to [inject](https://vuejs.org/v2/api/#provide-inject) into component

**props** - `Object`

**slots** - `Object`

**slots.name** - `Array<Component>|Component`

#### returns `Object` - Wrapper/ Vue Wrapper

#### example
```js
const wrapper = mount(Component, {
 globals: { $route: stub() }
 props: { myProp: 'my prop' },
 provide: { anotherProp: 'access via `inject`' },
 slots: {
  default: [AnotherComponent],
  header: HeaderComponent
 }
})
```

## shallow(Component, options)

Render component n level deeep, defaults to 1. stub child components so they can still be tested.

#### options `Object`

**attachToDocument** `Boolean` attach DOM to document. Default false

**depth** - `Number` - number of levels to render

**globals** - `Object` methods and properties to be added as globals

**props** - `Object`

**slots** - `Object`

**slots.name** - `Array<Component>|Component`

#### returns `Object` - Wrapper/ Vue Wrapper

#### example
```js
const wrapper = shallow(Component, {
 globals: { $route: stub() }
 props: { myProp: 'my prop' },
 slots: {
  default: [AnotherComponent],
  header: HeaderComponent
 }
})
```

## wrapper

### contains(selector)
Returns true if wrapper contains selector

**selector** - `String|Object` CSS selector or Vue component

**returns** - `Boolean`

**example**
```js
wrapper.contains('div')
```
### destroy()
Calls $destroy on vms

**comments** - maybe not needed. Same could be achieved with `wrapper.vm.$destory`

**example**
```js
wrapper.destroy()
```
### dispatch(event)
Dispatches native event or custom event to wrapper elements or vms

**event** - `String` name of event to be dispatched/emitted

**comments** - should this be broken into two methods - dispatch and emit?

**example**
```js
wrapper.dispatch('click')
```
### didEmit()
Asserts wrapper vm emitted event

**returns** - `Boolean`

**example**
```js
wrapper.didEmit('update')
```
### find(selector)
Returns true if wrapper contains selector

**selector** - `String|Object` CSS selector or Vue component

**returns** - `Object` wrapper containing new elements

**example**
```js
wrapper.find()
```
### hasAttribute(attribute, value?)
Returns true if wrapper DOM elements have attribute. If value is specified, checke the value of the attribute matches.

**attribute** - `String`
**value** (optional) - `String`

**returns** - `Boolean`

**example**
```js
wrapper.hasAttribute('attribute')
```
### hasClass(class)
Returns true if wrapper DOM elements have class

**class** - `String`

**returns** - `Boolean`

**example**
```js
wrapper.hasClass('class')
```
### hasStyle(style)
Returns true if wrapper DOM elements have style

**style** - `String`

**returns** - `Boolean`

**example**
```js
wrapper.hasProp('style')
```
### hasProp(prop)
Returns true if wrapper vm have prop

**prop** - `String`

**returns** - `Boolean`

**example**
```js
wrapper.hasProp('prop')
```
### html()
Renders HTML of wrapper elements

**returns** - `String` HTML of wrapper DOM node as a string

**example**
```js
wrapper.html()
```
### is(selector)
Asserts root wrapper nodes match selector

**returns** - `Boolean`

**example**
```js
wrapper.is('div')
```
### isEmpty()
Asserts root wrapper node contains no children

**returns** - `Boolean`

**example**
```js
wrapper.isEmpty()
```

### isVueInstance()
Asserts root wrapper node is vm

**returns** - `Boolean`

**example**
```js
wrapper.isVueComponent()
```
### name()
Returns name of vm or tag name of vNode

**returns** - `String` - name of component if vm, name of tag if vNode

**example**
```js
wrapper.name()
```

### setData(data)
Sets vm data and re renders

**comments** - should it re render, or should it be left to user?

**data** - `Object` - data to set

**example**
```js
wrapper.setData({data: 'value'})
```
### setProps(props)
Sets vm props and re renders

**comments** - should it re render, or should it be left to user?

**props** - `Object` - props to set

**example**
```js
wrapper.setProps({prop: 'value'})
```
### text()
Returns all text node content of vNode tree concatted to string

**returns** - `String` - content of all text nodes

**example**
```js
wrapper.text()
```
### update()
Forces vm to re render
**example**
```js
wrapper.update()
```
