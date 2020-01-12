# boot-mydev-mac
#My development tools setup for MacOS
#MySetUp

#Other peoples setup notes:
	http://sourabhbajaj.com/mac-setup/
	https://dev.to/equiman/setup-macos-for-development-3kc2

#MyTools
-Install  Xcode to get CLI tools that Home-brew depends on
	$ sudo xcode-select --install

-Install Homebrew
	$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

	-Uninstall if want to start again
	$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/uninstall)"
	
-Enable Home-brew installed programs  add to PATH
	$ echo 'PATH="/usr/local/bin:$PATH"' >> ~/.bash_profile
	-some additional doc reference https://docs.brew.sh

-Install iterm2
	$ brew cask install iterm2
  	-some additional config is optional
	https://sourabhbajaj.com/mac-setup/iTerm

-Install SDK Man
	$ curl -s "https://get.sdkman.io" | bash 
	-then in new terminal
	$ source "$HOME/.sdkman/bin/sdkman-init.sh"

-Install IntelliJ-Idea
	$ brew search intellij-idea-ce          # Searches all known Casks for a partial or exact match.
	$ brew cask info intellij-idea-ce       # Displays information about the given Cask
	$ brew cask install intellij-idea-ce    # Install the given cask.
	$ brew cleanup

-Install Graphviz
	$ brew install graphviz

-Install Archimate

-Install Helm?
??

—

#MyBasic-DevConfig
	$ sdk install java 8.0.232.hs-adpt
	$ sdk use java 8.0.232.hs-adpt
	$ sdk default java 8.0.232.hs-adpt

	$ sdk install gradle 6.0.1
	$ sdk use gradle 6.0.1
	$ sdk default gradle 6.0.1

	$ sdk install maven 3.6.3
	$ sdk use maven 3.6.3
	$ sdk default maven 3.6.3
—

#MyApps

-Install Docker (this is Docker Desktop version >19.03.5
  	$ brew cask install docker

-Install MongoDB
	$ brew cask install mongodb-compass

-Install RabbitMQ
	$ brew install rabbitmq
	$ echo 'PATH="/usr/local/opt/rabbitmq/sbin:$PATH"' >> ~/.bash_profile

 	$ brew services start rabbitmq
 	$ brew services stop rabbitmq
	or
	$ rabbitmq-server

	$ rabbitmqctl -n rabbit@localhost set_log_level info
	$ tail -100f /usr/local/var/log/rabbitmq/rabbit@localhost.log



