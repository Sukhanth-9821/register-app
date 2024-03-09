pipeline{
  agent any
  tools{
    jdk 'jdk17'
    maven 'maven3'
  }
  stages{
    Stage "GIT CHECKOUT"{
      Steps{
           git branch: 'main', url: 'https://github.com/Sukhanth-9821/register-app.git'
      
      }
    }
  }
  
}
