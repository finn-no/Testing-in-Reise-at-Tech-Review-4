## Tools & frameworks

* Spock
* Geb
* Karma
* BrowserStack
* Embedded Tomcat
* HTTP mocking
* Thrift stubbing

Note:

Vi bruker en del verktøy og rammeverk for å gjøre testingen enklere.

Spock er et test rammeverk som vi bruker på unit, modul og feature-testene. Det er noe som alle burde begynne å bruke med en gang, dvs. bytte ut JUnit. Det gjør testene mye mer konsise og lett-leste.

Geb brukes til frontend testing som en driver for WebDriver, dvs. det er et alternativ til Cucumber. Det blir brukt som et slags påbygg til Spock, som gjør det mulig å bruke mange av de kjekke mulighetene Spock gir ved frontend testing. Karma brukes til testing av javascript, hvor vi i tillegg til å kjøre det lokalt med PhantomJS kjører det i skyen på BrowserStack for å teste andre nettlesere.

Vi har laget en liten test utility som kan starte opp Tomcat før testene kjører, aka embedded tomcat. Slik blir det enkelt å kjøre modul-tester fra IntelliJ.

Alle modulene våre snakker over http med hverandre, så det er forholdsvis enkelt å mocke vekk modul-avhengigheter ved å kjøre opp en mock http server i testene. Vi har et par thrift-tjenester vi bruker, bl.a. Broadcast, så vi fikk fikset denne slik at den passet inn i test-oppsettet vårt.
