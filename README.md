# my-mxGraph

* If you want the container to have scrollbars, use the __overflow:auto CSS__ directive instead of overflow:hidden in the style of the container.
* If you want the graph to be read-only you can use __graph.setEnabled(false)__.
* To create a new graph instance, a DOM node (typically a DIV) is required:
```javascript
    var node = document.getElementById('id-of-graph-container');
    var graph = new mxGraph(node);
```
![graph](img/graph.png)

* __mxGraph.insertVertex(parent, id, value, x, y, width, height, style)__-creates and inserts a new vertex into the model,within a begin/end update call.Will create an mxCell object and return it from the method used.The parameters of the function are:
    * __parent__ – the cell which is the immediate parent of the new cell in the group structure. We will address the group structure shortly, but for now use __graph.getDefaultParent();__ as your default parent, as used in the HelloWorld example.
    * __id__ – this is a global unique identifier that describes the cell, it is always a string. This is primarily for referencing the cells in the persistent output externally. If you do not wish to maintain ids yourself, pass null into this parameter and ensure that mxGraphModel.isCreateIds() returns true. This way the model will manage the ids and ensure they are unique.
    * __value__ – this is the user object of the cell. User object are simply that, just objects, but form the objects that allow you to associate the business logic of an application with the visual representation of mxGraph. They will be described in more detail later in this manual, however, to start with if you use a string as the user object, this will be displayed as the label on the vertex or edge.
    * __x, y, width, height__ – as the names suggest, these are the x and y position of the top left corner of the vertex and its width and height.
    * __style__ – the style description to be applied to this vertex. Styles will be described in more detail shortly, but at a simple level this parameter is a string that follows a particular format. In the string appears zero or more style names and some number of key/value pairs that override the global style or set a new style. Until we create custom styles, we will just use those currently available.

### API
1. __IO__
    IO包中实现了类__mxObjectCodec__,这个类可以把JavasScript对象转为XML。
    IO包中主要的类是__mxCodec__
2. aa
