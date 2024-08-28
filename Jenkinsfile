pipeline{
    agent any
    environment {
        PATH = "$PATH:C:/Program Files/apache-maven-3.9.9-bin/apache-maven-3.9.9/bin"
    }
    stages{
       stage('GetCode'){
            steps{
                git branch:'main', url: 'https://github.com/mgidw/test.git'
            }
         }        
    stage('Build'){
             steps{
                sh 'mvn clean package'
            }
         }
       stage('SonarQube Analysis') {
    def mvn = tool 'Default Maven';
    withSonarQubeEnv() {
      sh "${mvn}/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=manya123 -Dsonar.projectName='manya123'"
    }
  }
       
    }

}

