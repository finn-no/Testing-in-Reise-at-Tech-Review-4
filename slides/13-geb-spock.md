## Geb and Spock

```groovy
def 'Enter credentials and login'() {
  given:
    at LoginPage
    def uid = System.getenv('FINN_UID')
    def pwd = System.getenv('FINN_PWD')

  when:
    email.value(uid)
    password.value(pwd)
    loginWithSPiD.click()

  then:
    at UserPage
}
```

Note:

Her er et eksempel på en Geb test skrevet i Spock. Den sjekker at browseren er på login-siden og setter uid/pwd fra env.vars. Deretter fyller den inn uid/pwd i formen på login-siden, for så å trykke på login-knappen. Så sjekker den at man kommer profil-siden.
