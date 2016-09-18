```javascript
var container = document.getElementById(x);

// 在container容器中创建graph
var graph = new mxGraph(container);

// 
var editor = new mxEditor();
var graph = editor.graph;

// 在container容器中创建带有model的graph
var model = new mxGraphModel();
var graph = new mxGraph(container, model);

// Disables the built-in context menu
// 禁用浏览器默认的右键菜单
mxEvent.disableContextMenu(container);

// 鼠标框选
new mxRubberband(graph);


// 设置建立连接时显示的图片
mxConnectionHandler.prototype.connectImage = new mxImage("xxx.png", 16, 16);
// 指定graph是否可以建立新连接，默认值false-不可
graph.setConnectable(true);
// 指定两个顶点之间是否能够建立多个连接，默认值true-可以
graph.setMultigraph(false);

// 图表是否只读，默认值true-可编辑
graph.setEnabled(false);

// 指定cells是否可改变大小，默认值true-可以
graph.setCellsResizable(false);




var vertex = new mxCell(xxx);
// 设置vertex的属性vertext为true,vertex的属性vertex默认为false
vertex.setVertex(true);
```