# linux-things

Emoji-Fonts

Packages that may help:

* ttf-ancient-fonts
* fonts-font-awesome
* ttf-bitstream-vera  
* fonts-symbola 
* ttf-ancient-fonts-symbola
* powerline - install for fanciful fonts in bash (such as the git branch icon used in oh-my-zsh:agnoster) (Alternatively, may check out the repo: [powerline/fonts](https://github.com/powerline/fonts)

And more, through manual installation:

* https://github.com/eosrei/emojione-color-font#install-on-linux

General fonts

Manual

* https://github.com/adobe-fonts/source-code-pro, see also: http://askubuntu.com/questions/193072/how-to-use-the-new-adobe-source-code-pro-font

Other stuff

* Pretty print JSON - python comes with a tool to do this. Just add an alias for `prettyjson` that points to `python -m json.tool`; then you can pipe an unformatted json string into it: `cat file.json | prettyjson`. See [here](http://stackoverflow.com/questions/352098/how-can-i-pretty-print-json/1920585#1920585)
* Pretty print XML - Install the package `libxml2-utils`, then use the program `xmllint`. E.g.: `cat file.xml | xmllint --format -`. [See here for more info](http://stackoverflow.com/a/16090892/3476713)
* `~/.bash_profile` only executed in non interactive shells. For the GUI environment, a good place is `~/.profile`. [See here for more info](http://askubuntu.com/questions/121073/why-bash-profile-is-not-getting-sourced-when-opening-a-terminal)
* Screen recording (gif) - use byzanz-record and gifsicle. See [here](http://askubuntu.com/questions/107726/how-to-create-animated-gif-images-of-a-screencast) and [here](http://tschf.github.io/2015/12/02/screencast-gif-in-ubuntu/) for more info.

Browser

* Fix flickering in Chrome on Ubuntu - `Settings > Advance Settings > System > uncheck the hardware acceleration`. See [here](http://askubuntu.com/questions/766725/annoying-flickering-in-16-04-lts-chrome)

Containers

* Docker - install using [this guide](https://docs.docker.com/engine/installation/linux/ubuntu/)

Atom

* Atom installed through umake (`umake ide atom`), doesn't currently set up `apm` in the path. Issue logged [here](https://github.com/ubuntu/ubuntu-make/issues/411). Set up link: `cd ~/.local/share/umake/bin && ln -s ~/.local/share/umake/ide/atom/resources/app/apm/node_modules/.bin/apm apm`

Nautilus

* By default, list view expansion icon is not displayed. This can be enabled from: Edit -> Preferences -> Display; The option at the bottom "Navigate folders in a tree". [See here](http://askubuntu.com/a/429220/50523).

Oracle

* Oracle tns names, when using instant client good place to chuck is oracle_home. e.g. export TNS_ADMIN=${ORACLE_HOME}. Then a tnsnames.ora entry will look like (below). Connect then with sqlplus user/pass@XE:

```
XE =
  (DESCRIPTION =
    (ADDRESS = (PROTOCOL = TCP)(HOST = 192.168.0.182)(PORT = 1521))
    (CONNECT_DATA =
      (SERVER = DEDICATED)
      (SERVICE_NAME = XE)
    )
  )
```

Git

* Global git ignore, configured with property `git config --global core.excludesfile`. See [here](http://stackoverflow.com/questions/7335420/global-git-ignore)

Programming

* xacobeo - great GUI tool for testing XPath string
