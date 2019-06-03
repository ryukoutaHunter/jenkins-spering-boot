pipeline{
  agent any

  stages{
    stage ('Compile Stage'){

      steps{
         withMaven(maven : 'apache-maven-3.6.1'){
            sh 'mvn clean compile'
         }
       }
    }

    stage ('Testing Stage'){
      steps{
          withMaven(maven : 'apache-maven-3.6.1'){
            sh 'mvn install'
          }
      }
    }

    stage ('Deployment Stage'){
      steps{
        withMaven(maven : 'apache-maven-3.6.1'){
          sh 'mvn deploy'
        }
      }
    }

  }
}