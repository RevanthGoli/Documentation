#  Installing OpenJDK on Linux Using a tar File

## Pre-Requisites

* A Linux-based operating system.
* Root or sudo privileges.

## Versions of OpenJDK:
  * OpenJDK 7
  * OpenJDK 8
  * OpenJDK 9
  * OpenJDK 11
  * OpenJDK 17
  * OpenJDK 22






## Steps

* Download the OpenJDK tar file:
   
    * For Official web site [Reffer Here](https://jdk.java.net/)
    * [preview](./images/jdk%201.png)
    * Visit the OpenJDK official website or another trusted source to download the desired version of OpenJDK.
    * Use wget or your web browser to download the tar file. For example:
    '''
     wget https://download.java.net/openjdk/jdkXX/ri/openjdk-XX+XX_linux-x64_bin.tar.gz
    '''
    * Replace XX with the appropriate version numbers.



## Download the tar file
wget https://download.java.net/openjdk/jdk17/ri/openjdk-17+35_linux-x64_bin.tar.gz


## Extract the tar file
tar -xzf openjdk-17+35_linux-x64_bin.tar.gz


## Move the extracted files
sudo mv jdk-17 /usr/local/


## Set up environment variables
echo 'export JAVA_HOME=/usr/local/jdk-17' >> ~/.bashrc
echo 'export PATH=$JAVA_HOME/bin:$PATH' >> ~/.bashrc


## Apply the changes
source ~/.bashrc


## Verify the installation
java -version
