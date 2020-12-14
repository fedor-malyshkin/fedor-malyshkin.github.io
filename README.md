# My portfolio's site

Available on https://fedor-malyshkin.github.io

## Contribution process:

* Update info on site, after that in CV and in LI (https://www.linkedin.com/in/fedor-malyshkin/)

## Calculate experience

4 (in magnetico) + (current year - 2015) = so for 2020 it will be  `4 + (2020-2015) = 9`

## Local testing (with Docker)

* Start docker (in this directory):

```shell
(intial) docker run -it -v `pwd`:/mnt -p 80:4000 --name jekyll ubuntu bash 
(start) docker start jekyll 
(login) docker exec -it  jekyll bash
```

* (in docker) Install Ruby:

```shell
apt-get update
apt-get install locales ruby-full build-essential zlib1g-dev python2
dpkg-reconfigure locales (select en_US.UTF-8 UTF-8, was 159)
update-locale LANG=en_US.UTF-8 
export  LANG=en_US.UTF-8 
````

* (in docker) Adjust Gem storage:

```shell
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

* (in docker) Finally, install Jekyll (https://jekyllrb.com/):

```shell
cd /mnt
gem install jekyll bundler 
```

* (in docker) Run Jekyll:

```shell
cd /mnt
bundle exec jekyll serve  --host 0.0.0.0
```

* (in docker) Update libs from time to time (must be run in site's directory):

```shell
cd /mnt
gem update
bundle update
```