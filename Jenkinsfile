pipeline {
    agent {
     
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
        stage('Test') { <1>
            steps {
                sh 'mvn test' <2>
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml' <3>
                }
            }
        }
    }
}
