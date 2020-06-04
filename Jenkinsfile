pipeline {
    agent any
    stages {
        stage('access vault'){
            steps{
                withVault(configuration: [timeout: 60, vaultCredentialId: 'vault-token', vaultUrl: 'http://localhost:8085'], vaultSecrets: [[path: 'secret2/Dockerhub', secretValues: [[vaultKey: 'username'], [vaultKey: 'password']]]]) {
                    sh "echo username=${username}"
                    sh "echo password=${password}"
                }
            }
        }
    }
}