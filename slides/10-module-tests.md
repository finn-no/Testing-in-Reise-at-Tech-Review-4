## Module tests

* Starts only 1 module
   * web or api or...
* 2 ways of testing
   * web modules --> emulate a user
   * other modules --> call the API
* Mocks out
   * other modules
   * external services

Note:

Modultester kjører bare opp en modul, f.eks. frontend eller api-artifaktet. Hvis det er en frontend modul emuleres en bruker på samme måte som for feature testene fra forrige slide. Ellers testes modulen gjennom APIet den eksponerer. Her mocker vi ut andre moduler og eksterne tjenester slik at vi kan konsentrere oss om hva modulen gjør og ikke hvordan andre moduler/eksterne tjenester oppfører seg.
