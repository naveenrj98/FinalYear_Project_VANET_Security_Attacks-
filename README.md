# FinalYear_Project_VANET_Security_Attacks-
Detection and Prevention of Security Attacks in VANET
## Step 1. To Run our project, following Software needs to be installed
**•	UBUNTU 18.0.0 +**
**•	Eclipse**
o	https://linoxide.com/linux-how-to/learn-how-install-latest-eclipse-ubuntu/
**•	MVN**
o	sudo apt-get install mvn
o	set MVN_HOME Path Variable
**•	JAVA** 
o	sudo apt-get install java
o	set JAVA_HOME Path variable
**•	Open JDK 8**
o	sudo apt-get install openjdk-8-jdk
o	sudo update-alternatives --set java/usr/lib/jvm/jdk1.8.0_version/bin/java

## Step 2. To Run the App, follow the following steps
•	Step 1:  Certificate Generation
o	Generate the new certificate by running the command
	./gen-cert.sh <vehicle1> <vehicle2> ..., new keys will also be generated for ca and RSU in the process.
•	Step 2: Install the App
o	Install All the dependencies required for the project, run the command:
	sudo apt-get  ./mvn-script.sh install
•	Step 3: Detection of Attack
o	Run the commands to detect and prevent attacks
	Method 1: sudo  ./mvn-script.sh <entity> [arguments]
•	entity: (VIN8 vehicle8 10,5 0,0 BAD_SIGNATURES)
o	BAD_POSITIONS: for Sybil Attack Detection
o	BAD_SIGNATURES: for Bad signature detection
o	BAD_CERTIFICATE: for bad certification detection
o	BAD_TIMESTAMPS: for Replay Attack Detection
o	BEACON_DOS: for DOS attack detection
•	arguments: (example)
o	VIN1 vehicle1 750,850 0,0 Sample Massage	
o	VIN8 vehicle8 10,5 0,0 BAD_SIGNATURES
o	VIN21 invalidCACert1 5,5 0,0 BAD_CERTIFICATE
o	VIN4 vehicle4 10,5 0,0 BAD_SIGNATURES
o	VIN6 vehicle6 10,5 0,0 BEACON_DOS
	Method 2: use the launcher to launch predefined profiles in: profiles_*.txt with: (if name is omited default profile_default.txt is assumed
•	sudo ./launcher  <any-profile-file>
Step 3: Follow the command instruction and execute the Proposed System.

