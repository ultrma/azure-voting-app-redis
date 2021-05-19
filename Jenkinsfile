pipeline {
    agent any
    
    stages {
        stage ('Verifying Branch'){
            steps {
                echo "$GIT_BRANCH"
            }
        }
        stage ('Test PS'){
            steps{
                powershell label: '', script:'Write-Output "Hello Powershell"'
            }
        }
        stage('Docker Build') {
            steps {
                pwsh (script:'Write-Output "Hello Powershell Core"')
                /*
                pwsh(script: 'docker images -a')
                pwsh(script: """
                    cd azure-vote/
                    docker images -a
                    docker build -t jenkins-pipeline .
                    docker images -a
                    cd ..
                """)
                */
            }
        }
    }
}