# Geb and Spock

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
