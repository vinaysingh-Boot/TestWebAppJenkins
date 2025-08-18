pipeline{
	agent any
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
				sh 'mvn clean compile'
			}
		}
		
		stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        
        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // example: copy war/jar to Tomcat, or upload to AWS S3
            }
        }
	}
}