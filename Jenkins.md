# Installing Jenkins on Linux Using apt 

# Prerequisites

* A Debian-based Linux distribution (e.g., Ubuntu).
* Root or sudo privileges.
* Java (JDK) installed (Jenkins requires Java to run).

#  Official Docs

* Official Documentation of Jenkins.
[Refer Here](https://www.jenkins.io/doc/)

# Steps


# Update the package index
sudo apt update


# Install Java
sudo apt install openjdk-11-jdk


# Verify Java installation
java -version


# Add Jenkins repository and GPG key
curl -fsSL https://pkg.jenkins.io/debian/jenkins.io.key | sudo tee /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null


# Update the package index again
sudo apt update


# Install Jenkins
sudo apt install jenkins


# Start and enable Jenkins
sudo systemctl start jenkins
sudo systemctl enable jenkins


# Adjust the firewall (if applicable)
sudo ufw allow 8080
sudo ufw reload


# Retrieve the initial admin password for Jenkins setup
sudo cat /var/lib/jenkins/secrets/initialAdminPassword


# Note :

* Ensure that your system is up-to-date by regularly running sudo apt update and sudo apt upgrade.

* Adjust the firewall rules as necessary, depending on your specific network configuration.

* If you encounter any issues, consult the Jenkins documentation for troubleshooting and additional configuration options.