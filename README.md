hawtio-plugin
=============

War Plugin for Hawtio [http://hawt.io/]

* build your WAR :

```ruby
mvn
```


* Check you Tomcat console : 

```ruby
INFO: Loading Blueprint contexts [file:/D:/Workspace/Workspace-Git/hawtio-plugin/target/simple-plugin-1.2-M8/WEB-INF/classes/
OSGI-INF/blueprint/blueprint.xml]
DEBUG | ContainerBackgroundProcessor[StandardEngine[Catalina]] | Instantiating components: [blueprintContainer, plugin]
DEBUG | ContainerBackgroundProcessor[StandardEngine[Catalina]] | Registering plugin hawtio:type=plugin,name=simple-plugin
27 ao¹t 2013 10:21:54 org.apache.catalina.core.StandardContext filterStart
```

* Watch your plugin in Hawtio web application


Edit your dashboard and include your JSON definition

```json
{
  "id": "4d5ff553f5982181d3",
  "title": "Simple plugin",
  "group": "Personal",
  "widgets": [
    {
      "id": "SimplePlugin",
      "title": "Simple plugin",
      "row": 1,
      "col": 2,
      "path": "jmx/charts",
      "include": "/hawtio-simple-plugin/app/html/simple.html",
      "search": {
        "nid": "root-hawtio-plugin",
        "att": "ProcessCpuLoad%2CSystemCpuLoad%2CSystemLoadAverage"
      },
      "hash": "",
      "size_x": 4,
      "size_y": 2
    }
  ],
  "uri": "/dashboards/team/all/simple-plugin.json"
}
```


