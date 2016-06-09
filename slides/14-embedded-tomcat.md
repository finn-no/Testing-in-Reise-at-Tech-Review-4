## Embedded Tomcat

```groovy
@Shared
def EmbeddedTomcat tomcat = new EmbeddedTomcat()

@Shared
def client

def setupSpec() {
  tomcat.start()
  client = new RESTClient("http://localhost:${tomcat.port}")
}

def cleanupSpec() {
  tomcat.stop()
}
```

Note:

Her er et eksempel på bruk av test utilitien for å kjøre opp Tomcat i en Spock test og stoppe den når testen er ferdig.
