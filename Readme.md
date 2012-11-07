This is basically a copy of mod-webserver from the vertx project.

The differences are:

* gradle plugin is groovy, not java
* original java source renamed and moved to groovy source file
* more recent versions of everything

To build,

```./mk dist```

Then follow the basic vertx tutorial for the webserver mod, except use this mod instead of the one from vertx as the webserver.

For example:

    def webServerConf = [
      port: 8080,
      host: 'localhost'
    ]
    
    container.deployModule('com.example.mods.webserver-v1.0', webServerConf);
