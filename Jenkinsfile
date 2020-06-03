pipeline {
    agent any
    stages {
        stage('git checkout') {
            steps {
                bat "https://github.com/sakhayadeep/vault-test.git"
            }
        }
 
        // stage('install') {
        //     steps {
        //         bat "mvn install"
        //     }
        // }

        // stage('test') {
        //     steps {
        //         bat "mvn test"
        //     }
        // }
    
        stage('package') {
            steps {
                bat "mvn clean package"
            }
        }
    }
}