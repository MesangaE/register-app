pipeline {
    agent { label 'Jenkins-Agent' }
    tools {
        jdk 'Java17'
        maven 'Maven3'
   }
   stages{
    stage("Cleanup Workspace"){
        steps{
        cleanWs()
        }
    }
    stage("Checkout from SCM"){
        steps{
        git branch: 'main' , credentialsId: 'github' , url: 'https://github.com/MesangaE/register-app'      }
        }

    stage("Build Application"){
        steps {
        sh "mvn clean package" 
        }
<<<<<<< HEAD
    }
  }
=======
   }
    stage("SonaqQube Analysis"){
        steps{
            script{
                 withSonarQubeEnv(credentialsId:'jenkins-sonarqube-token') {
                 sh "mvn sonar:sonar"
                 }
              }
          }
      }
   }
>>>>>>> 1ef9b732a04182b2ad41fbb120d8d6b5e7047a89
}

