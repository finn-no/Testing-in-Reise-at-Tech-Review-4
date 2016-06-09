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

For de som ikke har brukt det, så er Spock et test rammeverk dvs et alternativ til JUnit. Anbefaler alle til å begynne å bruke det i stedet for JUnit. Det gjør testene mye mer konsise og lett-leste. Vi bruker det på unit, modul og feature-testene.

Geb brukes til frontend testing som en driver for WebDriver, dvs. det er et alternativ til Cucumber. Det blir brukt som et slags påbygg til Spock, som gjør det mulig å bruke mange av de kjekke mulighetene Spock gir ved frontend testing. Karma brukes til testing av javascript, hvor vi i tillegg til å kjøre det lokalt med PhantomJS kjører det i skyen på BrowserStack for å teste andre nettlesere, dvs. for å sjekke at det ikke krasjer i IE.

Vi har laget en liten test utility som kan starte opp Tomcat før testene kjører, aka embedded tomcat. Slik blir det enkelt å kjøre modul-tester fra IntelliJ.

Alle modulene våre snakker over http med hverandre, så det er forholdsvis enkelt å mocke vekk modul-avhengigheter ved å kjøre opp en mock http server i testene. Vi har et par thrift-tjenester vi bruker, bl.a. Broadcast, så vi fikk fikset denne slik at den passet inn i test-oppsettet vårt.
