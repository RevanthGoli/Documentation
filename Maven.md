# Installing Apache Maven on Linux Using a tar File

# Prerequisites
    
   *  A Linux-based operating system.
   *  Root or sudo privileges.
   *  Java (JDK) installed.
  
# Official Docs

* Official Documentation of Apache Maven.

* [Refer Here](https://maven.apache.org/guides/index.html)


# Steps

* Download the Apache Maven tar file:

    * Visit the Apache Maven official website to download the desired    version of Maven.
    
    * Use wget or your web browser to download the tar file. For example:
    '''
    wget https://downloads.apache.org/maven/maven-3/3.8.6/binaries/apache-maven-3.8.6-bin.tar.gz
    '''
    
    * Replace 3.8.6 with the appropriate version numbers.

# Download the tar file
wget https://downloads.apache.org/maven/maven-3/3.8.6/binaries/apache-maven-3.8.6-bin.tar.gz


# Extract the tar file
tar -xzf apache-maven-3.8.6-bin.tar.gz


# Move the extracted files
sudo mv apache-maven-3.8.6 /usr/local/


# Set up environment variables
echo 'export M2_HOME=/usr/local/apache-maven-3.8.6' >> ~/.bashrc
echo 'export PATH=$M2_HOME/bin:$PATH' >> ~/.bashrc


# Apply the changes
source ~/.bashrc


# Verify the installation
mvn -version

# Notes:

* Replace 3.8.6 with the specific version numbers.

* If you prefer to install Maven in a different directory, adjust the paths accordingly.

* Ensure that Java (JDK) is installed and properly configured, as Maven requires Java to run.