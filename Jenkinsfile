
pipeline{
    agent { label 'dev' } 
    stages{
        stage(checkout){
            steps{
                checkout([$class: 'GitSCM', 
    branches: [[name: '*/master']], 
    userRemoteConfigs: [[credentialsId: 'e70848a0-aea8-4b8f-8a51-804ab59fb44b', url: 'https://github.com/busani9/nexusrepo.git']]
            ]) 
                
            }
                       }
        stage(build){
            steps{
            sh 'mvn package'
            }
        }
        stage(deploy){
            steps{
            sh 'scp /root/workspace/firstjob/target/*.war 3.9.190.132:/var/lib/tomcat/webapps/'
            }
        }
          }
        }
