## Testing in Reise at Tech Review #4 - 2016.06.09

This is a presentation on how FINN Reise does testing held at FINN Tech Review #4 2016.06.09.

To watch the presentation, just go to [https://finn-no.github.io/Testing-in-Reise-at-Tech-Review-4/](https://finn-no.github.io/Testing-in-Reise-at-Tech-Review-4/).

More info below for working on the code.

### Requirements

Make sure the correct node version is installed:

```
> node --version
v5.0.0

```

Install dependencies:

```
> npm install
```

### Run presentation

Use the following for serving the content:

```
> npm start
```

This will build the presentation, start a web server hosting it and
open the default browser showing it.

### Make changes to the presentation

First, start up the presentation in reload mode:

```
> npm run develop
```

Now when you change the presentation, every change will be reloaded
automatically in the browser.

### Deploy the presentation to GitHub Pages

Any changes made can be deployed to GitHub Pages like this:

```
> npm run deploy
```
