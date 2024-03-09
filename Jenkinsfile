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
  }
  
}
