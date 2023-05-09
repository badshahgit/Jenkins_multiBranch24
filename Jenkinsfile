node('built-in')

{

stage('Continuous loan_Download') 
   
	 {
	
    git 'https://github.com/badshahgit/Jenkins_multiBranch24.git'
    
	}

stage('Continuous ;oan_build') 
   
	 {
	
   sh label: '', script: 'mvn package'
	}

stage('Continuous loan_Deployment') 
   
	 {
	
 sh label: '', script: 'scp  /home/ubuntu/.jenkins/workspace/multibrnch/webapp/target/webapp.war  ubuntu@172.31.3.91:/var/lib/tomcat9/webapps/mainqaenv.war'
	}
stage('Continuous loan_Testing') 
   
	 {
	sh label: '', script: 'echo "Testing Passed"'
	}
stage('Continuous loan_Delivery') 
   
	 {
	sh label: '', script: 'scp  /home/ubuntu/.jenkins/workspace/multibrnch/webapp/target/webapp.war  ubuntu@172.31.10.74:/var/lib/tomcat9/webapps/mainprodenv.war'
	}
}
