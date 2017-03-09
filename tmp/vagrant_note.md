#### Installation
$ brew cask install vagrant    --appdir=/Applications
$ brew cask install virtualbox --appdir=/Applications

#### Popular commands
$ vagrant box add [options] <name, url, or path>
$ vagrant init [options] [name [url]]
$ vagrant up [options] [name]
$ vagrant ssh [options] [name] [-- extra ssh args]
$ vagrant package [options] [name]

#### Example
$ vagrant box add ubuntu/trusty64
$ vagrant init ubuntu/trusty64
$ vagrant up
$ vagrant ssh