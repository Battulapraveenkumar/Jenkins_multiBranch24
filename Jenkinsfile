node('built-in')
{
   

    stage('Continuous Download_Child') 
	{
    git 'https://github.com/sunildevops77/maven.git'
	}
    stage('Continuous Build_child') 
	{
    sh label: '', script: 'mvn package'
	}
stage('Continuous Deployment_child') 
   
	 {
	
 sh label: '', script: 'scp  /home/ubuntu/.jenkins/workspace/MultiBranchPipeline_loans/webapp/target/webapp.war  ubuntu@172.31.0.184:/var/lib/tomcat9/webapps/qaenv.war'
	}
stage('Continuous Testing_child') 
   
	 {
	sh label: '', script: 'echo "Testing Passed"'
	}
stage('Continuous Delivery_child') 
   
	 {
	sh label: '', script: 'scp  /home/ubuntu/.jenkins/workspace/MultiBranchPipeline_loans/webapp/target/webapp.war  ubuntu@172.31.4.165:/var/lib/tomcat9/webapps/prodenv.war'
	}

}
