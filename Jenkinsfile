
pipeline {
    agent {
        docker {
            image 'maven:3.8.6' 
            args '-v /root/.m2:/root/.m2' 
        }
    }
    environment {
    	hudson.plugins.git.GitSCM.ALLOW_LOCAL_CHECKOUT='true'
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}