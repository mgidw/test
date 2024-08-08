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
   stage('Build'){
          steps{                sh 'mvn clean package'           }         }

    }
        }
        }
       
    }
}
