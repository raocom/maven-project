pipeline {
    agent { dockerfile true }
    tools {
        maven 'localMaven'
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
                sh "docker build . -t tomcatwebapp:${env.BUILD_ID}"
            }
        }
    }
}