
# DDEV Kirby Plainkit

[Kirby CMS](https://getkirby.com/) meets [DDEV](https://ddev.com/) & [Gitpod](https://gitpod.io/).

**Try out in your browser:**

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/mandrasch/ddev-kirby-plainkit/)

**Local usage:**

Clone to your local laptop and run:

```
ddev start && ddev composer install && ddev launch
```

**About this starterkit**

See https://github.com/getkirby/plainkit for more information.

## How was this created?

**Kirby setup**

Based on ["Installing via composer"](https://getkirby.com/docs/cookbook/setup/composer#installing-composer)-docs.

```bash
ddev config --project-type=php --php-version="8.0"
ddev start
ddev ssh
composer create-project getkirby/plainkit install-folder && \
    echo "Moving installation to root folder ..." && \
    mv install-folder/README.md install-folder/README_kirby.md && \
    cp -Rp install-folder/. /var/www/html && \
    rm -rf install-folder/
exit 
ddev composer install
ddev launch
```

**Gitpod & DDEV**

Gitpod DDEV integration was done with helpful tips by [@shaal](https://github.com/shaal). See `.gitpod.yml` and `.gitpod/`-folder.

## Links

- See https://github.com/mandrasch/ddev-kirby-starterkit as well

## License

Kirby allows free local try outs, but for live sites purchasing a license is required.
[getkirby.com](https://getkirby.com) · [License agreement](https://getkirby.com/license)
