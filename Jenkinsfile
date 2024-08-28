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
//        stage('Build'){
//             steps{
//                 sh 'mvn clean package'
//             }
//          }
        stage('SonarQube analysis') {
//    def scannerHome = tool 'SonarQubeScanner-6.1.0';
        steps{
        withSonarQubeEnv('sonarqube-10.6.0') { 
        // If you have configured more than one global server connection, you can specify its name
//      sh "${scannerHome}/bin/sonar-scanner"
//         sh "mvn sonar:sonar"
    }
        }
        }
       
    }
}
    

