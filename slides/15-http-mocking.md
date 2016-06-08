## HTTP mocking

```groovy
def setupMockForCurrencyRates(String responseFromApi) {

  clientDriver.addExpectation(

    onRequestTo("/reise/valuta/").
      withMethod(GET).
      withAnyParams(),

    giveResponse(responseFromApi, JSON).
      after(0, TimeUnit.SECONDS).
      withStatus(OK.statusCode)
  )
}
```

Note:

Vi bruker nå en rammeverk som heter ClientDriver for mocking av http-tjenester, i dette eksempelet mocker vi ut api-kallene for uthenting av valuta-kurser.
