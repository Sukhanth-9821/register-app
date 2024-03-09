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
        script{
        withSonarQubeEnv(credentialsId: 'Sonar'){
        sh "mvn sonar:sonar -Dsonar.login=sqa_5ca37de718763953c2613adcafdc8be0602a581c"
}
        }
      }
    }

  }
  
}
