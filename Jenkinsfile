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
      def scannerHome = tool 'SonarQubeScanner-6.1.0';
    def mvn = tool 'Default Maven';
    withSonarQubeEnv('sonarqube-10.6.0') {
      sh "${mvn}/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=manya123 -Dsonar.projectName='manya123'"
    }
  }
       
    }

}

