pipeline {
    agent any 
    stages {
	    

        stage("Clone sources") { 
		
		checkout scm           
	}
	    
        stage('Validate') {
		
           sfdx force:mdapi:deploy -c -g -l NoTestRun -f ./manifest/package.xml -w -1 -u Test1
        }
		
		stage('Deploy') {
		
		sfdx force:mdapi:deploy -g -l NoTestRun -f ./manifest/package.xml -w -1 -u Test1
            
        }
    }
}
