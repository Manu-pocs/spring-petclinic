pipeline {
    agent {
        docker {
            image 'maven:3.8.4-jdk-8-slim'
            args '--network host -v /root/.m2:/root/.m2'
        }
    }
    stages {
        stage('Unit Tests') {
            steps {
                sh 'mvn -version'
                sh 'java -version'
                sh 'mvn test'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn -version'
                sh 'java -version'
                sh 'mvn package -Dmaven.test.skip=true'
            }
        }
    }
}
