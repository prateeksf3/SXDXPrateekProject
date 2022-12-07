pipeline 
{
    agent any  
    stages 
  { 
		stage('Authenticate') 
		{		
			 steps 
			 {		
					bat "sfdx force:auth:sfdxurl:store -f ./Auth_URL.txt -a POrg"
			 }			
		 }
      
		  stage('Validate') 
		 {		
			 steps 
			 {
					bat "sfdx force:source:deploy -c -p 'force-app' -u POrg"
			 }
       
     }

   }
}
