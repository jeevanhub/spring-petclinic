pipeline {
    agent 
  
    stages {
        stage('Build') {
            steps {
                //sh 'mvn -B -DskipTests clean package'
                sh 'echo "new jenkins file"'
            }
        }
        stage('Test') {
            steps {
                //sh 'mvn test'
            }
            post {
                always {
                   junit 'target/surefire-reports/*.xml'
                }
            }
        }
        stage('Deliver') {
            steps {
                sh './jenkins/scripts/deliver.sh'
            }
        }
    }
}

