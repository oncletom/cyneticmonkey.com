# cyneticmonkey.com

This is the professional showcase of [Thomas Parisot](http://case.oncle-tom.net).
If you want to hire a full-stack JavaScript developer for an interesting mission,
this is definitely the place to look.

This website is built using [punch](http://laktek.github.com/punch), *less*
and *mustache*.

## Install

The only prerequisite after cloning this repo and to install the dependencies:

```bash
npm install
```

## Run

The only thing to do to test locally is to run the following command:

```bash
npm start
```

It will run the dev version on [http://localhost:9009](http://localhost:9009).

## Deploy

Once satisfied with the result, there is a two step process before seeing the code live.

```bash
npm run-script build
npm run-script deploy
```

If you want to test the *deployed* code after the `generate` process, simply
configure a *vhost* towards the `output/` folder.

For example:

```apache
<VirtualHost *:80>
  ServerName local.mywebsite.com
  DocumentRoot /path/to/mywebsite.com/output

  <Directory /path/to/mywebsite.com/output>
    Options Indexes
    AllowOverride All
    Order allow,deny
    allow from all
  </Directory>
</VirtualHost>
```

