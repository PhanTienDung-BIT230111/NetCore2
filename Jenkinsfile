pipeline {
 agent any
 
 stages {
	stage('clone'){
		steps {
			echo 'Cloning source code'
			git branch:'main', url: 'https://github.com/PhanTienDung-BIT230111/NetCore2.git'
		}
	} // end clone

	stage('restore package') {
		steps
		{
			echo 'Restore package'
			bat 'dotnet restore'
		}
	}

	stage ('build') {
		steps {
			echo 'build project netcore'
			bat 'dotnet build  --configuration Release'
		}
	}
	
	stage ('tests') {
		steps{
			echo 'running test...'
			bat 'dotnet test --no-build --verbosity normal'
		}
	}


	

  } // end stages



}//end pipeline


