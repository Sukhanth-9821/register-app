pipeline{
  agent any
  tools{
    jdk 'java17'
    maven 'maven3'
  }
  stages{
    stage ("GIT CHECKOUT Stage"){
      steps{
           git branch: 'main', url: 'https://github.com/Sukhanth-9821/register-app.git'
      
      }
    }
    stage ("Build Step"){
      steps{
        sh 'mvn clean install package'
      }
    }
     stage ("Maven Test"){
      steps{
        sh 'mvn test'
      }
    }
    stage ("SonarQube Scanner"){
      steps{
        withSonarQubeEnv(credentialsId: 'Sonar'){
        sh "mvn sonar:sonar"
}
      }
    }
    stage("SonarQube QualityGate"){
      steps{
        waitForQualityGate abortPipeline: false, credentialsId: 'SonarNewmar2024'
      }
    }
  }
  
}
