
pipeline {
   agent { label 'dev' }
   stages {
       stage (checkout){
           steps {
            checkout([$class: 'GitSCM',
    branches: [[name: '*/master']],
    userRemoteConfigs: [[credentialsId: 'f1ac5d33-39cc-4531-b485-79bf53848d10', url: 'https://github.com/rohan4linux/nexusrepo-1.git']]
]) 
<<<<<<< HEAD
   }
     }  
   stage (build){
=======
           }
                }
     stage (build){
>>>>>>> e21de1b4a4b9b1d1bc8f4ccf78e56fcea1160a04
           steps {
               sh 'mvn package'
                 }
                         } 
              
   stage (sonar){
           steps {
               sh 'mvn sonar:sonar -Dsonar.host.url=http://15.206.123.54:9000 -Dsonar.credentials=admin:admin'
                 }
                         }              
              }
                  }
        
