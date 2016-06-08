## Feature tests

* End-2-end testing
* Starts the whole vertical
   * web, api, integration, solr, etc.
* The tests emulate a user
* Mocks out external services
   * Expedia, SAS, Star Tour, Ving, etc.

Note:

Feature tester er ende-til-ende testing, dvs. hele applikasjonen blir startet opp, frontend, api, solr, etc. Testen kjøres mot frontend ved å emulere en bruker. Den fyller ut felt, trykker på knapper/linker og sjekker hva som ligger på siden etter at "brukeren" har gjort noe. Her mocker vi vekk alle eksterne tjenester som expedia, sas, star tour, ving, etc.
