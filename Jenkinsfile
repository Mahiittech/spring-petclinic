pipeline {
    agent { label 'node1' }
        stages { 
        
        stage('git clonning') {
            
            steps{ 
                git branch: 'main', url: 'https://github.com/Mahiittech/spring-petclinic.git'
                
            }
        }
         stage('build the code and static code anaylysy'){
             steps{
                 withSonarQubeEnv('SONAR_LATEST'){
                 sh script: 'mvn clean package sonar:sonar'
                     
                 }
                 }
         }
                 
             }
         }
          
