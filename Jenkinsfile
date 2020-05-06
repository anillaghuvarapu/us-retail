pipeline {
   agent any

    tools{
        maven 'maven-linux'
       jdk 'java-linux'
     }

  stages{
      
      stage ('checkout'){
          
          steps{
              
              git 'https://github.com/anillaghuvarapu/us-retail.git'
          }
      }
      
      stage ('build'){
          
          steps{
              
              sh 'mvn clean package'
          } 
      }
      stage ('deploy'){
          
          steps{
              
              sh '/opt/deploy.sh'
          } 
      }
          stage ('artifact'){
          
          steps{
              
              archiveArtifacts 'target/*.war'
          } 
          }
          
      
#      stage ('email'){
 #         steps{
  #            
   #           mail bcc: '', body: 'Jenkins', cc: '', from: '', replyTo: '', subject: 'jenkinsjob', to: 'theetisatish@gmail.com'
    #      }
          
     # }
  }  
      
  
   
}
