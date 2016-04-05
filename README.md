JalonRender v0.0.1
===========

a very little bit template engine （v0.0.1&lt;1kb）

For example:

```
<!DOCTYPE html>
<html>
<head>
    <title>JalonRender</title>
</head>
<body>

<div id="myBox"></div>

<script type="text/javascript" src="jalonrender.min.js"></script>
<script type="text/html" id="user_tmpl">
    <h3><%=data.title %></h3>
    <ul>
        <% for(var i=0; i < data.list.length; i++ ) { %>
        <li>
            <span><%= data.list[i].text%></span>
            <% if(data.list[i].done) { %>
            <span style="color: red">√</span>
            <% } else { %>
            <span style="color: #ccc">☀</span>
            <% } %>
        </li>
        <% } %>
    </ul>
</script>
<script type="text/javascript">
    var data = {
        title: 'todo', list: [
            {text: '去吃饭!', done: true},
            {text: '去喝水!', done: false},
            {text: '去打球!', done: false}
        ]
    };
    var myBox = document.getElementById('myBox');
    myBox.innerHTML = render('user_tmpl', data);
</script>
</body>
</html>
```
