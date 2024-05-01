pipeline {
        agent any
parameters {
  choice choices: ['DEV', 'QA', 'UAT'], name: 'ENV'
}


        stages {
            stage('Checkout') {
                steps {
                        checkout scm
                      }}
                stage('Build') {
                   steps {
                          sh '/home/harshada/Documents/DevOps_software/apache-maven-3.9.6/bin/mvn install'
                         }}
                stage('Deployment'){
                   steps {
                sh 'cp target/SLACK-PROJECT.war /home/harshada/Documents/DevOps_software/apache-tomcat-9.0.88'
                        }}
stage('slack'){
steps { 
slackSend baseUrl: 'https://hooks.slack.com/services/', channel: 'slack-channel', color: 'good', message: 'I love my Nagpur', teamDomain: 'student', tokenCredentialId: '96f15b3f-4212-4530-9bc3-3d8794d797be', username: 'harshada' }}


}}

