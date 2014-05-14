JalonRender v0.0.1
===========

a very little bit template engine （v0.0.1&lt;1kb）

for example:

    <!DOCTYPE html>
    <html>
    <head>
        <title>JalonRender</title>
        <script type="text/javascript" src="jalonrender.min.js"></script>
    </head>
    <body>
    
    <div id="myBox"></div>
    
    <script type="text/html" id="user_tmpl">
        <ul>
            <% for ( var i = 0; i < users.length; i++ ) { %>
            <li><%=users[i].name%></li>
            <% } %>
        </ul>
    </script>
    <script type="text/javascript">
        var users=[
            {"name":"jalon"},
            {"name":"baby"},
            {"name":"volvo"}
        ];
        var myBox = document.getElementById("myBox");
        myBox.innerHTML = render("user_tmpl", users);
    </script>
    </body>
    </html>
