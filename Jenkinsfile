pipeline{
	agent any
	tools {
        maven 'my_maven'   // Name of Maven installed in Jenkins (Manage Jenkins > Global Tool Config)
        jdk 'java'        // Name of JDK installed in Jenkins
    }
	stages{
		stage('Checkout') {
            steps {
                // Pull source code from Git
                git branch: 'main',
                    url: 'https://github.com/vinaysingh-Boot/TestWebAppJenkins'
            }
        }
        
		stage('build'){
			steps{
				echo 'Building the project...'
				sh 'mvn clean compile'
			}
		}
	}
}