## Thrift stubbing

```groovy
public final class BroadcastTestServer {
  public BroadcastTestServer() {
    broadcastServer = new BroadcastServer(
      new BroadcastServiceHandler(new BroadcastMessageDaoStub()));
    int port = findFreePort();
    broadcastServer.setPort(port);
  }

  public void start() {
    copyIniFileToTmpDir();
    broadcastServer.start();
  }

  public void stop() {
    deleteTempIniFileIfExists();
    broadcastServer.stop();
  }
```

Note:

Dette er en test utility for å stubbe ut kall til broadcast-serveren. Dvs. at denne kjøres opp før testene. I andre tester der vi ikke tester at broadcast fungerer, slår vi den av med en config-fil.
