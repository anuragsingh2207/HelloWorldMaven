pipeline { 
    agent any 
    stages {
        stage('Build') { 
            steps {
                withMaven(maven : 'apache-maven-3.8.5'){
                        bat "mvn clean compile"
                }
            }
        }
        stage('Test'){
            steps {
                withMaven(maven : 'apache-maven-3.8.5'){
                        bat "mvn test"
                }

            }
        }
        stage('Deploy') {
            steps {
               withMaven(maven : 'apache-maven-3.8.5'){
                        bat "mvn deploy"
                }

            }
        }
    }
}
