pipeline {
    agent any

    stages {
        stage('checkout'){
            steps{
            cleanWs()
            checkout changelog: false, poll: false, scm: [$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github', url: 'https://github.com/venkatam0720/Test-Repo.git']]]
            }
        }
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
    }
}
