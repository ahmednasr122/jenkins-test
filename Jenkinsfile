pipeline {
    agent { label 'java-agent-01' }

    stages {
        stage('Checkout SCM') {
            steps {
                git branch: 'main', url: 'https://github.com/Hassan-Eid-Hassan/cicd-lab2.git'
            }
        }

        stage('Build App') {
            steps {
                sh 'mvn clean package -DskipTests'
            }
        }

        stage('Test App') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
