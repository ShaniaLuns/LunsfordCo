# Lunsford & Co. Website

## Local Development Instructions

Becuase this is a static HTML/CSS/JS site, there is no dev environment (i.e., `npm run`) or
any way to build a static distribution of the site. Also note that due to the static site layout
required to host on Vercel, you **cannot** simply open `index.html` in a browser and expect the
site to work as intended. 

Instead, the site can be hosted locally using the methods outlined below.

### 1. `serve`

NPM has a package called `serve` which will open up a local web server on http://localhost:8000. You can
intall and run it with the following commands:

```bash
npm install -g serve
serve public
```

### 2. `lite-server`

Because `serve` is designed to operate on static sites, it does not implement any sort of hot-reload like
Webpack and Vite do. However, `lite-server` will effectively simulate this functionality.

First, install `lite-server`:

```bash
npm install -g lite-server
```

Then, you have to tell it where the root of the website is stored. In this case, it's in `./public`. Create
a new file called `bs-config.json` at the root of the project and enter the following JSON:

```json
{
  "server": {
    "baseDir": "./public"
  }
}
```

Finally, run:

```bash
lite-server
```

To launch the dev environment.