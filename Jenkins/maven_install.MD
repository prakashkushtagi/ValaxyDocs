#  Install & configure Maven build tool on Jenkins
Maven is a code build tool which used to convert your code to artifact. this is widely used plugin to build in continuous integration

#### Follow this artical in **[YouTube](https://www.youtube.com/watch?v=wgfsVmHnAiM)**

#### Prerequisites
1. Jenkins server **[Get Help Here](https://www.youtube.com/watch?v=M32O4Yv0ANc)

#### Install Maven on Jenkins
Download maven packages https://maven.apache.org/download.cgi onto Jenkins server. In this case I am using /opt/maven as my installation directory
	- Link : https://maven.apache.org/download.cgi
```sh
  # Creating maven directory under /opt
  mkdir /opt/maven
  cd /opt/maven
  # downloading maven version 3.6.0
  wget http://mirror.olnevhost.net/pub/apache/maven/maven-3/3.0.5/binaries/apache-maven-3.0.5-bin.tar.gz
  tar xvf apache-maven-3.0.5-bin.tar.gz
  mv apache-maven-3.0.5  /usr/local/apache-maven
  
 ```
	
Setup M2_HOME and M2 paths in .bash_profile of user and add these to path variable

export M2_HOME=/usr/local/apache-maven
export M2=$M2_HOME/bin 
export PATH=$M2:$PATH

source ~/.bashrc

mvn –version

So far you have completed installation of maven software to support maven plugin on jenkins console. Let's jump onto jenkins to complete remining steps. 

#### Setup maven on jenkins console
- Install maven plugin without restart  
  - `Manage Jenkins` > `Jenkins Plugins` > `available` > `Maven Invoker`

- Configure java path
  - `Manage Jenkins` > `Global Tool Configuration` > `Maven`

#### Next Steps

- [x] [Configure Users & Groups in Jenkins](https://youtu.be/jZOqcB32dYM)
- [x] [Secure your Jenkins Server](https://youtu.be/19FmJumnkDc)
- [x] [Jenkins Plugin Installation](https://youtu.be/p_PqPBbjaZ4)
- [x] [Jenkins Master-Slave Configuration](https://youtu.be/hwrYURP4O2k)
