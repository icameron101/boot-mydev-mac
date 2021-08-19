#MySetUp
————————

https://brewinstall.org

#Other peoples setup notes:
	http://sourabhbajaj.com/mac-setup/
	https://dev.to/equiman/setup-macos-for-development-3kc2

#DB bits for VMR / Skype Webcam
https://www.citrix.com/en-gb/downloads/citrix-receiver/additional-client-software/hdx-realtime-media-engine-latest.html

———
https://realpython.com/intro-to-pyenv/#installing-pyenv

brew install openssl readline sqlite3 xz zlib


curl https://pyenv.run | bash

curl https://pyenv.run | bash

# Load pyenv automatically by adding
# the following to ~/.bashrc:

export PATH="$HOME/.pyenv/bin:$PATH"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"

exec "$SHELL"

pyenv install --list

pyenv install -v 3.7.3


—————
https://github.com/pyenv/pyenv/blob/master/README.md#homebrew-on-macos

brew install pyenv 
pyenv install 3.7.9
pyenv global 3.7.9
pyenv version
echo $0
echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.zshrc


echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc


exec "$SHELL"

https://google.github.io/mediapipe/solutions/hands#python-solution-api

python version
python3 version
python3 -m venv mp_env && source mp_env/bin/activate
python3 -m venv .venv source .venv/bin/activate

pip install mediapipe

python -m pip install opencv-python 


UNINTSTALL

rm -rf $(pyenv root)
 brew uninstall pyenv


git clone ssh://cameron.clarke@dbtechhackathon.com@source.developers.google.com:2022/p/hack-t6/r/hackathon-t6-git-repo 
——————





brew install --cask google-chrome


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
	$ brew install --cask iterm2
  	-some additional config is optional
	https://sourabhbajaj.com/mac-setup/iTerm

-Install SDK Man
	$ curl -s "https://get.sdkman.io" | bash 
	-then in new terminal
	$ source "$HOME/.sdkman/bin/sdkman-init.sh"

-Install Docker (this is Docker Desktop version >19.03.5
  	$ brew install docker

-Instal Kubernetes Minikube, depends on Docker
  	$ brew install kubectl

-Install IntelliJ-Idea
	$ brew install intellij-idea-ce    # Install the given cask.
            brew reinstall intellij-idea-ce
	$ brew cleanup

-Install VSC
        $ brew install --cask visual-studio-code
            Configure extensions: prettier / format on save

-Install Graphviz
	$ brew install graphviz

—Install PlantUml
      	$ brew install plantuml

-Install Archimate
   -via manual download and bit shift  to avoid corruption message
   -download and install collaboration plugin : https://github.com/archimatetool/archi-modelrepository-plugin/wiki




-Install DBeaver
	$ brew cask install dbeaver-community

—install Hashicorp Terraform https://gist.github.com/brianshumate/09adf967c563731ca1b0c4d39f7bcdc2
	$ brew install terraform


—Install Hashicorp Vault and Consul https://medium.com/hacker-soon/installation-of-consul-and-vault-in-mac-7d1ecf8facb2
	$ brew install consul
	$ brew install vault

—Install Azure CLI
	$ brew update && brew install azure-cli
        $ brew upgrade azure-cli



—Install flyway
      	$ brew install flyway

—Install Swagger-CodeGen
	$ brew install swagger-codger

—Install Apache Spark
	$ brew install apache-spark

—install Asciidoctorj
	$ sdk install asciidoctorj 2.3.1

brew cask install textmate

#MyBasic-DevConfig
	$ sdk install java 8.0.252.hs-adpt
	$ sdk use java 8.0.252.hs-adpt
	$ sdk default java 8.0.252.hs-adpt

	$ sdk install scala 3.0.1
	$ sdk use scala 3.0.1
	$ sdk default scala 3.0.1
    $ sdk install sbt 1.5.5

	$ sdk install gradle 6.5.1
	$ sdk use gradle 6.5.1
	$ sdk default gradle 6.5.1

	$ sdk install maven 3.6.3
	$ sdk use maven 3.6.3
	$ sdk default maven 3.6.3

	$ sdk install kotlin 1.3.61
	$ sdk use kotlin 1.3.61
	$ sdk default kotlin 1.3.61

      
       $ sdk i springboot 2.2.5.RELEASE
       $ spring init —build=gradle -name demo -groupId com.icameron101.gradle.demo

https://start.spring.io/#!type=gradle-project&language=kotlin&platformVersion=2.2.5.RELEASE&packaging=jar&jvmVersion=1.8&groupId=com.icameron101&artifactId=demo&name=demo&description=Demo%20project%20for%20Spring%20Boot&packageName=com.icameron101.demo

—

#MyApps

brew install --cask firefox

-Install MongoDB
	$ brew cask install mongodb-compass

-Install RabbitMQ
	$ brew install rabbitmq
	$ echo 'PATH="/usr/local/opt/rabbitmq/sbin:$PATH"' >> ~/.bash_profile
-Operate RabbitMQ
 	$ brew services start rabbitmq
 	$ brew services stop rabbitmq
	or
	$ rabbitmq-server

	$ rabbitmqctl -n rabbit@localhost set_log_level info
	$ tail -100f /usr/local/var/log/rabbitmq/rabbit@localhost.log

-Install Elastic Search https://www.elastic.co/guide/en/elasticsearch/reference/7.x/brew.html 
	$ brew tap elastic/tap
	$ brew install elastic/tap/elasticsearch-full

-Install Kafka https://smartechie.com/srplilu0gmail-com/trending/step-by-step-installing-kafka-in-mac/ 
	$ brew install Kafka
	$ brew services list
	$ brew services start zookeeper
	$ brew services start kafka
    -Operate Kafka
	$ kafka-topics --create --zookeeper localhost:2181 --replication-factor 1 --partitions 4 --topic test
	$ kafka-topics --describe --zookeeper localhost:2181 --topic test
	In a new terminal : $ kafka-console-producer --broker-list localhost:9092 --topic test
 	In a new terminal : $ kafka-console-consumer --bootstrap-server localhost:9092 --topic test --from-beginning
	$ kafka-topics --list --zookeeper localhost:9092

————————
docker pull Cloudera/quickstart:latest

docker image

docker run --hostname=quickstart.cloudera --privileged=true -t -i -p 8888:8888 -p 10000:10000 -p 10020:10020 -p 11000:11000 -p 18080:18080 -p 18081:18081 -p 18088:18088 -p 19888:19888 -p 21000:21000 -p 21050:21050 -p 2181:2181 -p 25000:25000 -p 25010:25010 -p 25020:25020 -p 50010:50010 -p 50030:50030 -p 50060:50060 -p 50070:50070 -p 50075:50075 -p 50090:50090 -p 60000:60000 -p 60010:60010 -p 60020:60020 -p 60030:60030 -p 7180:7180 -p 7183:7183 -p 7187:7187 -p 80:80 -p 8020:8020 -p 8032:8032 -p 802:8042 -p 8088:8088 -p 8983:8983 -p 9083:9083 4239cd2958c6 /usr/bin/docker-quickstart

docker ps -a

docker start <image>

docker exec -it <image> /bin/bash 

kill -9 $(jps | awk ‘{print $1}

——————————

https://minikube.sigs.k8s.io/docs/start/

brew install minikube







