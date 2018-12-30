# openapi

啟動swagger編輯器

<pre>
docker run --rm p 8082:8080 swaggerapi/swagger-editor
</pre>

可以設定預設是否展開

API_URL載入預設文件。

DOC_EXPANSION設定為預設不展開。

<pre>
docker run --name swagger-ui -d -p 8083:8080 -e API_URL=https://raw.githubusercontent.com/DevinY/openapi/master/openapi-jwt.yaml -e DOC_EXPANSION='none' swaggerapi/swagger-ui
</pre>

如果您使用D-Laravel，也可經由D-Laravel的.env載入

或是修改自己的docker-compose.yml檔，依service上的swagger範例，到自己的docker-compose.yml中。

D-Laravel於v1.6.18版加入swagger-editor.yml及swagger-ui.yml到service中囉。

<pre>
#===當您使用D-Laravel的.env功能時，請採用D-Laravel所提供的指令控制container!===
#MYSQL_ROOT_PASSWORD=secret
LARAVEL_INSTALLER='container'
DOCKER_SERVICES='docker-compose.yml service/redis.yml service/swagger-editor.yml service/swagger-ui.yml'
</pre>
