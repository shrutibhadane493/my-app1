pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'git 'https://github.com/shrutibhadane493/my-app1'
'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package -DskipTests'   // OR npm install
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'   // OR npm test
            }
            post {
                always {
                    junit '**/target/surefire-reports/*.xml'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo "Deployment Done"
            }
        }
    }
}
