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
              
              sh '/opt/scripts/deploy.sh'
          } 
      }
          stage ('artifact'){
          
          steps{
              
              archiveArtifacts 'target/*.war'
          } 
          }
          
      
          
  }  
      
  
   
}
