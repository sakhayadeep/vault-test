pipeline{
    agent none
    stages{
        stage("access vault"){
            steps{
                withVault(configuration: [timeout: 60, vaultCredentialId: 'vault-token', vaultUrl: 'http://host.docker.internal:8086'], vaultSecrets: [[path: 'test/test', secretValues: [[vaultKey: 'name'], [vaultKey: 'age']]]]) {
                    sh "name=${name}"
                    sh "age=${age}"
                }
            }
        }
    }
}