pipeline {
    agent any
    environment{
        PATH="/opt/maven/bin/:$PATH"
    }
    
    tools {
        maven "maven"
    }
    
    stages {
        stage ('GITCLONE') {
            steps {
                
            //   sh 'git clone https://github.com/devopsjune2024/devopsjan27.git'
            git branch: 'main', credentialsId: 'GIThub', url: 'https://github.com/devopsjune2024/devopsjan27.git'
              
            }
        }
        stage ('BUILD') {
            steps {
            sh 'mvn package'
            }
        }
    }
}
