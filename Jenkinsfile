
pipeline {
   agent any
   stages{
   stage('Checkout'){
       steps{
       checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'b8522e92-ee04-461e-9cf3-fe68e9ac6347', url: 'https://github.com/poornimayo/samejava.git']]])
       } 
   }
      stage('compile'){
            steps{
               bat label: '', script: '''mvn compile

'''
            }
            }
               
   stage('build'){
       steps{
       bat label: '', script: '''mvn clean package
'''
       }
   }
   stage('unit testing')
   {
       steps{
       bat label: '', script: '''mvn test
'''
       }
   }
   stage('run')
   {
       steps{
       bat label: '', script: '''mvn verify

'''
       }
   }
    
}
}
