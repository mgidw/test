pipeline{
    agent any
    environment {
        PATH = "$PATH:C:/Program Files/apache-maven-3.8.6-bin/apache-maven-3.8.6/bin"
    }
    stages{
       stage('GetCode'){
            steps{
                git branch:'main', url: 'https://github.com/mgidw/test.git'
            }
         }        
//        stage('Build'){
//             steps{
//                 sh 'mvn clean package'
//             }
//          }
        stage('SonarQube analysis') {
//    def scannerHome = tool 'SonarScanner 4.0';
        steps{
        withSonarQubeEnv('Sonarqube-9.6.1') { 
        // If you have configured more than one global server connection, you can specify its name
//      sh "${scannerHome}/bin/sonar-scanner"
//         sh "mvn sonar:sonar"
    }
        }
        }
       
    }
}
