pipeline {
   agent any
   stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '4bc6580e-41ab-4203-8f56-bcd3333e1c50', url: 'https://github.com/pandajyotsna23/test3.git']]])
                sh "ls -lart ./*"
            }
        }
        stage('build') {
            steps {
                sh "mvn install"
                sh "ls -lrt"
            }
        }
    }
}
