pipeline 
{
    agent any  
    stages 
  { 
		stage('Authenticate') 
		{		
			 steps 
			 {		
					sh "sfdx force:auth:sfdxurl:store -f ./Auth_URL.txt -a PrateekOrg"
			 }			
		 }
      
		  stage('Validate') 
		 {		
			 steps 
			 {
					sh "sfdx force:source:deploy -c -p 'force-app' -u PrateekOrg"
			 }
       
     }

   }
}
