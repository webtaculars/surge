# surge(.sh)

> Publish web apps to a CDN with a single command and no setup required.

_surge_ is a Command Line Interface that runs on the nodejs runtime (surge's only external dependency). Surge can be installed using npm (via `sudo npm install -g surge`). Once installed, `surge` is available from within your terminal. The following command will deploy the current working directory to the surge servers where the application will be available at sintaxi.com.

       path to project (defaults to current working dir)
             |
             | your domain (will propt you if not passed in)
             |     |
             ↓     ↓
    $ surge ./ sintaxi.com

Run `surge --help` to see the following overview of the `surge` command...

```
  Usage:
    surge [options]

  Options:
    -p, --project       path to projects asset directory (./)
    -d, --domain        domain of your project (<random>.surge.sh)
    -e, --endpoint      domain of API server (surge.sh)
    -a, --add           add collaborator via email address
    -r, --rem           remove collaborator via email address
    -v, --verbose       verbose output
    -h, --help          show this help message

  Shorthand usage:
    surge [project] [domain]

```

## CDN Features

- Custom CNAME & custom SSL
- Fallback 404.html pages
- HTML5 mode 200.html pages
- stays out of `git`s way
- supports clean URLs && trailing slashes `/`
- Implicit signup
- supports CNAME files

If you’re using tools like Grunt, Gulp, or a static site generator like Jekyll, your files are output into a compile directory like `_site/`, `build/`, or `www/`. From the root of your project, pass Surge the path to this directory to upload your compiled assets.

    surge www

You may also add this directory to your `.gitignore` to keep your compiled assets out of your Git history.

