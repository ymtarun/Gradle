pipeline {
    agent any  // Use any available agent

    tools {
        gradle 'Gradle'  // Ensure this matches the name configured in Jenkins
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/ymtarun/Gradle.git'
            }
        }

        stage('Build') {
            steps {
                sh 'gradle test'  // Run Maven build
            }
        }

        stage('Run') {
            steps {
                sh 'gradle run'  // Run unit tests
            }
        }
       }
       post{
       	success{
       		echo 'Build successfully'
       	}failure{
       		echo 'Build failure'
       	}
  }
}

    

