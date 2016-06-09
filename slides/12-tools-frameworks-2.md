## Tools & frameworks

* PMD
* Checkstyle
* FindBugs
* CodeNarc
* Jasper
* Gradle

Note:

Vi kjører også kodesjekker i bygget, og sjekker både prod og testkode med de samme reglene. Testkoden skal alltid holde like høy kvalitet som prod-koden! Vi tester også at JSPene kompilerer ok. Disse sjekkene gjør det også tryggere å ikke ha PR. Jeg har nevnt gradle her fordi den gjør det veldig mye enklere å få til testingen vi gjør.
