# openapi

啟動swagger編輯器

<pre>
docker run --rm p 8082:8080 swaggerapi/swagger-editor
</pre>

可以設定預設是否展開

API_UIL載入預設文件。

DOC_EXPANSION設定為預設不展開。

<pre>
docker run --name swagger-ui -d -p 8083:8080 -e API_URL=https://raw.githubusercontent.com/DevinY/openapi/master/openapi-jwt.yaml -e DOC_EXPANSION='none' swaggerapi/swagger-ui
</pre>

