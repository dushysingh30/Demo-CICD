docker build -t saurabhdevo1/demo-webapp:latest .
docker run -d -p 8081:8080  saurabhdevo1/demo-webapp:latest
http://localhost:9090/Demo-CICD/

#Script to run cd pipeline
echo 'process is running'
cd /usr/share/tomcat7/bin
sudo systemctl stop tomcat
sudo cp /var/lib/jenkins/workspace/MyFirst_CI_Pipeline/target/Demo-CICD.war /var/lib/tomcat7/webapps
sudo chmod -R 755 /usr/share/tomcat7/webapps/Demo-CICD.war
cd /usr/share/tomcat7/bin
sudo ./startup.sh
