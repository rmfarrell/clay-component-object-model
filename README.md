# Component Object Model
An object model for Clay components

# What's a COM?
A class which wraps the raw data of a component and exposes methods on it for easiliy
saving, traversing and analyizing a components within Clay.

A COM has a tree structure so intializing one with a data object will atttempt to transform each 
component within the object's scope recursively. 

For interoperability, you can transform the COM object back into an object literal by calling
`.toObject()` on the COM instance. `.toJSON()` will transform it to JSON.


# Intitialization
To initialize the COM class simply call `new COM` over a raw data object.
The initializer will attempt to create a COM object from the argument or throw an error.

```js
const COM = import 'clay-component-object-model'

fetchPageSomeComponentData(...)
  .then((results) => {
    const component = new COM(results)
  })

```

# API

## Transformations

### .toObject([recursive])

### .toJSON([recursive])

## REST requests

### .get([recursive])

### .post([recursive])

### .delete([recurisve])

## Tree traversal

### .children([recursive])

### .parent()

### .findByType(type)

### .find(query)

### .findComponentById(id)

### .getComponentsByType(type)

### .one(query)

## Getter/Setters

### .type (getter/ready-only)

### .sortWeight (getter/setter)

## Other Mutations

### .append(com)

### .remove(com)




