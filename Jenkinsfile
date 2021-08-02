
pipeline {
	agent any
  	tools { maven 'Maven3' }
    stages {
        stage('Hello') {
		
            steps {
                echo 'Hello World'
            }
        }
        stage('clean workstation'){
                steps{
            cleanWs()
        }
        }
        stage('Git') {
            steps {
                git branch: 'main', credentialsId: '743c6a44-a3bf-4ca7-baac-5f9f0e1941da', url: 'https://github.com/malleshdevops/hello-world.git'
            }
        }
        stage('build') {
            steps {
                sh script: 'mvn clean package'
            }
        }
        
        
    }
}
