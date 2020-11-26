pipeline {
	agent any
	parameters{
		choice(name: 'VERSION', choices: ['1.1.0','1.2.0','1.3.0'], description: '')
		boolean(name: 'executeTests',defaultValue: true, description: '')
	}
	stages{
		 stage("build"){
			steps{
			  echo 'building the application ...'
			}
      		stage("test"){
			steps{
			  echo 'testing the application ...'
			}
		}
      		stage("deploy"){
			steps{
			    echo "deploying version ${params.VERSION}"
			}
	}
	 post{//build status or build status change
		 always{
			 //send an emails to a teams about the build condition
		 }
		 success{ //or failure
			 //only revelant if the build succeded
		 }
	}

}

