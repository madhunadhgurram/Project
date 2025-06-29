# Project

Initially, we give infrastructure from terraform. 
Once infrastructure is done, developers will give the code.
The code we taken from the developer, we need to build the code, test the code, check the gate qualities of sonarqube. Once the sonarqube is passed. 
We need to get to the artifact. And the artifact we will store on the s3. 
Finally we're gonna do the deployment. We do deployment in the tomcat server. 
Once deployment is done, finally we will monitor the servers from prometheus and grafana.








(War file will store inside target folder in jenkins --> /var/lib/jenkins/workspace/netflix/target). We need to copy this war file to tomcat. So that we need to write a playbook(yaml code).
[ - hosts: all
  tasks:
    - name: copy the file to tomcat
      copy:
        src: /var/lib/jenkins/workspace/netflix-pipeline/target/NETFLIX-1.2.2.war
        dest: root/tomcat/webapps ]


         name: copy the file to tomcat
      copy:
        src: /var/lib/jenkins/workspace/netflix-pipeline/target/NETFLIX-1.2.2.war
        dest: root/tomcat/webapps 
