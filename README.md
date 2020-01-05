# My portfolio's site

Available on https://fedor-malyshkin.github.io

## Contribution process:
* Update info on site, after that in CV and in LI (https://www.linkedin.com/in/fedor-malyshkin/)

## Calculate experience
4 (in magnetico) + (current year - 2015) = so for 2020 it will be ( 4 + (2020-2015) = 9)


## Local testing
* Install Ruby: 
`sudo apt-get install ruby-full build-essential zlib1g-dev`
* Adjust Gem storage: 
```bash
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```
* Finally, install Jekyll (https://jekyllrb.com/):
`gem install jekyll bundler`
* Run Jekyll: 
`bundle exec jekyll serve`
* Update libs from time to time (must be run in site's directory):
```bash
gem update
bundle update
```