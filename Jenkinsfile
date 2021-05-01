
pipeline {
	
        tools {
    maven 'Maven3'
  }
    stages {
        stage('Hello') {
		agent { label 'jenkins_slave2' }
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
                git branch: 'develop', credentialsId: 'ff8d9146-de5d-43ee-9ff7-adaa9c888197', url: 'https://github.com/malleshdevops/hello-world.git'
            }
        }
        stage('build') {
            steps {
                sh script: 'mvn clean package'
            }
        }
        
        
    }
}
