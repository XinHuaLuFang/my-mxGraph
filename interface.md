```javascript
var container = document.getElementById(x);

// Creates the graph inside the given container
var graph = new mxGraph(container);

// Creates the model and the graph inside the container
// using the fastest rendering available on the browser
var model = new mxGraphModel();
var graph = new mxGraph(container, model);

// Disables the built-in context menu
// 禁用浏览器默认的右键菜单
mxEvent.disableContextMenu(container);

// 鼠标框选
new mxRubberband(graph);

// Disables basic selection and cell handing
// 图表只读无交互
graph.setEnabled(false);

//Specifies if the graph should allow new connections.
//指定graph是否可以建立新连接，默认值false
graph.setConnectable(true);
//Specifies if the graph should allow multiple connections between the same pair of vertices.
//指定两个顶点之间是否能够建立多个连接，默认值true
graph.setMultigraph(false);



var vertex = new mxCell(xxx);
//Specifies if the cell is a vertex.
//设置vertex的属性vertext为true,vertex的属性vertex默认为false
vertex.setVertex(true);
```