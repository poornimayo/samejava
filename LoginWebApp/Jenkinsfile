
pipeline {
   agent any
   stages{
   stage('Checkout'){
       steps{
       checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'b8522e92-ee04-461e-9cf3-fe68e9ac6347', url: 'https://github.com/poornimayo/samejava.git']]])
       } 
   }
   stage('static code analysis'){
       steps{
       echo "static code analysis"
       }
   }
   stage('build'){
       steps{
       echo "Build the code"
       }
   }
   stage('unit testing')
   {
       steps{
       echo "build the code"
       }
   }
   stage('delivery')
   {
       steps{
       echo "deliver the code"
       }
   }
}
}
