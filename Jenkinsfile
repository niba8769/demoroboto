pipeline {
    agent { 
        node {
            label 'docker-agent'
            }
        }
    
   stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'jenkins-user-github', url: 'https://github.com/niba8769/demoroboto.git']]])
                sh "ls -lart ./*"
            }
        }     
    }
    
}