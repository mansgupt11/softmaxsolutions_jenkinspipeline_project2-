pipeline {
	agent none
	tools {
    	maven 'my_mvn'
	}
	stages {
    	stage("Checkout") {   
        	agent { label 'jenkins_slave1' }
        	steps {               	 
            	git url: 'https://github.com/mansgupt11/softmaxsolutions_jenkinspipeline_project2-.git'          	 
           	 
        	}    
    	}
    	stage('Build') {
        	agent { label 'jenkins_slave1' }
        	steps {
        	sh "mvn compile"  	 
        	}
    	}
   	 
    	stage("Unit test") {          	 
        	agent { label 'jenkins_slave2' }
        	steps {  	 
            	git url: 'https://github.com/mansgupt11/softmaxsolutions_jenkinspipeline_project2-.git'
            	sh "mvn test"          	 
       	}     	 
    	}	 
   }

}
