# RedViking Argonaut Redirects

A simple project to handle URL redirects. 

Based upon [https://github.com/brunoluiz/_](https://github.com/brunoluiz/_) updating the config.yml will result in creating redirects (instead of using tinyURL, etc ... )

## Process 

### Prerequisites

* Github account w/ push access to [this project](https://github.com/RV-Argonaut/redirects)
* Installation of urlzap, for WSL2 or Ubuntu

```bash
wget https://github.com/brunoluiz/urlzap/releases/download/v1.0.0/urlzap_1.0.0_linux_amd64.deb
sudo dpkg -i urlzap_1.0.0_linux_amd64.deb
```

### Update Links

Use a procedure to update links: 

1. `git clone https://github.com/RV-Argonaut/redirects`
1. `git checkout main` 
1. Update the config.yml file
1. `git add config.yml`
1. `git commit -m 'chore: adds xxx site to redirects'`
1. `git push -u origin main`

#### make gh-pages branch to be the same as main

```
git checkout gh-pages
git reset --hard origin/main
```

#### Generate files

```
urlzap generate
```

#### add, commit and push generated files

```
git add --all
git commit -m 'chore: update HTML files'
git push -u origin gh-pages --force
```

url-redirects
